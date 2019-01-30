---
title: <claimTypeRequired>
ms.date: 03/30/2017
ms.assetid: c469d71f-6c77-4a24-97aa-53efa126ceef
author: BrucePerlerMS
ms.openlocfilehash: eafaf253e27db632f17acfce4445a07d18b109aa
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55277455"
---
# <a name="claimtyperequired"></a><span data-ttu-id="084c7-101">\<claimTypeRequired></span><span class="sxs-lookup"><span data-stu-id="084c7-101">\<claimTypeRequired></span></span>
<span data-ttu-id="084c7-102">必要な受信セキュリティ トークンのクレームのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="084c7-102">Specifies the set of required claims for incoming security tokens.</span></span>  
  
 <span data-ttu-id="084c7-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="084c7-103">\<system.identityModel></span></span>  
<span data-ttu-id="084c7-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="084c7-104">\<identityConfiguration></span></span>  
<span data-ttu-id="084c7-105">\<claimTypeRequired></span><span class="sxs-lookup"><span data-stu-id="084c7-105">\<claimTypeRequired></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="084c7-106">構文</span><span class="sxs-lookup"><span data-stu-id="084c7-106">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimTypeRequired>  
    </claimTypeRequired>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="084c7-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="084c7-107">Attributes and Elements</span></span>  
 <span data-ttu-id="084c7-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="084c7-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="084c7-109">属性</span><span class="sxs-lookup"><span data-stu-id="084c7-109">Attributes</span></span>  
 <span data-ttu-id="084c7-110">なし</span><span class="sxs-lookup"><span data-stu-id="084c7-110">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="084c7-111">子要素</span><span class="sxs-lookup"><span data-stu-id="084c7-111">Child Elements</span></span>  
  
|<span data-ttu-id="084c7-112">要素</span><span class="sxs-lookup"><span data-stu-id="084c7-112">Element</span></span>|<span data-ttu-id="084c7-113">説明</span><span class="sxs-lookup"><span data-stu-id="084c7-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="084c7-114">\<claimType></span><span class="sxs-lookup"><span data-stu-id="084c7-114">\<claimType></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimtype.md)|<span data-ttu-id="084c7-115">受け取ったセキュリティ トークンの 1 つの省略可能または必須のクレームを指定します。</span><span class="sxs-lookup"><span data-stu-id="084c7-115">Specifies a single optional or required claim for incoming security tokens.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="084c7-116">親要素</span><span class="sxs-lookup"><span data-stu-id="084c7-116">Parent Elements</span></span>  
  
|<span data-ttu-id="084c7-117">要素</span><span class="sxs-lookup"><span data-stu-id="084c7-117">Element</span></span>|<span data-ttu-id="084c7-118">説明</span><span class="sxs-lookup"><span data-stu-id="084c7-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="084c7-119">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="084c7-119">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="084c7-120">サービス レベルの id の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="084c7-120">Specifies service-level identity settings.</span></span>|
