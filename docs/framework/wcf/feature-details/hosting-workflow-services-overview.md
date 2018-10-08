---
title: ワークフロー サービスのホストの概要
ms.date: 03/30/2017
ms.assetid: 19f3704f-06bf-4eeb-8724-5224e02d7ead
ms.openlocfilehash: dbe271e30e9c4e98a52c01ffaa21de25c127c7ff
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/08/2018
ms.locfileid: "48850649"
---
# <a name="hosting-workflow-services-overview"></a><span data-ttu-id="e8f29-102">ワークフロー サービスのホストの概要</span><span class="sxs-lookup"><span data-stu-id="e8f29-102">Hosting Workflow Services Overview</span></span>
<span data-ttu-id="e8f29-103">ワークフロー サービスを実行するには、ホストされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8f29-103">Workflow services must be hosted to execute.</span></span> <span data-ttu-id="e8f29-104"><xref:System.ServiceModel.WorkflowServiceHost> は、複数のインスタンス、構成、および WCF メッセージングをサポートする標準ワークフロー ホストです (ワークフローはホストされるためにメッセージングを使用する必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="e8f29-104">The <xref:System.ServiceModel.WorkflowServiceHost> is the out-of-the-box workflow host that supports multiple instances, configuration, and WCF messaging (although the workflows aren’t required to use messaging in order to be hosted).</span></span>  <span data-ttu-id="e8f29-105">また、一連のサービス動作を介して永続性、追跡、およびインスタンス コントロールを統合します。</span><span class="sxs-lookup"><span data-stu-id="e8f29-105">It also integrates with persistence, tracking, and instance control through a set of service behaviors.</span></span>  <span data-ttu-id="e8f29-106">WCF の <xref:System.ServiceModel.ServiceHost> と同様に、<xref:System.ServiceModel.WorkflowServiceHost> は任意のマネージド .NET アプリケーションでの自己ホスト、または IIS/WAS での Web ホスト (.xamlx ファイルとして) が可能です。</span><span class="sxs-lookup"><span data-stu-id="e8f29-106">Just like WCF’s <xref:System.ServiceModel.ServiceHost>, the <xref:System.ServiceModel.WorkflowServiceHost> can be self-hosted in any managed .NET application, or web-hosted (as a .xamlx file) in IIS / WAS.</span></span>  <span data-ttu-id="e8f29-107">このセクションのトピックでは、ワークフロー サービスをホストする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e8f29-107">Topics in this section describe how to host a workflow service.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e8f29-108">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="e8f29-108">In This Section</span></span>  
 [<span data-ttu-id="e8f29-109">ワークフロー サービスのホスティング</span><span class="sxs-lookup"><span data-stu-id="e8f29-109">Hosting Workflow Services</span></span>](../../../../docs/framework/wcf/feature-details/hosting-workflow-services.md)  
 <span data-ttu-id="e8f29-110">ワークフロー サービスのホスティングについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e8f29-110">Describes hosting workflow services.</span></span>  
  
 [<span data-ttu-id="e8f29-111">ワークフロー サービス ホストの内部</span><span class="sxs-lookup"><span data-stu-id="e8f29-111">Workflow Service Host Internals</span></span>](../../../../docs/framework/wcf/feature-details/workflow-service-host-internals.md)  
 <span data-ttu-id="e8f29-112"><xref:System.ServiceModel.WorkflowServiceHost> がどのように受信メッセージを処理するかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e8f29-112">Describes how <xref:System.ServiceModel.WorkflowServiceHost> processes incoming messages.</span></span>  
  
 [<span data-ttu-id="e8f29-113">ワークフロー サービス ホストの拡張機能</span><span class="sxs-lookup"><span data-stu-id="e8f29-113">Workflow Service Host Extensibility</span></span>](../../../../docs/framework/wcf/feature-details/workflow-service-host-extensibility.md)  
 <span data-ttu-id="e8f29-114">ワークフロー サービス ホストの機能を拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e8f29-114">Describes how to extend the functionality of the workflow service host.</span></span>  
  
 [<span data-ttu-id="e8f29-115">ワークフロー コントロール エンドポイント</span><span class="sxs-lookup"><span data-stu-id="e8f29-115">Workflow Control Endpoint</span></span>](../../../../docs/framework/wcf/feature-details/workflow-control-endpoint.md)  
 <span data-ttu-id="e8f29-116">ワークフロー インスタンスを作成できるエンドポイントを定義する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e8f29-116">Describes how to define an endpoint that allows you to create workflow instances.</span></span>
  
 [<span data-ttu-id="e8f29-117">方法 : Windows Server AppFabric を使用してワークフロー サービスをホストする</span><span class="sxs-lookup"><span data-stu-id="e8f29-117">How to: Host a Workflow Service with Windows Server App Fabric</span></span>](../../../../docs/framework/wcf/feature-details/how-to-host-a-workflow-service-with-windows-server-app-fabric.md)  
 <span data-ttu-id="e8f29-118">Windows Server AppFabric の既存のワークフロー サービスをホストする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e8f29-118">Demonstrates how to host an existing workflow service in Windows Server App Fabric.</span></span>  
  
 [<span data-ttu-id="e8f29-119">WorkflowServiceHost の構成</span><span class="sxs-lookup"><span data-stu-id="e8f29-119">Configuring WorkflowServiceHost</span></span>](../../../../docs/framework/wcf/feature-details/configuring-workflowservicehost.md)  
 <span data-ttu-id="e8f29-120">永続性、追跡、アイドル状態、および未処理の例外動作を制御する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="e8f29-120">Describes how to control persistence, tracking, idle, and unhandled exception behavior.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="e8f29-121">参照</span><span class="sxs-lookup"><span data-stu-id="e8f29-121">Reference</span></span>  
 <xref:System.ServiceModel.Activities.WorkflowServiceHost>  
  
 <xref:System.ServiceModel.Activities.WorkflowService>  
  
 <xref:System.ServiceModel.Activation.ServiceHostFactory>  
  
 <xref:System.ServiceModel.Activation.ServiceHostFactoryBase>  
  
 <xref:System.ServiceModel.Activation.WorkflowServiceHostFactory>  
  
## <a name="related-sections"></a><span data-ttu-id="e8f29-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8f29-122">Related Sections</span></span>  
 [<span data-ttu-id="e8f29-123">ワークフロー サービス</span><span class="sxs-lookup"><span data-stu-id="e8f29-123">Workflow Services</span></span>](../../../../docs/framework/wcf/feature-details/workflow-services.md)
