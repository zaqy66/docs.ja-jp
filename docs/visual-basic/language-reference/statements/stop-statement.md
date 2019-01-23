---
title: Stop ステートメント (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Stop
helpviewer_keywords:
- breakpoints, Stop statements
- Stop statements [Visual Basic], syntax
- Stop statements [Visual Basic]
- execution [Visual Basic], suspending
- processing, interrupting
- processes, interrupting
- execution [Visual Basic], stopping
ms.assetid: c9a9fde0-d649-4662-9bef-bd0146ebc2a7
ms.openlocfilehash: fa9a1942903dff6f673d87b67ebcad047a410425
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624783"
---
# <a name="stop-statement-visual-basic"></a><span data-ttu-id="b02e4-102">Stop ステートメント (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b02e4-102">Stop Statement (Visual Basic)</span></span>
<span data-ttu-id="b02e4-103">実行を中断します。</span><span class="sxs-lookup"><span data-stu-id="b02e4-103">Suspends execution.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b02e4-104">構文</span><span class="sxs-lookup"><span data-stu-id="b02e4-104">Syntax</span></span>  
  
```  
Stop  
```  
  
## <a name="remarks"></a><span data-ttu-id="b02e4-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="b02e4-105">Remarks</span></span>  
 <span data-ttu-id="b02e4-106">配置できる`Stop`ステートメントの実行を中断する手順で任意の場所。</span><span class="sxs-lookup"><span data-stu-id="b02e4-106">You can place `Stop` statements anywhere in procedures to suspend execution.</span></span> <span data-ttu-id="b02e4-107">使用して、`Stop`ステートメントは、コード内のブレークポイントの設定に似ています。</span><span class="sxs-lookup"><span data-stu-id="b02e4-107">Using the `Stop` statement is similar to setting a breakpoint in the code.</span></span>  
  
 <span data-ttu-id="b02e4-108">`Stop`ステートメントのとは異なり、実行を中断`End`、すべてのファイルを終了したり、コンパイル済み実行可能 (.exe) ファイルで検出された場合を除き、任意の変数をクリアしません。</span><span class="sxs-lookup"><span data-stu-id="b02e4-108">The `Stop` statement suspends execution, but unlike `End`, it does not close any files or clear any variables, unless it is encountered in a compiled executable (.exe) file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b02e4-109">場合、`Stop`統合開発環境 (IDE) の外部で実行されているコードのステートメントが検出された場合、デバッガーが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b02e4-109">If the `Stop` statement is encountered in code that is running outside of the integrated development environment (IDE), the debugger is invoked.</span></span> <span data-ttu-id="b02e4-110">これは、コードがデバッグ、または製品のモードでコンパイルするかどうかに関係なく当てはまります。</span><span class="sxs-lookup"><span data-stu-id="b02e4-110">This is true regardless of whether the code was compiled in debug or retail mode.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b02e4-111">例</span><span class="sxs-lookup"><span data-stu-id="b02e4-111">Example</span></span>  
 <span data-ttu-id="b02e4-112">この例では、`Stop`ステートメント内の各繰り返しの実行を中断、`For...Next`ループします。</span><span class="sxs-lookup"><span data-stu-id="b02e4-112">This example uses the `Stop` statement to suspend execution for each iteration through the `For...Next` loop.</span></span>  
  
 [!code-vb[VbVbalrStatements#56](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/stop-statement_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="b02e4-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="b02e4-113">See also</span></span>
- [<span data-ttu-id="b02e4-114">End ステートメント</span><span class="sxs-lookup"><span data-stu-id="b02e4-114">End Statement</span></span>](../../../visual-basic/language-reference/statements/end-statement.md)
