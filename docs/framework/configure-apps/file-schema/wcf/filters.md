---
title: '&lt;フィルター&gt;'
ms.date: 03/30/2017
ms.assetid: 37a87222-ec78-4728-8105-9ca1bd961f0c
ms.openlocfilehash: aae70fbe873eee10fcf95dcdd443dfa9ae6efb57
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148969"
---
# <a name="ltfiltersgt"></a><span data-ttu-id="75f69-102">&lt;フィルター&gt;</span><span class="sxs-lookup"><span data-stu-id="75f69-102">&lt;filters&gt;</span></span>

<span data-ttu-id="75f69-103">`filters` 要素は、ログに記録されるメッセージの種類の制御に使用される XPath フィルターのコレクションを保持します。</span><span class="sxs-lookup"><span data-stu-id="75f69-103">The `filters` element holds a collection of XPath filters used to control what kind of message is logged.</span></span>

<span data-ttu-id="75f69-104">フィルターは、`logMessagesAtTransportLevel` を `true` に設定することによって指定されるトランスポート層でのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="75f69-104">Filters are applied only at the transport layer, specified by `logMessagesAtTransportLevel` is `true`.</span></span> <span data-ttu-id="75f69-105">サービス レベルおよび形式が正しくないメッセージ ログ記録は、フィルターの影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="75f69-105">Service level and malformed message logging are not affected by filters.</span></span>

<span data-ttu-id="75f69-106">コレクションにフィルターを追加するには、`add` を使用します。</span><span class="sxs-lookup"><span data-stu-id="75f69-106">To add a filter to the collection, use the `add` keyword.</span></span> <span data-ttu-id="75f69-107">1 つ以上のフィルターを定義した場合は、少なくとも 1 つのフィルターと一致するメッセージだけが記録されます。</span><span class="sxs-lookup"><span data-stu-id="75f69-107">When one or more filters are defined, only messages that match at least one of the filters are logged.</span></span> <span data-ttu-id="75f69-108">フィルターを定義しなかった場合は、すべてのメッセージが通過します。</span><span class="sxs-lookup"><span data-stu-id="75f69-108">If no filter is defined, all messages pass through.</span></span>

<span data-ttu-id="75f69-109">フィルターは、完全な XPath 構文をサポートし、構成ファイルでの出現順に適用されます。</span><span class="sxs-lookup"><span data-stu-id="75f69-109">Filters support the full XPath syntax, and are applied in the order they appear in the configuration file.</span></span> <span data-ttu-id="75f69-110">フィルターが構文的に正しくない場合は、構成例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="75f69-110">A syntactically incorrect filter results in a configuration exception.</span></span>

<span data-ttu-id="75f69-111">SOAP ヘッダー セクションがあるメッセージだけを記録するフィルターの設定方法の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="75f69-111">The following is an example of how to configure a filter that records only messages that have a SOAP Header section.</span></span>
  
```xml  
<messageLogging logEntireMessage="true"
                logMalformedMessages="true"
                logMessagesAtServiceLevel="true"
                logMessagesAtTransportLevel="true"
                maxMessagesToLog="420">
  <filters>
    <add xmlns:soap="http://www.w3.org/2003/05/soap-envelope">
      /soap:Envelope/soap:Headers
    </add>
  </filters>
</messageLogging>
```  
  
## <a name="see-also"></a><span data-ttu-id="75f69-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="75f69-112">See also</span></span>

 <span data-ttu-id="75f69-113"><xref:System.ServiceModel.Configuration.DiagnosticSection> <xref:System.ServiceModel.Diagnostics></span><span class="sxs-lookup"><span data-stu-id="75f69-113"><xref:System.ServiceModel.Configuration.DiagnosticSection> <xref:System.ServiceModel.Diagnostics></span></span>
 <xref:System.ServiceModel.Configuration.DiagnosticSection.MessageLogging%2A>
 <xref:System.ServiceModel.Configuration.MessageLoggingElement>
 <xref:System.ServiceModel.Configuration.MessageLoggingElement.Filters%2A>
 <xref:System.ServiceModel.Configuration.XPathMessageFilterElementCollection>
 <xref:System.ServiceModel.Configuration.XPathMessageFilterElement>
 <xref:System.ServiceModel.Dispatcher.XPathMessageFilter>
 <span data-ttu-id="75f69-114">[メッセージのログの構成](../../../../../docs/framework/wcf/diagnostics/configuring-message-logging.md) [ \<messageLogging >](../../../../../docs/framework/configure-apps/file-schema/wcf/messagelogging.md)</span><span class="sxs-lookup"><span data-stu-id="75f69-114">[Configuring Message Logging](../../../../../docs/framework/wcf/diagnostics/configuring-message-logging.md) [\<messageLogging>](../../../../../docs/framework/configure-apps/file-schema/wcf/messagelogging.md)</span></span>
