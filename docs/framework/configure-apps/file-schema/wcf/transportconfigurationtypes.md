---
title: '&lt;transportConfigurationTypes&gt;'
ms.date: 03/30/2017
ms.assetid: 929c8b0a-5460-4f66-a098-2cb8d4e10b69
ms.openlocfilehash: 5a51450d198ea395098f8a6a38d9104d0fe8538b
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145472"
---
# <a name="lttransportconfigurationtypesgt"></a><span data-ttu-id="e6797-102">&lt;transportConfigurationTypes&gt;</span><span class="sxs-lookup"><span data-stu-id="e6797-102">&lt;transportConfigurationTypes&gt;</span></span>
<span data-ttu-id="e6797-103">特定のトランスポートの型を識別する構成要素のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="e6797-103">Represents a collection of configuration elements that identify the type of a particular transport.</span></span> <span data-ttu-id="e6797-104">これはカスタム WAS プロトコルの追加に使用できます。</span><span class="sxs-lookup"><span data-stu-id="e6797-104">This can be used to add custom WAS protocols.</span></span>  
  
 <span data-ttu-id="e6797-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="e6797-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="e6797-106">\<serviceHostingEnvironment ></span><span class="sxs-lookup"><span data-stu-id="e6797-106">\<ServiceHostingEnvironment></span></span>  
<span data-ttu-id="e6797-107">\<transportConfigurationTypes ></span><span class="sxs-lookup"><span data-stu-id="e6797-107">\<transportConfigurationTypes></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6797-108">構文</span><span class="sxs-lookup"><span data-stu-id="e6797-108">Syntax</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <transportConfigurationTypes>
    <add name="String"
         transportConfigurationType="String" />
  </transportConfigurationTypes>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e6797-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="e6797-109">Attributes and Elements</span></span>  
 <span data-ttu-id="e6797-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="e6797-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e6797-111">属性</span><span class="sxs-lookup"><span data-stu-id="e6797-111">Attributes</span></span>  
  
|<span data-ttu-id="e6797-112">属性</span><span class="sxs-lookup"><span data-stu-id="e6797-112">Attribute</span></span>|<span data-ttu-id="e6797-113">説明</span><span class="sxs-lookup"><span data-stu-id="e6797-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e6797-114">name</span><span class="sxs-lookup"><span data-stu-id="e6797-114">name</span></span>|<span data-ttu-id="e6797-115">トランスポートの名前</span><span class="sxs-lookup"><span data-stu-id="e6797-115">The name of the transport</span></span>|  
|<span data-ttu-id="e6797-116">transportConfigurationType</span><span class="sxs-lookup"><span data-stu-id="e6797-116">transportConfigurationType</span></span>|<span data-ttu-id="e6797-117">トランスポートを実装する型</span><span class="sxs-lookup"><span data-stu-id="e6797-117">The type that implements the transport</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e6797-118">子要素</span><span class="sxs-lookup"><span data-stu-id="e6797-118">Child Elements</span></span>  
  
|<span data-ttu-id="e6797-119">要素</span><span class="sxs-lookup"><span data-stu-id="e6797-119">Element</span></span>|<span data-ttu-id="e6797-120">説明</span><span class="sxs-lookup"><span data-stu-id="e6797-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e6797-121">\<add></span><span class="sxs-lookup"><span data-stu-id="e6797-121">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-transportconfigurationtype.md)|<span data-ttu-id="e6797-122">特定のトランスポートの型を識別する構成要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="e6797-122">Adds a configuration element that identifies the type of a particular transport.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e6797-123">親要素</span><span class="sxs-lookup"><span data-stu-id="e6797-123">Parent Elements</span></span>  
  
|<span data-ttu-id="e6797-124">要素</span><span class="sxs-lookup"><span data-stu-id="e6797-124">Element</span></span>|<span data-ttu-id="e6797-125">説明</span><span class="sxs-lookup"><span data-stu-id="e6797-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e6797-126">\<serviceHostingEnvironment ></span><span class="sxs-lookup"><span data-stu-id="e6797-126">\<serviceHostingEnvironment></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md)|<span data-ttu-id="e6797-127">環境をホストするサービスがインスタンス化する特定のトランスポートの型を定義します。</span><span class="sxs-lookup"><span data-stu-id="e6797-127">Defines the type the service hosting environment instantiates for a particular transport.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e6797-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e6797-128">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>  
 <xref:System.ServiceModel.ServiceHostingEnvironment>  
 <xref:System.ServiceModel.Configuration.TransportConfigurationTypeElementCollection>  
 [<span data-ttu-id="e6797-129">ホスティング</span><span class="sxs-lookup"><span data-stu-id="e6797-129">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
