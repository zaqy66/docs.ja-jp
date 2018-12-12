---
title: テキスト ファイルではないデータで機械学習モデルをトレーニングする - ML.NET
description: ML.NET を使用して、機械学習モデルのトレーニングのために非ファイル トレーニング データを予測パイプラインの一部として読み込む方法について説明します。
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: 971c5c62acc9dd7bf29aa11ce898c2b76822c3d7
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53125403"
---
# <a name="train-a-machine-learning-model-with-data-thats-not-in-a-text-file---mlnet"></a><span data-ttu-id="fb14c-103">テキスト ファイルではないデータで機械学習モデルをトレーニングする - ML.NET</span><span class="sxs-lookup"><span data-stu-id="fb14c-103">Train a machine learning model with data that's not in a text file - ML.NET</span></span>

<span data-ttu-id="fb14c-104">ML.NET で一般的に実証されているユース ケースは、`TextLoader` を使ってファイルからトレーニング データを読み取る方法です。</span><span class="sxs-lookup"><span data-stu-id="fb14c-104">The commonly demonstrated use case for ML.NET is use the `TextLoader` to read the training data from a file.</span></span>
<span data-ttu-id="fb14c-105">ただし、実際のトレーニングのシナリオでは、データは次のようなそれ以外の場所にある場合があります。</span><span class="sxs-lookup"><span data-stu-id="fb14c-105">However, in real-time training scenarios the data can be elsewhere, such as:</span></span>

* <span data-ttu-id="fb14c-106">SQL テーブル</span><span class="sxs-lookup"><span data-stu-id="fb14c-106">in SQL tables</span></span>
* <span data-ttu-id="fb14c-107">ログ ファイルから抽出</span><span class="sxs-lookup"><span data-stu-id="fb14c-107">extracted from log files</span></span>
* <span data-ttu-id="fb14c-108">その場で生成</span><span class="sxs-lookup"><span data-stu-id="fb14c-108">generated on the fly</span></span>

<span data-ttu-id="fb14c-109">[スキーマの理解](https://github.com/dotnet/machinelearning/tree/master/docs/code/SchemaComprehension.md)を使って、既存の C# `IEnumerable` を `DataView` として ML.NET に取り込みます。</span><span class="sxs-lookup"><span data-stu-id="fb14c-109">Use [schema comprehension](https://github.com/dotnet/machinelearning/tree/master/docs/code/SchemaComprehension.md) to bring an existing C# `IEnumerable` into ML.NET as a `DataView`.</span></span>

<span data-ttu-id="fb14c-110">この例では、顧客チャーン予測モデルを構築し、実稼動システムから次の機能を抽出します。</span><span class="sxs-lookup"><span data-stu-id="fb14c-110">For this example, you'll build the customer churn prediction model, and extract the following features from your production system:</span></span>

* <span data-ttu-id="fb14c-111">顧客の ID (モデルでは無視されます)</span><span class="sxs-lookup"><span data-stu-id="fb14c-111">Customer ID (ignored by the model)</span></span>
* <span data-ttu-id="fb14c-112">顧客が解約済みかどうか (ターゲット 'ラベル')</span><span class="sxs-lookup"><span data-stu-id="fb14c-112">Whether the customer has churned (the target 'label')</span></span>
* <span data-ttu-id="fb14c-113">'人口統計カテゴリ' ('ヤング アダルト' のような 1 つの文字列)</span><span class="sxs-lookup"><span data-stu-id="fb14c-113">The 'demographic category' (one string, like 'young adult' etc.)</span></span>
* <span data-ttu-id="fb14c-114">過去 5 日間のアクセス数</span><span class="sxs-lookup"><span data-stu-id="fb14c-114">The number of visits from the last 5 days.</span></span>

```csharp
private class CustomerChurnInfo
{
    public string CustomerID { get; set; }
    public bool HasChurned { get; set; }
    public string DemographicCategory { get; set; }
    // Visits during last 5 days, latest to newest.
    [VectorType(5)]
    public float[] LastVisits { get; set; }
}
```

<span data-ttu-id="fb14c-115">このデータを `DataView` に読み込み、次のコードを使用して、モデルをトレーニングします。</span><span class="sxs-lookup"><span data-stu-id="fb14c-115">Load this data into the `DataView` and train the model, using the following code:</span></span>

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging,
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Step one: read the data as an IDataView.
// Let's assume that 'GetChurnData()' fetches and returns the training data from somewhere.
IEnumerable<CustomerChurnInfo> churnData = GetChurnInfo();

// Turn the data into the ML.NET data view.
// We can use CreateDataView or CreateStreamingDataView, depending on whether 'churnData' is an IList,
// or merely an IEnumerable.
var trainData = mlContext.CreateStreamingDataView(churnData);

// Build the learning pipeline.
// In our case, we will one-hot encode the demographic category, and concatenate that with the number of visits.
// We apply our FastTree binary classifier to predict the 'HasChurned' label.

var pipeline = mlContext.Transforms.Categorical.OneHotEncoding("DemographicCategory")
    .Append(mlContext.Transforms.Concatenate("Features", "DemographicCategory", "LastVisits"))
    .Append(mlContext.BinaryClassification.Trainers.FastTree("HasChurned", "Features", numTrees: 20));

var model = pipeline.Fit(trainData);
```
