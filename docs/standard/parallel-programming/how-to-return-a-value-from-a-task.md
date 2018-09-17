---
title: '方法: タスクから値を返す'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- tasks, how to return a value
ms.assetid: c4bc0f44-eba2-4e96-9e03-1cc787461e61
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2af0f82e66da1c8db5e17863dfad861c8a7d195e
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2018
ms.locfileid: "45618755"
---
# <a name="how-to-return-a-value-from-a-task"></a><span data-ttu-id="99928-102">方法: タスクから値を返す</span><span class="sxs-lookup"><span data-stu-id="99928-102">How to: Return a Value from a Task</span></span>
<span data-ttu-id="99928-103">この例では、<xref:System.Threading.Tasks.Task%601?displayProperty=nameWithType> の型を使用して <xref:System.Threading.Tasks.Task%601.Result%2A> プロパティから値を返す方法を示します。</span><span class="sxs-lookup"><span data-stu-id="99928-103">This example shows how to use the <xref:System.Threading.Tasks.Task%601?displayProperty=nameWithType> type to return a value from the <xref:System.Threading.Tasks.Task%601.Result%2A> property.</span></span> <span data-ttu-id="99928-104">C:\Users\Public\Pictures\Sample Pictures\ ディレクトリが存在している必要があり、それがファイルを含んでいる必要があります。</span><span class="sxs-lookup"><span data-stu-id="99928-104">It requires that the C:\Users\Public\Pictures\Sample Pictures\ directory exists, and that it contains files.</span></span>  
  
## <a name="example"></a><span data-ttu-id="99928-105">例</span><span class="sxs-lookup"><span data-stu-id="99928-105">Example</span></span>  
 [!code-csharp[TPL#10](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl/cs/returnavalue10.cs#10)]
 [!code-vb[TPL#10](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl/vb/10_returnavalue.vb#10)]  
  
 <span data-ttu-id="99928-106"><xref:System.Threading.Tasks.Task%601.Result%2A> プロパティは、タスクが終了するまで呼び出し元のスレッドをブロックします。</span><span class="sxs-lookup"><span data-stu-id="99928-106">The <xref:System.Threading.Tasks.Task%601.Result%2A> property blocks the calling thread until the task finishes.</span></span>  
  
 <span data-ttu-id="99928-107">1 つの <xref:System.Threading.Tasks.Task%601?displayProperty=nameWithType> の結果を継続タスクに渡す方法を確認するには、「[継続タスクを使用したタスクの連結](../../../docs/standard/parallel-programming/chaining-tasks-by-using-continuation-tasks.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99928-107">To see how to pass the result of one <xref:System.Threading.Tasks.Task%601?displayProperty=nameWithType> to a continuation task, see [Chaining Tasks by Using Continuation Tasks](../../../docs/standard/parallel-programming/chaining-tasks-by-using-continuation-tasks.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99928-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="99928-108">See also</span></span>

- [<span data-ttu-id="99928-109">タスク ベースの非同期プログラミング</span><span class="sxs-lookup"><span data-stu-id="99928-109">Task-based Asynchronous Programming</span></span>](../../../docs/standard/parallel-programming/task-based-asynchronous-programming.md)  
- [<span data-ttu-id="99928-110">PLINQ および TPL のラムダ式</span><span class="sxs-lookup"><span data-stu-id="99928-110">Lambda Expressions in PLINQ and TPL</span></span>](../../../docs/standard/parallel-programming/lambda-expressions-in-plinq-and-tpl.md)
