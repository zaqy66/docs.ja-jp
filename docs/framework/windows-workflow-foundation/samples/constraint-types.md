---
title: 制約の種類
ms.date: 03/30/2017
ms.assetid: b6b246e6-1130-4698-9625-c5c42abcbfed
ms.openlocfilehash: 202a2c7b3a3fc400552e42c8606457964af66af2
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43401533"
---
# <a name="constraint-types"></a>制約の種類
このサンプルでは、ワークフローに制約を適用する 2 種類の方法を示します。1 つはアクティビティの内部 (ビルド) から適用する方法で、もう 1 つはアクティビティの外部 (ポリシー) から適用する方法です。 このシナリオでは、(サードパーティのソフトウェア会社の) アクティビティ作成者が 2 つの引数間のリレーションシップを検証します。 ここでは、コストが価格以下になるようにする必要があります。 これは、一般的な検証ビルド制約です。  
  
 次に、ショップ オーナーがこの一般的なアクティビティに検証を追加します。 ここでは、製品のほとんどを $9.99 以下にします。 したがって、`CreateProduct` アクティビティに基づくポリシー制約を使用します。  
  
 このサンプルでは、次の操作を行います。  
  
 アクティビティ作成者 (ビルド) は、次を行う必要があります。  
  
-   制約 (`PriceGreaterThanCost`) を作成します。 ここには、すべての検証ロジックが存在します。  
  
-   `System.Activities.CodeActivity.OnGetConstraints()` をオーバーライドし、制約 (`PriceGreaterThanCost`) を制約 <xref:System.Collections.IList> に追加します。  
  
 ワークフロー作成者 (ポリシー) は、次を行う必要があります。  
  
-   検証するアクティビティのインスタンスを含むワークフローを作成します (`CreateProduct`)。  
  
-   制約 (`MaxPrice`) を作成します。  
  
-   <xref:System.Activities.Validation.ValidationSettings> インスタンス (`validationSettings`) を作成し、制約 (`MaxPrice`) をコレクション `AdditionalConstraints` に追加します。 ここで、ワークフロー作成者は、シーケンスや並列などのアクティビティにポリシー制約を追加できます。  
  
-   <xref:System.Activities.Validation.ActivityValidationServices.Validate%2A> を呼び出すと、<xref:System.Activities.Validation.ValidationResults> オブジェクトの <xref:System.Activities.Validation.ValidationError> コレクションが返されます。  
  
-   (省略可能) <xref:System.Activities.Validation.ValidationError> オブジェクトを出力します。  
  
### <a name="to-set-up-build-and-run-the-sample"></a>サンプルをセットアップ、ビルド、および実行するには  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] で ConstraintTypes.sln サンプル ソリューションを開きます。  
  
2.  ソリューションをビルドして実行します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\Validation\ConstraintLibrary`