---
title: <add> の <commonParameters>
ms.date: 03/30/2017
ms.assetid: 3713bf25-20c8-455f-bb85-de46b6487932
ms.openlocfilehash: 63ff98d91db7c8c112b0b00e9bd37c3262bcad6d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55258625"
---
# <a name="add-of-commonparameters"></a><span data-ttu-id="64572-102">\<add> of \<commonParameters></span><span class="sxs-lookup"><span data-stu-id="64572-102">\<add> of \<commonParameters></span></span>
<span data-ttu-id="64572-103">複数のサービスでグローバルに使用されるパラメーターの名前と値のペアを指定します。</span><span class="sxs-lookup"><span data-stu-id="64572-103">Specifies a name-value pair of parameters that are used globally across multiple services.</span></span> <span data-ttu-id="64572-104">このパラメーターには通常、永続性サービスによって共有されるデータベース接続文字列が格納されます。</span><span class="sxs-lookup"><span data-stu-id="64572-104">Typically this parameter includes the database connection string that might be shared by durable services.</span></span>  
  
 <span data-ttu-id="64572-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="64572-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="64572-106">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="64572-106">\<behaviors></span></span>  
<span data-ttu-id="64572-107">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="64572-107">\<serviceBehaviors></span></span>  
<span data-ttu-id="64572-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="64572-108">\<behavior></span></span>  
<span data-ttu-id="64572-109">\<workflowRuntime></span><span class="sxs-lookup"><span data-stu-id="64572-109">\<workflowRuntime></span></span>  
<span data-ttu-id="64572-110">\<commonParameters></span><span class="sxs-lookup"><span data-stu-id="64572-110">\<commonParameters></span></span>  
<span data-ttu-id="64572-111">\<add></span><span class="sxs-lookup"><span data-stu-id="64572-111">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64572-112">構文</span><span class="sxs-lookup"><span data-stu-id="64572-112">Syntax</span></span>  
  
```xml  
<workflowRuntime>
  <commonParameters>
    <add name="String" value="String" />
  </commonParameters>
</workflowRuntime>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="64572-113">属性および要素</span><span class="sxs-lookup"><span data-stu-id="64572-113">Attributes and Elements</span></span>  
 <span data-ttu-id="64572-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="64572-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="64572-115">属性</span><span class="sxs-lookup"><span data-stu-id="64572-115">Attributes</span></span>  
  
|<span data-ttu-id="64572-116">属性</span><span class="sxs-lookup"><span data-stu-id="64572-116">Attribute</span></span>|<span data-ttu-id="64572-117">説明</span><span class="sxs-lookup"><span data-stu-id="64572-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="64572-118">name</span><span class="sxs-lookup"><span data-stu-id="64572-118">name</span></span>|<span data-ttu-id="64572-119">サービスに対して指定されたパラメーターの名前。</span><span class="sxs-lookup"><span data-stu-id="64572-119">The name of the parameter specified for a service.</span></span>|  
|<span data-ttu-id="64572-120">value</span><span class="sxs-lookup"><span data-stu-id="64572-120">value</span></span>|<span data-ttu-id="64572-121">サービスに対して指定されたパラメーターの値。</span><span class="sxs-lookup"><span data-stu-id="64572-121">The value of the parameter specified for a service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="64572-122">子要素</span><span class="sxs-lookup"><span data-stu-id="64572-122">Child Elements</span></span>  
 <span data-ttu-id="64572-123">なし。</span><span class="sxs-lookup"><span data-stu-id="64572-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="64572-124">親要素</span><span class="sxs-lookup"><span data-stu-id="64572-124">Parent Elements</span></span>  
  
|<span data-ttu-id="64572-125">要素</span><span class="sxs-lookup"><span data-stu-id="64572-125">Element</span></span>|<span data-ttu-id="64572-126">説明</span><span class="sxs-lookup"><span data-stu-id="64572-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="64572-127">\<commonParameters></span><span class="sxs-lookup"><span data-stu-id="64572-127">\<commonParameters></span></span>](https://msdn.microsoft.com/library/d0e1e6fc-985a-4713-b7da-194e30dfab4c)|<span data-ttu-id="64572-128">サービスによって使用される共通パラメーターのコレクション。</span><span class="sxs-lookup"><span data-stu-id="64572-128">A collection of common parameters used by services.</span></span> <span data-ttu-id="64572-129">このコレクションには通常、永続性サービスによって共有されるデータベース接続文字列が格納されます。</span><span class="sxs-lookup"><span data-stu-id="64572-129">This collection will typically include the database connection string that might be shared by durable services.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="64572-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="64572-130">Remarks</span></span>  
 <span data-ttu-id="64572-131">最初の要素 `<commonParameters>` は、複数のサービスでグローバルに使用されるパラメーターを定義します (たとえば `ConnectionString` を使用する場合の <xref:System.Workflow.Runtime.Hosting.SharedConnectionWorkflowCommitWorkBatchService>)。</span><span class="sxs-lookup"><span data-stu-id="64572-131">The `<commonParameters>` element defines any parameters that are used globally across multiple services, for example `ConnectionString` when using the <xref:System.Workflow.Runtime.Hosting.SharedConnectionWorkflowCommitWorkBatchService>.</span></span>  
  
 <span data-ttu-id="64572-132"><xref:System.Workflow.Runtime.Hosting.DefaultWorkflowCommitWorkBatchService> や <xref:System.Workflow.Runtime.Hosting.SqlWorkflowPersistenceService> など、作業バッチを永続的ストアにコミットするサービスでは、`EnableRetries` パラメーターを次の例のように使用することで、トランザクションの再試行を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="64572-132">For services that commit work batches to persistence stores, such as <xref:System.Workflow.Runtime.Hosting.DefaultWorkflowCommitWorkBatchService> and <xref:System.Workflow.Runtime.Hosting.SqlWorkflowPersistenceService>, you can enable them to retry their transaction by using the `EnableRetries` parameter as shown in the following example:</span></span>  
  
```xml  
<workflowRuntime name="SampleApplication"
                 unloadOnIdle="false">
  <commonParameters>
    <add name="ConnectionString"
         value="Initial Catalog=WorkflowStore;Data Source=localhost;Integrated Security=SSPI;" />
    <add name="EnableRetries"
         value="True" />
  </commonParameters>
  <services>
    <add type="System.Workflow.Runtime.Hosting.SqlWorkflowPersistenceService, System.Workflow.Runtime, Version=3.0.00000.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"
         enableRetries="False" />
  </services>
</workflowRuntime>
```  
  
 <span data-ttu-id="64572-133">注意して、`EnableRetries`パラメーターで設定できますか、グローバル レベル (ように、 *CommonParameters*セクション)、または個々 のサービスをサポートする`EnableRetries`(ように、*サービス*セクション)。</span><span class="sxs-lookup"><span data-stu-id="64572-133">Notice that the `EnableRetries` parameter can be set at either a global level (as shown in the *CommonParameters* section) or for individual services that support `EnableRetries` (as shown in the *Services* section).</span></span>  
  
 <span data-ttu-id="64572-134">動作を制御する構成ファイルの使用の詳細については、<xref:System.Workflow.Runtime.WorkflowRuntime>オブジェクトの Windows Workflow Foundation ホスト アプリケーションでは、次を参照してください。[ワークフロー構成ファイル](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))します。</span><span class="sxs-lookup"><span data-stu-id="64572-134">For more information on using a configuration file to control the behavior of a <xref:System.Workflow.Runtime.WorkflowRuntime> object of a Windows Workflow Foundation host application, see [Workflow Configuration Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="64572-135">例</span><span class="sxs-lookup"><span data-stu-id="64572-135">Example</span></span>  
  
```xml  
<commonParameters>
  <add name="ConnectionString"
       value="Initial Catalog=WorkflowStore;Data Source=localhost;Integrated Security=SSPI;" />
  <add name="EnableRetries"
       value="true" />
</commonParameters>
```  
  
## <a name="see-also"></a><span data-ttu-id="64572-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="64572-136">See also</span></span>
- <xref:System.ServiceModel.Configuration.WorkflowRuntimeElement>
- <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>
- <xref:System.Workflow.Runtime.WorkflowRuntime>
- <xref:System.Workflow.Runtime.Hosting.DefaultWorkflowCommitWorkBatchService>
- <xref:System.Workflow.Runtime.Hosting.SqlWorkflowPersistenceService>
- <span data-ttu-id="64572-137">[ワークフロー構成ファイル](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="64572-137">[Workflow Configuration Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span></span>
- [<span data-ttu-id="64572-138">\<commonParameters></span><span class="sxs-lookup"><span data-stu-id="64572-138">\<commonParameters></span></span>](https://msdn.microsoft.com/library/d0e1e6fc-985a-4713-b7da-194e30dfab4c)
