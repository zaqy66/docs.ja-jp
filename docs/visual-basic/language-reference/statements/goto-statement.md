---
title: GoTo ステートメント (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.GoTo
helpviewer_keywords:
- GoTo statement [Visual Basic]
- control flow [Visual Basic], branching
- unconditional branching [Visual Basic]
- branching [Visual Basic]
- branching [Visual Basic], unconditional
- branching [Visual Basic], conditional
- conditional statements [Visual Basic], GoTo statement
- GoTo statement [Visual Basic], syntax
ms.assetid: 313274c2-8ab3-4b9c-9ba3-0fd6798e4f6d
ms.openlocfilehash: adb7668b6a818b2042a38f9458685a6f93085dc8
ms.sourcegitcommit: 869b5832b667915ac4a5dd8c86b1109ed26b6c08
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/28/2018
ms.locfileid: "39332988"
---
# <a name="goto-statement"></a><span data-ttu-id="79c70-102">GoTo ステートメント</span><span class="sxs-lookup"><span data-stu-id="79c70-102">GoTo Statement</span></span>
<span data-ttu-id="79c70-103">プロシージャ内の指定した行に無条件に分岐します。</span><span class="sxs-lookup"><span data-stu-id="79c70-103">Branches unconditionally to a specified line in a procedure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79c70-104">構文</span><span class="sxs-lookup"><span data-stu-id="79c70-104">Syntax</span></span>  
  
```  
GoTo line  
```  
  
## <a name="part"></a><span data-ttu-id="79c70-105">パーツ</span><span class="sxs-lookup"><span data-stu-id="79c70-105">Part</span></span>  
 `line`  
 <span data-ttu-id="79c70-106">必須。</span><span class="sxs-lookup"><span data-stu-id="79c70-106">Required.</span></span> <span data-ttu-id="79c70-107">任意の行のラベル。</span><span class="sxs-lookup"><span data-stu-id="79c70-107">Any line label.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="79c70-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="79c70-108">Remarks</span></span>  
 <span data-ttu-id="79c70-109">`GoTo`のみが表示されるプロシージャ内の行にステートメントを分岐できます。</span><span class="sxs-lookup"><span data-stu-id="79c70-109">The `GoTo` statement can branch only to lines in the procedure in which it appears.</span></span> <span data-ttu-id="79c70-110">ラベルを 1 行が必要`GoTo`を参照できます。</span><span class="sxs-lookup"><span data-stu-id="79c70-110">The line must have a line label that `GoTo` can refer to.</span></span> <span data-ttu-id="79c70-111">詳細については、次を参照してください。[方法: ラベル ステートメント](../../../visual-basic/programming-guide/program-structure/how-to-label-statements.md)します。</span><span class="sxs-lookup"><span data-stu-id="79c70-111">For more information, see [How to: Label Statements](../../../visual-basic/programming-guide/program-structure/how-to-label-statements.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="79c70-112">`GoTo` ステートメントすると、コードが読み取りおよびメンテナンスを困難になります。</span><span class="sxs-lookup"><span data-stu-id="79c70-112">`GoTo` statements can make code difficult to read and maintain.</span></span> <span data-ttu-id="79c70-113">可能であれば、制御構造を使用します。</span><span class="sxs-lookup"><span data-stu-id="79c70-113">Whenever possible, use a control structure instead.</span></span> <span data-ttu-id="79c70-114">詳細については、次を参照してください。[制御フロー](../../../visual-basic/programming-guide/language-features/control-flow/index.md)します。</span><span class="sxs-lookup"><span data-stu-id="79c70-114">For more information, see [Control Flow](../../../visual-basic/programming-guide/language-features/control-flow/index.md).</span></span>  
  
 <span data-ttu-id="79c70-115">使用することはできません、`GoTo`外からの分岐にステートメントを`For`.`Next`, `For Each`...`Next`, `SyncLock`...`End SyncLock`, `Try`...`Catch`...`Finally`, `With`...`End With`、または`Using`.`End Using`内のラベルに構築します。</span><span class="sxs-lookup"><span data-stu-id="79c70-115">You cannot use a `GoTo` statement to branch from outside a `For`...`Next`, `For Each`...`Next`, `SyncLock`...`End SyncLock`, `Try`...`Catch`...`Finally`, `With`...`End With`, or `Using`...`End Using` construction to a label inside.</span></span>  
  
## <a name="branching-and-try-constructions"></a><span data-ttu-id="79c70-116">分岐と構築をお試しください</span><span class="sxs-lookup"><span data-stu-id="79c70-116">Branching and Try Constructions</span></span>  
 <span data-ttu-id="79c70-117">内で、 `Try`.`Catch`...`Finally`で分岐に、構築、次の規則の適用、`GoTo`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="79c70-117">Within a `Try`...`Catch`...`Finally` construction, the following rules apply to branching with the `GoTo` statement.</span></span>  
  
|<span data-ttu-id="79c70-118">ブロックまたは地域</span><span class="sxs-lookup"><span data-stu-id="79c70-118">Block or region</span></span>|<span data-ttu-id="79c70-119">外部からへの分岐</span><span class="sxs-lookup"><span data-stu-id="79c70-119">Branching in from outside</span></span>|<span data-ttu-id="79c70-120">外部への分岐からの内部</span><span class="sxs-lookup"><span data-stu-id="79c70-120">Branching out from inside</span></span>|  
|---------------------|-------------------------------|-------------------------------|  
|<span data-ttu-id="79c70-121">`Try` ブロック</span><span class="sxs-lookup"><span data-stu-id="79c70-121">`Try` block</span></span>|<span data-ttu-id="79c70-122">のみ、`Catch`同じ構築ブロック<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="79c70-122">Only from a `Catch` block of the same construction <sup>1</sup></span></span>|<span data-ttu-id="79c70-123">のみ、全体の構造の外部</span><span class="sxs-lookup"><span data-stu-id="79c70-123">Only to outside the whole construction</span></span>|  
|<span data-ttu-id="79c70-124">`Catch` ブロック</span><span class="sxs-lookup"><span data-stu-id="79c70-124">`Catch` block</span></span>|<span data-ttu-id="79c70-125">許可しません。</span><span class="sxs-lookup"><span data-stu-id="79c70-125">Never allowed</span></span>|<span data-ttu-id="79c70-126">のみ、全体の構造の外部にまたは、`Try`同じ構築ブロック<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="79c70-126">Only to outside the whole construction, or to the `Try` block of the same construction <sup>1</sup></span></span>|  
|<span data-ttu-id="79c70-127">`Finally` ブロック</span><span class="sxs-lookup"><span data-stu-id="79c70-127">`Finally` block</span></span>|<span data-ttu-id="79c70-128">許可しません。</span><span class="sxs-lookup"><span data-stu-id="79c70-128">Never allowed</span></span>|<span data-ttu-id="79c70-129">許可しません。</span><span class="sxs-lookup"><span data-stu-id="79c70-129">Never allowed</span></span>|  
  
 <span data-ttu-id="79c70-130"><sup>1</sup>場合`Try`.`Catch`...`Finally`構築が、別の入れ子になった、`Catch`ブロックに分岐、`Try`ブロックの他にコピーせずに、独自の入れ子のレベルにある`Try`ブロックします。</span><span class="sxs-lookup"><span data-stu-id="79c70-130"><sup>1</sup> If one `Try`...`Catch`...`Finally` construction is nested within another, a `Catch` block can branch into the `Try` block at its own nesting level, but not into any other `Try` block.</span></span> <span data-ttu-id="79c70-131">入れ子になった`Try`.`Catch`...`Finally`構築を完全に含める必要があります、`Try`または`Catch`ブロックを入れ子になってを作成します。</span><span class="sxs-lookup"><span data-stu-id="79c70-131">A nested `Try`...`Catch`...`Finally` construction must be contained completely in a `Try` or `Catch` block of the construction within which it is nested.</span></span>  
  
 <span data-ttu-id="79c70-132">次の図では 1 つ`Try`別内で入れ子になった構築します。</span><span class="sxs-lookup"><span data-stu-id="79c70-132">The following illustration shows one `Try` construction nested within another.</span></span> <span data-ttu-id="79c70-133">2 つの構築ブロック間でさまざまな分岐は、有効または無効と表示されています。</span><span class="sxs-lookup"><span data-stu-id="79c70-133">Various branches among the blocks of the two constructions are indicated as valid or invalid.</span></span>  
  
 <span data-ttu-id="79c70-134">![Try 構造内の分岐のグラフィック ダイアグラム](../../../visual-basic/language-reference/statements/media/trybranching.gif "TryBranching")</span><span class="sxs-lookup"><span data-stu-id="79c70-134">![Graphic diagram of branching in Try constructions](../../../visual-basic/language-reference/statements/media/trybranching.gif "TryBranching")</span></span>  
<span data-ttu-id="79c70-135">Try 構造内の有効および無効な分岐</span><span class="sxs-lookup"><span data-stu-id="79c70-135">Valid and invalid branches in Try constructions</span></span>  
  
## <a name="example"></a><span data-ttu-id="79c70-136">例</span><span class="sxs-lookup"><span data-stu-id="79c70-136">Example</span></span>  
 <span data-ttu-id="79c70-137">次の例では、`GoTo`ステートメントをプロシージャ内の行ラベルに分岐します。</span><span class="sxs-lookup"><span data-stu-id="79c70-137">The following example uses the `GoTo` statement to branch to line labels in a procedure.</span></span>  
  
 [!code-vb[VbVbalrStatements#31](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/goto-statement_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="79c70-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="79c70-138">See Also</span></span>  
 [<span data-ttu-id="79c70-139">Do...Loop ステートメント</span><span class="sxs-lookup"><span data-stu-id="79c70-139">Do...Loop Statement</span></span>](../../../visual-basic/language-reference/statements/do-loop-statement.md)  
 [<span data-ttu-id="79c70-140">For...Next ステートメント</span><span class="sxs-lookup"><span data-stu-id="79c70-140">For...Next Statement</span></span>](../../../visual-basic/language-reference/statements/for-next-statement.md)  
 [<span data-ttu-id="79c70-141">For Each...Next ステートメント</span><span class="sxs-lookup"><span data-stu-id="79c70-141">For Each...Next Statement</span></span>](../../../visual-basic/language-reference/statements/for-each-next-statement.md)  
 [<span data-ttu-id="79c70-142">If...Then...Else ステートメント</span><span class="sxs-lookup"><span data-stu-id="79c70-142">If...Then...Else Statement</span></span>](../../../visual-basic/language-reference/statements/if-then-else-statement.md)  
 [<span data-ttu-id="79c70-143">Select...Case ステートメント</span><span class="sxs-lookup"><span data-stu-id="79c70-143">Select...Case Statement</span></span>](../../../visual-basic/language-reference/statements/select-case-statement.md)  
 [<span data-ttu-id="79c70-144">Try...Catch...Finally ステートメント</span><span class="sxs-lookup"><span data-stu-id="79c70-144">Try...Catch...Finally Statement</span></span>](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)  
 [<span data-ttu-id="79c70-145">While...End While ステートメント</span><span class="sxs-lookup"><span data-stu-id="79c70-145">While...End While Statement</span></span>](../../../visual-basic/language-reference/statements/while-end-while-statement.md)  
 [<span data-ttu-id="79c70-146">With...End With ステートメント</span><span class="sxs-lookup"><span data-stu-id="79c70-146">With...End With Statement</span></span>](../../../visual-basic/language-reference/statements/with-end-with-statement.md)
