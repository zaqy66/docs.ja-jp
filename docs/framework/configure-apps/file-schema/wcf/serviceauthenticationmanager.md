---
title: <serviceAuthenticationManager>
ms.date: 03/30/2017
ms.assetid: 5d69e64f-f325-4d55-8e2d-0fb30f222dda
ms.openlocfilehash: 7708dd8a572dd24c2852410b1781fce2807efab9
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55263486"
---
# <a name="serviceauthenticationmanager"></a><span data-ttu-id="9b4ed-101">\<serviceAuthenticationManager></span><span class="sxs-lookup"><span data-stu-id="9b4ed-101">\<serviceAuthenticationManager></span></span>
<span data-ttu-id="9b4ed-102">サービス レベルで転送、メッセージ、または送信元の有効性を確立するワークフロー構成要素を提供します。</span><span class="sxs-lookup"><span data-stu-id="9b4ed-102">Provides a workflow configuration element that establishes at the service level the validity of a transmission, message, or originator.</span></span>  
  
<span data-ttu-id="9b4ed-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="9b4ed-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="9b4ed-104">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="9b4ed-104">\<behaviors></span></span>  
<span data-ttu-id="9b4ed-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="9b4ed-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="9b4ed-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="9b4ed-106">\<behavior></span></span>  
<span data-ttu-id="9b4ed-107">\<serviceAuthenticationManager></span><span class="sxs-lookup"><span data-stu-id="9b4ed-107">\<serviceAuthenticationManager></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9b4ed-108">構文</span><span class="sxs-lookup"><span data-stu-id="9b4ed-108">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <serviceAuthenticationManager serviceAuthenticationManagerType="String" />
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9b4ed-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="9b4ed-109">Attributes and Elements</span></span>  
 <span data-ttu-id="9b4ed-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="9b4ed-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9b4ed-111">属性</span><span class="sxs-lookup"><span data-stu-id="9b4ed-111">Attributes</span></span>  
  
|<span data-ttu-id="9b4ed-112">属性</span><span class="sxs-lookup"><span data-stu-id="9b4ed-112">Attribute</span></span>|<span data-ttu-id="9b4ed-113">説明</span><span class="sxs-lookup"><span data-stu-id="9b4ed-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9b4ed-114">serviceAuthenticationManagerType</span><span class="sxs-lookup"><span data-stu-id="9b4ed-114">serviceAuthenticationManagerType</span></span>|<span data-ttu-id="9b4ed-115">現在の動作の認証ポリシーの種類を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="9b4ed-115">A string that specifies the type of the authentication policy for the current behavior.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9b4ed-116">子要素</span><span class="sxs-lookup"><span data-stu-id="9b4ed-116">Child Elements</span></span>  
 <span data-ttu-id="9b4ed-117">なし。</span><span class="sxs-lookup"><span data-stu-id="9b4ed-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9b4ed-118">親要素</span><span class="sxs-lookup"><span data-stu-id="9b4ed-118">Parent Elements</span></span>  
  
|<span data-ttu-id="9b4ed-119">要素</span><span class="sxs-lookup"><span data-stu-id="9b4ed-119">Element</span></span>|<span data-ttu-id="9b4ed-120">説明</span><span class="sxs-lookup"><span data-stu-id="9b4ed-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9b4ed-121">\<behavior></span><span class="sxs-lookup"><span data-stu-id="9b4ed-121">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="9b4ed-122">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b4ed-122">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9b4ed-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b4ed-123">See also</span></span>
- <xref:System.ServiceModel.Configuration.ServiceAuthenticationElement>
