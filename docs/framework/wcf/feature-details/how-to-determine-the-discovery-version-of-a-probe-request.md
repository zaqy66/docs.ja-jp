---
title: '方法: Probe 要求の探索バージョンを特定する'
ms.date: 03/30/2017
ms.assetid: b3c4e2e2-2957-4074-ae6a-776a5ca84278
ms.openlocfilehash: 356ddd76bdee0698fa446d830791f702af5742b9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54595124"
---
# <a name="how-todetermine-the-discovery-version-of-a-probe-request"></a><span data-ttu-id="a42e8-102">方法: Probe 要求の探索バージョンを特定する</span><span class="sxs-lookup"><span data-stu-id="a42e8-102">How to:Determine the Discovery Version of a Probe Request</span></span>
<span data-ttu-id="a42e8-103">探索プロキシでは、異なる探索バージョンを使用する複数の探索エンドポイントを公開する場合があります。</span><span class="sxs-lookup"><span data-stu-id="a42e8-103">A discovery proxy may expose multiple discovery endpoints using different discovery versions.</span></span> <span data-ttu-id="a42e8-104">プロキシでは、UDP マルチキャスト Probe 要求を受け取った場合、マルチキャスト抑制メッセージで応答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a42e8-104">When a UDP multicast Probe request arrives at the proxy the proxy should respond with a multicast suppression message.</span></span> <span data-ttu-id="a42e8-105">これを行うには、要求の探索バージョンを特定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a42e8-105">In order to do this it would have to know the discovery version of the request.</span></span>  
  
### <a name="to-determine-the-discovery-version-of-a-probe-request"></a><span data-ttu-id="a42e8-106">Probe 要求の探索バージョンを特定するには</span><span class="sxs-lookup"><span data-stu-id="a42e8-106">To Determine the Discovery Version of a Probe Request</span></span>  
  
1.  <span data-ttu-id="a42e8-107">次のコードに示すように、Probe 要求に応答するメソッド (<xref:System.ServiceModel.Discovery.DiscoveryProxy.OnBeginFind%2A> など) で静的 <xref:System.ServiceModel.OperationContext.Current%2A> プロパティを使用して <xref:System.ServiceModel.Discovery.DiscoveryOperationContextExtension> を検索します。</span><span class="sxs-lookup"><span data-stu-id="a42e8-107">In the method that responds to a Probe request (for example <xref:System.ServiceModel.Discovery.DiscoveryProxy.OnBeginFind%2A>) use the static <xref:System.ServiceModel.OperationContext.Current%2A> property to search for a <xref:System.ServiceModel.Discovery.DiscoveryOperationContextExtension> as shown in the following code.</span></span>  
  
    ```  
    DiscoveryOperationContextExtension doce = OperationContext.Current.Extensions.Find<DiscoveryOperationContextExtension>();  
    // Access the discovery version from the DiscoveryOperationContextExtension  
    doce.DiscoveryVersion;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="a42e8-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="a42e8-108">See also</span></span>

- <xref:System.ServiceModel.Discovery.Configuration.AnnouncementEndpointElement.DiscoveryVersion%2A>
- [<span data-ttu-id="a42e8-109">探索プロキシの実装</span><span class="sxs-lookup"><span data-stu-id="a42e8-109">Implementing a Discovery Proxy</span></span>](../../../../docs/framework/wcf/feature-details/implementing-a-discovery-proxy.md)
