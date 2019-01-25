---
title: '&lt;serviceActivations&gt;'
ms.date: 03/30/2017
ms.assetid: 97e665b6-1c51-410b-928a-9bb42c954ddb
ms.openlocfilehash: 5da05c7b6a9685b9e34b3181ce8e0bd31ccd052b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54704957"
---
# <a name="ltserviceactivationsgt"></a><span data-ttu-id="e602f-102">&lt;serviceActivations&gt;</span><span class="sxs-lookup"><span data-stu-id="e602f-102">&lt;serviceActivations&gt;</span></span>
<span data-ttu-id="e602f-103">仮想サービス アクティベーション設定を定義する設定を追加することができます、Windows Communication Foundation (WCF) サービスの型にマップする構成要素。</span><span class="sxs-lookup"><span data-stu-id="e602f-103">A configuration element that allows you to add settings that define virtual service activation settings that map to your Windows Communication Foundation (WCF) service types.</span></span> <span data-ttu-id="e602f-104">これにより、.svc ファイルを使用せずに、WAS/IIS でホストされているサービスをアクティブ化できます。</span><span class="sxs-lookup"><span data-stu-id="e602f-104">This makes it possible to activate services hosted in WAS/IIS without an .svc file.</span></span>  
  
 <span data-ttu-id="e602f-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="e602f-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="e602f-106">\<serviceHostingEnvironment></span><span class="sxs-lookup"><span data-stu-id="e602f-106">\<serviceHostingEnvironment></span></span>  
<span data-ttu-id="e602f-107">\<serviceActivations></span><span class="sxs-lookup"><span data-stu-id="e602f-107">\<serviceActivations></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e602f-108">構文</span><span class="sxs-lookup"><span data-stu-id="e602f-108">Syntax</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <serviceActivations>
    <add factory="String"
         service="String" />
  </serviceActivations>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e602f-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="e602f-109">Attributes and Elements</span></span>  
 <span data-ttu-id="e602f-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="e602f-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e602f-111">属性</span><span class="sxs-lookup"><span data-stu-id="e602f-111">Attributes</span></span>  
 <span data-ttu-id="e602f-112">なし。</span><span class="sxs-lookup"><span data-stu-id="e602f-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="e602f-113">子要素</span><span class="sxs-lookup"><span data-stu-id="e602f-113">Child Elements</span></span>  
  
|<span data-ttu-id="e602f-114">要素</span><span class="sxs-lookup"><span data-stu-id="e602f-114">Element</span></span>|<span data-ttu-id="e602f-115">説明</span><span class="sxs-lookup"><span data-stu-id="e602f-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e602f-116">\<add></span><span class="sxs-lookup"><span data-stu-id="e602f-116">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-serviceactivations.md)|<span data-ttu-id="e602f-117">サービス アプリケーションのアクティベーションを指定する構成要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="e602f-117">Adds a configuration element that specifies the activation of a service application.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e602f-118">親要素</span><span class="sxs-lookup"><span data-stu-id="e602f-118">Parent Elements</span></span>  
  
|<span data-ttu-id="e602f-119">要素</span><span class="sxs-lookup"><span data-stu-id="e602f-119">Element</span></span>|<span data-ttu-id="e602f-120">説明</span><span class="sxs-lookup"><span data-stu-id="e602f-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e602f-121">\<serviceHostingEnvironment></span><span class="sxs-lookup"><span data-stu-id="e602f-121">\<serviceHostingEnvironment></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md)|<span data-ttu-id="e602f-122">環境をホストするサービスがインスタンス化する特定のトランスポートの型を定義します。</span><span class="sxs-lookup"><span data-stu-id="e602f-122">Defines the type the service hosting environment instantiates for a particular transport.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e602f-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="e602f-123">Remarks</span></span>  
 <span data-ttu-id="e602f-124">web.config ファイルでアクティベーション設定を構成する方法を次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="e602f-124">The following example shows how to configure activation settings within your web.config file.</span></span>  
  
```xml  
<configuration>
  <system.serviceModel>
    <serviceHostingEnvironment>
      <serviceActivations>
        <add service="GreetingService" />
      </serviceActivations>
    </serviceHostingEnvironment>
  </system.serviceModel>
</configuration>
```  
  
 <span data-ttu-id="e602f-125">この構成を使用して、.svc ファイルを使用せずに、GreetingService をアクティブ化できます。</span><span class="sxs-lookup"><span data-stu-id="e602f-125">Using this configuration, you can activate the GreetingService without using an .svc file.</span></span>  
  
 <span data-ttu-id="e602f-126">`<serviceHostingEnvironment>` はアプリケーション レベルの構成であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e602f-126">Note that `<serviceHostingEnvironment>` is an application level configuration.</span></span> <span data-ttu-id="e602f-127">構成を格納した `web.config` は、仮想アプリケーションのルートの下に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e602f-127">You have to place the `web.config` containing the configuration under the root of the virtual Application.</span></span> <span data-ttu-id="e602f-128">また、`serviceHostingEnvironment` は machinetoApplication の継承可能なセクションです。</span><span class="sxs-lookup"><span data-stu-id="e602f-128">In addition, `serviceHostingEnvironment` is a machinetoApplication inheritable section.</span></span> <span data-ttu-id="e602f-129">コンピューターのルートに単一のサービスを登録すると、アプリケーションの各サービスはこのサービスを継承します。</span><span class="sxs-lookup"><span data-stu-id="e602f-129">If you register a single service in the root of the machine, every service in the application will inherit this service.</span></span>  
  
 <span data-ttu-id="e602f-130">構成ベースのアクティベーションは、http および非 http プロトコル経由のアクティベーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e602f-130">Configuration-based activation supports activation over both http and non-http protocol.</span></span> <span data-ttu-id="e602f-131">relatativeAddress では、.svc、.xoml、.xamlx などの拡張子が必要です。</span><span class="sxs-lookup"><span data-stu-id="e602f-131">It requires extensions in the relatativeAddress i.e. .svc, .xoml or .xamlx.</span></span> <span data-ttu-id="e602f-132">既知の buildProviders に対して独自の拡張子をマップできます。これにより、任意の拡張子を使用してサービスをアクティブ化できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e602f-132">You can map your own extensions to the know buildProviders, which will then enable you to activate service over any extension.</span></span> <span data-ttu-id="e602f-133">競合が発生した場合には、`<serviceActivations>` セクションにより、.svc の登録がオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="e602f-133">Upon conflict, the `<serviceActivations>` section overrides .svc registrations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e602f-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="e602f-134">See also</span></span>
- <xref:System.ServiceModel.Configuration.ServiceActivationElementCollection>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
