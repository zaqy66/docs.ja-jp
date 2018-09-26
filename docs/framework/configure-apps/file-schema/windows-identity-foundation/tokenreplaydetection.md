---
title: '&lt;tokenReplayDetection&gt;'
ms.date: 03/30/2017
ms.assetid: ac3f588e-5f75-4275-b969-2d492ecc3b47
author: BrucePerlerMS
ms.openlocfilehash: bd2272cb83dc0183d5008cfa178e11783f51ca2d
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47205932"
---
# <a name="lttokenreplaydetectiongt"></a><span data-ttu-id="312de-102">&lt;tokenReplayDetection&gt;</span><span class="sxs-lookup"><span data-stu-id="312de-102">&lt;tokenReplayDetection&gt;</span></span>
<span data-ttu-id="312de-103">トークン リプレイ検出が有効にし、トークンの有効期限を指定します。</span><span class="sxs-lookup"><span data-stu-id="312de-103">Enables token replay detection and specifies the expiration time for tokens.</span></span>  
  
 <span data-ttu-id="312de-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="312de-104">\<system.identityModel></span></span>  
<span data-ttu-id="312de-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="312de-105">\<identityConfiguration></span></span>  
<span data-ttu-id="312de-106">\<tokenReplayDetection ></span><span class="sxs-lookup"><span data-stu-id="312de-106">\<tokenReplayDetection></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="312de-107">構文</span><span class="sxs-lookup"><span data-stu-id="312de-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <tokenReplayDetection enabled=xs:boolean expirationPeriod=TimeSpan>  
    </tokenReplayDetection>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="type"></a><span data-ttu-id="312de-108">型</span><span class="sxs-lookup"><span data-stu-id="312de-108">Type</span></span>  
 <xref:System.IdentityModel.Configuration.TokenReplayDetectionElement>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="312de-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="312de-109">Attributes and Elements</span></span>  
 <span data-ttu-id="312de-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="312de-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="312de-111">属性</span><span class="sxs-lookup"><span data-stu-id="312de-111">Attributes</span></span>  
  
|<span data-ttu-id="312de-112">属性</span><span class="sxs-lookup"><span data-stu-id="312de-112">Attribute</span></span>|<span data-ttu-id="312de-113">説明</span><span class="sxs-lookup"><span data-stu-id="312de-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="312de-114">enabled</span><span class="sxs-lookup"><span data-stu-id="312de-114">enabled</span></span>|<span data-ttu-id="312de-115">トークン リプレイ検出が有効かどうかを指定する値トークンを有効にするには"true"にリプレイ検出を示します。</span><span class="sxs-lookup"><span data-stu-id="312de-115">A value that specifies whether token replay detection is enabled; "true" to enable token replay detection.</span></span>|  
|<span data-ttu-id="312de-116">expirationPeriod</span><span class="sxs-lookup"><span data-stu-id="312de-116">expirationPeriod</span></span>|<span data-ttu-id="312de-117">A<xref:System.TimeSpan>項目は期限切れになり、キャッシュから削除されたと見なされますまでの最大時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="312de-117">A <xref:System.TimeSpan> that specifies the maximum amount of time before an item is considered expired and removed from the cache.</span></span>  <span data-ttu-id="312de-118">指定する方法の詳細についての<xref:System.TimeSpan>値を参照してください[Timespan 値](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md)します。</span><span class="sxs-lookup"><span data-stu-id="312de-118">For more information about how to specify <xref:System.TimeSpan> values, see [Timespan Values](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="312de-119">子要素</span><span class="sxs-lookup"><span data-stu-id="312de-119">Child Elements</span></span>  
 <span data-ttu-id="312de-120">なし</span><span class="sxs-lookup"><span data-stu-id="312de-120">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="312de-121">親要素</span><span class="sxs-lookup"><span data-stu-id="312de-121">Parent Elements</span></span>  
  
|<span data-ttu-id="312de-122">要素</span><span class="sxs-lookup"><span data-stu-id="312de-122">Element</span></span>|<span data-ttu-id="312de-123">説明</span><span class="sxs-lookup"><span data-stu-id="312de-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="312de-124">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="312de-124">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="312de-125">サービス レベルの id の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="312de-125">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="312de-126">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="312de-126">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="312de-127">トークン ハンドラー コレクションのセキュリティの構成を提供します。</span><span class="sxs-lookup"><span data-stu-id="312de-127">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="312de-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="312de-128">Remarks</span></span>  
 <span data-ttu-id="312de-129">A`<tokenReplayDetection>`下で、サービス レベルで要素を指定することができます、`<identityConfiguration>`要素またはセキュリティ トークン ハンドラー コレクション レベルの下で、`<securityTokenHandlerConfiguration>`要素。</span><span class="sxs-lookup"><span data-stu-id="312de-129">A `<tokenReplayDetection>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="312de-130">トークン ハンドラー コレクションの設定は、サービスに指定されているものをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="312de-130">Settings on a token handler collection override those specified on the service.</span></span>  
  
 <span data-ttu-id="312de-131">トークン再生キャッシュの型がで指定された、 [ \<tokenReplayCache >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md)要素。</span><span class="sxs-lookup"><span data-stu-id="312de-131">The type of the token replay cache is specified by the [\<tokenReplayCache>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md) element.</span></span>
