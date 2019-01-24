---
title: '&lt;privacyNoticeAt&gt;'
ms.date: 03/30/2017
ms.assetid: 4cc96942-4eb9-4241-b2fd-45aa239915e8
ms.openlocfilehash: bf694911e0715275991084604ce44535d9183eff
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54683717"
---
# <a name="ltprivacynoticeatgt"></a><span data-ttu-id="d915f-102">&lt;privacyNoticeAt&gt;</span><span class="sxs-lookup"><span data-stu-id="d915f-102">&lt;privacyNoticeAt&gt;</span></span>
<span data-ttu-id="d915f-103">`wsFederationHttp` バインディングで使用されるプライバシーに関する声明を指定する構成要素を表します。</span><span class="sxs-lookup"><span data-stu-id="d915f-103">Represents a configuration element that specifies a privacy notice used in `wsFederationHttp` binding.</span></span>  
  
 <span data-ttu-id="d915f-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="d915f-104">\<system.serviceModel></span></span>  
<span data-ttu-id="d915f-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="d915f-105">\<bindings></span></span>  
<span data-ttu-id="d915f-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="d915f-106">\<customBinding></span></span>  
<span data-ttu-id="d915f-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="d915f-107">\<binding></span></span>  
<span data-ttu-id="d915f-108">\<privacyNotice></span><span class="sxs-lookup"><span data-stu-id="d915f-108">\<privacyNotice></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d915f-109">構文</span><span class="sxs-lookup"><span data-stu-id="d915f-109">Syntax</span></span>  
  
```xml  
<privacyNotice url="String"
               version="Integer" />
```  
  
## <a name="type"></a><span data-ttu-id="d915f-110">型</span><span class="sxs-lookup"><span data-stu-id="d915f-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d915f-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="d915f-111">Attributes and Elements</span></span>  
 <span data-ttu-id="d915f-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="d915f-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d915f-113">属性</span><span class="sxs-lookup"><span data-stu-id="d915f-113">Attributes</span></span>  
  
|<span data-ttu-id="d915f-114">属性</span><span class="sxs-lookup"><span data-stu-id="d915f-114">Attribute</span></span>|<span data-ttu-id="d915f-115">説明</span><span class="sxs-lookup"><span data-stu-id="d915f-115">Description</span></span>|  
|---------------|-----------------|  
|`url`|<span data-ttu-id="d915f-116">プライバシーに関する声明の場所を示す URI を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="d915f-116">A string that specifies the URI at which the privacy notice is located.</span></span>|  
|`version`|<span data-ttu-id="d915f-117">このプライバシーに関する声明のバージョンを指定する整数。</span><span class="sxs-lookup"><span data-stu-id="d915f-117">An integer that specifies the version of this privacy notice.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d915f-118">子要素</span><span class="sxs-lookup"><span data-stu-id="d915f-118">Child Elements</span></span>  
 <span data-ttu-id="d915f-119">なし。</span><span class="sxs-lookup"><span data-stu-id="d915f-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d915f-120">親要素</span><span class="sxs-lookup"><span data-stu-id="d915f-120">Parent Elements</span></span>  
  
|<span data-ttu-id="d915f-121">要素</span><span class="sxs-lookup"><span data-stu-id="d915f-121">Element</span></span>|<span data-ttu-id="d915f-122">説明</span><span class="sxs-lookup"><span data-stu-id="d915f-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d915f-123">\<binding></span><span class="sxs-lookup"><span data-stu-id="d915f-123">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="d915f-124">カスタム バインドのすべてのバインド機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="d915f-124">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d915f-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="d915f-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.PrivacyNoticeElement>
- <xref:System.ServiceModel.Channels.PrivacyNoticeBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="d915f-126">バインディング</span><span class="sxs-lookup"><span data-stu-id="d915f-126">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="d915f-127">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="d915f-127">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="d915f-128">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="d915f-128">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="d915f-129">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="d915f-129">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
