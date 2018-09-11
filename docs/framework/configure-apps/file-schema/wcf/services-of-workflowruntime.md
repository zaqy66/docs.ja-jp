---
title: '&lt;workflowRuntime&gt; の &lt;services&gt;'
ms.date: 03/30/2017
ms.assetid: 219a05b1-f573-45c9-849b-e86bc373b62f
ms.openlocfilehash: 44da735ab1aa2391fe882dfba6e1afc47be746ff
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44368022"
---
# <a name="ltservicesgt-of-ltworkflowruntimegt"></a><span data-ttu-id="93e1a-102">&lt;workflowRuntime&gt; の &lt;services&gt;</span><span class="sxs-lookup"><span data-stu-id="93e1a-102">&lt;services&gt; of &lt;workflowRuntime&gt;</span></span>
<span data-ttu-id="93e1a-103"><xref:System.Workflow.Runtime.WorkflowRuntime> エンジンに追加されるサービスのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="93e1a-103">Represents a collection of services that will be added to the <xref:System.Workflow.Runtime.WorkflowRuntime> engine.</span></span> <span data-ttu-id="93e1a-104">要素は、<xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="93e1a-104">The elements are of type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span></span>  <span data-ttu-id="93e1a-105">コレクションで指定されたサービスはワークフロー ランタイム エンジンによって初期化され、適切な <xref:System.Workflow.Runtime.WorkflowRuntime> コンストラクターが呼び出されるとワークフロー ランタイム エンジンのサービスに追加されます。</span><span class="sxs-lookup"><span data-stu-id="93e1a-105">The services specified in the collection will be initialized by the workflow runtime engine and added to its services when the appropriate <xref:System.Workflow.Runtime.WorkflowRuntime> constructor is called.</span></span> <span data-ttu-id="93e1a-106">したがって、コレクションで指定されたサービスは、そのコンストラクターのシグネチャに関して一定の規則に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="93e1a-106">Therefore, the services specified in the collection must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="93e1a-107">詳細については、「<xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93e1a-107">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93e1a-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="93e1a-108">See Also</span></span>  
 <xref:System.Workflow.Runtime.WorkflowRuntime>  
 <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>  
 <xref:System.Workflow.Runtime.WorkflowRuntime>  
 <span data-ttu-id="93e1a-109">[ワークフロー構成ファイル](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="93e1a-109">[Workflow Configuration Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span></span>
