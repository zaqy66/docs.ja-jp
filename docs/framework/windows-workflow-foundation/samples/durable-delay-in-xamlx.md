---
title: XAMLX における永続的な遅延
ms.date: 03/30/2017
ms.assetid: efc38df4-2d34-453c-8e59-2c21d1307354
ms.openlocfilehash: 1eef9211c67d190ecb5f329c481fa2e3d1763353
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2018
ms.locfileid: "44708686"
---
# <a name="durable-delay-in-xamlx"></a>XAMLX における永続的な遅延
このサンプルでは、永続的な遅延を使用する方法を示します。これは、遅延の間、ワークフローを永続的なデバイスに永続化する遅延のことです。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\DurableDelayXamlx`  
  
## <a name="discussion"></a>説明  
 このサンプル ワークフローには、遅延によって分割された 2 つのローカル ファイルへのメッセージが含まれています。 遅延が発生すると、ワークフローがアンロードされ、ワークフローはメモリに再読み込みされるまでワークフロー インスタンス ストアで 5 秒間待機します。  
  
 .Xamlx ファイルは、Visual Studio でホストされるワークフロー サービスです。 Visual Studio では、ワークフロー ホストにワークフロー サービスを使用する Cassini を使用します。  
  
 ワークフロー サービス ホストは、ワークフローをホストするだけでなく、読み込みとアンロードを行うことによってワークフロー インスタンスを管理します。 Windows Workflow Foundation (WF) の定義 (ワークフロー サービス ホスト) 上のインスタンスを開始する設定へのメッセージを送信するクライアントを<xref:System.ServiceModel.Activities.Receive>ワークフロー内のアクティビティ。 この <xref:System.ServiceModel.Activities.Receive> は、<xref:System.ServiceModel.Activities.Receive.CanCreateInstance%2A> プロパティが `true` に設定されているため、メッセージを受信した後にワークフローの新しいインスタンスを作成できます。  
  
 初期化中に、ワークフロー サービス ホストに対してインスタンスを永続化ストア (データベース) にアンロードするように指定する、インスタンスのアンロード動作が構成ファイルに追加されます。 このサンプルでは、(遅延が発生して) ワークフローがアイドル状態になった直後にインスタンスがアンロードされます。  
  
#### <a name="to-use-this-sample"></a>このサンプルを使用するには  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] のコマンド プロンプトを開きます。  
  
2.  DurableDelayXamlx\CS フォルダーに移動します。  
  
3.  Setup.cmd を実行します。  
  
4.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] を管理者として実行します。  
  
5.  DurableDelayXamlx.sln ソリューション ファイルを開きます。  
  
6.  **ソリューション エクスプ ローラー**ソリューションを右クリックし、選択、**プロパティ**します。  
  
7.  選択**マルチ スタートアップ プロジェクト**に両方のプロジェクトを設定および**開始**します。  
  
8.  ソリューションをビルドするには、Ctrl キーと Shift キーを押しながら B キーを押します。  
  
9. ソリューションを実行するには、Ctrl キーを押しながら F5 キーを押します。  
  
#### <a name="to-uninstall-this-sample"></a>このサンプルをアンインストールするには  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] のコマンド プロンプトを開きます。  
  
2.  DurableDelayXamlx\CS フォルダーに移動します。  
  
3.  Cleanup.cmd を実行します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\DurableDelayXamlX`
