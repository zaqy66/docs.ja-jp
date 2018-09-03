---
title: Send によるチャネル キャッシュ
ms.date: 03/30/2017
ms.assetid: e69a2502-25cb-43bf-b8d2-95fbdecb41cb
ms.openlocfilehash: 619088def1f5e443a31244516655d75d1e25c9cb
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2018
ms.locfileid: "43475856"
---
# <a name="channel-caching-with-send"></a>Send によるチャネル キャッシュ
<xref:System.ServiceModel.Activities.SendMessageChannelCache> を使用すると、ユーザーは <xref:System.ServiceModel.Activities.Send> および <xref:System.ServiceModel.Activities.SendParametersContent> アクティビティでさまざまなレベルのチャネル キャッシュを利用できます。 既定では、インスタンス レベルのキャッシュが有効になっています。このサンプルでは、次の機能を示します。  
  
1.  アプリケーション ドメイン間での <xref:System.ServiceModel.Activities.SendMessageChannelCache> の共有。  
  
2.  チャネル キャッシュの無効化。  
  
3.  <xref:System.ServiceModel.Activities.SendMessageChannelCache> 内のワークフロー インスタンス間での <xref:System.ServiceModel.Activities.WorkflowServiceHost> の共有。  
  
## <a name="demonstrates"></a>使用例  
 <xref:System.ServiceModel.Activities.SendMessageChannelCache> 拡張、<xref:System.ServiceModel.Activities.Send>、<xref:System.ServiceModel.Activities.Receive>、<xref:System.ServiceModel.Activities.ReceiveContent>、および <xref:System.ServiceModel.Activities.SendReply> アクティビティ。  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>サンプルをセットアップ、ビルド、および実行するには  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] でプロジェクト ソリューションを読み込み、プロジェクトをビルドします。  
  
2.  \EchoWorkflowService\bin\debug に生成された EchoWorkflowService アプリケーションを実行します。  
  
3.  \EchoWorkflowClient\bin\debug に生成された EchoWorkflowClient アプリケーションを実行します。  
  
4.  クライアントは、サービスで Echo 操作を呼び出し、結果を出力します。 結果が出力されたら、Enter キーを押してクライアントを終了し、サービスを終了します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\ChannelCache`
