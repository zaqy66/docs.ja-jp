---
title: <exposedMethod>
ms.date: 03/30/2017
ms.assetid: 61c938cd-4ee9-4b06-ab28-922ef491ab11
ms.openlocfilehash: 151929cd99df08b705bee94eb6fd6f10c254a660
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55259853"
---
# <a name="exposedmethod"></a><span data-ttu-id="423ed-101">\<exposedMethod ></span><span class="sxs-lookup"><span data-stu-id="423ed-101">\<exposedMethod></span></span>
<span data-ttu-id="423ed-102">COM+ コンポーネントのインターフェイスが Web サービスとして公開されるときに公開される COM+ メソッドを表します。</span><span class="sxs-lookup"><span data-stu-id="423ed-102">Represents a COM+ method that is exposed when the interface on a COM+ component is exposed as a Web service.</span></span>  
  
 <span data-ttu-id="423ed-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="423ed-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="423ed-104">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="423ed-104">\<comContracts></span></span>  
<span data-ttu-id="423ed-105">\<comContract></span><span class="sxs-lookup"><span data-stu-id="423ed-105">\<comContract></span></span>  
<span data-ttu-id="423ed-106">\<メソッド ></span><span class="sxs-lookup"><span data-stu-id="423ed-106">\<methods></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="423ed-107">構文</span><span class="sxs-lookup"><span data-stu-id="423ed-107">Syntax</span></span>  
  
```xml  
<comContracts>
  <comContract>
    <exposedMethods>
      <exposedMethod name="String" />
    </exposedMethods>
  </comContract>
</comContracts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="423ed-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="423ed-108">Attributes and Elements</span></span>  
 <span data-ttu-id="423ed-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="423ed-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="423ed-110">属性</span><span class="sxs-lookup"><span data-stu-id="423ed-110">Attributes</span></span>  
  
|<span data-ttu-id="423ed-111">属性</span><span class="sxs-lookup"><span data-stu-id="423ed-111">Attribute</span></span>|<span data-ttu-id="423ed-112">説明</span><span class="sxs-lookup"><span data-stu-id="423ed-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="423ed-113">name</span><span class="sxs-lookup"><span data-stu-id="423ed-113">name</span></span>|<span data-ttu-id="423ed-114">COM+ コンポーネントのインターフェイスが Web サービスとして公開されるときに公開される COM+ メソッドを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="423ed-114">A string that contains the COM+ method that is exposed when the interface on a COM+ component is exposed as a Web service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="423ed-115">子要素</span><span class="sxs-lookup"><span data-stu-id="423ed-115">Child Elements</span></span>  
 <span data-ttu-id="423ed-116">なし。</span><span class="sxs-lookup"><span data-stu-id="423ed-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="423ed-117">親要素</span><span class="sxs-lookup"><span data-stu-id="423ed-117">Parent Elements</span></span>  
  
|<span data-ttu-id="423ed-118">要素</span><span class="sxs-lookup"><span data-stu-id="423ed-118">Element</span></span>|<span data-ttu-id="423ed-119">説明</span><span class="sxs-lookup"><span data-stu-id="423ed-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="423ed-120">\<exposedMethods ></span><span class="sxs-lookup"><span data-stu-id="423ed-120">\<exposedMethods></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethods.md)|<span data-ttu-id="423ed-121">コレクション[ \<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md)要素。</span><span class="sxs-lookup"><span data-stu-id="423ed-121">A collection of [\<exposedMethod>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="423ed-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="423ed-122">Remarks</span></span>  
 <span data-ttu-id="423ed-123">COM+ 統合構成ツール (ComSvcConfig.exe) を使用して、COM インターフェイスから特定のメソッドを追加して、生成されるサービス コントラクトに表示できます。</span><span class="sxs-lookup"><span data-stu-id="423ed-123">The COM+ integration configuration tool (ComSvcConfig.exe) can be used to add specific methods from a COM interface to appear on the generated service contract.</span></span>  
  
 <span data-ttu-id="423ed-124">たとえば、次のコマンドを使用して、`IFinances`.Financial コンポーネントの `ItemOrders` COM インターフェイスから、3 つの名前付きメソッドを、生成されるサービス コントラクトに追加できます。</span><span class="sxs-lookup"><span data-stu-id="423ed-124">For example, you can use the following command to add the three named methods from the `IFinances` COM interface on the `ItemOrders`.Financial component, to the generated service contract.</span></span>  
  
 `ComSvcConfig.exe /i /application:OnlineStore /contract:ItemOrders.Financial,IFinances.{TransferFunds,AddFunds,RemoveFunds} /hosting:complus`  
  
 <span data-ttu-id="423ed-125">ComSvcConfig.exe も実行すると、ときに一覧表示する前に説明したメソッドを次のサービス コントラクトが生成されます[ \<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md)要素。</span><span class="sxs-lookup"><span data-stu-id="423ed-125">When you also run the ComSvcConfig.exe, it then generates the following service contract listing the previously mentioned methods as [\<exposedMethod>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) elements.</span></span>  
  
```xml  
<comContract contractType="{C551FBA9-E3AA-4272-8C2A-84BD8D290AC7}"
             name="IFinances"
             namespace="http://contoso.com/services/financial">
  <exposedMethod name="TransferFunds"/>
  <exposedMethod name="AddFunds"/>
  <exposedMethod name="RemoveFunds"/>
</comContract>
```  
  
 <span data-ttu-id="423ed-126">ランタイムの一覧に含まれるメソッドのみを追加することを反映して、サービス コントラクトを生成するサービスの初期化時、 [ \<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md)要素。</span><span class="sxs-lookup"><span data-stu-id="423ed-126">At service initialization time, the runtime attempts to generate a service contract by reflecting over and adding only the methods included in the list of [\<exposedMethod>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) elements.</span></span> <span data-ttu-id="423ed-127">トレースは、サービス コントラクトに含まれないインターフェイス メソッド用に作成されます。</span><span class="sxs-lookup"><span data-stu-id="423ed-127">A trace is produced for every interface method that is not included on the service contract.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="423ed-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="423ed-128">See also</span></span>
- <xref:System.ServiceModel.Configuration.ComMethodElementCollection>
- <xref:System.ServiceModel.Configuration.ComMethodElement>
- [<span data-ttu-id="423ed-129">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="423ed-129">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)
- [<span data-ttu-id="423ed-130">COM+ アプリケーションとの統合</span><span class="sxs-lookup"><span data-stu-id="423ed-130">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)
- [<span data-ttu-id="423ed-131">方法: COM + サービス設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="423ed-131">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
