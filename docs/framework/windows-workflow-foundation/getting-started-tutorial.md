---
title: Tutorial2 を作業の開始
ms.date: 03/30/2017
helpviewer_keywords:
- WF [WF], getting started
- Windows Workflow Foundation [WF], getting started
ms.assetid: c2d3585f-6b1a-4d4f-9865-bd7cd31c5d42
ms.openlocfilehash: 99daa524f041ffcd096195fc79527557b8f2697d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54591985"
---
# <a name="getting-started-tutorial"></a><span data-ttu-id="49b0a-102">チュートリアル入門</span><span class="sxs-lookup"><span data-stu-id="49b0a-102">Getting Started Tutorial</span></span>
<span data-ttu-id="49b0a-103">このセクションには、一連 Windows Workflow Foundation (WF) のアプリケーションのプログラミングを紹介するチュートリアル トピックにはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="49b0a-103">This section contains a set of walkthrough topics that introduce you to programming Windows Workflow Foundation (WF) applications.</span></span> <span data-ttu-id="49b0a-104">これらのトピックの手順に従って、数値推測ゲーム アプリケーションを構築します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-104">By following the procedures in these topics, you will build an application that is a number guessing game.</span></span> <span data-ttu-id="49b0a-105">チュートリアルの最初のトピックでは、ワークフローに必要なカスタム アクティビティを作成する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-105">The first topic in the tutorial leads you through the steps to create the custom activities required for the workflow.</span></span> <span data-ttu-id="49b0a-106">2 番目のトピックでは、カスタム アクティビティをビルトイン ワークフロー アクティビティと共にフローチャート ワークフローにアセンブルします。</span><span class="sxs-lookup"><span data-stu-id="49b0a-106">In the second topic, these activities are assembled along with built-in workflow activities into a flowchart workflow.</span></span> <span data-ttu-id="49b0a-107">3 番目のトピックでは、ホスト アプリケーションを構成してワークフローを実行します。最後のトピックでは永続化の概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-107">In the third topic, the host application is configured to run the workflow, and in the final topic persistence is introduced.</span></span> <span data-ttu-id="49b0a-108">このプロセスの各手順はその前の手順に基づいているため、順番に完了することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="49b0a-108">Each step in this process depends on the previous steps, so we recommend that you complete them in order.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="49b0a-109">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="49b0a-109">In This Section</span></span>  
 [<span data-ttu-id="49b0a-110">方法: アクティビティを作成します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-110">How to: Create an Activity</span></span>](../../../docs/framework/windows-workflow-foundation/how-to-create-an-activity.md)  
 <span data-ttu-id="49b0a-111"><xref:System.Activities.NativeActivity%601> から派生するカスタム アクティビティを作成する方法、およびアクティビティ デザイナーを使用してカスタム アクティビティをビルトイン アクティビティと共に複合アクティビティへと構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-111">Describes how to create a custom activity that derives from <xref:System.Activities.NativeActivity%601>, and how to compose this activity along with a built-in activity into a composite activity using the activity designer.</span></span>  
  
 [<span data-ttu-id="49b0a-112">方法: ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-112">How to: Create a Workflow</span></span>](../../../docs/framework/windows-workflow-foundation/how-to-create-a-workflow.md)  
 <span data-ttu-id="49b0a-113">ビルトイン アクティビティと前のチュートリアルのカスタム アクティビティを使用して、フローチャート、シーケンシャル、およびステート マシンのワークフローを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-113">Describes how to create flowchart, sequential, and state machine workflows by using built-in activities and the custom activities from the preceding tutorial.</span></span>  
  
 [<span data-ttu-id="49b0a-114">方法: ワークフローを実行します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-114">How to: Run a Workflow</span></span>](../../../docs/framework/windows-workflow-foundation/how-to-run-a-workflow.md)  
 <span data-ttu-id="49b0a-115">ホスト環境からワークフローを呼び出す方法、データをワークフローとの間でやり取りする方法、およびブックマークを再開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-115">Describes how to invoke a workflow from a host environment, pass data into and out of a workflow, and how to resume bookmarks.</span></span>  
  
 [<span data-ttu-id="49b0a-116">方法: 作成して実行する時間の長いワークフローの実行</span><span class="sxs-lookup"><span data-stu-id="49b0a-116">How to: Create and Run a Long Running Workflow</span></span>](../../../docs/framework/windows-workflow-foundation/how-to-create-and-run-a-long-running-workflow.md)  
 <span data-ttu-id="49b0a-117">永続性をワークフロー アプリケーションに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-117">Describes how to add persistence to a workflow application.</span></span>  
  
 [<span data-ttu-id="49b0a-118">方法: カスタム追跡参加要素を作成します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-118">How to: Create a Custom Tracking Participant</span></span>](../../../docs/framework/windows-workflow-foundation/how-to-create-a-custom-tracking-participant.md)  
 <span data-ttu-id="49b0a-119">カスタムの追跡参加要素と追跡プロファイルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-119">Describes how to create a custom tracking participant and tracking profile.</span></span>  
  
 [<span data-ttu-id="49b0a-120">方法: 複数のバージョンをワークフロー サイド バイ サイドのホストします。</span><span class="sxs-lookup"><span data-stu-id="49b0a-120">How to: Host Multiple Versions of a Workflow Side-by-Side</span></span>](../../../docs/framework/windows-workflow-foundation/how-to-host-multiple-versions-of-a-workflow-side-by-side.md)  
 <span data-ttu-id="49b0a-121">`WorkflowIdentity` を使用して、ワークフローの複数バージョンを同時にホストする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-121">Describes how to use `WorkflowIdentity` to host multiple versions of a workflow side-by-side.</span></span>  
  
 [<span data-ttu-id="49b0a-122">方法: 実行中のワークフロー インスタンスの定義を更新します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-122">How to: Update the Definition of a Running Workflow Instance</span></span>](../../../docs/framework/windows-workflow-foundation/how-to-update-the-definition-of-a-running-workflow-instance.md)  
 <span data-ttu-id="49b0a-123">動的更新を使用して、実行中のワークフロー インスタンスを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="49b0a-123">Describes how to use dynamic update to modify running workflow instances.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="49b0a-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="49b0a-124">See also</span></span>
- [<span data-ttu-id="49b0a-125">Windows Workflow Foundation プログラミング</span><span class="sxs-lookup"><span data-stu-id="49b0a-125">Windows Workflow Foundation Programming</span></span>](../../../docs/framework/windows-workflow-foundation/programming.md)
