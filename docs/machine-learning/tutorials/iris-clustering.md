---
title: ML.NET を使用してアヤメの花をクラスター化する (クラスタリング)
description: クラスタリングのシナリオで ML.NET を使用する方法について説明します
author: pkulikov
ms.author: johalex
ms.date: 07/02/2018
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: 46db9dc7ff425c483f1a9f61da5e806e598b16d5
ms.sourcegitcommit: 60645077dc4b62178403145f8ef691b13ffec28e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/10/2018
ms.locfileid: "37937167"
---
# <a name="tutorial-use-mlnet-to-cluster-iris-flowers-clustering"></a>チュートリアル: ML.NET を使用してアヤメの花をクラスター化する (クラスタリング)

> [!NOTE]
> このトピックは現在プレビュー中の ML.NET について述べており、内容が変更される場合があります。 詳しくは、[ML.NET の概要](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet)に関するページをご覧ください。

このチュートリアルでは、ML.NET を使って[あやめのデータ セット](https://en.wikipedia.org/wiki/Iris_flower_data_set)の[クラスタリング モデル](../resources/tasks.md#clustering)を作成する方法を示します。

このチュートリアルでは、次の作業を行う方法について説明します。
> [!div class="checklist"]
> - 問題を把握する
> - 適切な機械学習タスクを選択する
> - データを準備する
> - データを読み込んで変換する
> - 学習アルゴリズムを選択する
> - モデルをトレーニングする
> - モデルを使用して予測を行う

## <a name="prerequisites"></a>必須コンポーネント

- [Visual Studio 2017 15.6 以降](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)が ".NET Core クロスプラット フォーム開発" とともにインストールされていること。

## <a name="understand-the-problem"></a>問題を把握する

この問題は、アヤメの花のセットを特徴に基づいて異なるグループに分類するというものです。 対象となる特徴は、がくの長さと幅および花弁の長さと幅です。 このチュートリアルでは、各花の種類は不明であるものとします。 特徴からデータ セットの構造を理解し、データのインスタンスがこの構造にどのように当てはまるかを予測します。

## <a name="select-the-appropriate-machine-learning-task"></a>適切な機械学習タスクを選択する

各花がどのグループに属するかわからないので、[教師なし機械学習](../resources/glossary.md#unsupervised-machine-learning)タスクを選択します。 同じグループ内の要素同士の方が他のグループの要素より似ているようにデータ セットをグループに分割するので、[クラスタリング](../resources/tasks.md#clustering)機械学習タスクを使用します。

## <a name="create-a-console-application"></a>コンソール アプリケーションを作成する

1. Visual Studio 2017 を開きます。 **[ファイル]** > **[新規作成]** > **[プロジェクト]** をメニュー バーから選択します。 **[新しいプロジェクト]** ダイアログで、**[Visual C#]** ノードを選択し、**[.NET Core]** ノードを選択します。 次に、**[コンソール アプリ (.NET Core)]** プロジェクト テンプレートを選択します。 **[名前]** テキスト ボックスに「IrisClustering」と入力し、**[OK]** ボタンを選びます。

1. プロジェクトに *Data* という名前のディレクトリを作成して、データ セットとモデルのファイルを保存します。

    **ソリューション エクスプローラー**で、プロジェクトを右クリックし、**[追加]** > **[新しいフォルダー]** を選択します。 「Data」と入力して Enter キーを押します。

1. **Microsoft.ML** NuGet パッケージをインストールします。

    **ソリューション エクスプローラー**で、プロジェクトを右クリックし、**[NuGet パッケージの管理]** を選択します。 [パッケージ ソース] として "nuget.org" を選択し、**[参照]** タブを選択して「**Microsoft.ML**」を検索します。一覧からそのパッケージを選択し、**[インストール]** を選択します。 **[変更のプレビュー]** ダイアログの **[OK]** を選択します。表示されているパッケージのライセンス条項に同意する場合は、**[ライセンスの同意]** ダイアログの **[同意する]** を選択します。

## <a name="prepare-the-data"></a>データを準備する

1. [iris.data](https://github.com/dotnet/machinelearning/blob/master/test/data/iris.data) データ セットをダウンロードし、前の手順で作成した *Data* フォルダーに保存します。 あやめのデータ セットについて詳しくは、Wikipedia の「[Iris flower data set](https://en.wikipedia.org/wiki/Iris_flower_data_set)」(あやめのデータ セット) のページと、データ セットのソースである「[Iris Data Set](http://archive.ics.uci.edu/ml/datasets/Iris)」(あやめのデータ セット) のページをご覧ください。

1. **ソリューション エクスプローラー**で、*iris.data* ファイルを右クリックして、**[プロパティ]** を選択します。 **[詳細設定]** で、**[出力ディレクトリにコピー]** の値を **[新しい場合はコピーする]** に変更します。

*Iris.data* ファイルには、次の値を表す 5 つの列が含まれます。

- がくの長さ (センチメートル単位)
- がくの幅 (センチメートル単位)
- 花弁の長さ (センチメートル単位)
- 花弁の幅 (センチメートル単位)
- アヤメの種類

クラスタリングの例が目的なので、このチュートリアルでは最後の列を無視します。

## <a name="create-data-classes"></a>データ クラスを作成する

入力データと予測のためのクラスを作成します。

1. **ソリューション エクスプローラー**で、プロジェクトを右クリックし、**[追加]** > **[新しい項目]** を選択します。
1. **[新しい項目の追加]** ダイアログ ボックスで、**[クラス]** を選択し、**[名前]** フィールドを「*IrisData.cs*」に変更します。 次に、**[追加]** を選択します。
1. 以下の `using` ディレクティブを新しいファイルに追加します。

   [!code-csharp[Add necessary usings](../../../samples/machine-learning/tutorials/IrisClustering/IrisData.cs#1)]

既存のクラス定義を削除し、`IrisData` クラスと `ClusterPrediction` クラスを定義する次のコードを *IrisData.cs* ファイルに追加します。

[!code-csharp[Define data classes](../../../samples/machine-learning/tutorials/IrisClustering/IrisData.cs#2)]

`IrisData` は入力データ クラスであり、データ セットの各特徴の定義が含まれます。 [Column](xref:Microsoft.ML.Runtime.Api.ColumnAttribute) 属性を使用して、データ セット ファイル内のソース列のインデックスを指定します。

`ClusterPrediction` クラスは、`IrisData` インスタンスに適用されたクラスタリング モデルの出力を表します。 [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) 属性を使って、`PredictedClusterId` フィールドを **PredictedLabel** 列に、`Distances` フィールドを **Score** 列に、それぞれバインドします。 クラスタリング タスクの場合、これらの列には次の意味があります。

- **PredictedLabel** 列には、予測されたクラスターの ID が含まれます。
- **Score** 列には、クラスターの重心へのユークリッド距離を二乗した値の配列が含まれます。 配列の長さは、クラスターの数と同じです。

> [!NOTE]
> 入力データと予測データのクラス内の浮動小数点値を表すには、`float` 型を使います。

## <a name="define-data-and-model-paths"></a>データおよびモデルのパスを定義する

*Program.cs* ファイルに戻り、データ セット ファイルと、モデルを保存するファイルへのパスを保持するために、2 つのフィールドを追加します。

- `_dataPath` には、モデルのトレーニングに使用するデータ セットがあるファイルへのパスが含まれます。
- `_modelPath` には、トレーニング済みモデルが格納されるファイルへのパスが含まれます。

`Main` メソッドのすぐ上に次のコードを追加して、それらのパスを指定します。

[!code-csharp[Initialize paths](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#1)]

上記のコードをコンパイルするには、*Program.cs* ファイルの先頭に次の `using` ディレクティブを追加します。

[!code-csharp[Add usings for paths](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#2)]

## <a name="create-a-learning-pipeline"></a>学習パイプラインを作成する

以下の追加の `using` ディレクティブを、*Program.cs* ファイルの先頭に追加します。

[!code-csharp[Add Microsoft.ML usings](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#3)]

`Main` メソッドで、`Console.WriteLine("Hello World!")` を次のコードに置き換えます。

[!code-csharp[Call the Train method](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#4)]

`Train` メソッドは、モデルをトレーニングします。 `Main` メソッドのすぐ下に、次のコードを使ってそのメソッドを作成します。

```csharp
private static PredictionModel<IrisData, ClusterPrediction> Train()
{

}
```

学習パイプラインは、モデルのトレーニングに必要なすべてのデータとアルゴリズムを読み込みます。 `Train` メソッドに次のコードを追加します。

[!code-csharp[Initialize pipeline](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#5)]

## <a name="load-and-transform-data"></a>データを読み込んで変換する

実行する最初のステップでは、トレーニング データ セットを読み込みます。 ここでは、トレーニング データ セットは、`_dataPath` フィールドによってパスが定義されるテキスト ファイルに格納されます。 ファイル内の列はコンマ (",") で区切られます。 `Train` メソッドに次のコードを追加します。

[!code-csharp[Add step to load data](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#6)]

次のステップでは、<xref:Microsoft.ML.Transforms.ColumnConcatenator> 変換クラスを使用して、すべての特徴列を **Features** 列に結合します。 既定では、学習アルゴリズムは **Features** 列の特徴のみを処理します。 次のコードを追加します。

[!code-csharp[Add step to concatenate columns](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#7)]

## <a name="choose-a-learning-algorithm"></a>学習アルゴリズムを選択する

データをパイプラインに追加して正しい入力形式に変換したら、学習アルゴリズム (**ラーナー**) を選択します。 ラーナーはモデルをトレーニングします。 ML.NET が提供する <xref:Microsoft.ML.Trainers.KMeansPlusPlusClusterer> ラーナーでは、初期クラスターの重心を選択するメソッドが改良された [k 平均法アルゴリズム](https://en.wikipedia.org/wiki/K-means_clustering)が実装されています。

前の手順で追加したデータ処理コードの後にある `Train` メソッドに次のコードを追加します。

[!code-csharp[Add a learner step](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#8)]

<xref:Microsoft.ML.Trainers.KMeansPlusPlusClusterer.K?displayProperty=nameWithType> プロパティを使ってクラスターの数を指定します。 上記のコードでは、データ セットを 3 つのクラスターに分割することが指定されています。

## <a name="train-the-model"></a>モデルをトレーニングする

前のセクションで追加した手順では、トレーニング用にパイプラインを準備しましたが、トレーニングは実行されていません。 `pipeline.Train<TInput, TOutput>` メソッドは、`TInput` 型のインスタンスを取り込んで `TOutput` 型のインスタンスを出力するモデルを生成します。 `Train` メソッドに次のコードを追加します。

[!code-csharp[Train the model and return](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#9)]

### <a name="save-the-model"></a>モデルを保存する

この時点で、既存または新規のどの .NET アプリケーションにも統合できるモデルができました。 モデルを .zip ファイルに保存するには、`Main` メソッドで `Train` メソッドを呼び出している場所の下に、次のコードを追加します。

[!code-csharp[Save the model](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#10)]

`Main` メソッドで `await` を使用する場合は、`Main` メソッドに `async` 修飾子が必要です。このメソッドは `Task` を返す必要があります。

[!code-csharp[Make the Main method async](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#11)]

また、*Program.cs* ファイルの先頭に次の `using` ディレクティブを追加する必要もあります。

[!code-csharp[Add System.Threading.Tasks using](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#12)]

`async Main` メソッドは C# 7.1 に追加された機能であり、プロジェクトの既定の言語バージョンは C# 7.0 であるため、言語バージョンを C# 7.1 以降に変更する必要があります。 そのためには、**ソリューション エクスプローラー**でプロジェクト ノードを右クリックして、**[プロパティ]** を選択します。 **[ビルド]** タブを選択し、**[詳細設定]** ボタンを選択します。 ドロップダウンで **[C# 7.1]** (またはそれ以降のバージョン) を選択します。 **[OK]** ボタンを選択します。

## <a name="use-the-model-for-predictions"></a>モデルを使用して予測を行う

テスト データのインスタンスを格納するための `TestIrisData` クラスを作成します。

1. **ソリューション エクスプローラー**で、プロジェクトを右クリックし、**[追加]** > **[新しい項目]** を選択します。
1. **[新しい項目の追加]** ダイアログ ボックスで、**[クラス]** を選択し、**[名前]** フィールドを「*TestIrisData.cs*」に変更します。 次に、**[追加]** を選択します。
1. 次の例に示すように、静的になるようにクラスを変更します。

   [!code-csharp[Make class static](../../../samples/machine-learning/tutorials/IrisClustering/TestIrisData.cs#1)]

このチュートリアルでは、このクラスで 1 つのあやめのデータ インスタンスを示します。 他のシナリオを追加してモデルで実験できます。 `TestIrisData` クラスに次のコードを追加します。

[!code-csharp[Test data](../../../samples/machine-learning/tutorials/IrisClustering/TestIrisData.cs#2)]

指定した項目が属するクラスターを発見するには、*Program.cs* ファイルに戻り、次のコードを `Main` メソッドに追加します。

[!code-csharp[Predict and output results](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#13)]

プログラムを実行し、指定したデータ インスタンスが含まれるクラスターと、そのインスタンスからクラスターの重心までの平方距離を確認します。 結果は以下のようになるはずです。 パイプラインの処理により、警告または処理メッセージが表示される場合があります。 わかりやすくするために、それらは次の出力から削除してあります。

```text
Cluster: 2
Distances: 0.4192338 0.0008847713 0.9660053
```

おめでとうございます!  これで、アヤメのクラスタリングの機械学習モデルを作成し、それを使用して予測を行うことができました。 このチュートリアルのソース コードは、[dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/IrisClustering) GitHub リポジトリで確認できます。

## <a name="next-steps"></a>次の手順

このチュートリアルでは、次の作業を行う方法を学びました。
> [!div class="checklist"]
> - 問題を把握する
> - 適切な機械学習タスクを選択する
> - データを準備する
> - データを読み込んで変換する
> - 学習アルゴリズムを選択する
> - モデルをトレーニングする
> - モデルを使用して予測を行う

学習を続けてその他のサンプルを確認するには、GitHub リポジトリをご覧ください。
> [!div class="nextstepaction"]
> [dotnet/machinelearning GitHub リポジトリ](https://github.com/dotnet/machinelearning/)
