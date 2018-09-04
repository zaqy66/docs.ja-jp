---
title: 再帰プロシージャ (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], that call themselves
- procedures [Visual Basic], recursive
- procedures [Visual Basic], calling
- recursive procedures
- functions [Visual Basic], calling recursively
- recursion
ms.assetid: ba1d3962-b4c3-48d3-875e-96fdb4198327
ms.openlocfilehash: 0bb89ac855d65d7677a062346db8665698dbb805
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43514343"
---
# <a name="recursive-procedures-visual-basic"></a><span data-ttu-id="a0216-102">再帰プロシージャ (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a0216-102">Recursive Procedures (Visual Basic)</span></span>
<span data-ttu-id="a0216-103">A*再帰*手順は、自分自身を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a0216-103">A *recursive* procedure is one that calls itself.</span></span> <span data-ttu-id="a0216-104">通常、これは Visual Basic コードを記述する最も効果的な方法ではありません。</span><span class="sxs-lookup"><span data-stu-id="a0216-104">In general, this is not the most effective way to write Visual Basic code.</span></span>  
  
 <span data-ttu-id="a0216-105">次の手順では、元の引数の階乗を計算するのに再帰を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0216-105">The following procedure uses recursion to calculate the factorial of its original argument.</span></span>  
  
 [!code-vb[VbVbcnProcedures#51](./codesnippet/VisualBasic/recursive-procedures_1.vb)]  
  
## <a name="considerations-with-recursive-procedures"></a><span data-ttu-id="a0216-106">再帰プロシージャに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="a0216-106">Considerations with Recursive Procedures</span></span>  
 <span data-ttu-id="a0216-107">**制限条件**します。</span><span class="sxs-lookup"><span data-stu-id="a0216-107">**Limiting Conditions**.</span></span> <span data-ttu-id="a0216-108">再帰処理を終了するには少なくとも 1 つの条件をテストする再帰的な手順を設計する必要があり、妥当な数の再帰呼び出し内でこのような条件が満たされていないケースを処理することも必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0216-108">You must design a recursive procedure to test for at least one condition that can terminate the recursion, and you must also handle the case where no such condition is satisfied within a reasonable number of recursive calls.</span></span> <span data-ttu-id="a0216-109">失敗せずに満たすことが少なくとも 1 つの条件がない、プロシージャを実行する可能性が高く無限ループで実行します。</span><span class="sxs-lookup"><span data-stu-id="a0216-109">Without at least one condition that can be met without fail, your procedure runs a high risk of executing in an infinite loop.</span></span>  
  
 <span data-ttu-id="a0216-110">**メモリ使用状況**。</span><span class="sxs-lookup"><span data-stu-id="a0216-110">**Memory Usage**.</span></span> <span data-ttu-id="a0216-111">アプリケーションが、ローカル変数の領域量が制限されています。</span><span class="sxs-lookup"><span data-stu-id="a0216-111">Your application has a limited amount of space for local variables.</span></span> <span data-ttu-id="a0216-112">プロシージャが、それ自体を呼び出すたびに、ローカル変数の追加のコピーの領域を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0216-112">Each time a procedure calls itself, it uses more of that space for additional copies of its local variables.</span></span> <span data-ttu-id="a0216-113">最終的と、このプロセスが無期限に解決しない場合は、<xref:System.StackOverflowException>エラー。</span><span class="sxs-lookup"><span data-stu-id="a0216-113">If this process continues indefinitely, it eventually causes a <xref:System.StackOverflowException> error.</span></span>  
  
 <span data-ttu-id="a0216-114">**効率**します。</span><span class="sxs-lookup"><span data-stu-id="a0216-114">**Efficiency**.</span></span> <span data-ttu-id="a0216-115">ほとんどの場合に、再帰はループを置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="a0216-115">You can almost always substitute a loop for recursion.</span></span> <span data-ttu-id="a0216-116">ループでは、引数の受け渡し、追加のストレージを初期化し、値を返すのオーバーヘッドはありません。</span><span class="sxs-lookup"><span data-stu-id="a0216-116">A loop does not have the overhead of passing arguments, initializing additional storage, and returning values.</span></span> <span data-ttu-id="a0216-117">パフォーマンスは、再帰的な呼び出しなしの方があります。</span><span class="sxs-lookup"><span data-stu-id="a0216-117">Your performance can be much better without recursive calls.</span></span>  
  
 <span data-ttu-id="a0216-118">**相互再帰**します。</span><span class="sxs-lookup"><span data-stu-id="a0216-118">**Mutual Recursion**.</span></span> <span data-ttu-id="a0216-119">2 つの手順では、互いを呼び出す場合、パフォーマンスが大きく低下、または、無限ループでもを確認する場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0216-119">You might observe very poor performance, or even an infinite loop, if two procedures call each other.</span></span> <span data-ttu-id="a0216-120">このような設計は、1 つの再帰プロシージャと同じ問題を提示しますが、検出およびデバッグが困難になることができます。</span><span class="sxs-lookup"><span data-stu-id="a0216-120">Such a design presents the same problems as a single recursive procedure, but can be harder to detect and debug.</span></span>  
  
 <span data-ttu-id="a0216-121">**かっこで囲んで呼び出す**します。</span><span class="sxs-lookup"><span data-stu-id="a0216-121">**Calling with Parentheses**.</span></span> <span data-ttu-id="a0216-122">ときに、`Function`プロシージャを呼び出す再帰的に、引数リストがない場合でも、プロシージャ名、かっこを従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0216-122">When a `Function` procedure calls itself recursively, you must follow the procedure name with parentheses, even if there is no argument list.</span></span> <span data-ttu-id="a0216-123">関数名を取得する場合は、関数の戻り値を表すとします。</span><span class="sxs-lookup"><span data-stu-id="a0216-123">Otherwise, the function name is taken as representing the return value of the function.</span></span>  
  
 <span data-ttu-id="a0216-124">**テスト**します。</span><span class="sxs-lookup"><span data-stu-id="a0216-124">**Testing**.</span></span> <span data-ttu-id="a0216-125">再帰プロシージャを記述する場合はいくつかの制限の条件を満たしているかどうかを確認する非常に慎重にテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0216-125">If you write a recursive procedure, you should test it very carefully to make sure it always meets some limiting condition.</span></span> <span data-ttu-id="a0216-126">再帰の呼び出しが多すぎるため、メモリ不足が実行できないということを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0216-126">You should also ensure that you cannot run out of memory due to having too many recursive calls.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0216-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0216-127">See Also</span></span>  
 <xref:System.StackOverflowException>  
 [<span data-ttu-id="a0216-128">手順</span><span class="sxs-lookup"><span data-stu-id="a0216-128">Procedures</span></span>](./index.md)  
 [<span data-ttu-id="a0216-129">Sub プロシージャ</span><span class="sxs-lookup"><span data-stu-id="a0216-129">Sub Procedures</span></span>](./sub-procedures.md)  
 [<span data-ttu-id="a0216-130">Function プロシージャ</span><span class="sxs-lookup"><span data-stu-id="a0216-130">Function Procedures</span></span>](./function-procedures.md)  
 [<span data-ttu-id="a0216-131">Property プロシージャ</span><span class="sxs-lookup"><span data-stu-id="a0216-131">Property Procedures</span></span>](./property-procedures.md)  
 [<span data-ttu-id="a0216-132">演算子プロシージャ</span><span class="sxs-lookup"><span data-stu-id="a0216-132">Operator Procedures</span></span>](./operator-procedures.md)  
 [<span data-ttu-id="a0216-133">プロシージャのパラメーターと引数</span><span class="sxs-lookup"><span data-stu-id="a0216-133">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)  
 [<span data-ttu-id="a0216-134">プロシージャのオーバーロード</span><span class="sxs-lookup"><span data-stu-id="a0216-134">Procedure Overloading</span></span>](./procedure-overloading.md)  
 [<span data-ttu-id="a0216-135">プロシージャのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a0216-135">Troubleshooting Procedures</span></span>](./troubleshooting-procedures.md)  
 [<span data-ttu-id="a0216-136">ループ構造</span><span class="sxs-lookup"><span data-stu-id="a0216-136">Loop Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)  
 [<span data-ttu-id="a0216-137">例外のトラブルシューティング : System.StackOverflowException</span><span class="sxs-lookup"><span data-stu-id="a0216-137">Troubleshooting Exceptions: System.StackOverflowException</span></span>](https://msdn.microsoft.com/library/51b71217-c507-4f5b-bc35-0236180d7968)
