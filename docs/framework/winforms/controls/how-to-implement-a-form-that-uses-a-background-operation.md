---
title: '方法: バック グラウンド操作を使用してフォームを実装します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- threading [Windows Forms], forms
- BackgroundWorker component
- background tasks
- forms [Windows Forms], multithreading
- components [Windows Forms], asynchronous
- forms [Windows Forms], background operations
- background threads
- threading [Windows Forms], background operations
- background operations
ms.assetid: 9f483f93-1613-4be1-a021-b4934e9c78f3
ms.openlocfilehash: a472226103f077975c9c6ddc744d419cfcc390cf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54532137"
---
# <a name="how-to-implement-a-form-that-uses-a-background-operation"></a><span data-ttu-id="66b91-102">方法: バック グラウンド操作を使用してフォームを実装します。</span><span class="sxs-lookup"><span data-stu-id="66b91-102">How to: Implement a Form That Uses a Background Operation</span></span>
<span data-ttu-id="66b91-103">次のサンプル プログラムは、フィボナッチの数列を計算するフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="66b91-103">The following example program creates a form that calculates Fibonacci numbers.</span></span> <span data-ttu-id="66b91-104">計算では、ユーザー インターフェイス スレッドとは別にあるスレッドで実行されるので、ユーザー インターフェイスは引き続き、計算の進行に伴う遅延なしに実行されます。</span><span class="sxs-lookup"><span data-stu-id="66b91-104">The calculation runs on a thread that is separate from the user interface thread, so the user interface continues to run without delays as the calculation proceeds.</span></span>  
  
 <span data-ttu-id="66b91-105">Visual Studio では、このタスクに対する広範なサポートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="66b91-105">There is extensive support for this task in Visual Studio.</span></span>  
  
 <span data-ttu-id="66b91-106">参照してください[チュートリアル。バック グラウンド操作を使用するフォームを実装する](https://msdn.microsoft.com/library/b2zk6580\(v=vs.110\))します。</span><span class="sxs-lookup"><span data-stu-id="66b91-106">Also see [Walkthrough: Implementing a Form That Uses a Background Operation](https://msdn.microsoft.com/library/b2zk6580\(v=vs.110\)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="66b91-107">例</span><span class="sxs-lookup"><span data-stu-id="66b91-107">Example</span></span>  
 [!code-cpp[System.ComponentModel.BackgroundWorker#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#1)]
 [!code-csharp[System.ComponentModel.BackgroundWorker#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="66b91-108">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="66b91-108">Compiling the Code</span></span>  
 <span data-ttu-id="66b91-109">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="66b91-109">This example requires:</span></span>  
  
-   <span data-ttu-id="66b91-110">System、System.Drawing、および System.Windows.Forms の各アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="66b91-110">References to the System, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="66b91-111">コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。</span><span class="sxs-lookup"><span data-stu-id="66b91-111">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="66b91-112">新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="66b91-112">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="66b91-113">参照してください[方法。Visual Studio を使用して、完全な Windows フォームのコードの例をコンパイルして](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))します。</span><span class="sxs-lookup"><span data-stu-id="66b91-113">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="66b91-114">信頼性の高いプログラミング</span><span class="sxs-lookup"><span data-stu-id="66b91-114">Robust Programming</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="66b91-115">どのような種類のマルチスレッドを使用している場合でも、非常に深刻で複雑なバグを引き起こしてしまう可能性があります。</span><span class="sxs-lookup"><span data-stu-id="66b91-115">When using multithreading of any sort, you potentially expose yourself to very serious and complex bugs.</span></span> <span data-ttu-id="66b91-116">マルチスレッドを使用するソリューションを実装する前に、「[マネージド スレッド処理の実施](../../../../docs/standard/threading/managed-threading-best-practices.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66b91-116">Consult the [Managed Threading Best Practices](../../../../docs/standard/threading/managed-threading-best-practices.md) before implementing any solution that uses multithreading.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="66b91-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="66b91-117">See also</span></span>
- <xref:System.ComponentModel.BackgroundWorker>
- <xref:System.ComponentModel.DoWorkEventArgs>
- [<span data-ttu-id="66b91-118">イベントベースの非同期パターンの概要</span><span class="sxs-lookup"><span data-stu-id="66b91-118">Event-based Asynchronous Pattern Overview</span></span>](../../../../docs/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview.md)
- [<span data-ttu-id="66b91-119">マネージド スレッド処理の実施</span><span class="sxs-lookup"><span data-stu-id="66b91-119">Managed Threading Best Practices</span></span>](../../../../docs/standard/threading/managed-threading-best-practices.md)
