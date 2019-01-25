---
title: Microsoft.Transactions.TransactionBridge.EnlistTransactionFailure
ms.date: 03/30/2017
ms.assetid: 1b9f5139-e122-4716-9ef7-2f38e1813993
ms.openlocfilehash: 4f51777ae690178b83d353f72e63a6f2958b1592
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54674584"
---
# <a name="microsofttransactionstransactionbridgeenlisttransactionfailure"></a>Microsoft.Transactions.TransactionBridge.EnlistTransactionFailure
WS-AT プロトコル サービスは、指定されたコーディネーション コンテキストを使用してトランザクションに参加することができませんでした。  
  
## <a name="description"></a>説明  
 指定された 2PC プロトコルのトランザクションに MSDTC が参加できない場合にトレースされます。  これは、トランザクションが存在しなくなった場合、参加が許可されなくなった場合、または既に参加が多すぎる場合に発生する可能性があります。  
  
## <a name="troubleshooting"></a>トラブルシューティング  
 トレース メッセージ内のステータス文字列を調べて、アクション可能な項目が存在するかどうかを確認します。  
  
## <a name="see-also"></a>関連項目
- [トレース](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [トレースを使用したアプリケーションのトラブルシューティング](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [管理と診断](../../../../../docs/framework/wcf/diagnostics/index.md)
