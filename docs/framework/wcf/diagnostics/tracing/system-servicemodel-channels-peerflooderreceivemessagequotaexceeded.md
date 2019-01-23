---
title: System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded
ms.date: 03/30/2017
ms.assetid: b8371d0a-843e-440b-b86a-6996db131cb0
ms.openlocfilehash: 3ce6b3021f47708c222c3ec5a88d474d17106748
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54500993"
---
# <a name="systemservicemodelchannelspeerflooderreceivemessagequotaexceeded"></a>System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded
メッセージの受信速度が速すぎます。  
  
## <a name="description"></a>説明  
 このトレースは、受信メッセージの処理を試みたときに行われます。 特定の近隣ノードでクォータ セットが超過しているため、メッセージをその近隣ノードに転送できません。 応答しない近隣ノードが、メッセージ保留のバックログをクリアできなかった場合にこの状態が発生します。  
  
## <a name="troubleshooting"></a>トラブルシューティング  
 メッシュ内でメッセージが送信される速度を遅くしてください。  
  
## <a name="see-also"></a>関連項目
- [トレース](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [トレースを使用したアプリケーションのトラブルシューティング](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [管理と診断](../../../../../docs/framework/wcf/diagnostics/index.md)
