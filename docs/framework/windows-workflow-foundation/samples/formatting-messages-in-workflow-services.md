---
title: ワークフロー サービスでのメッセージの書式設定
ms.date: 03/30/2017
ms.assetid: 6d15d44b-20f8-4cb7-bd4f-598c32781ebc
ms.openlocfilehash: eb9a6b3a83a28154dc968bd4c1c41d34028bdd41
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44198973"
---
# <a name="formatting-messages-in-workflow-services"></a>ワークフロー サービスでのメッセージの書式設定
このサンプルでは、メッセージング アクティビティ (WF サービス) で使用できるユーザーの種類を示します。 サンプルのサービスは、簡単な費用承認サービスで、3 つの操作を公開します。 `ApproveExpense` はデータ コントラクト型を受け取り、既知の型を使用する方法を示します。 この操作では、費用の金額に基づいて `true` または `false` を返します。 `ApprovePO` XmlSerializer 型を受け取り、返します`true`または`false`経費量に基づいています。`ApprovedVendor` メッセージ コントラクト型を受け取り、返します`true`または`false`仕入先が、承認済みのベンダーの一覧にある場合、または要求が経理部 (finance 部門は、すべてのベンダーを使用できます) に付属している場合。  
  
#### <a name="to-use-this-sample"></a>このサンプルを使用するには  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] でプロジェクト ソリューションを読み込み、プロジェクトをビルドします。  
  
2.  最初に、[ソリューションの基本ディレクトリ]\FormatterService\bin\debug\ に生成されたサービスを実行します。  
  
3.  2 番目に、[ソリューションの基本ディレクトリ]\FormatterClient\bin\debug に生成されたクライアント アプリケーションを実行します。  
  
4.  クライアントは、サービスで 3 つの操作を呼び出し、結果を出力します。 完了したら、Enter キーを押してクライアントを終了し、サービスを終了します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\Formatter`