---
title: External Data Exchange での Interop の使用
ms.date: 03/30/2017
ms.assetid: 96f6fe26-5305-494f-9119-7748e0c4b3fa
ms.openlocfilehash: 534321e5b5568e0dd0988333dc98ccc18ff33df8
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/14/2018
ms.locfileid: "45616313"
---
# <a name="using-interop-with-external-data-exchange"></a><span data-ttu-id="587fe-102">External Data Exchange での Interop の使用</span><span class="sxs-lookup"><span data-stu-id="587fe-102">Using Interop with External Data Exchange</span></span>
<span data-ttu-id="587fe-103"><xref:System.Activities.Statements.Interop>から Windows Workflow Foundation (WF) でアクティビティを実行するアクティビティを使用できます[!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)]と[!INCLUDE[netfx35_long](../../../../includes/netfx35-long-md.md)](WF3) 内での Windows Workflow Foundation でワークフローと[!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)](WF4)。</span><span class="sxs-lookup"><span data-stu-id="587fe-103">The <xref:System.Activities.Statements.Interop> activity can be used to execute activities from Windows Workflow Foundation (WF) in [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)] and [!INCLUDE[netfx35_long](../../../../includes/netfx35-long-md.md)] (WF3), and workflows within Windows Workflow Foundation in [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] (WF4).</span></span> <span data-ttu-id="587fe-104">このサンプルは、WF4 ワークフロー サービスの <xref:System.Workflow.Activities.ExternalDataExchangeService> アクティビティを使用して、<xref:System.Activities.Statements.Interop> (およびメソッドを呼び出してイベントを処理するための対応するカスタム アクティビティ) を使用する WF3 ワークフローを設定および実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="587fe-104">This sample shows how to configure and run a WF3 workflow that uses <xref:System.Workflow.Activities.ExternalDataExchangeService> (and corresponding custom activities for calling methods and handling events) by using the <xref:System.Activities.Statements.Interop> activity in a WF4 workflow service.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="587fe-105">サンプルは、既にコンピューターにインストールされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="587fe-105">The samples may already be installed on your machine.</span></span> <span data-ttu-id="587fe-106">続行する前に、次の (既定の) ディレクトリを確認してください。</span><span class="sxs-lookup"><span data-stu-id="587fe-106">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="587fe-107">このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。</span><span class="sxs-lookup"><span data-stu-id="587fe-107">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="587fe-108">このサンプルは、次のディレクトリに格納されます。</span><span class="sxs-lookup"><span data-stu-id="587fe-108">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Migration\ExternalDataExchange`  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="587fe-109">このサンプルを使用するには</span><span class="sxs-lookup"><span data-stu-id="587fe-109">To use this sample</span></span>  
  
1.  <span data-ttu-id="587fe-110">[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] で ExternalDataExchange.sln ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="587fe-110">Open the ExternalDataExchange.sln file in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span></span>  
  
2.  <span data-ttu-id="587fe-111">サンプルをビルドするには、Ctrl キーと Shift キーを押しながら B キーを押します。</span><span class="sxs-lookup"><span data-stu-id="587fe-111">To build the sample, press CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="587fe-112">サンプルを実行するには、F5 キーを押します。</span><span class="sxs-lookup"><span data-stu-id="587fe-112">To run the sample, press F5.</span></span>
