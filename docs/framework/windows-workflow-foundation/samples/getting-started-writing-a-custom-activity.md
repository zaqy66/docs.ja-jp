---
title: カスタム アクティビティの記述について
ms.date: 03/30/2017
ms.assetid: 3902f5fa-8a43-4048-8a6a-6b15472f90f0
ms.openlocfilehash: 4d9c140ca230750ca1119b33252b1edb8796d458
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43776659"
---
# <a name="getting-started-writing-a-custom-activity"></a><span data-ttu-id="b169c-102">カスタム アクティビティの記述について</span><span class="sxs-lookup"><span data-stu-id="b169c-102">Getting Started Writing a Custom Activity</span></span>
<span data-ttu-id="b169c-103">このサンプルでは、XAML で単純なカスタム アクティビティを定義する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b169c-103">This sample demonstrates how to define a simple custom activity in XAML.</span></span> <span data-ttu-id="b169c-104">このアクティビティの名前は `Rhyme` で、ロジックは 3 つの連続する <xref:System.Activities.Statements.WriteLine> アクティビティです。</span><span class="sxs-lookup"><span data-stu-id="b169c-104">The activity is given the name `Rhyme`, and its logic is a sequence of three <xref:System.Activities.Statements.WriteLine> activities.</span></span>  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="b169c-105">サンプルをセットアップ、ビルド、および実行するには</span><span class="sxs-lookup"><span data-stu-id="b169c-105">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="b169c-106">開く、 **Simple.sln**サンプル ソリューション[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]します。</span><span class="sxs-lookup"><span data-stu-id="b169c-106">Open the **Simple.sln** sample solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span></span>  
  
2.  <span data-ttu-id="b169c-107">ソリューションをビルドして実行します。</span><span class="sxs-lookup"><span data-stu-id="b169c-107">Build and run the solution.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="b169c-108">サンプルは、既にコンピューターにインストールされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="b169c-108">The samples may already be installed on your machine.</span></span> <span data-ttu-id="b169c-109">続行する前に、次の (既定の) ディレクトリを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b169c-109">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="b169c-110">このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。</span><span class="sxs-lookup"><span data-stu-id="b169c-110">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="b169c-111">このサンプルは、次のディレクトリに格納されます。</span><span class="sxs-lookup"><span data-stu-id="b169c-111">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\Composite\GettingStarted`