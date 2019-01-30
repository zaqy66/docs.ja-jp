---
title: <serviceActivations>
ms.date: 03/30/2017
ms.assetid: 97e665b6-1c51-410b-928a-9bb42c954ddb
ms.openlocfilehash: 7a091ecfbc0f4773ece620f93a9f21c219fcccb6
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55256705"
---
# <a name="serviceactivations"></a><span data-ttu-id="d6a57-101">\<serviceActivations></span><span class="sxs-lookup"><span data-stu-id="d6a57-101">\<serviceActivations></span></span>
<span data-ttu-id="d6a57-102">仮想サービス アクティベーション設定を定義する設定を追加することができます、Windows Communication Foundation (WCF) サービスの型にマップする構成要素。</span><span class="sxs-lookup"><span data-stu-id="d6a57-102">A configuration element that allows you to add settings that define virtual service activation settings that map to your Windows Communication Foundation (WCF) service types.</span></span> <span data-ttu-id="d6a57-103">これにより、.svc ファイルを使用せずに、WAS/IIS でホストされているサービスをアクティブ化できます。</span><span class="sxs-lookup"><span data-stu-id="d6a57-103">This makes it possible to activate services hosted in WAS/IIS without an .svc file.</span></span>  
  
 <span data-ttu-id="d6a57-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="d6a57-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="d6a57-105">\<serviceHostingEnvironment></span><span class="sxs-lookup"><span data-stu-id="d6a57-105">\<serviceHostingEnvironment></span></span>  
<span data-ttu-id="d6a57-106">\<serviceActivations></span><span class="sxs-lookup"><span data-stu-id="d6a57-106">\<serviceActivations></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d6a57-107">構文</span><span class="sxs-lookup"><span data-stu-id="d6a57-107">Syntax</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <serviceActivations>
    <add factory="String"
         service="String" />
  </serviceActivations>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d6a57-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="d6a57-108">Attributes and Elements</span></span>  
 <span data-ttu-id="d6a57-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="d6a57-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d6a57-110">属性</span><span class="sxs-lookup"><span data-stu-id="d6a57-110">Attributes</span></span>  
 <span data-ttu-id="d6a57-111">なし。</span><span class="sxs-lookup"><span data-stu-id="d6a57-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d6a57-112">子要素</span><span class="sxs-lookup"><span data-stu-id="d6a57-112">Child Elements</span></span>  
  
|<span data-ttu-id="d6a57-113">要素</span><span class="sxs-lookup"><span data-stu-id="d6a57-113">Element</span></span>|<span data-ttu-id="d6a57-114">説明</span><span class="sxs-lookup"><span data-stu-id="d6a57-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d6a57-115">\<add></span><span class="sxs-lookup"><span data-stu-id="d6a57-115">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-serviceactivations.md)|<span data-ttu-id="d6a57-116">サービス アプリケーションのアクティベーションを指定する構成要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="d6a57-116">Adds a configuration element that specifies the activation of a service application.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d6a57-117">親要素</span><span class="sxs-lookup"><span data-stu-id="d6a57-117">Parent Elements</span></span>  
  
|<span data-ttu-id="d6a57-118">要素</span><span class="sxs-lookup"><span data-stu-id="d6a57-118">Element</span></span>|<span data-ttu-id="d6a57-119">説明</span><span class="sxs-lookup"><span data-stu-id="d6a57-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d6a57-120">\<serviceHostingEnvironment></span><span class="sxs-lookup"><span data-stu-id="d6a57-120">\<serviceHostingEnvironment></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md)|<span data-ttu-id="d6a57-121">環境をホストするサービスがインスタンス化する特定のトランスポートの型を定義します。</span><span class="sxs-lookup"><span data-stu-id="d6a57-121">Defines the type the service hosting environment instantiates for a particular transport.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d6a57-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="d6a57-122">Remarks</span></span>  
 <span data-ttu-id="d6a57-123">web.config ファイルでアクティベーション設定を構成する方法を次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="d6a57-123">The following example shows how to configure activation settings within your web.config file.</span></span>  
  
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
  
 <span data-ttu-id="d6a57-124">この構成を使用して、.svc ファイルを使用せずに、GreetingService をアクティブ化できます。</span><span class="sxs-lookup"><span data-stu-id="d6a57-124">Using this configuration, you can activate the GreetingService without using an .svc file.</span></span>  
  
 <span data-ttu-id="d6a57-125">`<serviceHostingEnvironment>` はアプリケーション レベルの構成であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d6a57-125">Note that `<serviceHostingEnvironment>` is an application level configuration.</span></span> <span data-ttu-id="d6a57-126">構成を格納した `web.config` は、仮想アプリケーションのルートの下に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6a57-126">You have to place the `web.config` containing the configuration under the root of the virtual Application.</span></span> <span data-ttu-id="d6a57-127">また、`serviceHostingEnvironment` は machinetoApplication の継承可能なセクションです。</span><span class="sxs-lookup"><span data-stu-id="d6a57-127">In addition, `serviceHostingEnvironment` is a machinetoApplication inheritable section.</span></span> <span data-ttu-id="d6a57-128">コンピューターのルートに単一のサービスを登録すると、アプリケーションの各サービスはこのサービスを継承します。</span><span class="sxs-lookup"><span data-stu-id="d6a57-128">If you register a single service in the root of the machine, every service in the application will inherit this service.</span></span>  
  
 <span data-ttu-id="d6a57-129">構成ベースのアクティベーションは、http および非 http プロトコル経由のアクティベーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d6a57-129">Configuration-based activation supports activation over both http and non-http protocol.</span></span> <span data-ttu-id="d6a57-130">relatativeAddress では、.svc、.xoml、.xamlx などの拡張子が必要です。</span><span class="sxs-lookup"><span data-stu-id="d6a57-130">It requires extensions in the relatativeAddress i.e. .svc, .xoml or .xamlx.</span></span> <span data-ttu-id="d6a57-131">既知の buildProviders に対して独自の拡張子をマップできます。これにより、任意の拡張子を使用してサービスをアクティブ化できるようになります。</span><span class="sxs-lookup"><span data-stu-id="d6a57-131">You can map your own extensions to the know buildProviders, which will then enable you to activate service over any extension.</span></span> <span data-ttu-id="d6a57-132">競合が発生した場合には、`<serviceActivations>` セクションにより、.svc の登録がオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="d6a57-132">Upon conflict, the `<serviceActivations>` section overrides .svc registrations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6a57-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="d6a57-133">See also</span></span>
- <xref:System.ServiceModel.Configuration.ServiceActivationElementCollection>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
