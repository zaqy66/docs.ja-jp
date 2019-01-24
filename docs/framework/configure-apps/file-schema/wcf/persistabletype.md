---
title: '&lt;persistableType&gt;'
ms.date: 03/30/2017
ms.assetid: e5425fe6-523a-4076-aab4-2c2515b1d830
ms.openlocfilehash: b9d61a736a2f8650c543433931d57e156d115018
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706853"
---
# <a name="ltpersistabletypegt"></a><span data-ttu-id="6e7d2-102">&lt;persistableType&gt;</span><span class="sxs-lookup"><span data-stu-id="6e7d2-102">&lt;persistableType&gt;</span></span>
<span data-ttu-id="6e7d2-103">すべての永続型を指定します。</span><span class="sxs-lookup"><span data-stu-id="6e7d2-103">Specifies all the persistable types.</span></span>  
  
 <span data-ttu-id="6e7d2-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="6e7d2-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="6e7d2-105">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="6e7d2-105">\<comContracts></span></span>  
<span data-ttu-id="6e7d2-106">\<comContract></span><span class="sxs-lookup"><span data-stu-id="6e7d2-106">\<comContract></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e7d2-107">構文</span><span class="sxs-lookup"><span data-stu-id="6e7d2-107">Syntax</span></span>  
  
```xml  
<comContracts>
  <comContract>
    <persistableTypes>
      <persistableType id="String"
                       name="String">
      </persistableType>
    </persistableTypes>
  </comContract>
</comContracts>
```  
  
## <a name="type"></a><span data-ttu-id="6e7d2-108">型</span><span class="sxs-lookup"><span data-stu-id="6e7d2-108">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6e7d2-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="6e7d2-109">Attributes and Elements</span></span>  
 <span data-ttu-id="6e7d2-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="6e7d2-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6e7d2-111">属性</span><span class="sxs-lookup"><span data-stu-id="6e7d2-111">Attributes</span></span>  
  
|<span data-ttu-id="6e7d2-112">属性</span><span class="sxs-lookup"><span data-stu-id="6e7d2-112">Attribute</span></span>|<span data-ttu-id="6e7d2-113">説明</span><span class="sxs-lookup"><span data-stu-id="6e7d2-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6e7d2-114">id</span><span class="sxs-lookup"><span data-stu-id="6e7d2-114">id</span></span>|<span data-ttu-id="6e7d2-115">永続型の一意の ID を指定する文字列を含む必須属性。</span><span class="sxs-lookup"><span data-stu-id="6e7d2-115">A required attribute that contains a string that specifies a unique identifier for a persistable type.</span></span>|  
|<span data-ttu-id="6e7d2-116">name</span><span class="sxs-lookup"><span data-stu-id="6e7d2-116">name</span></span>|<span data-ttu-id="6e7d2-117">永続型の名前を指定する文字列を含む省略可能な属性。</span><span class="sxs-lookup"><span data-stu-id="6e7d2-117">An optional attribute that contains a string that specifies the name of the persistable type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6e7d2-118">子要素</span><span class="sxs-lookup"><span data-stu-id="6e7d2-118">Child Elements</span></span>  
 <span data-ttu-id="6e7d2-119">なし</span><span class="sxs-lookup"><span data-stu-id="6e7d2-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6e7d2-120">親要素</span><span class="sxs-lookup"><span data-stu-id="6e7d2-120">Parent Elements</span></span>  
  
|<span data-ttu-id="6e7d2-121">要素</span><span class="sxs-lookup"><span data-stu-id="6e7d2-121">Element</span></span>|<span data-ttu-id="6e7d2-122">説明</span><span class="sxs-lookup"><span data-stu-id="6e7d2-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6e7d2-123">\<persistableTypes></span><span class="sxs-lookup"><span data-stu-id="6e7d2-123">\<persistableTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/persistabletypes.md)|<span data-ttu-id="6e7d2-124">`persistableType` 要素のコレクション。</span><span class="sxs-lookup"><span data-stu-id="6e7d2-124">A collection of `persistableType` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6e7d2-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="6e7d2-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.ComPersistableTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ComPersistableTypeElement>
- [<span data-ttu-id="6e7d2-126">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="6e7d2-126">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)
- [<span data-ttu-id="6e7d2-127">COM+ アプリケーションとの統合</span><span class="sxs-lookup"><span data-stu-id="6e7d2-127">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)
- [<span data-ttu-id="6e7d2-128">方法: COM + サービス設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="6e7d2-128">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
