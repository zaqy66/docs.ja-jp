---
title: <sessionTokenRequirement>
ms.date: 03/30/2017
ms.assetid: 496a1735-cbb7-49d5-a6aa-dd5550462073
author: BrucePerlerMS
ms.openlocfilehash: 0c575e02862884e8f7ecf062138c36fe731f8e19
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271903"
---
# <a name="sessiontokenrequirement"></a><span data-ttu-id="25679-101">\<sessionTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="25679-101">\<sessionTokenRequirement></span></span>
<span data-ttu-id="25679-102">構成を提供、<xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler>クラスまたは派生クラス。</span><span class="sxs-lookup"><span data-stu-id="25679-102">Provides configuration for the <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="25679-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="25679-103">\<system.identityModel></span></span>  
<span data-ttu-id="25679-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="25679-104">\<identityConfiguration></span></span>  
<span data-ttu-id="25679-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="25679-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="25679-106">\<add></span><span class="sxs-lookup"><span data-stu-id="25679-106">\<add></span></span>  
<span data-ttu-id="25679-107">\<sessionTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="25679-107">\<sessionTokenRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="25679-108">構文</span><span class="sxs-lookup"><span data-stu-id="25679-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="25679-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="25679-109">Attributes and Elements</span></span>  
 <span data-ttu-id="25679-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="25679-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="25679-111">属性</span><span class="sxs-lookup"><span data-stu-id="25679-111">Attributes</span></span>  
  
|<span data-ttu-id="25679-112">属性</span><span class="sxs-lookup"><span data-stu-id="25679-112">Attribute</span></span>|<span data-ttu-id="25679-113">説明</span><span class="sxs-lookup"><span data-stu-id="25679-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="25679-114">有効期間</span><span class="sxs-lookup"><span data-stu-id="25679-114">lifetime</span></span>|<span data-ttu-id="25679-115">セッション トークンの有効期間を指定します。</span><span class="sxs-lookup"><span data-stu-id="25679-115">Specifies the lifetime of session tokens.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="25679-116">子要素</span><span class="sxs-lookup"><span data-stu-id="25679-116">Child Elements</span></span>  
 <span data-ttu-id="25679-117">なし</span><span class="sxs-lookup"><span data-stu-id="25679-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="25679-118">親要素</span><span class="sxs-lookup"><span data-stu-id="25679-118">Parent Elements</span></span>  
  
|<span data-ttu-id="25679-119">要素</span><span class="sxs-lookup"><span data-stu-id="25679-119">Element</span></span>|<span data-ttu-id="25679-120">説明</span><span class="sxs-lookup"><span data-stu-id="25679-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="25679-121">\<add></span><span class="sxs-lookup"><span data-stu-id="25679-121">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="25679-122">トークン ハンドラー コレクションには、指定したセキュリティ トークン ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="25679-122">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="25679-123">例</span><span class="sxs-lookup"><span data-stu-id="25679-123">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">           
    <sessionTokenRequirement lifetime="10:00" />  
</add>  
```
