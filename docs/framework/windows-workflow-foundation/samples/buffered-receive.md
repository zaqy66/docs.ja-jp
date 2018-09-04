---
title: バッファーされた受信機能
ms.date: 03/30/2017
ms.assetid: 9d46d9b9-96c9-4531-9695-ab526b4d704a
ms.openlocfilehash: b95577c71493275f30703b4366fab32a51097bd2
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43526805"
---
# <a name="buffered-receive"></a>バッファーされた受信機能
このサンプルを設定して、Windows Workflow Foundation (WF) のバッファーされた受信機能を構成する方法を示します。 バッファーされた受信機能を使用すると、ワークフロー作成者は、メッセージが受信される順序を考慮することなくワークフローを作成できます。 バッファーされた受信機能では、メッセージがローカルにバッファーされ、ワークフローで受信準備が整ったときにメッセージが配信されます。  
  
## <a name="demonstrates"></a>使用例  
 メッセージング アクティビティと共にバッファーされた受信機能を使用した、順番を無視したメッセージ処理。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\BufferedReceive`  
  
## <a name="discussion"></a>説明  
 使用してこのサンプルでは、Windows Communication Foundation (WCF) サービスが実装は[!INCLUDE[wf1](../../../../includes/wf1-md.md)]のシーケンスがあります<xref:System.ServiceModel.Activities.Receive>アクティビティ。 このワークフローは、ローン承認のための 3 つの通知を受け取る単純なローン承認プロセスをモデル化しています。 Windows Communication Foundation (WCF) クライアント アプリケーションでは、サービスが要求の逆の順序で次の 3 つの関連付けられた通知を送信します。 サービスでバッファーされた受信機能が有効になっているので、順番を無視した各メッセージがサービスにバッファーされ、ワークフローで受信準備が整ったときに処理されます。  
  
 バッファーされた受信機能では、バインディングによる <xref:System.ServiceModel.Activities.ReceiveContent> のサポートが必要なので、サービスで <xref:System.ServiceModel.NetMsmqBinding> が使用されます。 バインディングのための特別な構成は不要なので、既定の設定が使用されます。  
  
```xml  
<endpoint address ="net.msmq://localhost/private/LoanService/Service1.xamlx"  
                  binding="netMsmqBinding"  
                  contract="ILoanService"/>  
```  
  
 また、サービスでは、<xref:System.ServiceModel.Description.ServiceMetadataBehavior> を使用してサービスのメタデータが公開されます。  
  
 同様に、<xref:System.ServiceModel.NetMsmqBinding> を使用してクライアント エンドポイントが構成されます。 クライアント コードと構成を使用して生成されて、**サービス参照の追加**Visual Studio の機能です。 App.config ファイルで生成されたクライアント エンドポイントを次の例に示します。  
  
```xml  
<endpoint address="net.msmq://localhost/private/LoanService/Service1.xamlx"  
                binding="netMsmqBinding" bindingConfiguration="NetMsmqBinding_ILoanService"  
                contract="ServiceReference1.ILoanService" name="NetMsmqBinding_ILoanService" />  
```  
  
 このサンプルでは、次の Windows コンポーネントが有効になっている必要があります。  
  
1.  [!INCLUDE[iis60](../../../../includes/iis60-md.md)]  
  
2.  [!INCLUDE[iis60](../../../../includes/iis60-md.md)] と互換性のある管理、IIS メタベースおよび IIS 6 構成との互換性  
  
3.  World Wide Web サービス、アプリケーション開発機能、および ASP.NET  
  
4.  Microsoft メッセージ キュー (MSMQ) サーバー  
  
#### <a name="to-set-up-and-build-the-sample"></a>サンプルをセットアップしてビルドするには  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] コマンド プロンプトで、「`aspnet_regiis –I`」と入力して ASP.NET を登録し、Enter キーを押します。  
  
2.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] を管理者として実行します。  
  
3.  LoanService.sln を開きます。  
  
4.  LoanService プロジェクト用の仮想ディレクトリを作成する場合は、選択を求められたら**はい**します。  
  
#### <a name="to-set-up-the-service-queues"></a>サービス キューを設定するには  
  
1.  F5 キーを押して LoanClient アプリケーションを実行し、キューを作成して Service1.xamlx で定義されたサービスをアクティブ化します。  
  
2.  開く、**コンピュータの管理**コンソールで、コマンド プロンプトから Compmgmt.msc を実行します。  
  
3.  **コンピュータの管理**コンソールで、**サービス**、**アプリケーション**、**メッセージ キュー**、**専用キュー**.  
  
4.  Loanservice/service1.xamlx キューを右クリックして**プロパティ**します。  
  
5.  選択、**セキュリティ**タブをクリックし、追加**のすべてのユーザーは受信メッセージ**、**メッセージのピーク**と**メッセージの送信**アクセス許可。  
  
6.  [!INCLUDE[iis60](../../../../includes/iis60-md.md)] マネージャーを開きます。  
  
7.  参照する**Server**、**サイト**、 **Default Web site**、**プライベート**、 **LoanService** を選択します。**高度なオプション**  
  
8.  変更、**有効なプロトコル**する**http**、 **net.msmq**します。  
  
#### <a name="to-run-the-sample"></a>サンプルを実行するには  
  
1.  参照する http://localhost/private/loanservice/service1.xamlxにサービスが実行されていることを確認します。  
  
2.  F5 キーを押して LoanClient アプリケーションを実行します。 ワークフローが完了したら、メッセージ交換の結果を示す out.txt ファイルが C:\Inbox に保存されます。  
  
#### <a name="to-clean-up"></a>クリーンアップするには  
  
1.  開く、**コンピュータの管理**コンソールで、コマンド プロンプトから Compmgmt.msc を実行します。  
  
2.  展開**サービス**と**アプリケーション**、**メッセージ キュー**、**専用キュー**します。  
  
3.  loanservice/service1.xamlx キューを削除します。  
  
4.  C:\Inbox ディレクトリを削除します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\BufferedReceive`
