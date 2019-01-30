---
title: <remove>
ms.date: 03/30/2017
ms.assetid: 4058e2f1-7db4-4d1a-84dd-1b52836f2ae6
author: BrucePerlerMS
ms.openlocfilehash: a54957458311e2d5941d1aa1c2486a2f66994d9b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55288133"
---
# <a name="remove"></a><span data-ttu-id="6b0c5-101">\<remove></span><span class="sxs-lookup"><span data-stu-id="6b0c5-101">\<remove></span></span>
<span data-ttu-id="6b0c5-102">トークン ハンドラー コレクションから指定したセキュリティ トークン ハンドラーを削除します。</span><span class="sxs-lookup"><span data-stu-id="6b0c5-102">Removes the specified security token handler from the token handler collection.</span></span>  
  
 <span data-ttu-id="6b0c5-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="6b0c5-103">\<system.identityModel></span></span>  
<span data-ttu-id="6b0c5-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="6b0c5-104">\<identityConfiguration></span></span>  
<span data-ttu-id="6b0c5-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="6b0c5-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="6b0c5-106">\<remove></span><span class="sxs-lookup"><span data-stu-id="6b0c5-106">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6b0c5-107">構文</span><span class="sxs-lookup"><span data-stu-id="6b0c5-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6b0c5-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="6b0c5-108">Attributes and Elements</span></span>  
 <span data-ttu-id="6b0c5-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="6b0c5-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6b0c5-110">属性</span><span class="sxs-lookup"><span data-stu-id="6b0c5-110">Attributes</span></span>  
  
|<span data-ttu-id="6b0c5-111">属性</span><span class="sxs-lookup"><span data-stu-id="6b0c5-111">Attribute</span></span>|<span data-ttu-id="6b0c5-112">説明</span><span class="sxs-lookup"><span data-stu-id="6b0c5-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6b0c5-113">型</span><span class="sxs-lookup"><span data-stu-id="6b0c5-113">type</span></span>|<span data-ttu-id="6b0c5-114">削除するトークン ハンドラーの CLR 型名。</span><span class="sxs-lookup"><span data-stu-id="6b0c5-114">The CLR type name of the token handler to be removed.</span></span> <span data-ttu-id="6b0c5-115">詳細を指定する方法については、`type`属性は、「[カスタム型の参照](https://msdn.microsoft.com/library/7286d2e3-c63d-49fd-abdc-ce2705f22c24)します。</span><span class="sxs-lookup"><span data-stu-id="6b0c5-115">For more information about how to specify the `type` attribute, see [Custom Type References](https://msdn.microsoft.com/library/7286d2e3-c63d-49fd-abdc-ce2705f22c24).</span></span> <span data-ttu-id="6b0c5-116">必須。</span><span class="sxs-lookup"><span data-stu-id="6b0c5-116">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6b0c5-117">子要素</span><span class="sxs-lookup"><span data-stu-id="6b0c5-117">Child Elements</span></span>  
 <span data-ttu-id="6b0c5-118">なし</span><span class="sxs-lookup"><span data-stu-id="6b0c5-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6b0c5-119">親要素</span><span class="sxs-lookup"><span data-stu-id="6b0c5-119">Parent Elements</span></span>  
  
|<span data-ttu-id="6b0c5-120">要素</span><span class="sxs-lookup"><span data-stu-id="6b0c5-120">Element</span></span>|<span data-ttu-id="6b0c5-121">説明</span><span class="sxs-lookup"><span data-stu-id="6b0c5-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6b0c5-122">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="6b0c5-122">\<securityTokenHandlers></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|<span data-ttu-id="6b0c5-123">エンドポイントに登録されているセキュリティ トークン ハンドラーのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b0c5-123">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="6b0c5-124">例</span><span class="sxs-lookup"><span data-stu-id="6b0c5-124">Example</span></span>  
 <span data-ttu-id="6b0c5-125">次の XML の使用を示しています、`<add>`と`<remove>`に既定のセッション トークン ハンドラーをカスタム セッション トークン ハンドラーに置き換える要素。</span><span class="sxs-lookup"><span data-stu-id="6b0c5-125">The following XML shows the use of the `<add>` and `<remove>` elements to replace the default session token handler with a custom session token handler.</span></span> <span data-ttu-id="6b0c5-126">XML から取得されますが、`ClaimsAwareWebFarm`サンプル。</span><span class="sxs-lookup"><span data-stu-id="6b0c5-126">The XML is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<securityTokenHandlers>  
  <remove type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
  <add type="System.IdentityModel.Services.Tokens.MachineKeySessionSecurityTokenHandler, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
</securityTokenHandlers>  
```
