---
title: '方法: タスクに EAP パターンをラップする'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- tasks, how to wrap EAP patterns
ms.assetid: f11ed467-af2f-4504-8a2e-299a6c36d44e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a4287879bd95f7bc1e1dc99f74fa0d7cc0fe737f
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/18/2018
ms.locfileid: "46004261"
---
# <a name="how-to-wrap-eap-patterns-in-a-task"></a>方法: タスクに EAP パターンをラップする
次の例では、<xref:System.Threading.Tasks.TaskCompletionSource%601> を使用して、任意のシーケンスのイベント ベースの非同期パターン (EAP) 操作を公開する方法を示します。 また、この例は <xref:System.Threading.CancellationToken> を使用して、<xref:System.Net.WebClient> オブジェクトの組み込みキャンセル メソッドを呼び出す方法も示しています。  
  
## <a name="example"></a>例  
 [!code-csharp[FromAsync#08](../../../samples/snippets/csharp/VS_Snippets_Misc/fromasync/cs/fromasync.cs#08)]
 [!code-vb[FromAsync#08](../../../samples/snippets/visualbasic/VS_Snippets_Misc/fromasync/vb/module1.vb#08)]  
  
## <a name="see-also"></a>関連項目

- [TPL と従来の .NET Framework 非同期プログラミング](../../../docs/standard/parallel-programming/tpl-and-traditional-async-programming.md)
