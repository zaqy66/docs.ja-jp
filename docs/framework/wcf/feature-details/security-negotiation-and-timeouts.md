---
title: セキュリティ ネゴシエーションとタイムアウト
ms.date: 03/30/2017
ms.assetid: 02a428f1-84e5-4d28-a11f-53ce31d63196
ms.openlocfilehash: dfabdb05c7658e3cf9eb5b325597360bbc0bb588
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50037799"
---
# <a name="security-negotiation-and-timeouts"></a><span data-ttu-id="5a36b-102">セキュリティ ネゴシエーションとタイムアウト</span><span class="sxs-lookup"><span data-stu-id="5a36b-102">Security Negotiation and Timeouts</span></span>
<span data-ttu-id="5a36b-103">クライアントとサービスの認証と Windows Communication Foundation (WCF) には、認証の一部としてサービス資格情報をネゴシエートする場所のモードがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="5a36b-103">When clients and services authenticate, Windows Communication Foundation (WCF) supports a mode where the service credential is negotiated as part of authentication.</span></span> <span data-ttu-id="5a36b-104">このようなシナリオでは、サービス資格情報をクライアントに反映させるために、クライアントとサービスの間でマルチレッグ交換が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5a36b-104">In such scenarios, a potentially multi-leg exchange occurs between the client and the service to propagate the service credential to the client.</span></span> <span data-ttu-id="5a36b-105"><xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> プロパティは、マルチレッグ交換の完了に要する時間を制御します。</span><span class="sxs-lookup"><span data-stu-id="5a36b-105">The <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> property controls how long the multi-leg exchange can take to complete.</span></span> <span data-ttu-id="5a36b-106">ただし、このタイムアウトは、実際に、単一の要求 - 応答よりも長い時間が交換にかかる場合のみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="5a36b-106">However, this timeout only applies if the exchange actually takes more that a single request-response.</span></span> <span data-ttu-id="5a36b-107">単一のラウンド トリップでネゴシエーションが完了する場合、このタイムアウトは適用されません。</span><span class="sxs-lookup"><span data-stu-id="5a36b-107">In cases where the negotiation completes in a single round trip, the timeout does not apply.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5a36b-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a36b-108">See Also</span></span>  
 <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>  
 [<span data-ttu-id="5a36b-109">方法 : 時刻のずれの最大値を設定する</span><span class="sxs-lookup"><span data-stu-id="5a36b-109">How to: Set a Max Clock Skew</span></span>](../../../../docs/framework/wcf/feature-details/how-to-set-a-max-clock-skew.md)
