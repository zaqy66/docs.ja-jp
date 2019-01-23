---
title: '&lt;services&gt; の &lt;add&gt;'
ms.date: 03/30/2017
ms.assetid: 6bdc4590-aa9c-4ec8-9345-879d780cd141
ms.openlocfilehash: dc68357332ebe06affd18f1539a66587b6ed1b91
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549995"
---
# <a name="ltaddgt-of-ltservicesgt"></a><span data-ttu-id="0676d-102">&lt;services&gt; の &lt;add&gt;</span><span class="sxs-lookup"><span data-stu-id="0676d-102">&lt;add&gt; of &lt;services&gt;</span></span>
<span data-ttu-id="0676d-103">インスタンスの設定を指定<xref:System.Workflow.Runtime.WorkflowRuntime>ワークフロー ベースの Windows Communication Foundation (WCF) サービスをホストするためです。</span><span class="sxs-lookup"><span data-stu-id="0676d-103">Specifies settings for an instance of <xref:System.Workflow.Runtime.WorkflowRuntime> for hosting workflow-based Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="0676d-104">この要素は <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="0676d-104">This element is of type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span></span>  
  
 <span data-ttu-id="0676d-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="0676d-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="0676d-106">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="0676d-106">\<behaviors></span></span>  
<span data-ttu-id="0676d-107">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="0676d-107">\<serviceBehaviors></span></span>  
<span data-ttu-id="0676d-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="0676d-108">\<behavior></span></span>  
<span data-ttu-id="0676d-109">\<services></span><span class="sxs-lookup"><span data-stu-id="0676d-109">\<services></span></span>  
<span data-ttu-id="0676d-110">\<add></span><span class="sxs-lookup"><span data-stu-id="0676d-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0676d-111">構文</span><span class="sxs-lookup"><span data-stu-id="0676d-111">Syntax</span></span>  
  
```xml  
<workflowRuntime>
  <services>
    <add type="String" />
  </services>
</workflowRuntime>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0676d-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="0676d-112">Attributes and Elements</span></span>  
 <span data-ttu-id="0676d-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="0676d-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0676d-114">属性</span><span class="sxs-lookup"><span data-stu-id="0676d-114">Attributes</span></span>  
  
|<span data-ttu-id="0676d-115">属性</span><span class="sxs-lookup"><span data-stu-id="0676d-115">Attribute</span></span>|<span data-ttu-id="0676d-116">説明</span><span class="sxs-lookup"><span data-stu-id="0676d-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0676d-117">型</span><span class="sxs-lookup"><span data-stu-id="0676d-117">type</span></span>|<span data-ttu-id="0676d-118">初期化するサービスのアセンブリ修飾型名を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="0676d-118">A string that specifies the assembly-qualified type name of the service to be initialized.</span></span> <span data-ttu-id="0676d-119">指定されたサービスは、そのコンストラクターのシグネチャに関して一定の規則に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0676d-119">The service specified must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="0676d-120">詳細については、「<xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0676d-120">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0676d-121">子要素</span><span class="sxs-lookup"><span data-stu-id="0676d-121">Child Elements</span></span>  
 <span data-ttu-id="0676d-122">なし。</span><span class="sxs-lookup"><span data-stu-id="0676d-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0676d-123">親要素</span><span class="sxs-lookup"><span data-stu-id="0676d-123">Parent Elements</span></span>  
  
|<span data-ttu-id="0676d-124">要素</span><span class="sxs-lookup"><span data-stu-id="0676d-124">Element</span></span>|<span data-ttu-id="0676d-125">説明</span><span class="sxs-lookup"><span data-stu-id="0676d-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0676d-126">\<services></span><span class="sxs-lookup"><span data-stu-id="0676d-126">\<services></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/services-of-workflowruntime.md)|<span data-ttu-id="0676d-127"><xref:System.Workflow.Runtime.WorkflowRuntime> エンジンに追加されるサービスのコレクション。</span><span class="sxs-lookup"><span data-stu-id="0676d-127">A collection of services that will be added to the <xref:System.Workflow.Runtime.WorkflowRuntime> engine.</span></span> <span data-ttu-id="0676d-128">要素は、<xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="0676d-128">The elements are of type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span></span>  <span data-ttu-id="0676d-129">コレクションで指定されたサービスはワークフロー ランタイム エンジンによって初期化され、適切な <xref:System.Workflow.Runtime.WorkflowRuntime> コンストラクターが呼び出されるとワークフロー ランタイム エンジンのサービスに追加されます。</span><span class="sxs-lookup"><span data-stu-id="0676d-129">The services specified in the collection will be initialized by the workflow runtime engine and added to its services when the appropriate <xref:System.Workflow.Runtime.WorkflowRuntime> constructor is called.</span></span> <span data-ttu-id="0676d-130">したがって、コレクションで指定されたサービスは、そのコンストラクターのシグネチャに関して一定の規則に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0676d-130">Therefore, the services specified in the collection must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="0676d-131">詳細については、「<xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0676d-131">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0676d-132">Remarks</span><span class="sxs-lookup"><span data-stu-id="0676d-132">Remarks</span></span>  
 <span data-ttu-id="0676d-133">この要素で指定されたサービスはワークフロー ランタイム エンジンによって初期化され、適切な <xref:System.Workflow.Runtime.WorkflowRuntime> コンストラクターが呼び出されるとワークフロー ランタイム エンジンのサービスに追加されます。</span><span class="sxs-lookup"><span data-stu-id="0676d-133">The service specified in this element will be initialized by the workflow runtime engine and added to its services when the appropriate <xref:System.Workflow.Runtime.WorkflowRuntime> constructor is called.</span></span> <span data-ttu-id="0676d-134">したがって、指定されたサービスは、そのコンストラクターのシグネチャに関して一定の規則に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0676d-134">Therefore, the service specified must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="0676d-135">詳細については、「<xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0676d-135">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0676d-136">例</span><span class="sxs-lookup"><span data-stu-id="0676d-136">Example</span></span>  
  
```xml  
<serviceBehaviors>
  <behavior name="ServiceBehavior">
    <workflowRuntime name="WorkflowServiceHostRuntime"
                     validateOnCreate="true"
                     enablePerformanceCounters="true">
      <services>
        <add type="NetFx.Checkin.Scenario.WorkflowServices.WorkflowBasedServices.Common.TestPersistenceService.FilePersistenceService, NetFx.Checkin.Scenario.WorkflowServices.WorkflowBasedServices.Common" />
      </services>
    </workflowRuntime>
  </behavior>
</serviceBehaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="0676d-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="0676d-137">See also</span></span>
- <xref:System.ServiceModel.Configuration.WorkflowRuntimeElement>
- <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>
- <xref:System.Workflow.Runtime.WorkflowRuntime>
- <span data-ttu-id="0676d-138">[ワークフロー構成ファイル](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="0676d-138">[Workflow Configuration Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span></span>
