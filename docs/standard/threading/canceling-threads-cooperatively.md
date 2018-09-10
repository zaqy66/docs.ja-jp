---
title: スレッドの協調的な取り消し
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- threads, cancellation
ms.assetid: d2d6d5fd-e263-4fa0-847b-2fc3e0d82337
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bd32deb9c8719a12b76aaea8ec91a17471cf18f9
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/10/2018
ms.locfileid: "44259861"
---
# <a name="canceling-threads-cooperatively"></a><span data-ttu-id="8c931-102">スレッドの協調的な取り消し</span><span class="sxs-lookup"><span data-stu-id="8c931-102">Canceling threads cooperatively</span></span>

<span data-ttu-id="8c931-103">.NET Framework 4 より前のバージョンの .NET Framework には、開始されたスレッドを協調的に取り消す手段は組み込まれていませんでした。</span><span class="sxs-lookup"><span data-stu-id="8c931-103">Prior to the .NET Framework 4, the .NET Framework provided no built-in way to cancel a thread cooperatively after it was started.</span></span> <span data-ttu-id="8c931-104">ただし、.NET Framework 4 以降、<xref:System.Threading.Tasks.Task?displayProperty=nameWithType> オブジェクトや PLINQ クエリを取り消す場合と同様に、<xref:System.Threading.CancellationToken?displayProperty=nameWithType> を使用してスレッドを取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="8c931-104">However, starting with the .NET Framework 4, you can use a <xref:System.Threading.CancellationToken?displayProperty=nameWithType> to cancel threads, just as you can use them to cancel <xref:System.Threading.Tasks.Task?displayProperty=nameWithType> objects or PLINQ queries.</span></span> <span data-ttu-id="8c931-105"><xref:System.Threading.Thread?displayProperty=nameWithType> クラスにはキャンセル トークンのサポートは組み込まれていませんが、<xref:System.Threading.ParameterizedThreadStart> デリゲートを受け取る <xref:System.Threading.Thread> コンストラクターを使用して、トークンをスレッド プロシージャに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="8c931-105">Although the <xref:System.Threading.Thread?displayProperty=nameWithType> class does not offer built-in support for cancellation tokens, you can pass a token to a thread procedure by using the <xref:System.Threading.Thread> constructor that takes a <xref:System.Threading.ParameterizedThreadStart> delegate.</span></span> <span data-ttu-id="8c931-106">この方法を次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="8c931-106">The following example demonstrates how to do this.</span></span>  
  
 [!code-csharp[Cancellation#14](../../../samples/snippets/csharp/VS_Snippets_Misc/cancellation/cs/CooperativeThreads.cs#14)]
 [!code-vb[Cancellation#14](../../../samples/snippets/visualbasic/VS_Snippets_Misc/cancellation/vb/CooperativeThreads.vb#14)]  
  
## <a name="see-also"></a><span data-ttu-id="8c931-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c931-107">See also</span></span>

- [<span data-ttu-id="8c931-108">スレッドの使用とスレッド処理</span><span class="sxs-lookup"><span data-stu-id="8c931-108">Using Threads and Threading</span></span>](using-threads-and-threading.md)
