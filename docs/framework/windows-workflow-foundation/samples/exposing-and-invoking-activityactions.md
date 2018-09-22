---
title: ActivityAction の公開と呼び出し
ms.date: 03/30/2017
ms.assetid: 97ce4797-426e-463d-9cc4-1261afad6df4
ms.openlocfilehash: 99207c33d82ec9028da2355cc792c366dc5e0cc6
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2018
ms.locfileid: "46583061"
---
# <a name="exposing-and-invoking-activityactions"></a><span data-ttu-id="f6d56-102">ActivityAction の公開と呼び出し</span><span class="sxs-lookup"><span data-stu-id="f6d56-102">Exposing and Invoking ActivityActions</span></span>
<span data-ttu-id="f6d56-103">このサンプルでは、<xref:System.Activities.ActivityAction> を含むカスタム アクティビティを開発する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f6d56-103">This sample demonstrates how to develop a custom activity that has an <xref:System.Activities.ActivityAction>.</span></span> <span data-ttu-id="f6d56-104">また、<xref:System.Activities.ActivityAction> の実装を提供して、このアクティビティを使用する方法も示します。</span><span class="sxs-lookup"><span data-stu-id="f6d56-104">It also demonstrates how to use this activity by providing an implementation of the <xref:System.Activities.ActivityAction>.</span></span>  
  
 <span data-ttu-id="f6d56-105"><xref:System.Activities.ActivityAction> 「ホール」特定のシグネチャを持つアクティビティのユーザーがカスタム動作にプラグインできるを公開するアクティビティの作成者を許可します。</span><span class="sxs-lookup"><span data-stu-id="f6d56-105">An <xref:System.Activities.ActivityAction> allows an activity author to expose "holes" with specific signatures where the activity user can plug in a custom behavior.</span></span> <span data-ttu-id="f6d56-106">たとえば、<xref:System.Activities.Statements.ForEach%601> アクティビティ (項目のコレクションで動作します) の <xref:System.Activities.ActivityAction> では、アクティビティ ユーザーは現在の反復処理項目で機能する動作をプラグインできます。</span><span class="sxs-lookup"><span data-stu-id="f6d56-106">For example, the <xref:System.Activities.Statements.ForEach%601> activity, (which operates over a collection of items), has an <xref:System.Activities.ActivityAction> that allows the activity user to plug in behavior that operates on the current iteration item.</span></span>  
  
## <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="f6d56-107">サンプルをセットアップ、ビルド、および実行するには</span><span class="sxs-lookup"><span data-stu-id="f6d56-107">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="f6d56-108">開く、 **ActivityAction.sln**サンプル ソリューション[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]します。</span><span class="sxs-lookup"><span data-stu-id="f6d56-108">Open the **ActivityAction.sln** sample solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span></span>  
  
2.  <span data-ttu-id="f6d56-109">ソリューションをビルドして実行します。</span><span class="sxs-lookup"><span data-stu-id="f6d56-109">Build and run the solution.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="f6d56-110">サンプルは、既にコンピューターにインストールされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="f6d56-110">The samples may already be installed on your machine.</span></span> <span data-ttu-id="f6d56-111">続行する前に、次の (既定の) ディレクトリを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f6d56-111">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="f6d56-112">このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。</span><span class="sxs-lookup"><span data-stu-id="f6d56-112">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="f6d56-113">このサンプルは、次のディレクトリに格納されます。</span><span class="sxs-lookup"><span data-stu-id="f6d56-113">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\Code-Bodied\ActivityAction`