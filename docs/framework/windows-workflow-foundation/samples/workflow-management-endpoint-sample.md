---
title: ワークフロー管理エンドポイントのサンプル
ms.date: 03/30/2017
ms.assetid: 3ac6e08f-c43d-4bb7-83c3-e3890a4dac03
ms.openlocfilehash: 3d99cbef20895381f5e40ee939e1d94a409f1391
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44360623"
---
# <a name="workflow-management-endpoint-sample"></a>ワークフロー管理エンドポイントのサンプル
このサンプルでは、ワークフロー コントロール エンドポイントを使用して、ローカルとリモートの両方でワークフローを作成および実行する方法を示します。 このサンプルでは、コントロール エンドポイントをホストし、そのコントロール エンドポイントを呼び出すクライアントを記述して、ワークフローのインスタンスを作成および実行する方法を示します。 このワークフローはサービスではありません。  
  
 サンプルのサービス側では、ワークフローが WorkflowServiceHost を使用してホストされており、クライアントが管理操作 (保留、開始など) を実行できるように WorkflowControlEndpoint が追加されています。 ワークフローを作成できるように、ユーザー定義 CreationEndpoint も追加されています。 次に、サービスは、中断状態のワークフローを開始するこれらのエンドポイントを使用して、ワークフローを再開します。 クライアントはクライアント コードから同じ操作を実行します。 これらの詳細については、「インターフェイスの[ワークフロー コントロール エンドポイント](../../../../docs/framework/wcf/feature-details/workflow-control-endpoint.md)と[方法: IIS でサービス以外ワークフローのホスト](../../../../docs/framework/wcf/feature-details/how-to-host-a-non-service-workflow-in-iis.md)  
  
#### <a name="to-run-the-sample"></a>サンプルを実行するには  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] を管理者権限で実行します。  
  
2.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] で ManagementEndpoint.sln ソリューションを開きます。  
  
3.  ソリューションをビルドするには、CTRL + SHIFT + B キーを押しますまたは選択**ソリューションのビルド**から、**ビルド**メニュー。  
  
4.  ManagementEndpoint.exe アプリケーションを起動します。  
  
5.  Client.exe アプリケーションを起動します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Execution\ManagementEndpoint`