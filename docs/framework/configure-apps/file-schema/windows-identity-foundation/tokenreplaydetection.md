---
title: <tokenReplayDetection>
ms.date: 03/30/2017
ms.assetid: ac3f588e-5f75-4275-b969-2d492ecc3b47
author: BrucePerlerMS
ms.openlocfilehash: 4deeb1d84f2621adb7ff1b649a505138b6856ec1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55283076"
---
# <a name="tokenreplaydetection"></a><span data-ttu-id="82a17-101">\<tokenReplayDetection></span><span class="sxs-lookup"><span data-stu-id="82a17-101">\<tokenReplayDetection></span></span>
<span data-ttu-id="82a17-102">トークン リプレイ検出が有効にし、トークンの有効期限を指定します。</span><span class="sxs-lookup"><span data-stu-id="82a17-102">Enables token replay detection and specifies the expiration time for tokens.</span></span>  
  
 <span data-ttu-id="82a17-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="82a17-103">\<system.identityModel></span></span>  
<span data-ttu-id="82a17-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="82a17-104">\<identityConfiguration></span></span>  
<span data-ttu-id="82a17-105">\<tokenReplayDetection></span><span class="sxs-lookup"><span data-stu-id="82a17-105">\<tokenReplayDetection></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82a17-106">構文</span><span class="sxs-lookup"><span data-stu-id="82a17-106">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <tokenReplayDetection enabled=xs:boolean expirationPeriod=TimeSpan>  
    </tokenReplayDetection>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="type"></a><span data-ttu-id="82a17-107">型</span><span class="sxs-lookup"><span data-stu-id="82a17-107">Type</span></span>  
 <xref:System.IdentityModel.Configuration.TokenReplayDetectionElement>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="82a17-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="82a17-108">Attributes and Elements</span></span>  
 <span data-ttu-id="82a17-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="82a17-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="82a17-110">属性</span><span class="sxs-lookup"><span data-stu-id="82a17-110">Attributes</span></span>  
  
|<span data-ttu-id="82a17-111">属性</span><span class="sxs-lookup"><span data-stu-id="82a17-111">Attribute</span></span>|<span data-ttu-id="82a17-112">説明</span><span class="sxs-lookup"><span data-stu-id="82a17-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="82a17-113">enabled</span><span class="sxs-lookup"><span data-stu-id="82a17-113">enabled</span></span>|<span data-ttu-id="82a17-114">トークン リプレイ検出が有効かどうかを指定する値トークンを有効にするには"true"にリプレイ検出を示します。</span><span class="sxs-lookup"><span data-stu-id="82a17-114">A value that specifies whether token replay detection is enabled; "true" to enable token replay detection.</span></span>|  
|<span data-ttu-id="82a17-115">expirationPeriod</span><span class="sxs-lookup"><span data-stu-id="82a17-115">expirationPeriod</span></span>|<span data-ttu-id="82a17-116">A<xref:System.TimeSpan>項目は期限切れになり、キャッシュから削除されたと見なされますまでの最大時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="82a17-116">A <xref:System.TimeSpan> that specifies the maximum amount of time before an item is considered expired and removed from the cache.</span></span>  <span data-ttu-id="82a17-117">指定する方法の詳細についての<xref:System.TimeSpan>値を参照してください[Timespan 値](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md)します。</span><span class="sxs-lookup"><span data-stu-id="82a17-117">For more information about how to specify <xref:System.TimeSpan> values, see [Timespan Values](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="82a17-118">子要素</span><span class="sxs-lookup"><span data-stu-id="82a17-118">Child Elements</span></span>  
 <span data-ttu-id="82a17-119">なし</span><span class="sxs-lookup"><span data-stu-id="82a17-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="82a17-120">親要素</span><span class="sxs-lookup"><span data-stu-id="82a17-120">Parent Elements</span></span>  
  
|<span data-ttu-id="82a17-121">要素</span><span class="sxs-lookup"><span data-stu-id="82a17-121">Element</span></span>|<span data-ttu-id="82a17-122">説明</span><span class="sxs-lookup"><span data-stu-id="82a17-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="82a17-123">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="82a17-123">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="82a17-124">サービス レベルの id の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="82a17-124">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="82a17-125">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="82a17-125">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="82a17-126">トークン ハンドラー コレクションのセキュリティの構成を提供します。</span><span class="sxs-lookup"><span data-stu-id="82a17-126">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="82a17-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="82a17-127">Remarks</span></span>  
 <span data-ttu-id="82a17-128">A`<tokenReplayDetection>`下で、サービス レベルで要素を指定することができます、`<identityConfiguration>`要素またはセキュリティ トークン ハンドラー コレクション レベルの下で、`<securityTokenHandlerConfiguration>`要素。</span><span class="sxs-lookup"><span data-stu-id="82a17-128">A `<tokenReplayDetection>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="82a17-129">トークン ハンドラー コレクションの設定は、サービスに指定されているものをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="82a17-129">Settings on a token handler collection override those specified on the service.</span></span>  
  
 <span data-ttu-id="82a17-130">トークン再生キャッシュの型がで指定された、 [ \<tokenReplayCache >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md)要素。</span><span class="sxs-lookup"><span data-stu-id="82a17-130">The type of the token replay cache is specified by the [\<tokenReplayCache>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md) element.</span></span>
