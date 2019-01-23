---
title: '&lt;tokenReplayCache&gt;'
ms.date: 03/30/2017
ms.assetid: 1572ab23-6933-41b5-bfb4-0c4548145500
author: BrucePerlerMS
ms.openlocfilehash: 1e89afc5764dbdb86e87d2307425299dff57c686
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54525167"
---
# <a name="lttokenreplaycachegt"></a><span data-ttu-id="4cfdf-102">&lt;tokenReplayCache&gt;</span><span class="sxs-lookup"><span data-stu-id="4cfdf-102">&lt;tokenReplayCache&gt;</span></span>
<span data-ttu-id="4cfdf-103">トークン再生キャッシュ サービスまたはセキュリティ トークン ハンドラー コレクションに登録します。</span><span class="sxs-lookup"><span data-stu-id="4cfdf-103">Registers a token replay cache with a service or a security token handler collection.</span></span>  
  
 <span data-ttu-id="4cfdf-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="4cfdf-104">\<system.identityModel></span></span>  
<span data-ttu-id="4cfdf-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="4cfdf-105">\<identityConfiguration></span></span>  
<span data-ttu-id="4cfdf-106">\<caches></span><span class="sxs-lookup"><span data-stu-id="4cfdf-106">\<caches></span></span>  
<span data-ttu-id="4cfdf-107">\<tokenReplayCache></span><span class="sxs-lookup"><span data-stu-id="4cfdf-107">\<tokenReplayCache></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4cfdf-108">構文</span><span class="sxs-lookup"><span data-stu-id="4cfdf-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
      <tokenReplayCache type=xs:string>  
      </tokenReplayCache>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4cfdf-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="4cfdf-109">Attributes and Elements</span></span>  
 <span data-ttu-id="4cfdf-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="4cfdf-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4cfdf-111">属性</span><span class="sxs-lookup"><span data-stu-id="4cfdf-111">Attributes</span></span>  
  
|<span data-ttu-id="4cfdf-112">属性</span><span class="sxs-lookup"><span data-stu-id="4cfdf-112">Attribute</span></span>|<span data-ttu-id="4cfdf-113">説明</span><span class="sxs-lookup"><span data-stu-id="4cfdf-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4cfdf-114">型</span><span class="sxs-lookup"><span data-stu-id="4cfdf-114">type</span></span>|<span data-ttu-id="4cfdf-115">派生した型、<xref:System.IdentityModel.Tokens.TokenReplayCache>クラス。</span><span class="sxs-lookup"><span data-stu-id="4cfdf-115">A type that derives from the <xref:System.IdentityModel.Tokens.TokenReplayCache> class.</span></span> <span data-ttu-id="4cfdf-116">詳細については、ユーザー設定を指定する方法についての`type`、[カスタム型の参照] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cfdf-116">For more information about how to specify a custom `type`, see [Custom Type References].</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4cfdf-117">子要素</span><span class="sxs-lookup"><span data-stu-id="4cfdf-117">Child Elements</span></span>  
 <span data-ttu-id="4cfdf-118">なし</span><span class="sxs-lookup"><span data-stu-id="4cfdf-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4cfdf-119">親要素</span><span class="sxs-lookup"><span data-stu-id="4cfdf-119">Parent Elements</span></span>  
  
|<span data-ttu-id="4cfdf-120">要素</span><span class="sxs-lookup"><span data-stu-id="4cfdf-120">Element</span></span>|<span data-ttu-id="4cfdf-121">説明</span><span class="sxs-lookup"><span data-stu-id="4cfdf-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4cfdf-122">\<caches></span><span class="sxs-lookup"><span data-stu-id="4cfdf-122">\<caches></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|<span data-ttu-id="4cfdf-123">サービスまたはセキュリティ トークン ハンドラー コレクションで使用されるキャッシュを登録します。</span><span class="sxs-lookup"><span data-stu-id="4cfdf-123">Registers the caches used by a service or a security token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4cfdf-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="4cfdf-124">Remarks</span></span>  
 <span data-ttu-id="4cfdf-125">トークン再生キャッシュを使用して、再生されたトークンを検出できます。</span><span class="sxs-lookup"><span data-stu-id="4cfdf-125">The token replay cache is used to detect replayed tokens.</span></span> <span data-ttu-id="4cfdf-126">トークン リプレイ検出が有効になっている、 [ \<tokenReplayDetection >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md)要素もトークンの最大有効期限を指定します。</span><span class="sxs-lookup"><span data-stu-id="4cfdf-126">Token replay detection is enabled by the [\<tokenReplayDetection>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md) element, which also specifies the maximum expiration time for tokens.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4cfdf-127">例</span><span class="sxs-lookup"><span data-stu-id="4cfdf-127">Example</span></span>  
 <span data-ttu-id="4cfdf-128">次の XML は、再生されたトークンを検出するためのカスタム キャッシュの構成を示しています。</span><span class="sxs-lookup"><span data-stu-id="4cfdf-128">The following XML shows the configuration of a custom cache for detecting replayed tokens.</span></span>  
  
```xml  
<caches>  
  <tokenReplayCache type="MyCacheLibrary.MyTokenReplayCache, MyCacheLibrary">  
  </tokenReplayCache>  
</caches>  
```  
  
## <a name="see-also"></a><span data-ttu-id="4cfdf-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="4cfdf-129">See also</span></span>
- <xref:System.IdentityModel.Tokens.TokenReplayCache>
- [<span data-ttu-id="4cfdf-130">\<tokenReplayDetection></span><span class="sxs-lookup"><span data-stu-id="4cfdf-130">\<tokenReplayDetection></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md)
