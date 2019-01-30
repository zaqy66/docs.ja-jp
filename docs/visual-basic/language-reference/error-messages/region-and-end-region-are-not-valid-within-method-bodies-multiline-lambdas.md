---
title: "'#Region' および ' #End Region' ステートメントはメソッド本体や複数行ラムダ内では有効ではありません。"
ms.date: 07/20/2015
f1_keywords:
- bc32025
- vbc32025
helpviewer_keywords:
- BC32025
ms.assetid: 43707bf1-1c6b-4d82-b081-e5a17dca51c1
ms.openlocfilehash: 2a2f5692518c6784dfc6e3be6302f1e8dcf2aaa7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55265572"
---
# <a name="region-and-end-region-statements-are-not-valid-within-method-bodiesmultiline-lambdas"></a><span data-ttu-id="a74ad-102">'#Region' および '#End Region' ステートメントは、メソッド本体や複数行ラムダの内部では有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="a74ad-102">'#Region' and '#End Region' statements are not valid within method bodies/multiline lambdas</span></span>
<span data-ttu-id="a74ad-103">`#Region`ブロックは、クラス、モジュール、または名前空間レベルで宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a74ad-103">The `#Region` block must be declared at a class, module, or namespace level.</span></span> <span data-ttu-id="a74ad-104">折りたたみ可能な領域は、1 つ以上のプロシージャを含めることができますが、開始またはプロシージャの内部で終了することはできません。</span><span class="sxs-lookup"><span data-stu-id="a74ad-104">A collapsible region can include one or more procedures, but it cannot begin or end inside of a procedure.</span></span>  
  
 <span data-ttu-id="a74ad-105">**エラー ID:** BC32025</span><span class="sxs-lookup"><span data-stu-id="a74ad-105">**Error ID:** BC32025</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a74ad-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="a74ad-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="a74ad-107">前の手順が正しくで終了することを確認、`End Function`または`End Sub`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="a74ad-107">Ensure that the preceding procedure is properly terminated with an `End Function` or `End Sub` statement.</span></span>  
  
2.  <span data-ttu-id="a74ad-108">いることを確認、`#Region`と`#End Region`ディレクティブは、同じコード ブロックにします。</span><span class="sxs-lookup"><span data-stu-id="a74ad-108">Ensure that the `#Region` and `#End Region` directives are in the same code block.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a74ad-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="a74ad-109">See also</span></span>
- [<span data-ttu-id="a74ad-110">#Region ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="a74ad-110">#Region Directive</span></span>](../../../visual-basic/language-reference/directives/region-directive.md)
