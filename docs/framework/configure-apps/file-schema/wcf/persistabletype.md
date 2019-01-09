---
title: '&lt;persistableType&gt;'
ms.date: 03/30/2017
ms.assetid: e5425fe6-523a-4076-aab4-2c2515b1d830
ms.openlocfilehash: 92c59b3804e22c62340acccc1e12e594203c8e8b
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145420"
---
# <a name="ltpersistabletypegt"></a><span data-ttu-id="485cb-102">&lt;persistableType&gt;</span><span class="sxs-lookup"><span data-stu-id="485cb-102">&lt;persistableType&gt;</span></span>
<span data-ttu-id="485cb-103">すべての永続型を指定します。</span><span class="sxs-lookup"><span data-stu-id="485cb-103">Specifies all the persistable types.</span></span>  
  
 <span data-ttu-id="485cb-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="485cb-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="485cb-105">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="485cb-105">\<comContracts></span></span>  
<span data-ttu-id="485cb-106">\<comContract ></span><span class="sxs-lookup"><span data-stu-id="485cb-106">\<comContract></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="485cb-107">構文</span><span class="sxs-lookup"><span data-stu-id="485cb-107">Syntax</span></span>  
  
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
  
## <a name="type"></a><span data-ttu-id="485cb-108">型</span><span class="sxs-lookup"><span data-stu-id="485cb-108">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="485cb-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="485cb-109">Attributes and Elements</span></span>  
 <span data-ttu-id="485cb-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="485cb-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="485cb-111">属性</span><span class="sxs-lookup"><span data-stu-id="485cb-111">Attributes</span></span>  
  
|<span data-ttu-id="485cb-112">属性</span><span class="sxs-lookup"><span data-stu-id="485cb-112">Attribute</span></span>|<span data-ttu-id="485cb-113">説明</span><span class="sxs-lookup"><span data-stu-id="485cb-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="485cb-114">id</span><span class="sxs-lookup"><span data-stu-id="485cb-114">id</span></span>|<span data-ttu-id="485cb-115">永続型の一意の ID を指定する文字列を含む必須属性。</span><span class="sxs-lookup"><span data-stu-id="485cb-115">A required attribute that contains a string that specifies a unique identifier for a persistable type.</span></span>|  
|<span data-ttu-id="485cb-116">name</span><span class="sxs-lookup"><span data-stu-id="485cb-116">name</span></span>|<span data-ttu-id="485cb-117">永続型の名前を指定する文字列を含む省略可能な属性。</span><span class="sxs-lookup"><span data-stu-id="485cb-117">An optional attribute that contains a string that specifies the name of the persistable type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="485cb-118">子要素</span><span class="sxs-lookup"><span data-stu-id="485cb-118">Child Elements</span></span>  
 <span data-ttu-id="485cb-119">なし</span><span class="sxs-lookup"><span data-stu-id="485cb-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="485cb-120">親要素</span><span class="sxs-lookup"><span data-stu-id="485cb-120">Parent Elements</span></span>  
  
|<span data-ttu-id="485cb-121">要素</span><span class="sxs-lookup"><span data-stu-id="485cb-121">Element</span></span>|<span data-ttu-id="485cb-122">説明</span><span class="sxs-lookup"><span data-stu-id="485cb-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="485cb-123">\<persistableTypes></span><span class="sxs-lookup"><span data-stu-id="485cb-123">\<persistableTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/persistabletypes.md)|<span data-ttu-id="485cb-124">`persistableType` 要素のコレクション。</span><span class="sxs-lookup"><span data-stu-id="485cb-124">A collection of `persistableType` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="485cb-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="485cb-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ComPersistableTypeElementCollection>  
 <xref:System.ServiceModel.Configuration.ComPersistableTypeElement>  
 [<span data-ttu-id="485cb-126">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="485cb-126">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)  
 [<span data-ttu-id="485cb-127">COM+ アプリケーションとの統合</span><span class="sxs-lookup"><span data-stu-id="485cb-127">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)  
 [<span data-ttu-id="485cb-128">方法: COM + サービス設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="485cb-128">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
