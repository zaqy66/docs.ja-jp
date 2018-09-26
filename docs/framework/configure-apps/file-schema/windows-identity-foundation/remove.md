---
title: '&lt;remove&gt;'
ms.date: 03/30/2017
ms.assetid: 4058e2f1-7db4-4d1a-84dd-1b52836f2ae6
author: BrucePerlerMS
ms.openlocfilehash: 410fef1a43f9202d56c4957b1162c53ee056ae3f
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47198723"
---
# <a name="ltremovegt"></a><span data-ttu-id="c51e2-102">&lt;remove&gt;</span><span class="sxs-lookup"><span data-stu-id="c51e2-102">&lt;remove&gt;</span></span>
<span data-ttu-id="c51e2-103">トークン ハンドラー コレクションから指定したセキュリティ トークン ハンドラーを削除します。</span><span class="sxs-lookup"><span data-stu-id="c51e2-103">Removes the specified security token handler from the token handler collection.</span></span>  
  
 <span data-ttu-id="c51e2-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="c51e2-104">\<system.identityModel></span></span>  
<span data-ttu-id="c51e2-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="c51e2-105">\<identityConfiguration></span></span>  
<span data-ttu-id="c51e2-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="c51e2-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="c51e2-107">\<remove></span><span class="sxs-lookup"><span data-stu-id="c51e2-107">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c51e2-108">構文</span><span class="sxs-lookup"><span data-stu-id="c51e2-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c51e2-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="c51e2-109">Attributes and Elements</span></span>  
 <span data-ttu-id="c51e2-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="c51e2-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c51e2-111">属性</span><span class="sxs-lookup"><span data-stu-id="c51e2-111">Attributes</span></span>  
  
|<span data-ttu-id="c51e2-112">属性</span><span class="sxs-lookup"><span data-stu-id="c51e2-112">Attribute</span></span>|<span data-ttu-id="c51e2-113">説明</span><span class="sxs-lookup"><span data-stu-id="c51e2-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c51e2-114">型</span><span class="sxs-lookup"><span data-stu-id="c51e2-114">type</span></span>|<span data-ttu-id="c51e2-115">削除するトークン ハンドラーの CLR 型名。</span><span class="sxs-lookup"><span data-stu-id="c51e2-115">The CLR type name of the token handler to be removed.</span></span> <span data-ttu-id="c51e2-116">詳細を指定する方法については、`type`属性は、「[カスタム型の参照](https://msdn.microsoft.com/library/7286d2e3-c63d-49fd-abdc-ce2705f22c24)します。</span><span class="sxs-lookup"><span data-stu-id="c51e2-116">For more information about how to specify the `type` attribute, see [Custom Type References](https://msdn.microsoft.com/library/7286d2e3-c63d-49fd-abdc-ce2705f22c24).</span></span> <span data-ttu-id="c51e2-117">必須。</span><span class="sxs-lookup"><span data-stu-id="c51e2-117">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c51e2-118">子要素</span><span class="sxs-lookup"><span data-stu-id="c51e2-118">Child Elements</span></span>  
 <span data-ttu-id="c51e2-119">なし</span><span class="sxs-lookup"><span data-stu-id="c51e2-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c51e2-120">親要素</span><span class="sxs-lookup"><span data-stu-id="c51e2-120">Parent Elements</span></span>  
  
|<span data-ttu-id="c51e2-121">要素</span><span class="sxs-lookup"><span data-stu-id="c51e2-121">Element</span></span>|<span data-ttu-id="c51e2-122">説明</span><span class="sxs-lookup"><span data-stu-id="c51e2-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c51e2-123">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="c51e2-123">\<securityTokenHandlers></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|<span data-ttu-id="c51e2-124">エンドポイントに登録されているセキュリティ トークン ハンドラーのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="c51e2-124">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="c51e2-125">例</span><span class="sxs-lookup"><span data-stu-id="c51e2-125">Example</span></span>  
 <span data-ttu-id="c51e2-126">次の XML の使用を示しています、`<add>`と`<remove>`に既定のセッション トークン ハンドラーをカスタム セッション トークン ハンドラーに置き換える要素。</span><span class="sxs-lookup"><span data-stu-id="c51e2-126">The following XML shows the use of the `<add>` and `<remove>` elements to replace the default session token handler with a custom session token handler.</span></span> <span data-ttu-id="c51e2-127">XML から取得されますが、`ClaimsAwareWebFarm`サンプル。</span><span class="sxs-lookup"><span data-stu-id="c51e2-127">The XML is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<securityTokenHandlers>  
  <remove type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
  <add type="System.IdentityModel.Services.Tokens.MachineKeySessionSecurityTokenHandler, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
</securityTokenHandlers>  
```
