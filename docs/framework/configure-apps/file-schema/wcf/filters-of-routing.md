---
title: '&lt;routing&gt; の &lt;filters&gt;'
ms.date: 03/30/2017
ms.assetid: 7993cf90-9afd-4c3c-9608-184d5da1105c
ms.openlocfilehash: 468c10bc06b60f80ce93cf413c02582fe3861f70
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54704434"
---
# <a name="ltfiltersgt-of-ltroutinggt"></a><span data-ttu-id="215f0-102">&lt;routing&gt; の &lt;filters&gt;</span><span class="sxs-lookup"><span data-stu-id="215f0-102">&lt;filters&gt; of &lt;routing&gt;</span></span>

<span data-ttu-id="215f0-103">Windows Communication Foundation (WCF) の種類を指定するルーティング フィルター セットを定義する構成セクションを表します。<xref:System.ServiceModel.Dispatcher.MessageFilter>受信メッセージを評価するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="215f0-103">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages.</span></span>

<span data-ttu-id="215f0-104">[**\<system.serviceModel>**](system-servicemodel.md) </span><span class="sxs-lookup"><span data-stu-id="215f0-104">[**\<system.serviceModel>**](system-servicemodel.md) </span></span>  
<span data-ttu-id="215f0-105">&nbsp;&nbsp;[**\<ルーティング >**](routing.md) </span><span class="sxs-lookup"><span data-stu-id="215f0-105">&nbsp;&nbsp;[**\<routing>**](routing.md) </span></span>  
<span data-ttu-id="215f0-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<filters>**</span><span class="sxs-lookup"><span data-stu-id="215f0-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<filters>**</span></span>
  
## <a name="syntax"></a><span data-ttu-id="215f0-107">構文</span><span class="sxs-lookup"><span data-stu-id="215f0-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <routing>
    <filters>
      <filter customType="String"
              filterData="String"
              filterType="Action/Address/AddressPrefix/And/Custom/Endpoint/MatchAll/XPath"
              name="String" />
    </filters>
  </routing>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="215f0-108">属性と要素</span><span class="sxs-lookup"><span data-stu-id="215f0-108">Attributes and elements</span></span>

<span data-ttu-id="215f0-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="215f0-109">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="215f0-110">属性</span><span class="sxs-lookup"><span data-stu-id="215f0-110">Attributes</span></span>

<span data-ttu-id="215f0-111">なし</span><span class="sxs-lookup"><span data-stu-id="215f0-111">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="215f0-112">子要素</span><span class="sxs-lookup"><span data-stu-id="215f0-112">Child elements</span></span>

|     | <span data-ttu-id="215f0-113">説明</span><span class="sxs-lookup"><span data-stu-id="215f0-113">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="215f0-114">**\<フィルター >**</span><span class="sxs-lookup"><span data-stu-id="215f0-114">**\<filter>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filter.md) | <span data-ttu-id="215f0-115">Windows Communication Foundation (WCF) の種類を決定するルーティング フィルターを含む<xref:System.ServiceModel.Dispatcher.MessageFilter>受信メッセージの評価時に使用されます。</span><span class="sxs-lookup"><span data-stu-id="215f0-115">Contains a routing filter that determines the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> will be used when evaluating incoming messages.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="215f0-116">親要素</span><span class="sxs-lookup"><span data-stu-id="215f0-116">Parent elements</span></span>

|     | <span data-ttu-id="215f0-117">説明</span><span class="sxs-lookup"><span data-stu-id="215f0-117">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="215f0-118">**\<ルーティング >**</span><span class="sxs-lookup"><span data-stu-id="215f0-118">**\<routing>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md) | <span data-ttu-id="215f0-119">Windows Communication Foundation (WCF) の種類を指定するルーティング フィルター セットを定義する構成セクションを表します<xref:System.ServiceModel.Dispatcher.MessageFilter>受信メッセージの評価とルーティング テーブルをするターゲット エンドポイントを定義するときに使用される。フィルターが一致したときにメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="215f0-119">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span> |

## <a name="see-also"></a><span data-ttu-id="215f0-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="215f0-120">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.FilterElement?displayProperty=nameWithType>
