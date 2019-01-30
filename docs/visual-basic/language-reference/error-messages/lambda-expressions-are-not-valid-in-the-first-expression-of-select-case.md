---
title: ラムダ式は、'Select Case' ステートメントの最初の式では有効ではありません
ms.date: 07/20/2015
f1_keywords:
- bc36635
- vbc36635
helpviewer_keywords:
- BC36635
ms.assetid: 74609979-9c03-4864-bbce-f588aa2e0917
ms.openlocfilehash: d56515093020a4c987d132491957ce6db9e21683
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55287795"
---
# <a name="lambda-expressions-are-not-valid-in-the-first-expression-of-a-select-case-statement"></a><span data-ttu-id="db4d0-102">ラムダ式は、'Select Case' ステートメントの最初の式では有効ではありません</span><span class="sxs-lookup"><span data-stu-id="db4d0-102">Lambda expressions are not valid in the first expression of a 'Select Case' statement</span></span>
<span data-ttu-id="db4d0-103">テスト式でのラムダ式を使用することはできません、`Select Case`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="db4d0-103">You cannot use a lambda expression for the test expression in a `Select Case` statement.</span></span> <span data-ttu-id="db4d0-104">ラムダ式の定義は、関数、およびのテスト式を返す、`Select Case`ステートメントは、基本データ型である必要があります。</span><span class="sxs-lookup"><span data-stu-id="db4d0-104">Lambda expression definitions return functions, and the test expression of a `Select Case` statement must be an elementary data type.</span></span>  
  
 <span data-ttu-id="db4d0-105">次のコードでは、このエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="db4d0-105">The following code causes this error:</span></span>  
  
```vb  
' Select Case (Function(arg) arg Is Nothing)  
    ' List of the cases.  
' End Select  
```  
  
 <span data-ttu-id="db4d0-106">**エラー ID:** BC36635</span><span class="sxs-lookup"><span data-stu-id="db4d0-106">**Error ID:** BC36635</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="db4d0-107">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="db4d0-107">To correct this error</span></span>  
  
-   <span data-ttu-id="db4d0-108">コードを調べて、 `If...Then...Else` ステートメントなどの別の条件構造を使用できないかをご確認ください。</span><span class="sxs-lookup"><span data-stu-id="db4d0-108">Examine your code to determine whether a different conditional construction, such as an `If...Then...Else` statement, would work for you.</span></span>  
  
-   <span data-ttu-id="db4d0-109">指定した、関数を呼び出す次のコードに示すように。</span><span class="sxs-lookup"><span data-stu-id="db4d0-109">You may have intended to call the function, as shown in the following code:</span></span>  
  
```vb  
Dim num? As Integer  
Select Case ((Function(arg? As Integer) arg Is Nothing)(num))  
    ' List of the cases  
End Select  
```  
  
## <a name="see-also"></a><span data-ttu-id="db4d0-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="db4d0-110">See also</span></span>
- [<span data-ttu-id="db4d0-111">ラムダ式</span><span class="sxs-lookup"><span data-stu-id="db4d0-111">Lambda Expressions</span></span>](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [<span data-ttu-id="db4d0-112">If...Then...Else ステートメント</span><span class="sxs-lookup"><span data-stu-id="db4d0-112">If...Then...Else Statement</span></span>](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
- [<span data-ttu-id="db4d0-113">Select...Case ステートメント</span><span class="sxs-lookup"><span data-stu-id="db4d0-113">Select...Case Statement</span></span>](../../../visual-basic/language-reference/statements/select-case-statement.md)
