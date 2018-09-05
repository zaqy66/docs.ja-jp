---
title: エラーの送信と処理
ms.date: 03/30/2017
ms.assetid: 98e8e04d-2ac9-4a33-ae08-462f757a7a14
ms.openlocfilehash: 896f209e7daeeab2bb33c1fde15298aae96c8776
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43733366"
---
# <a name="sending-and-handling-faults"></a>エラーの送信と処理
このサンプルでは、<xref:System.ServiceModel.Activities.SendReply> および <xref:System.ServiceModel.Activities.ReceiveReply> メッセージング アクティビティを使用して、予期したエラーと予期しないエラーを送受信する方法を示します。 このシナリオでは、最初のクライアント要求で、その <xref:System.ServiceModel.Activities.Send.KnownTypes%2A> コレクションに含まれている予期したエラーが発生します。 次のいくつかのクライアント要求によって、予期しないエラーを受信してから、最後の要求が成功します。  
  
## <a name="to-use-this-sample"></a>このサンプルを使用するには  
  
1.  開いている[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]を右クリックし、管理者特権でのアクセス許可を持つ、[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]アイコンを**管理者として実行**します。  
  
2.  Faults.sln ソリューション ファイルを開きます。  
  
3.  ソリューションをビルドするには、Ctrl キーと Shift キーを押しながら B キーを押します。  
  
4.  サービス プロジェクトを実行します。  
  
    1.  **ソリューション エクスプ ローラー**を右クリックし、`FaultService`順に選択して**スタートアップ プロジェクトとして設定**します。  
  
    2.  Ctrl キーを押しながら、F5 キーを押します。  
  
5.  別のコピーを開く[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]を右クリックし、管理者特権でのアクセス許可を持つ、[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]アイコンを**管理者として実行**します。  
  
6.  Faults.sln ソリューション ファイルを開きます。  
  
7.  クライアント プロジェクトを実行します。  
  
    1.  **ソリューション エクスプ ローラー**を右クリックし、`FaultClient`順に選択して**スタートアップ プロジェクトとして設定**します。  
  
    2.  Ctrl キーを押しながら、F5 キーを押します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\Faults`