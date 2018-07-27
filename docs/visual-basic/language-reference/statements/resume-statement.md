---
title: Resume ステートメント (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Resume
- vb.ResumeNext
helpviewer_keywords:
- Next statement [Visual Basic], Resume
- Resume Next statement [Visual Basic]
- execution [Visual Basic], resuming
- run-time errors [Visual Basic], resuming after
- Resume statement [Visual Basic], syntax
- errors [Visual Basic], resuming after
- Error statement [Visual Basic], and Resume statement
- execution
- Resume statement [Visual Basic]
ms.assetid: e24d058b-1a5c-4274-acb9-7d295d3ea537
ms.openlocfilehash: 853f3fe060b70c8a43957d3c843fb95539981679
ms.sourcegitcommit: 70c76a12449439bac0f7a359866be5a0311ce960
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/27/2018
ms.locfileid: "39296157"
---
# <a name="resume-statement"></a><span data-ttu-id="189b9-102">Resume ステートメント</span><span class="sxs-lookup"><span data-stu-id="189b9-102">Resume Statement</span></span>
<span data-ttu-id="189b9-103">エラー処理ルーチンを完了した後は、実行を再開します。</span><span class="sxs-lookup"><span data-stu-id="189b9-103">Resumes execution after an error-handling routine is finished.</span></span>  
  
 <span data-ttu-id="189b9-104">非構造化例外処理を使用するのではなく、可能であれば、コード内の構造化例外処理を使用することをお勧め、`On Error`と`Resume`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="189b9-104">We suggest that you use structured exception handling in your code whenever possible, rather than using unstructured exception handling and the `On Error` and `Resume` statements.</span></span> <span data-ttu-id="189b9-105">詳しくは、「[Try...Catch...Finally ステートメント](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="189b9-105">For more information, see [Try...Catch...Finally Statement](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="189b9-106">構文</span><span class="sxs-lookup"><span data-stu-id="189b9-106">Syntax</span></span>  
  
```  
Resume [ Next | line ]  
```  
  
## <a name="parts"></a><span data-ttu-id="189b9-107">指定項目</span><span class="sxs-lookup"><span data-stu-id="189b9-107">Parts</span></span>  
 `Resume`  
 <span data-ttu-id="189b9-108">必須。</span><span class="sxs-lookup"><span data-stu-id="189b9-108">Required.</span></span> <span data-ttu-id="189b9-109">エラー ハンドラーと同じ手順でエラーが発生した場合、エラーの原因となったステートメントを使用して実行を再開します。</span><span class="sxs-lookup"><span data-stu-id="189b9-109">If the error occurred in the same procedure as the error handler, execution resumes with the statement that caused the error.</span></span> <span data-ttu-id="189b9-110">呼び出されたプロシージャでエラーが発生した場合は、最後に、エラー処理ルーチンを含むプロシージャから呼び出されたステートメントの実行が再開されます。</span><span class="sxs-lookup"><span data-stu-id="189b9-110">If the error occurred in a called procedure, execution resumes at the statement that last called out of the procedure containing the error-handling routine.</span></span>  
  
 `Next`  
 <span data-ttu-id="189b9-111">任意。</span><span class="sxs-lookup"><span data-stu-id="189b9-111">Optional.</span></span> <span data-ttu-id="189b9-112">エラー ハンドラーと同じ手順でエラーが発生した場合、エラーの原因となったステートメントの直後のステートメントの実行が再開されます。</span><span class="sxs-lookup"><span data-stu-id="189b9-112">If the error occurred in the same procedure as the error handler, execution resumes with the statement immediately following the statement that caused the error.</span></span> <span data-ttu-id="189b9-113">最後に、エラー処理ルーチンを含むプロシージャから呼び出されたステートメントの直後のステートメントの実行が再開される呼び出されたプロシージャでエラーが発生した場合 (または`On Error Resume Next`ステートメント)。</span><span class="sxs-lookup"><span data-stu-id="189b9-113">If the error occurred in a called procedure, execution resumes with the statement immediately following the statement that last called out of the procedure containing the error-handling routine (or `On Error Resume Next` statement).</span></span>  
  
 `line`  
 <span data-ttu-id="189b9-114">任意。</span><span class="sxs-lookup"><span data-stu-id="189b9-114">Optional.</span></span> <span data-ttu-id="189b9-115">要求で指定した行で実行が再開される`line`引数。</span><span class="sxs-lookup"><span data-stu-id="189b9-115">Execution resumes at the line specified in the required `line` argument.</span></span> <span data-ttu-id="189b9-116">`line`引数を行ラベルまたは行番号、エラー ハンドラーと同じ手順である必要があります。</span><span class="sxs-lookup"><span data-stu-id="189b9-116">The `line` argument is a line label or line number and must be in the same procedure as the error handler.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="189b9-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="189b9-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="189b9-118">非構造化例外処理を使用するのではなく、可能であれば、コード内の構造化例外処理を使用することをお勧め、`On Error`と`Resume`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="189b9-118">We recommend that you use structured exception handling in your code whenever possible, rather than using unstructured exception handling and the `On Error` and `Resume` statements.</span></span> <span data-ttu-id="189b9-119">詳しくは、「[Try...Catch...Finally ステートメント](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="189b9-119">For more information, see [Try...Catch...Finally Statement](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).</span></span>  
  
 <span data-ttu-id="189b9-120">使用する場合、`Resume`ステートメント任意の場所以外のエラー処理ルーチンで、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="189b9-120">If you use a `Resume` statement anywhere other than in an error-handling routine, an error occurs.</span></span>  
  
 <span data-ttu-id="189b9-121">`Resume`を含むすべてのプロシージャでは、ステートメントを使用できません、`Try...Catch...Finally`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="189b9-121">The `Resume` statement cannot be used in any procedure that contains a `Try...Catch...Finally` statement.</span></span>  
  
## <a name="example"></a><span data-ttu-id="189b9-122">例</span><span class="sxs-lookup"><span data-stu-id="189b9-122">Example</span></span>  
 <span data-ttu-id="189b9-123">この例では、`Resume`ステートメントをプロシージャのエラー処理を終了し、エラーの原因となったステートメントの実行を再開します。</span><span class="sxs-lookup"><span data-stu-id="189b9-123">This example uses the `Resume` statement to end error handling in a procedure and then resume execution with the statement that caused the error.</span></span> <span data-ttu-id="189b9-124">使用方法を説明するエラー番号 55 が生成された、`Resume`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="189b9-124">Error number 55 is generated to illustrate use of the `Resume` statement.</span></span>  
  
 [!code-vb[VbVbalrErrorHandling#16](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/resume-statement_1.vb)]  
  
## <a name="requirements"></a><span data-ttu-id="189b9-125">必要条件</span><span class="sxs-lookup"><span data-stu-id="189b9-125">Requirements</span></span>  
 <span data-ttu-id="189b9-126">**Namespace:** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)</span><span class="sxs-lookup"><span data-stu-id="189b9-126">**Namespace:** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)</span></span>  
  
 <span data-ttu-id="189b9-127">**アセンブリ:** Visual Basic ランタイム ライブラリ (Microsoft.VisualBasic.dll)</span><span class="sxs-lookup"><span data-stu-id="189b9-127">**Assembly:** Visual Basic Runtime Library (in Microsoft.VisualBasic.dll)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="189b9-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="189b9-128">See Also</span></span>  
 [<span data-ttu-id="189b9-129">Try...Catch...Finally ステートメント</span><span class="sxs-lookup"><span data-stu-id="189b9-129">Try...Catch...Finally Statement</span></span>](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)  
 [<span data-ttu-id="189b9-130">Error ステートメント</span><span class="sxs-lookup"><span data-stu-id="189b9-130">Error Statement</span></span>](../../../visual-basic/language-reference/statements/error-statement.md)  
 [<span data-ttu-id="189b9-131">On Error ステートメント</span><span class="sxs-lookup"><span data-stu-id="189b9-131">On Error Statement</span></span>](../../../visual-basic/language-reference/statements/on-error-statement.md)
