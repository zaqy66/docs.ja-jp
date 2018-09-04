---
title: '&lt;remove&gt;'
ms.date: 03/30/2017
ms.assetid: 4058e2f1-7db4-4d1a-84dd-1b52836f2ae6
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 596cab4494ef3ba200fd0a046d7935f648fb7c4f
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43503216"
---
# <a name="ltremovegt"></a><span data-ttu-id="5f16b-102">&lt;remove&gt;</span><span class="sxs-lookup"><span data-stu-id="5f16b-102">&lt;remove&gt;</span></span>
<span data-ttu-id="5f16b-103">トークン ハンドラー コレクションから指定したセキュリティ トークン ハンドラーを削除します。</span><span class="sxs-lookup"><span data-stu-id="5f16b-103">Removes the specified security token handler from the token handler collection.</span></span>  
  
 <span data-ttu-id="5f16b-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="5f16b-104">\<system.identityModel></span></span>  
<span data-ttu-id="5f16b-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="5f16b-105">\<identityConfiguration></span></span>  
<span data-ttu-id="5f16b-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="5f16b-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="5f16b-107">\<remove></span><span class="sxs-lookup"><span data-stu-id="5f16b-107">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f16b-108">構文</span><span class="sxs-lookup"><span data-stu-id="5f16b-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <remove type=xs:string >  
      </remove>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5f16b-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="5f16b-109">Attributes and Elements</span></span>  
 <span data-ttu-id="5f16b-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="5f16b-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5f16b-111">属性</span><span class="sxs-lookup"><span data-stu-id="5f16b-111">Attributes</span></span>  
  
|<span data-ttu-id="5f16b-112">属性</span><span class="sxs-lookup"><span data-stu-id="5f16b-112">Attribute</span></span>|<span data-ttu-id="5f16b-113">説明</span><span class="sxs-lookup"><span data-stu-id="5f16b-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5f16b-114">型</span><span class="sxs-lookup"><span data-stu-id="5f16b-114">type</span></span>|<span data-ttu-id="5f16b-115">削除するトークン ハンドラーの CLR 型名。</span><span class="sxs-lookup"><span data-stu-id="5f16b-115">The CLR type name of the token handler to be removed.</span></span> <span data-ttu-id="5f16b-116">詳細を指定する方法については、`type`属性は、「[カスタム型の参照](https://msdn.microsoft.com/library/7286d2e3-c63d-49fd-abdc-ce2705f22c24)します。</span><span class="sxs-lookup"><span data-stu-id="5f16b-116">For more information about how to specify the `type` attribute, see [Custom Type References](https://msdn.microsoft.com/library/7286d2e3-c63d-49fd-abdc-ce2705f22c24).</span></span> <span data-ttu-id="5f16b-117">必須。</span><span class="sxs-lookup"><span data-stu-id="5f16b-117">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5f16b-118">子要素</span><span class="sxs-lookup"><span data-stu-id="5f16b-118">Child Elements</span></span>  
 <span data-ttu-id="5f16b-119">なし</span><span class="sxs-lookup"><span data-stu-id="5f16b-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5f16b-120">親要素</span><span class="sxs-lookup"><span data-stu-id="5f16b-120">Parent Elements</span></span>  
  
|<span data-ttu-id="5f16b-121">要素</span><span class="sxs-lookup"><span data-stu-id="5f16b-121">Element</span></span>|<span data-ttu-id="5f16b-122">説明</span><span class="sxs-lookup"><span data-stu-id="5f16b-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5f16b-123">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="5f16b-123">\<securityTokenHandlers></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|<span data-ttu-id="5f16b-124">エンドポイントに登録されているセキュリティ トークン ハンドラーのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="5f16b-124">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="5f16b-125">例</span><span class="sxs-lookup"><span data-stu-id="5f16b-125">Example</span></span>  
 <span data-ttu-id="5f16b-126">次の XML の使用を示しています、`<add>`と`<remove>`に既定のセッション トークン ハンドラーをカスタム セッション トークン ハンドラーに置き換える要素。</span><span class="sxs-lookup"><span data-stu-id="5f16b-126">The following XML shows the use of the `<add>` and `<remove>` elements to replace the default session token handler with a custom session token handler.</span></span> <span data-ttu-id="5f16b-127">XML から取得されますが、`ClaimsAwareWebFarm`サンプル。</span><span class="sxs-lookup"><span data-stu-id="5f16b-127">The XML is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<securityTokenHandlers>  
  <remove type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
  <add type="System.IdentityModel.Services.Tokens.MachineKeySessionSecurityTokenHandler, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
</securityTokenHandlers>  
```
