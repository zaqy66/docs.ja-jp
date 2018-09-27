---
title: '&lt;ClaimType&gt;'
ms.date: 03/30/2017
ms.assetid: d17b5831-9a2c-45c4-b0d1-68f48e72e861
author: BrucePerlerMS
ms.openlocfilehash: 805377565b6e835fd9ffba915a003bc56529a3b6
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2018
ms.locfileid: "47234962"
---
# <a name="ltclaimtypegt"></a><span data-ttu-id="dc0d7-102">&lt;ClaimType&gt;</span><span class="sxs-lookup"><span data-stu-id="dc0d7-102">&lt;claimType&gt;</span></span>
<span data-ttu-id="dc0d7-103">受け取ったセキュリティ トークンの 1 つの省略可能または必須のクレームを指定します。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-103">Specifies a single optional or required claim for incoming security tokens.</span></span>  
  
 <span data-ttu-id="dc0d7-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="dc0d7-104">\<system.identityModel></span></span>  
<span data-ttu-id="dc0d7-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="dc0d7-105">\<identityConfiguration></span></span>  
<span data-ttu-id="dc0d7-106">\<claimTypeRequired ></span><span class="sxs-lookup"><span data-stu-id="dc0d7-106">\<claimTypeRequired></span></span>  
<span data-ttu-id="dc0d7-107">\<claimType ></span><span class="sxs-lookup"><span data-stu-id="dc0d7-107">\<claimType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc0d7-108">構文</span><span class="sxs-lookup"><span data-stu-id="dc0d7-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimTypeRequired>  
      <claimType type=URI optional=xs:boolean >  
      </claimType>  
    </claimTypeRequired>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dc0d7-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="dc0d7-109">Attributes and Elements</span></span>  
 <span data-ttu-id="dc0d7-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dc0d7-111">属性</span><span class="sxs-lookup"><span data-stu-id="dc0d7-111">Attributes</span></span>  
  
|<span data-ttu-id="dc0d7-112">属性</span><span class="sxs-lookup"><span data-stu-id="dc0d7-112">Attribute</span></span>|<span data-ttu-id="dc0d7-113">説明</span><span class="sxs-lookup"><span data-stu-id="dc0d7-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="dc0d7-114">型</span><span class="sxs-lookup"><span data-stu-id="dc0d7-114">type</span></span>|<span data-ttu-id="dc0d7-115">要求の種類。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-115">The claim type.</span></span> <span data-ttu-id="dc0d7-116">通常は URI です。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-116">Typically a URI.</span></span> <span data-ttu-id="dc0d7-117">必須。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-117">Required.</span></span>|  
|<span data-ttu-id="dc0d7-118">optional</span><span class="sxs-lookup"><span data-stu-id="dc0d7-118">optional</span></span>|<span data-ttu-id="dc0d7-119">要求の種類が省略可能かどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-119">A boolean value that specifies whether the claim type is optional.</span></span> <span data-ttu-id="dc0d7-120">任意。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-120">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dc0d7-121">子要素</span><span class="sxs-lookup"><span data-stu-id="dc0d7-121">Child Elements</span></span>  
 <span data-ttu-id="dc0d7-122">なし</span><span class="sxs-lookup"><span data-stu-id="dc0d7-122">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dc0d7-123">親要素</span><span class="sxs-lookup"><span data-stu-id="dc0d7-123">Parent Elements</span></span>  
  
|<span data-ttu-id="dc0d7-124">要素</span><span class="sxs-lookup"><span data-stu-id="dc0d7-124">Element</span></span>|<span data-ttu-id="dc0d7-125">説明</span><span class="sxs-lookup"><span data-stu-id="dc0d7-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dc0d7-126">\<claimTypeRequired ></span><span class="sxs-lookup"><span data-stu-id="dc0d7-126">\<claimTypeRequired></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimtyperequired.md)|<span data-ttu-id="dc0d7-127">必要な受信セキュリティ トークンのクレームのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-127">Specifies the set of required claims for incoming security tokens.</span></span>|
