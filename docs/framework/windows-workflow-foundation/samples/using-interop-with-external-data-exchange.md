---
title: External Data Exchange での Interop の使用
ms.date: 03/30/2017
ms.assetid: 96f6fe26-5305-494f-9119-7748e0c4b3fa
ms.openlocfilehash: 534321e5b5568e0dd0988333dc98ccc18ff33df8
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43804829"
---
# <a name="using-interop-with-external-data-exchange"></a>External Data Exchange での Interop の使用
<xref:System.Activities.Statements.Interop>から Windows Workflow Foundation (WF) でアクティビティを実行するアクティビティを使用できます[!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)]と[!INCLUDE[netfx35_long](../../../../includes/netfx35-long-md.md)](WF3) 内での Windows Workflow Foundation でワークフローと[!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)](WF4)。 このサンプルは、WF4 ワークフロー サービスの <xref:System.Workflow.Activities.ExternalDataExchangeService> アクティビティを使用して、<xref:System.Activities.Statements.Interop> (およびメソッドを呼び出してイベントを処理するための対応するカスタム アクティビティ) を使用する WF3 ワークフローを設定および実行する方法を示します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Migration\ExternalDataExchange`  
  
#### <a name="to-use-this-sample"></a>このサンプルを使用するには  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] で ExternalDataExchange.sln ファイルを開きます。  
  
2.  サンプルをビルドするには、Ctrl キーと Shift キーを押しながら B キーを押します。  
  
3.  サンプルを実行するには、F5 キーを押します。
