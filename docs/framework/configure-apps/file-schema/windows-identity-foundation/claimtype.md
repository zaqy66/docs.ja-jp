---
title: '&lt;ClaimType&gt;'
ms.date: 03/30/2017
ms.assetid: d17b5831-9a2c-45c4-b0d1-68f48e72e861
author: BrucePerlerMS
ms.openlocfilehash: 805377565b6e835fd9ffba915a003bc56529a3b6
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47084216"
---
# <a name="ltclaimtypegt"></a><span data-ttu-id="940c1-102">&lt;ClaimType&gt;</span><span class="sxs-lookup"><span data-stu-id="940c1-102">&lt;claimType&gt;</span></span>
<span data-ttu-id="940c1-103">受け取ったセキュリティ トークンの 1 つの省略可能または必須のクレームを指定します。</span><span class="sxs-lookup"><span data-stu-id="940c1-103">Specifies a single optional or required claim for incoming security tokens.</span></span>  
  
 <span data-ttu-id="940c1-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="940c1-104">\<system.identityModel></span></span>  
<span data-ttu-id="940c1-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="940c1-105">\<identityConfiguration></span></span>  
<span data-ttu-id="940c1-106">\<claimTypeRequired ></span><span class="sxs-lookup"><span data-stu-id="940c1-106">\<claimTypeRequired></span></span>  
<span data-ttu-id="940c1-107">\<claimType ></span><span class="sxs-lookup"><span data-stu-id="940c1-107">\<claimType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="940c1-108">構文</span><span class="sxs-lookup"><span data-stu-id="940c1-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="940c1-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="940c1-109">Attributes and Elements</span></span>  
 <span data-ttu-id="940c1-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="940c1-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="940c1-111">属性</span><span class="sxs-lookup"><span data-stu-id="940c1-111">Attributes</span></span>  
  
|<span data-ttu-id="940c1-112">属性</span><span class="sxs-lookup"><span data-stu-id="940c1-112">Attribute</span></span>|<span data-ttu-id="940c1-113">説明</span><span class="sxs-lookup"><span data-stu-id="940c1-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="940c1-114">型</span><span class="sxs-lookup"><span data-stu-id="940c1-114">type</span></span>|<span data-ttu-id="940c1-115">要求の種類。</span><span class="sxs-lookup"><span data-stu-id="940c1-115">The claim type.</span></span> <span data-ttu-id="940c1-116">通常は URI です。</span><span class="sxs-lookup"><span data-stu-id="940c1-116">Typically a URI.</span></span> <span data-ttu-id="940c1-117">必須。</span><span class="sxs-lookup"><span data-stu-id="940c1-117">Required.</span></span>|  
|<span data-ttu-id="940c1-118">optional</span><span class="sxs-lookup"><span data-stu-id="940c1-118">optional</span></span>|<span data-ttu-id="940c1-119">要求の種類が省略可能かどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="940c1-119">A boolean value that specifies whether the claim type is optional.</span></span> <span data-ttu-id="940c1-120">任意。</span><span class="sxs-lookup"><span data-stu-id="940c1-120">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="940c1-121">子要素</span><span class="sxs-lookup"><span data-stu-id="940c1-121">Child Elements</span></span>  
 <span data-ttu-id="940c1-122">なし</span><span class="sxs-lookup"><span data-stu-id="940c1-122">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="940c1-123">親要素</span><span class="sxs-lookup"><span data-stu-id="940c1-123">Parent Elements</span></span>  
  
|<span data-ttu-id="940c1-124">要素</span><span class="sxs-lookup"><span data-stu-id="940c1-124">Element</span></span>|<span data-ttu-id="940c1-125">説明</span><span class="sxs-lookup"><span data-stu-id="940c1-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="940c1-126">\<claimTypeRequired ></span><span class="sxs-lookup"><span data-stu-id="940c1-126">\<claimTypeRequired></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimtyperequired.md)|<span data-ttu-id="940c1-127">必要な受信セキュリティ トークンのクレームのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="940c1-127">Specifies the set of required claims for incoming security tokens.</span></span>|
