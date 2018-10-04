---
title: '&lt;claimTypeRequired&gt;'
ms.date: 03/30/2017
ms.assetid: c469d71f-6c77-4a24-97aa-53efa126ceef
author: BrucePerlerMS
ms.openlocfilehash: df4494de6b76943849db2bedef8f43ad894b6bd1
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48780662"
---
# <a name="ltclaimtyperequiredgt"></a><span data-ttu-id="bf882-102">&lt;claimTypeRequired&gt;</span><span class="sxs-lookup"><span data-stu-id="bf882-102">&lt;claimTypeRequired&gt;</span></span>
<span data-ttu-id="bf882-103">必要な受信セキュリティ トークンのクレームのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="bf882-103">Specifies the set of required claims for incoming security tokens.</span></span>  
  
 <span data-ttu-id="bf882-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="bf882-104">\<system.identityModel></span></span>  
<span data-ttu-id="bf882-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="bf882-105">\<identityConfiguration></span></span>  
<span data-ttu-id="bf882-106">\<claimTypeRequired ></span><span class="sxs-lookup"><span data-stu-id="bf882-106">\<claimTypeRequired></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bf882-107">構文</span><span class="sxs-lookup"><span data-stu-id="bf882-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimTypeRequired>  
    </claimTypeRequired>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bf882-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="bf882-108">Attributes and Elements</span></span>  
 <span data-ttu-id="bf882-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="bf882-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bf882-110">属性</span><span class="sxs-lookup"><span data-stu-id="bf882-110">Attributes</span></span>  
 <span data-ttu-id="bf882-111">なし</span><span class="sxs-lookup"><span data-stu-id="bf882-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="bf882-112">子要素</span><span class="sxs-lookup"><span data-stu-id="bf882-112">Child Elements</span></span>  
  
|<span data-ttu-id="bf882-113">要素</span><span class="sxs-lookup"><span data-stu-id="bf882-113">Element</span></span>|<span data-ttu-id="bf882-114">説明</span><span class="sxs-lookup"><span data-stu-id="bf882-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bf882-115">\<claimType ></span><span class="sxs-lookup"><span data-stu-id="bf882-115">\<claimType></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimtype.md)|<span data-ttu-id="bf882-116">受け取ったセキュリティ トークンの 1 つの省略可能または必須のクレームを指定します。</span><span class="sxs-lookup"><span data-stu-id="bf882-116">Specifies a single optional or required claim for incoming security tokens.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="bf882-117">親要素</span><span class="sxs-lookup"><span data-stu-id="bf882-117">Parent Elements</span></span>  
  
|<span data-ttu-id="bf882-118">要素</span><span class="sxs-lookup"><span data-stu-id="bf882-118">Element</span></span>|<span data-ttu-id="bf882-119">説明</span><span class="sxs-lookup"><span data-stu-id="bf882-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bf882-120">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="bf882-120">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="bf882-121">サービス レベルの id の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="bf882-121">Specifies service-level identity settings.</span></span>|
