---
title: Microsoft.Transactions.TransactionBridge.RegisterParticipantFailure
ms.date: 03/30/2017
ms.assetid: 3a4ead79-8550-4037-84e3-fd70ff56e001
ms.openlocfilehash: b94c017f6ed3a76a6bc5ed2cb970877ad18ef9ea
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610423"
---
# <a name="microsofttransactionstransactionbridgeregisterparticipantfailure"></a>Microsoft.Transactions.TransactionBridge.RegisterParticipantFailure
WS-AT プロトコル サービスは、制御プロトコルの参加要素の登録に失敗しました。  
  
## <a name="description"></a>説明  
 MSDTC により無効な登録要求が検出された場合にトレースされます。 これは、複数の完了登録要求や内部エラーによって発生することがあります。  
  
## <a name="troubleshooting"></a>トラブルシューティング  
 完了を複数回登録しないでください。  また、トレース メッセージ内のステータス文字列を調べて、アクション可能な項目が存在するかどうかを確認します。  
  
## <a name="see-also"></a>関連項目
- [トレース](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [トレースを使用したアプリケーションのトラブルシューティング](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [管理と診断](../../../../../docs/framework/wcf/diagnostics/index.md)
