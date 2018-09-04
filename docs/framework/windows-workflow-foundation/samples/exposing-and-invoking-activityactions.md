---
title: ActivityAction の公開と呼び出し
ms.date: 03/30/2017
ms.assetid: 97ce4797-426e-463d-9cc4-1261afad6df4
ms.openlocfilehash: f36d88fc54e5150927113ed8825fbccad84129d4
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43520124"
---
# <a name="exposing-and-invoking-activityactions"></a>ActivityAction の公開と呼び出し
このサンプルでは、<xref:System.Activities.ActivityAction> を含むカスタム アクティビティを開発する方法を示します。 また、<xref:System.Activities.ActivityAction> の実装を提供して、このアクティビティを使用する方法も示します。  
  
 <xref:System.Activities.ActivityAction> 「ホール」特定のシグネチャを持つアクティビティのユーザーがカスタム動作にプラグインできるを公開するアクティビティの作成者を許可します。 たとえば、 <!--zz <xref:System.Activities.Statements.ForEach>--> `System.Activities.Statements.ForEach`アクティビティが (で動作します項目のコレクション)、<xref:System.Activities.ActivityAction>アクティビティのユーザーの操作対象のイテレーションの現在の項目の動作をプラグインできるようにします。  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>サンプルをセットアップ、ビルド、および実行するには  
  
1.  開く、 **ActivityAction.sln**サンプル ソリューション[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]します。  
  
2.  ソリューションをビルドして実行します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\Code-Bodied\ActivityAction`