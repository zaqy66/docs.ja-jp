---
title: '&#39;#Region&#39;と&#39;#End Region&#39;ステートメントがメソッド本体や複数行ラムダ内では有効ではありません。'
ms.date: 07/20/2015
f1_keywords:
- bc32025
- vbc32025
helpviewer_keywords:
- BC32025
ms.assetid: 43707bf1-1c6b-4d82-b081-e5a17dca51c1
ms.openlocfilehash: 55399cd123ce4d67cc833f2eabe3230acdafc0bf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54737216"
---
# <a name="39region39-and-39end-region39-statements-are-not-valid-within-method-bodiesmultiline-lambdas"></a><span data-ttu-id="0522a-102">&#39;#Region&#39;と&#39;#End Region&#39;ステートメントがメソッド本体や複数行ラムダ内では有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="0522a-102">&#39;#Region&#39; and &#39;#End Region&#39; statements are not valid within method bodies/multiline lambdas</span></span>
<span data-ttu-id="0522a-103">`#Region`ブロックは、クラス、モジュール、または名前空間レベルで宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0522a-103">The `#Region` block must be declared at a class, module, or namespace level.</span></span> <span data-ttu-id="0522a-104">折りたたみ可能な領域は、1 つ以上のプロシージャを含めることができますが、開始またはプロシージャの内部で終了することはできません。</span><span class="sxs-lookup"><span data-stu-id="0522a-104">A collapsible region can include one or more procedures, but it cannot begin or end inside of a procedure.</span></span>  
  
 <span data-ttu-id="0522a-105">**エラー ID:** BC32025</span><span class="sxs-lookup"><span data-stu-id="0522a-105">**Error ID:** BC32025</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="0522a-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="0522a-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="0522a-107">前の手順が正しくで終了することを確認、`End Function`または`End Sub`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="0522a-107">Ensure that the preceding procedure is properly terminated with an `End Function` or `End Sub` statement.</span></span>  
  
2.  <span data-ttu-id="0522a-108">いることを確認、`#Region`と`#End Region`ディレクティブは、同じコード ブロックにします。</span><span class="sxs-lookup"><span data-stu-id="0522a-108">Ensure that the `#Region` and `#End Region` directives are in the same code block.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0522a-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="0522a-109">See also</span></span>
- [<span data-ttu-id="0522a-110">#Region ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="0522a-110">#Region Directive</span></span>](../../../visual-basic/language-reference/directives/region-directive.md)
