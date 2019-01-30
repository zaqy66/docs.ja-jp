---
title: <backupLists>
ms.date: 03/30/2017
ms.assetid: 593b3390-f65b-4684-ad40-0596b62f0954
ms.openlocfilehash: 6ac7ff19c76097cb54e7b77db21cad50b49513c0
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55280749"
---
# <a name="backuplists"></a><span data-ttu-id="4b583-101">\<backupLists ></span><span class="sxs-lookup"><span data-stu-id="4b583-101">\<backupLists></span></span>
<span data-ttu-id="4b583-102">エラー処理に使用されるバックアップ サービス セットを定義する構成セクションを表します。</span><span class="sxs-lookup"><span data-stu-id="4b583-102">Represents a configuration section for defining a set of backup services used in error handling.</span></span> <span data-ttu-id="4b583-103">各子要素は、プライマリ エンドポイントに接続できない場合に使用するルーティング サービスが希望されるエンドポイントのセットを列挙したバックアップ リストです。</span><span class="sxs-lookup"><span data-stu-id="4b583-103">Each child element is a backup list that enumerates a set of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span> <span data-ttu-id="4b583-104">リストの最初のエンドポイントがダウンしていると、ルーティング サービスは自動的にリスト内で次にあるエンドポイントにフェールオーバーします。</span><span class="sxs-lookup"><span data-stu-id="4b583-104">If the first endpoint in the list is down, the Routing Service will automatically fail-over to the next one in the list.</span></span>  <span data-ttu-id="4b583-105">これにより、クライアント アプリケーションに複雑なパターンの処理方法やサービスの配置場所を示すことなく、アプリケーションの信頼性を高めることができます。</span><span class="sxs-lookup"><span data-stu-id="4b583-105">This gives you a quick way to add reliability to your application without having to teach your client application how to handle complex patterns or where all of your services are deployed.</span></span>  
  
 <span data-ttu-id="4b583-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="4b583-106">\<system.serviceModel></span></span>  
<span data-ttu-id="4b583-107">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="4b583-107">\<routing></span></span>  
<span data-ttu-id="4b583-108">\<backupLists ></span><span class="sxs-lookup"><span data-stu-id="4b583-108">\<backupLists></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b583-109">構文</span><span class="sxs-lookup"><span data-stu-id="4b583-109">Syntax</span></span>  
  
```xml  
<routing>
  <backupLists>
    <backupList name="String">
      <add endpointName="String" />
    </backupList>
  </backupLists>
</routing>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4b583-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="4b583-110">Attributes and Elements</span></span>  
 <span data-ttu-id="4b583-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="4b583-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4b583-112">属性</span><span class="sxs-lookup"><span data-stu-id="4b583-112">Attributes</span></span>  
 <span data-ttu-id="4b583-113">なし。</span><span class="sxs-lookup"><span data-stu-id="4b583-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4b583-114">子要素</span><span class="sxs-lookup"><span data-stu-id="4b583-114">Child Elements</span></span>  
  
|<span data-ttu-id="4b583-115">要素</span><span class="sxs-lookup"><span data-stu-id="4b583-115">Element</span></span>|<span data-ttu-id="4b583-116">説明</span><span class="sxs-lookup"><span data-stu-id="4b583-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4b583-117">\<filter></span><span class="sxs-lookup"><span data-stu-id="4b583-117">\<filter></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filter.md)|<span data-ttu-id="4b583-118">プライマリ エンドポイントに接続できない場合に使用するルーティング サービスが希望されるエンドポイントの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4b583-118">Contains a list of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span> <span data-ttu-id="4b583-119">.</span><span class="sxs-lookup"><span data-stu-id="4b583-119">.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4b583-120">親要素</span><span class="sxs-lookup"><span data-stu-id="4b583-120">Parent Elements</span></span>  
  
|<span data-ttu-id="4b583-121">要素</span><span class="sxs-lookup"><span data-stu-id="4b583-121">Element</span></span>|<span data-ttu-id="4b583-122">説明</span><span class="sxs-lookup"><span data-stu-id="4b583-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4b583-123">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="4b583-123">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="4b583-124">Windows Communication Foundation (WCF) の種類を指定するルーティング フィルター セットを定義する構成セクションを表します<xref:System.ServiceModel.Dispatcher.MessageFilter>受信メッセージの評価とルーティング テーブルをするターゲット エンドポイントを定義するときに使用される。フィルターが一致したときにメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="4b583-124">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4b583-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b583-125">See also</span></span>
- <xref:System.ServiceModel.Routing.Configuration.BackupEndpointCollection?displayProperty=nameWithType>
