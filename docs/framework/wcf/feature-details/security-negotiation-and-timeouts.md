---
title: セキュリティ ネゴシエーションとタイムアウト
ms.date: 03/30/2017
ms.assetid: 02a428f1-84e5-4d28-a11f-53ce31d63196
ms.openlocfilehash: 38dce9bd6587850a5e3327600bb8bc13c48b93e1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54592615"
---
# <a name="security-negotiation-and-timeouts"></a><span data-ttu-id="0ffa9-102">セキュリティ ネゴシエーションとタイムアウト</span><span class="sxs-lookup"><span data-stu-id="0ffa9-102">Security Negotiation and Timeouts</span></span>
<span data-ttu-id="0ffa9-103">クライアントとサービスの認証と Windows Communication Foundation (WCF) には、認証の一部としてサービス資格情報をネゴシエートする場所のモードがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="0ffa9-103">When clients and services authenticate, Windows Communication Foundation (WCF) supports a mode where the service credential is negotiated as part of authentication.</span></span> <span data-ttu-id="0ffa9-104">このようなシナリオでは、サービス資格情報をクライアントに反映させるために、クライアントとサービスの間でマルチレッグ交換が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0ffa9-104">In such scenarios, a potentially multi-leg exchange occurs between the client and the service to propagate the service credential to the client.</span></span> <span data-ttu-id="0ffa9-105"><xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> プロパティは、マルチレッグ交換の完了に要する時間を制御します。</span><span class="sxs-lookup"><span data-stu-id="0ffa9-105">The <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> property controls how long the multi-leg exchange can take to complete.</span></span> <span data-ttu-id="0ffa9-106">ただし、このタイムアウトは、実際に、単一の要求 - 応答よりも長い時間が交換にかかる場合のみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="0ffa9-106">However, this timeout only applies if the exchange actually takes more that a single request-response.</span></span> <span data-ttu-id="0ffa9-107">単一のラウンド トリップでネゴシエーションが完了する場合、このタイムアウトは適用されません。</span><span class="sxs-lookup"><span data-stu-id="0ffa9-107">In cases where the negotiation completes in a single round trip, the timeout does not apply.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ffa9-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="0ffa9-108">See also</span></span>
- <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
- [<span data-ttu-id="0ffa9-109">方法: 最大クロックのずれを設定</span><span class="sxs-lookup"><span data-stu-id="0ffa9-109">How to: Set a Max Clock Skew</span></span>](../../../../docs/framework/wcf/feature-details/how-to-set-a-max-clock-skew.md)
