---
title: セキュリティ ネゴシエーションとタイムアウト
ms.date: 03/30/2017
ms.assetid: 02a428f1-84e5-4d28-a11f-53ce31d63196
author: BrucePerlerMS
ms.openlocfilehash: 6b6c9c6ed44eb3ebefb21f2fbff1e73171262ed7
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47088309"
---
# <a name="security-negotiation-and-timeouts"></a>セキュリティ ネゴシエーションとタイムアウト
クライアントとサービスの認証と Windows Communication Foundation (WCF) には、認証の一部としてサービス資格情報をネゴシエートする場所のモードがサポートされます。 このようなシナリオでは、サービス資格情報をクライアントに反映させるために、クライアントとサービスの間でマルチレッグ交換が発生する可能性があります。 <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> プロパティは、マルチレッグ交換の完了に要する時間を制御します。 ただし、このタイムアウトは、実際に、単一の要求 - 応答よりも長い時間が交換にかかる場合のみ適用されます。 単一のラウンド トリップでネゴシエーションが完了する場合、このタイムアウトは適用されません。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>  
 [方法 : 時刻のずれの最大値を設定する](../../../../docs/framework/wcf/feature-details/how-to-set-a-max-clock-skew.md)
