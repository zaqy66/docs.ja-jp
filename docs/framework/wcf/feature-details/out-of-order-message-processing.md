---
title: 順番を無視したメッセージの処理
ms.date: 03/30/2017
ms.assetid: 33fc62a5-5d59-461c-a37a-0e1b51ac763d
ms.openlocfilehash: 3beca8d73788d177d07868d7169d8aea3ecd8e80
ms.sourcegitcommit: 3b9b7ae6771712337d40374d2fef6b25b0d53df6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/04/2019
ms.locfileid: "54029946"
---
# <a name="out-of-order-message-processing"></a><span data-ttu-id="f1bd1-102">順番を無視したメッセージの処理</span><span class="sxs-lookup"><span data-stu-id="f1bd1-102">Out-of-Order Message Processing</span></span>
<span data-ttu-id="f1bd1-103">ワークフロー サービスは、特定の順序で送信されるメッセージに依存する場合があります。</span><span class="sxs-lookup"><span data-stu-id="f1bd1-103">Workflow services may depend on messages being sent in a specific order.</span></span> <span data-ttu-id="f1bd1-104">ワークフロー サービスには 1 つ以上の <xref:System.ServiceModel.Activities.Receive> アクティビティが含まれ、それぞれの <xref:System.ServiceModel.Activities.Receive> アクティビティは特定のメッセージに対応しています。</span><span class="sxs-lookup"><span data-stu-id="f1bd1-104">A workflow service contains one or more <xref:System.ServiceModel.Activities.Receive> activities and each <xref:System.ServiceModel.Activities.Receive> activity is expecting a specific message.</span></span> <span data-ttu-id="f1bd1-105">特定のトランスポート配信保証がないと、クライアントから送信されるメッセージに遅延が生じ、それによって、ワークフロー サービスが予期しない順序でメッセージが配信されることがあります。</span><span class="sxs-lookup"><span data-stu-id="f1bd1-105">Without particular transport delivery guarantees, messages sent by clients may be delayed and therefore delivered in an order the workflow service may not expect.</span></span> <span data-ttu-id="f1bd1-106">特定の順序でメッセージが送信されることを必要としないワークフローは、通常、Parallel アクティビティを使用して実装されます。</span><span class="sxs-lookup"><span data-stu-id="f1bd1-106">Implementing a workflow service that does not require messages be sent in a specific order is normally done using a Parallel activity.</span></span> <span data-ttu-id="f1bd1-107">アプリケーション プロトコルがより複雑な場合は、ワークフローがすぐに複雑になります。</span><span class="sxs-lookup"><span data-stu-id="f1bd1-107">For a more complicated application protocol, the workflow would become very complex very quickly.</span></span>  <span data-ttu-id="f1bd1-108">Windows Communication Foundation (WCF) 機能の処理順序のメッセージの入れ子になった並列アクティビティの複雑さがすべてないこのようなワークフローを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f1bd1-108">The out-of-order message processing feature in Windows Communication Foundation (WCF) allows you to create such a workflow without all of the complexity of nested Parallel activities.</span></span> <span data-ttu-id="f1bd1-109">順序のメッセージの処理のみをサポートするチャネルでサポートされて<xref:System.ServiceModel.Channels.ReceiveContext>WCF MSMQ バインディングなど。</span><span class="sxs-lookup"><span data-stu-id="f1bd1-109">Out-of-order message processing is only supported on channels that support <xref:System.ServiceModel.Channels.ReceiveContext> such as the WCF MSMQ bindings.</span></span>  
  
## <a name="enabling-out-of-order-message-processing"></a><span data-ttu-id="f1bd1-110">順番を無視したメッセージ処理の有効化</span><span class="sxs-lookup"><span data-stu-id="f1bd1-110">Enabling Out-Of-Order Message Processing</span></span>  
 <span data-ttu-id="f1bd1-111">順番を無視したメッセージ処理は、ワークフロー サービスで <xref:System.ServiceModel.Activities.WorkflowService.AllowBufferedReceive%2A> プロパティを `true` に設定することで有効化できます。</span><span class="sxs-lookup"><span data-stu-id="f1bd1-111">Out-of-order message processing is enabled by setting the <xref:System.ServiceModel.Activities.WorkflowService.AllowBufferedReceive%2A> property to `true` on the WorkflowService.</span></span> <span data-ttu-id="f1bd1-112">次の例は、コードで <xref:System.ServiceModel.Activities.WorkflowService.AllowBufferedReceive%2A> プロパティを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f1bd1-112">The following example shows how to set the <xref:System.ServiceModel.Activities.WorkflowService.AllowBufferedReceive%2A> property in code.</span></span>  
  
```csharp  
// Code: Opt-in to Buffered Receive processing...  
WorkflowService service = new WorkflowService  
{  
    Name="MyService",  
    Body = workflow,  
    AllowBufferedReceive = true  
};  
```  
  
 <span data-ttu-id="f1bd1-113">また、次の例に示すように、XAML で `AllowBufferedReceive` 属性をワークフロー サービスに適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="f1bd1-113">You can also apply the `AllowBufferedReceive` attribute to a workflow service in XAML as shown in the following example.</span></span>  
  
```xaml  
// Xaml: Opt-in to Buffered Receive processing...  
<WorkflowService AllowBufferedReceive="True">  
   <!--the actual children activities -->  
</Sequence>  
```  
  
## <a name="see-also"></a><span data-ttu-id="f1bd1-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1bd1-114">See Also</span></span>  
 <xref:System.ServiceModel.Channels.ReceiveContext>  
 [<span data-ttu-id="f1bd1-115">ワークフロー サービス</span><span class="sxs-lookup"><span data-stu-id="f1bd1-115">Workflow Services</span></span>](../../../../docs/framework/wcf/feature-details/workflow-services.md)  
 [<span data-ttu-id="f1bd1-116">キューと信頼できるセッション</span><span class="sxs-lookup"><span data-stu-id="f1bd1-116">Queues and Reliable Sessions</span></span>](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md)
