---
title: '&lt;workflowInstanceManagement&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 63ac89ba-c844-4ae2-96ae-cd752a90a109
ms.openlocfilehash: ba3d9415efc21012b470fd2e9a7f426ca8f3aad1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54662063"
---
# <a name="ltworkflowinstancemanagementgt"></a><span data-ttu-id="90f66-102">&lt;workflowInstanceManagement&gt;</span><span class="sxs-lookup"><span data-stu-id="90f66-102">&lt;workflowInstanceManagement&gt;</span></span>
<span data-ttu-id="90f66-103">ワークフロー インスタンスの実行方法を制御する設定を指定するためのサービス動作。これには、永続する未処理の例外動作やアイドル状態の動作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="90f66-103">A service behavior that enables you to specify settings that control how workflow instances are run, including persistence, unhandled Exception behavior and idle behavior.</span></span>  
  
<span data-ttu-id="90f66-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="90f66-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="90f66-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="90f66-105">\<behaviors></span></span>  
<span data-ttu-id="90f66-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="90f66-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="90f66-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="90f66-107">\<behavior></span></span>  
<span data-ttu-id="90f66-108">\<workflowInstanceManagement></span><span class="sxs-lookup"><span data-stu-id="90f66-108">\<workflowInstanceManagement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="90f66-109">構文</span><span class="sxs-lookup"><span data-stu-id="90f66-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <workflowInstanceManagement authorizedWindowsGroup="" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="90f66-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="90f66-110">Attributes and Elements</span></span>  
 <span data-ttu-id="90f66-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="90f66-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="90f66-112">属性</span><span class="sxs-lookup"><span data-stu-id="90f66-112">Attributes</span></span>  
  
|<span data-ttu-id="90f66-113">属性</span><span class="sxs-lookup"><span data-stu-id="90f66-113">Attribute</span></span>|<span data-ttu-id="90f66-114">説明</span><span class="sxs-lookup"><span data-stu-id="90f66-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="90f66-115">authorizedWindowsGroup</span><span class="sxs-lookup"><span data-stu-id="90f66-115">authorizedWindowsGroup</span></span>||  
  
### <a name="child-elements"></a><span data-ttu-id="90f66-116">子要素</span><span class="sxs-lookup"><span data-stu-id="90f66-116">Child Elements</span></span>  
 <span data-ttu-id="90f66-117">なし。</span><span class="sxs-lookup"><span data-stu-id="90f66-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="90f66-118">親要素</span><span class="sxs-lookup"><span data-stu-id="90f66-118">Parent Elements</span></span>  
  
|<span data-ttu-id="90f66-119">要素</span><span class="sxs-lookup"><span data-stu-id="90f66-119">Element</span></span>|<span data-ttu-id="90f66-120">説明</span><span class="sxs-lookup"><span data-stu-id="90f66-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="90f66-121">\<動作 > の\<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="90f66-121">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="90f66-122">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="90f66-122">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="90f66-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="90f66-123">See also</span></span>
- <xref:System.ServiceModel.Activities.Description.WorkflowInstanceManagementBehavior>
- <xref:System.ServiceModel.Activities.Configuration.WorkflowInstanceManagementElement>
