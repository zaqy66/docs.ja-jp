---
title: ReceiveContext が有効な WCF チャネル
ms.date: 03/30/2017
ms.assetid: d990d119-7321-4b8c-852b-10256f59f9b0
ms.openlocfilehash: d7f80d0874606129876fbf7dfa30c0327680b922
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43442747"
---
# <a name="receivecontext-enabled-wcf-channels"></a>ReceiveContext が有効な WCF チャネル
このサンプルでは、<xref:System.ServiceModel.Channels.ReceiveContext> を有効にした WCF チャネルの有用性を示します。 このサンプルでは、NetMSMQ チャネルを使用して 2 つの数値の積を見つけるサービスを実装します。  
  
 <xref:System.ServiceModel.Channels.ReceiveContext> クラスを使用すると、メッセージの内容を検査した後でも、メッセージにアクセスするか、メッセージをキューに残してさらに処理するかをアプリケーションで指定できます。 このサンプルでは、クライアントがランダムな整数をトランザクション キューに送信します。 `ProductCalculator` サービスはメッセージを受信し、そのメッセージの内容 (整数) を検索して、積が計算できるかどうかを確認します。 サービス操作で積が計算されない場合、メッセージはキューに戻されます。このメッセージはキューをリッスンするサービスでもう一度受信できます。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Binding\Net\MSMQ\ReceiveContextProductGenerator`  
  
#### <a name="to-use-this-sample"></a>このサンプルを使用するには  
  
1.  Microsoft Message Queuing (MSMQ) がインストールされていることを確認します。  
  
    1.  MSMQ を [!INCLUDE[lserver](../../../../includes/lserver-md.md)] にインストールするには  
  
        1.  **サーバー マネージャー**、 をクリックして**機能**します。  
  
        2.  右側のウィンドウで**機能の概要**、 をクリックして**機能の追加**します。  
  
        3.  結果ウィンドウで、展開**メッセージ キュー**します。  
  
        4.  展開**メッセージ キュー サービス**します。  
  
        5.  クリックして**ディレクトリ サービス統合**(コンピューターの場合、ドメインに参加している)、順にクリックします**HTTP サポート**します。  
  
        6.  クリックして**次**、順にクリックします**インストール**します。  
  
    2.  MSMQ を [!INCLUDE[wv](../../../../includes/wv-md.md)] にインストールするには  
  
        1.  **[コントロール パネル]** を開きます。  
  
        2.  クリックして**プログラム**し、**プログラムと機能**、 をクリックして**Windows 機能の有効化オンとオフを**します。  
  
        3.  展開**Microsoft メッセージ キュー (MSMQ) Server**、展開**Microsoft メッセージ キュー (MSMQ) Server Core**、しインストールする次のメッセージ キュー機能のチェック ボックスを選択します。  
  
            -   [メッセージ キュー サーバー]  
  
            -   [MSMQ Active Directory Domain Services Integration] \(ドメインに参加するコンピューターの場合\)  
  
            -   [MSMQ HTTP サポート]  
  
        4.  **[OK]** をクリックします。  
  
        5.  コンピューターを再起動するメッセージが表示されたら、クリックして**OK**インストールを完了します。  
  
2.  [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] がコンピューターにインストールされていることを確認します。  
  
3.  [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] を使用して、ReceiveContextProductGenerator.sln ソリューション ファイルを開きます。  
  
4.  ソリューションをビルドするには、Ctrl キーと Shift キーを押しながら B キーを押します。  
  
5.  ソリューションを実行するには、Ctrl キーを押しながら F5 キーを押します。
