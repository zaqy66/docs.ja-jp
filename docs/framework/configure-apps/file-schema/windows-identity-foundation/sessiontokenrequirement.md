---
title: '&lt;sessionTokenRequirement&gt;'
ms.date: 03/30/2017
ms.assetid: 496a1735-cbb7-49d5-a6aa-dd5550462073
author: BrucePerlerMS
ms.openlocfilehash: 4d5d2348f04ace7596a3a513c5106ea612dc17b7
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48792930"
---
# <a name="ltsessiontokenrequirementgt"></a><span data-ttu-id="3f094-102">&lt;sessionTokenRequirement&gt;</span><span class="sxs-lookup"><span data-stu-id="3f094-102">&lt;sessionTokenRequirement&gt;</span></span>
<span data-ttu-id="3f094-103">構成を提供、<xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler>クラスまたは派生クラス。</span><span class="sxs-lookup"><span data-stu-id="3f094-103">Provides configuration for the <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="3f094-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="3f094-104">\<system.identityModel></span></span>  
<span data-ttu-id="3f094-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="3f094-105">\<identityConfiguration></span></span>  
<span data-ttu-id="3f094-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="3f094-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="3f094-107">\<add></span><span class="sxs-lookup"><span data-stu-id="3f094-107">\<add></span></span>  
<span data-ttu-id="3f094-108">\<sessionTokenRequirement ></span><span class="sxs-lookup"><span data-stu-id="3f094-108">\<sessionTokenRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f094-109">構文</span><span class="sxs-lookup"><span data-stu-id="3f094-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">  
        <sessionTokenRequirement lifetime=TimeSpan >  
        </sessionTokenRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3f094-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="3f094-110">Attributes and Elements</span></span>  
 <span data-ttu-id="3f094-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="3f094-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3f094-112">属性</span><span class="sxs-lookup"><span data-stu-id="3f094-112">Attributes</span></span>  
  
|<span data-ttu-id="3f094-113">属性</span><span class="sxs-lookup"><span data-stu-id="3f094-113">Attribute</span></span>|<span data-ttu-id="3f094-114">説明</span><span class="sxs-lookup"><span data-stu-id="3f094-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3f094-115">有効期間</span><span class="sxs-lookup"><span data-stu-id="3f094-115">lifetime</span></span>|<span data-ttu-id="3f094-116">セッション トークンの有効期間を指定します。</span><span class="sxs-lookup"><span data-stu-id="3f094-116">Specifies the lifetime of session tokens.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3f094-117">子要素</span><span class="sxs-lookup"><span data-stu-id="3f094-117">Child Elements</span></span>  
 <span data-ttu-id="3f094-118">なし</span><span class="sxs-lookup"><span data-stu-id="3f094-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3f094-119">親要素</span><span class="sxs-lookup"><span data-stu-id="3f094-119">Parent Elements</span></span>  
  
|<span data-ttu-id="3f094-120">要素</span><span class="sxs-lookup"><span data-stu-id="3f094-120">Element</span></span>|<span data-ttu-id="3f094-121">説明</span><span class="sxs-lookup"><span data-stu-id="3f094-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3f094-122">\<add></span><span class="sxs-lookup"><span data-stu-id="3f094-122">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="3f094-123">トークン ハンドラー コレクションには、指定したセキュリティ トークン ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="3f094-123">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="3f094-124">例</span><span class="sxs-lookup"><span data-stu-id="3f094-124">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">           
    <sessionTokenRequirement lifetime="10:00" />  
</add>  
```
