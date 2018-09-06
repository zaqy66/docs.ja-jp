---
title: 'チュートリアル : 拡張性のあるアプリケーションの作成'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- views [.NET Framework], add-in pipeline
- host-side adapters for add-ins [.NET Framework]
- add-in pipeline [.NET Framework], creating
- add-in-side adapter [.NET Framework]
- contracts for add-in pipelines [.NET Framework]
ms.assetid: 694a33c5-a040-450d-aed5-ac49fc88ce61
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5d2aaeaffaf3abbe1e8efcdb57d40e6ae60f89b5
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43875097"
---
# <a name="walkthrough-creating-an-extensible-application"></a>チュートリアル : 拡張性のあるアプリケーションの作成
このチュートリアルでは、簡単な計算機機能を実行するアドインのパイプラインを作成する方法について説明します。 実際のシナリオは含まれていません代わりに、パイプラインとアドインを追加できるようにするホストのサービスの基本的な機能を示します。  
  
 このチュートリアルでは、次のタスクについて説明します。  
  
-   Visual Studio ソリューションを作成します。  
  
-   パイプライン ディレクトリ構造を作成します。  
  
-   ビューのコントラクトを作成します。  
  
-   追加アドイン側アダプターを作成します。  
  
-   ホスト側アダプターを作成します。  
  
-   ホストを作成します。  
  
-   アドインを作成します。  
  
-   パイプラインをデプロイします。  
  
-   ホスト アプリケーションを実行します。  
  
 このパイプラインは、シリアル化可能な型のみを渡します (<xref:System.Double>と<xref:System.String>)、ホストとアドイン間。 複雑なデータ型のコレクションを渡す方法を示す例を参照してください[チュートリアル: ホスト間でコレクションを渡すと、アドイン](https://msdn.microsoft.com/library/b532c604-548e-4fab-b11c-377257dd0ee5)します。  
  
 このパイプラインのコントラクトは、算術演算の 4 つのオブジェクト モデルを定義します。 追加、減算、乗算、および除算します。 ホストからアドインなど、2 + 2 を計算する数式れ、アドインのホストに結果を返します。  
  
 計算ツール アドインのバージョン 2 より高度を示し、バージョン管理を示します。 説明されている、[チュートリアル: 変更のホストとしての旧バージョンとの互換性を有効にする](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848)します。  
  
## <a name="prerequisites"></a>必須コンポーネント  
 このチュートリアルを完了するための要件は次のとおりです。  
  
-   Visual Studio  
  
## <a name="creating-a-visual-studio-solution"></a>Visual Studio ソリューションを作成します。  
 Visual Studio でソリューションを使用して、パイプライン セグメントのプロジェクトが含まれます。  
  
#### <a name="to-create-the-pipeline-solution"></a>パイプラインのソリューションを作成するには  
  
1.  Visual Studio で、という名前の新しいプロジェクトを作成`Calc1Contract`です。 基に、**クラス ライブラリ**テンプレート。  
  
2.  ソリューションの名前を`CalculatorV1`します。  
  
## <a name="creating-the-pipeline-directory-structure"></a>パイプライン ディレクトリ構造を作成します。  
 アドイン モデルでは、指定したディレクトリ構造に配置するパイプライン セグメントのアセンブリが必要です。 パイプラインの構造の詳細については、次を参照してください。[パイプライン開発の必要条件](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)します。  
  
#### <a name="to-create-the-pipeline-directory-structure"></a>パイプライン ディレクトリ構造を作成するには  
  
1.  コンピューターに任意の場所、アプリケーション フォルダーを作成します。  
  
2.  、そのフォルダー内には、次の構造を作成します。  
  
    ```  
    Pipeline  
      AddIns  
        CalcV1  
        CalcV2  
      AddInSideAdapters  
      AddInViews  
      Contracts  
      HostSideAdapters  
    ```  
  
     アプリケーション フォルダー内のパイプラインのフォルダー構造を配置する必要はありません。それは利便性のためにはここで行われます。 適切な手順、チュートリアルのパイプライン フォルダー構造が別の場所にある場合は、コードを変更する方法について説明します。 パイプライン ディレクトリ要件の説明を参照[パイプライン開発の必要条件](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)します。  
  
    > [!NOTE]
    >  `CalcV2`フォルダーは、このチュートリアルでは使用されません。 のプレース ホルダーは[チュートリアル: 変更のホストとしての旧バージョンとの互換性を有効にする](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848)します。  
  
## <a name="creating-the-contract-and-views"></a>コントラクトとビューの作成  
 このパイプラインのコントラクト セグメントの定義、`ICalc1Contract`を 4 つのメソッドを定義するインターフェイス: `add`、 `subtract`、 `multiply`、および`divide`します。  
  
#### <a name="to-create-the-contract"></a>コントラクトを作成するには  
  
1.  という名前の Visual Studio ソリューションで`CalculatorV1`、オープン、`Calc1Contract`プロジェクト。  
  
2.  **ソリューション エクスプ ローラー**には、次のアセンブリへの参照を追加、`Calc1Contract`プロジェクト。  
  
     System.AddIn.Contract.dll  
  
     System.AddIn.dll  
  
3.  **ソリューション エクスプ ローラー**、新規に追加される既定のクラスを除外する**クラス ライブラリ**プロジェクト。  
  
4.  **ソリューション エクスプ ローラー**、プロジェクトに新しい項目の追加を使用して、**インターフェイス**テンプレート。 **新しい項目の追加**ダイアログ ボックスで、インターフェイスの名前`ICalc1Contract`します。  
  
5.  インターフェイスのファイルの名前空間参照を追加<xref:System.AddIn.Contract>と<xref:System.AddIn.Pipeline>します。  
  
6.  このコントラクト セグメントを完了するのにには、次のコードを使用します。 このインターフェイスがありますに注意してください、<xref:System.AddIn.Pipeline.AddInContractAttribute>属性。  
  
     [!code-csharp[AddInP1Contract#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1Contract/cs/ICalc1Contract.cs#1)]
     [!code-vb[AddInP1Contract#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1Contract/vb/ICalc1Contract.vb#1)]  
  
7.  必要に応じて、Visual Studio ソリューションをビルドします。 最後の手順が、各手順は、各プロジェクトがあることを確認した後にビルドが修正されるまでは、ソリューションを実行することはできません。  
  
 アドイン ビューとホストの表示のため、アドインをアドインでの最初のバージョンで特に通常同じコードを持つ、同時に、ビューを簡単に作成することができます。 1 要素のみが異なる: アドイン ビューが必要です、<xref:System.AddIn.Pipeline.AddInBaseAttribute>属性は、アドインのホスト ビューですべての属性が必要ありません。  
  
#### <a name="to-create-the-add-in-view"></a>アドイン ビューを作成するには  
  
1.  という名前の新しいプロジェクトを追加`Calc1AddInView`を`CalculatorV1`ソリューション。 基に、**クラス ライブラリ**テンプレート。  
  
2.  **ソリューション エクスプ ローラー**に System.AddIn.dll への参照を追加、`Calc1AddInView`プロジェクト。  
  
3.  **ソリューション エクスプ ローラー**、新規に追加される既定のクラスを除外する**クラス ライブラリ**プロジェクト、およびプロジェクトに新しい項目の追加を使用して、**インターフェイス**テンプレート。 **新しい項目の追加**ダイアログ ボックスで、インターフェイスの名前`ICalculator`します。  
  
4.  インターフェイスのファイルへの参照を名前空間を追加します。<xref:System.AddIn.Pipeline>します。  
  
5.  このアドインのビューを完了するのにには、次のコードを使用します。 このインターフェイスがありますに注意してください、<xref:System.AddIn.Pipeline.AddInBaseAttribute>属性。  
  
     [!code-csharp[AddInP1AddInViews#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1AddInViews/cs/Calc1AddInView.cs#1)]
     [!code-vb[AddInP1AddInViews#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1AddInViews/vb/Calc1AddInView.vb#1)]  
  
6.  必要に応じて、Visual Studio ソリューションをビルドします。  
  
#### <a name="to-create-the-host-view-of-the-add-in"></a>アドインのホスト ビューを作成するには  
  
1.  という名前の新しいプロジェクトを追加`Calc1HVA`を`CalculatorV1`ソリューション。 基に、**クラス ライブラリ**テンプレート。  
  
2.  **ソリューション エクスプ ローラー**、新規に追加される既定のクラスを除外する**クラス ライブラリ**プロジェクト、およびプロジェクトに新しい項目の追加を使用して、**インターフェイス**テンプレート。 **新しい項目の追加**ダイアログ ボックスで、インターフェイスの名前`ICalculator`します。  
  
3.  インターフェイス ファイルに次のコードを使用して、アドインのホスト ビューを完了します。  
  
     [!code-csharp[AddInP1HVA#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1HVA/cs/calc1hva.cs#1)]
     [!code-vb[AddInP1HVA#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1HVA/vb/Calc1HVA.vb#1)]  
  
4.  必要に応じて、Visual Studio ソリューションをビルドします。  
  
## <a name="creating-the-add-in-side-adapter"></a>アドイン側アダプターを作成します。  
 このアドイン側アダプターは、1 つのビューからコントラクトへのアダプターで構成されます。 このパイプライン セグメントは、型をアドイン ビューからコントラクトに変換します。  
  
 このパイプラインで、アドイン、ホストにサービスを提供します。 と種類が、アドインからホストにフローします。 ホストからアドインへの種類がフローしないために、このパイプラインのアドイン側のコントラクトからビューへのアダプターを含める必要はありません。  
  
#### <a name="to-create-the-add-in-side-adapter"></a>追加アドイン側アダプターを作成するには  
  
1.  という名前の新しいプロジェクトを追加`Calc1AddInSideAdapter`を`CalculatorV1`ソリューション。 基に、**クラス ライブラリ**テンプレート。  
  
2.  **ソリューション エクスプ ローラー**には、次のアセンブリへの参照を追加、`Calc1AddInSideAdapter`プロジェクト。  
  
     System.AddIn.dll  
  
     System.AddIn.Contract.dll  
  
3.  隣接するパイプライン セグメントのプロジェクトへのプロジェクト参照を追加します。  
  
     `Calc1AddInView`  
  
     `Calc1Contract`  
  
4.  各プロジェクト参照を選択し、**プロパティ**設定**ローカル コピー**に**False**します。 Visual Basic で使用して、**参照** タブの**プロジェクトのプロパティ**を設定する**ローカル コピー**に**False**の 2 つのプロジェクト参照。  
  
5.  プロジェクトの既定のクラスの名前を変更`CalculatorViewToContractAddInSideAdapter`します。  
  
6.  クラス ファイルで名前空間参照を追加<xref:System.AddIn.Pipeline>します。  
  
7.  クラス ファイルで、隣接するセグメントの名前空間の参照を追加します:`CalcAddInViews`と`CalculatorContracts`します。 (この名前空間の参照は、Visual basic で`Calc1AddInView.CalcAddInViews`と`Calc1Contract.CalculatorContracts`Visual Basic プロジェクトで既定の名前空間をオフにしている場合を除き、します)。  
  
8.  適用、<xref:System.AddIn.Pipeline.AddInAdapterAttribute>属性を`CalculatorViewToContractAddInSideAdapter`クラスに追加アドイン側アダプターとして識別します。  
  
9. ように、`CalculatorViewToContractAddInSideAdapter`クラスを継承<xref:System.AddIn.Pipeline.ContractBase>の既定の実装を提供する、<xref:System.AddIn.Contract.IContract>インターフェイス、およびパイプラインのコントラクト インターフェイスを実装して`ICalc1Contract`します。  
  
10. 受け取るパブリック コンス トラクターを追加、`ICalculator`というプライベート フィールドにキャッシュ、および、基底クラスのコンス トラクターを呼び出します。  
  
11. メンバーを実装する`ICalc1Contract`の対応するメンバーを呼び出すだけです、`ICalculator`インスタンスをコンス トラクターに渡され、結果を返します。 これは、ビューを適応 (`ICalculator`)、コントラクト (`ICalc1Contract`)。  
  
     次のコードでは、完成した追加アドイン側アダプターを示します。  
  
     [!code-csharp[AddInP1AddInSideAdapters#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1AddInSideAdapters/cs/Calc1ViewToContractAddInSideAdapter.cs#1)]
     [!code-vb[AddInP1AddInSideAdapters#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1AddInSideAdapters/vb/Calc1ViewToContractAddInSideAdapter.vb#1)]  
  
12. 必要に応じて、Visual Studio ソリューションをビルドします。  
  
## <a name="creating-the-host-side-adapter"></a>ホスト側アダプターを作成します。  
 このホスト側アダプターは、1 つのコントラクトからビューへのアダプターで構成されます。 このセグメントでは、コントラクトのアドインのホスト ビューを適合させます。  
  
 このパイプラインでは、アドインのホストと型フローにサービスをホストにアドインから提供します。 ホストからアドインへの種類がフローしないために、ビューからコントラクトへのアダプターを含める必要はありません。  
  
 有効期間管理を実装するには、使用、<xref:System.AddIn.Pipeline.ContractHandle>コントラクトに有効期間トークンをアタッチするオブジェクト。 有効期間管理を機能させるために、このハンドルへの参照を維持する必要があります。 トークンが適用されると、追加のプログラミングは必要ありませんのでは使用しなくなったとガベージ コレクションで利用できるように、アドイン システムがオブジェクトの破棄できます。 詳細については、次を参照してください。[有効期間管理](https://msdn.microsoft.com/library/57a9c87e-394c-4fef-89f2-aa4223a2aeb5)します。  
  
#### <a name="to-create-the-host-side-adapter"></a>ホスト側アダプターを作成するには  
  
1.  という名前の新しいプロジェクトを追加`Calc1HostSideAdapter`を`CalculatorV1`ソリューション。 基に、**クラス ライブラリ**テンプレート。  
  
2.  **ソリューション エクスプ ローラー**には、次のアセンブリへの参照を追加、`Calc1HostSideAdapter`プロジェクト。  
  
     System.AddIn.dll  
  
     System.AddIn.Contract.dll  
  
3.  隣接するセグメントのプロジェクトへのプロジェクト参照を追加します。  
  
     `Calc1Contract`  
  
     `Calc1HVA`  
  
4.  各プロジェクト参照を選択し、**プロパティ**設定**ローカル コピー**に**False**します。 Visual Basic で使用して、**参照** タブの**プロジェクトのプロパティ**を設定する**ローカル コピー**に**False**の 2 つのプロジェクト参照。  
  
5.  プロジェクトの既定のクラスの名前を変更`CalculatorContractToViewHostSideAdapter`します。  
  
6.  クラス ファイルで名前空間参照を追加<xref:System.AddIn.Pipeline>します。  
  
7.  クラス ファイルで、隣接するセグメントの名前空間の参照を追加します:`CalcHVAs`と`CalculatorContracts`します。 (この名前空間の参照は、Visual basic で`Calc1HVA.CalcHVAs`と`Calc1Contract.CalculatorContracts`Visual Basic プロジェクトで既定の名前空間をオフにしている場合を除き、します)。  
  
8.  適用、<xref:System.AddIn.Pipeline.HostAdapterAttribute>属性を`CalculatorContractToViewHostSideAdapter`クラス、ホスト側アダプター セグメントとして識別します。  
  
9. ように、`CalculatorContractToViewHostSideAdapter`クラスで、追加のホスト ビューを表すインターフェイスを実装: `Calc1HVAs.ICalculator` (`Calc1HVA.CalcHVAs.ICalculator` Visual Basic で)。  
  
10. パイプラインのコントラクトの型を受け取るパブリック コンス トラクターを追加`ICalc1Contract`します。 コンス トラクターは、コントラクトへの参照をキャッシュする必要があります。 作成し、新しいキャッシュも<xref:System.AddIn.Pipeline.ContractHandle>、コントラクトのアドインの有効期間を管理します。  
  
    > [!IMPORTANT]
    >  <xref:System.AddIn.Pipeline.ContractHandle>有効期間管理に不可欠です。 参照の保持に失敗した場合、<xref:System.AddIn.Pipeline.ContractHandle>オブジェクトのガベージ コレクションによって回収され、プログラムで想定されていないときに、パイプラインはシャット ダウンします。 など、診断が困難なエラーが生じる<xref:System.AppDomainUnloadedException>します。 シャット ダウンは、パイプラインの有効期間のステージは通常この条件は、エラーを検出するために、有効期間管理コードの方法はありません。  
  
11. メンバーを実装する`ICalculator`の対応するメンバーを呼び出すだけです、`ICalc1Contract`インスタンスをコンス トラクターに渡され、結果を返します。 これは、コントラクトを適応 (`ICalc1Contract`) ビューに (`ICalculator`)。  
  
     次のコードでは、完成したホスト側アダプターを示します。  
  
     [!code-csharp[AddInP1HostSideAdapters#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1HostSideAdapters/cs/Calc1ContractToViewHostSideAdapter.cs#1)]
     [!code-vb[AddInP1HostSideAdapters#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1HostSideAdapters/vb/Calc1ContractToViewHostSideAdapter.vb#1)]  
  
12. 必要に応じて、Visual Studio ソリューションをビルドします。  
  
## <a name="creating-the-host"></a>ホストの作成  
 ホスト アプリケーションは、アドインのホスト ビュー アドインと対話します。 アドインの検出とアクティブ化によって提供されるメソッドを使用して、<xref:System.AddIn.Hosting.AddInStore>と<xref:System.AddIn.Hosting.AddInToken>クラスは、次の操作します。  
  
-   パイプラインとアドインの情報のキャッシュを更新します。  
  
-   ホスト ビューの種類のアドインの検索`ICalculator`、指定したパイプラインのルート ディレクトリの下。  
  
-   アドインを使用する指定を求めるボックスをオンにします。  
  
-   指定したセキュリティ信頼レベルで新しいアプリケーション ドメインでの選択のアドインをアクティブ化します。  
  
-   カスタム実行`RunCalculator`メソッドで、アドインのホスト ビューで指定されたアドインのメソッドを呼び出します。  
  
#### <a name="to-create-the-host"></a>ホストを作成するには  
  
1.  という名前の新しいプロジェクトを追加`Calc1Host`を`CalculatorV1`ソリューション。 基に、**コンソール アプリケーション**テンプレート。  
  
2.  **ソリューション エクスプ ローラー**、System.AddIn.dll アセンブリへの参照を追加、`Calc1Host`プロジェクト。  
  
3.  プロジェクト参照を追加、`Calc1HVA`プロジェクト。 プロジェクト参照を選択し、**プロパティ**設定**ローカル コピー**に**False**します。 Visual Basic で使用して、**参照**のタブ**プロジェクトのプロパティ**を設定する**ローカル コピー**に**False**します。  
  
4.  クラス ファイル (Visual Basic でのモジュール) の名前を変更`MathHost1`します。  
  
5.  Visual Basic で使用して、**アプリケーション**のタブ、**プロジェクト プロパティ**ダイアログ ボックスを設定**スタートアップ オブジェクト**に**Sub Main**します。  
  
6.  そのクラスまたはモジュール ファイルに名前空間参照を追加<xref:System.AddIn.Hosting>します。  
  
7.  クラスまたはモジュール ファイルで、アドインのホスト ビューの名前空間参照を追加:`CalcHVAs`します。 (Visual Basic の場合は、この名前空間のリファレンスは`Calc1HVA.CalcHVAs`Visual Basic プロジェクトで既定の名前空間をオフにしている場合を除き、します)。  
  
8.  **ソリューション エクスプ ローラー**、ソリューションの選択との間、**プロジェクト**メニュー**プロパティ**。 **ソリューション プロパティ ページ**ダイアログ ボックスで、セット、**シングル スタートアップ プロジェクト**をこのホスト アプリケーション プロジェクト。  
  
9. クラスまたはモジュール ファイルを使用、<xref:System.AddIn.Hosting.AddInStore.Update%2A?displayProperty=nameWithType>メソッド キャッシュを更新します。 使用して、<xref:System.AddIn.Hosting.AddInStore.FindAddIn%2A?displayProperty=nameWithType>メソッドを使用して、トークンのコレクションを取得、<xref:System.AddIn.Hosting.AddInToken.Activate%2A?displayProperty=nameWithType>アドインをアクティブ化するメソッド。  
  
     次のコードでは、完全なホスト アプリケーションを示します。  
  
     [!code-csharp[AddInP1Host#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1Host/cs/MathHost1.cs#1)]
     [!code-vb[AddInP1Host#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1Host/vb/MathHost1.vb#1)]  
  
    > [!NOTE]
    >  このコードでは、パイプラインのフォルダー構造がアプリケーション フォルダー内にあることを前提としています。 他の場所で配置する場合は、設定するコードの行を変更、`addInRoot`変数、変数が、パイプライン ディレクトリ構造へのパスが含まれるようにします。  
  
     コードを使用して、`ChooseCalculator`メソッドをトークンを一覧表示し、アドインを選択するユーザーに確認します。 `RunCalculator`メソッドは、単純な算術式のユーザーに求めますを使用して式を解析し、`Parser`クラス、さらに、アドインによって返される結果が表示されます。  
  
10. 必要に応じて、Visual Studio ソリューションをビルドします。  
  
## <a name="creating-the-add-in"></a>アドインを作成します。  
 アドインをアドイン ビューによって指定されたメソッドを実装します。 このアドインでは、実装、 `Add`、 `Subtract`、 `Multiply`、および`Divide`操作し、ホストに、結果を返します。  
  
#### <a name="to-create-the-add-in"></a>アドインを作成するには  
  
1.  という名前の新しいプロジェクトを追加`AddInCalcV1`を`CalculatorV1`ソリューション。 基に、**クラス ライブラリ**テンプレート。  
  
2.  **ソリューション エクスプ ローラー**、System.AddIn.dll アセンブリへの参照をプロジェクトに追加します。  
  
3.  プロジェクト参照を追加、`Calc1AddInView`プロジェクト。 プロジェクト参照を選択し、**プロパティ**設定**ローカル コピー**に**False**します。 Visual Basic で使用して、**参照**のタブ**プロジェクトのプロパティ**を設定する**ローカルにコピー**に**False**プロジェクト参照。  
  
4.  クラスの名前変更`AddInCalcV1`します。  
  
5.  クラス ファイルで名前空間への参照を追加<xref:System.AddIn>およびアドイン ビュー セグメント: `CalcAddInViews` (`Calc1AddInView.CalcAddInViews` Visual Basic で)。  
  
6.  適用、<xref:System.AddIn.AddInAttribute>属性を`AddInCalcV1`アドインとしてクラスを識別するために、クラス。  
  
7.  ように、`AddInCalcV1`アドイン ビューを表すインターフェイスを実装するクラス。 `CalcAddInViews.ICalculator` (`Calc1AddInView.CalcAddInViews.ICalculator` Visual Basic で)。  
  
8.  メンバーを実装する`ICalculator`適切な計算の結果を返すことによって。  
  
     完了したアドインの次のコードを示しています。  
  
     [!code-csharp[AddInP1AddInCalcV1#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1AddInCalcV1/cs/AddInCalcV1.cs#1)]
     [!code-vb[AddInP1AddInCalcV1#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1AddInCalcV1/vb/AddInCalcV1.vb#1)]  
  
9. 必要に応じて、Visual Studio ソリューションをビルドします。  
  
## <a name="deploying-the-pipeline"></a>パイプラインを展開します。  
 ビルドし、必要なパイプライン ディレクトリ構造に追加のセグメントをデプロイする準備が整いました。  
  
#### <a name="to-deploy-the-segments-to-the-pipeline"></a>パイプライン セグメントをデプロイするには  
  
1.  ソリューション内の各プロジェクトを使用して、**ビルド**タブ**プロジェクトのプロパティ**(、**コンパイル**Visual Basic でのタブ) の値を設定する、**出力パス** (、**ビルド出力パス**Visual Basic で)。 アプリケーションのフォルダーの名前を付けた場合`MyApp`、次のフォルダーに、プロジェクトのビルドはたとえば。  
  
    |プロジェクト|パス|  
    |-------------|----------|  
    |AddInCalcV1|MyApp\Pipeline\AddIns\CalcV1|  
    |Calc1AddInSideAdapter|MyApp\Pipeline\AddInSideAdapters|  
    |Calc1AddInView|MyApp\Pipeline\AddInViews|  
    |Calc1Contract|MyApp\Pipeline\Contracts|  
    |Calc1Host|MyApp|  
    |Calc1HostSideAdapter|MyApp\Pipeline\HostSideAdapters|  
    |Calc1HVA|MyApp|  
  
    > [!NOTE]
    >  パイプライン フォルダー構造をアプリケーション フォルダー以外の場所に配置した場合は、それに応じて、テーブルのパスを変更する必要があります。 パイプライン ディレクトリ要件の説明を参照[パイプライン開発の必要条件](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)します。  
  
2.  Visual Studio ソリューションをビルドします。  
  
3.  アセンブリが適切なディレクトリにコピーされたことと、アセンブリの余分なコピーが正しくないフォルダーにインストールされていないことを確認するアプリケーションとパイプラインのディレクトリを確認します。  
  
    > [!NOTE]
    >  変更していない場合**ローカル コピー**に**False**の`Calc1AddInView`プロジェクトで参照、`AddInCalcV1`プロジェクト、ローダー コンテキストの問題により、アドインに配置されているからです。  
  
     パイプラインを展開する方法の詳細については、次を参照してください。[パイプライン開発の必要条件](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)します。  
  
## <a name="running-the-host-application"></a>ホスト アプリケーションの実行  
 ホストを実行し、アドインを操作する準備が整いました。  
  
#### <a name="to-run-the-host-application"></a>ホスト アプリケーションを実行するには  
  
1.  コマンド プロンプトで、アプリケーション ディレクトリに移動し、ホスト アプリケーションを実行`Calc1Host.exe`します。  
  
2.  ホストは、すべて使用可能なアドインの型を検索し、アドインを選択するように求められます。 入力**1** for のみ使用可能なアドイン。  
  
3.  計算の数式を入力**2 + 2**します。 数字と演算子の間にスペースが必要があります。  
  
4.  型**終了**キーを押すと、 **」と入力**キー アプリケーションを終了します。  
  
## <a name="see-also"></a>関連項目  
 [チュートリアル: ホスト変更時の下位互換性を有効にします。](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848)  
 [チュートリアル: アドインとホスト間でコレクションの引き渡し](https://msdn.microsoft.com/library/b532c604-548e-4fab-b11c-377257dd0ee5)  
 [パイプライン開発の必要条件](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)  
 [コントラクト、ビュー、およびアダプター](https://msdn.microsoft.com/library/a6460173-9507-4b87-8c07-d4ee245d715c)  
 [パイプライン開発](../../../docs/framework/add-ins/pipeline-development.md)
