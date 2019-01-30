---
title: <tokenReplayCache>
ms.date: 03/30/2017
ms.assetid: 1572ab23-6933-41b5-bfb4-0c4548145500
author: BrucePerlerMS
ms.openlocfilehash: dfa6c0d84582d55595f00f149adfdcaa9d554d6b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271951"
---
# <a name="tokenreplaycache"></a><span data-ttu-id="bbece-101">\<tokenReplayCache></span><span class="sxs-lookup"><span data-stu-id="bbece-101">\<tokenReplayCache></span></span>
<span data-ttu-id="bbece-102">トークン再生キャッシュ サービスまたはセキュリティ トークン ハンドラー コレクションに登録します。</span><span class="sxs-lookup"><span data-stu-id="bbece-102">Registers a token replay cache with a service or a security token handler collection.</span></span>  
  
 <span data-ttu-id="bbece-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="bbece-103">\<system.identityModel></span></span>  
<span data-ttu-id="bbece-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="bbece-104">\<identityConfiguration></span></span>  
<span data-ttu-id="bbece-105">\<caches></span><span class="sxs-lookup"><span data-stu-id="bbece-105">\<caches></span></span>  
<span data-ttu-id="bbece-106">\<tokenReplayCache></span><span class="sxs-lookup"><span data-stu-id="bbece-106">\<tokenReplayCache></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bbece-107">構文</span><span class="sxs-lookup"><span data-stu-id="bbece-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bbece-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="bbece-108">Attributes and Elements</span></span>  
 <span data-ttu-id="bbece-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="bbece-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bbece-110">属性</span><span class="sxs-lookup"><span data-stu-id="bbece-110">Attributes</span></span>  
  
|<span data-ttu-id="bbece-111">属性</span><span class="sxs-lookup"><span data-stu-id="bbece-111">Attribute</span></span>|<span data-ttu-id="bbece-112">説明</span><span class="sxs-lookup"><span data-stu-id="bbece-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="bbece-113">型</span><span class="sxs-lookup"><span data-stu-id="bbece-113">type</span></span>|<span data-ttu-id="bbece-114">派生した型、<xref:System.IdentityModel.Tokens.TokenReplayCache>クラス。</span><span class="sxs-lookup"><span data-stu-id="bbece-114">A type that derives from the <xref:System.IdentityModel.Tokens.TokenReplayCache> class.</span></span> <span data-ttu-id="bbece-115">詳細については、ユーザー設定を指定する方法についての`type`、[カスタム型の参照] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bbece-115">For more information about how to specify a custom `type`, see [Custom Type References].</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bbece-116">子要素</span><span class="sxs-lookup"><span data-stu-id="bbece-116">Child Elements</span></span>  
 <span data-ttu-id="bbece-117">なし</span><span class="sxs-lookup"><span data-stu-id="bbece-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="bbece-118">親要素</span><span class="sxs-lookup"><span data-stu-id="bbece-118">Parent Elements</span></span>  
  
|<span data-ttu-id="bbece-119">要素</span><span class="sxs-lookup"><span data-stu-id="bbece-119">Element</span></span>|<span data-ttu-id="bbece-120">説明</span><span class="sxs-lookup"><span data-stu-id="bbece-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bbece-121">\<caches></span><span class="sxs-lookup"><span data-stu-id="bbece-121">\<caches></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|<span data-ttu-id="bbece-122">サービスまたはセキュリティ トークン ハンドラー コレクションで使用されるキャッシュを登録します。</span><span class="sxs-lookup"><span data-stu-id="bbece-122">Registers the caches used by a service or a security token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bbece-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="bbece-123">Remarks</span></span>  
 <span data-ttu-id="bbece-124">トークン再生キャッシュを使用して、再生されたトークンを検出できます。</span><span class="sxs-lookup"><span data-stu-id="bbece-124">The token replay cache is used to detect replayed tokens.</span></span> <span data-ttu-id="bbece-125">トークン リプレイ検出が有効になっている、 [ \<tokenReplayDetection >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md)要素もトークンの最大有効期限を指定します。</span><span class="sxs-lookup"><span data-stu-id="bbece-125">Token replay detection is enabled by the [\<tokenReplayDetection>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md) element, which also specifies the maximum expiration time for tokens.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bbece-126">例</span><span class="sxs-lookup"><span data-stu-id="bbece-126">Example</span></span>  
 <span data-ttu-id="bbece-127">次の XML は、再生されたトークンを検出するためのカスタム キャッシュの構成を示しています。</span><span class="sxs-lookup"><span data-stu-id="bbece-127">The following XML shows the configuration of a custom cache for detecting replayed tokens.</span></span>  
  
```xml  
<caches>  
  <tokenReplayCache type="MyCacheLibrary.MyTokenReplayCache, MyCacheLibrary">  
  </tokenReplayCache>  
</caches>  
```  
  
## <a name="see-also"></a><span data-ttu-id="bbece-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="bbece-128">See also</span></span>
- <xref:System.IdentityModel.Tokens.TokenReplayCache>
- [<span data-ttu-id="bbece-129">\<tokenReplayDetection></span><span class="sxs-lookup"><span data-stu-id="bbece-129">\<tokenReplayDetection></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md)
