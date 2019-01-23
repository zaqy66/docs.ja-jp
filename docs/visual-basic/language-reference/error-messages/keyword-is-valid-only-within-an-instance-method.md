---
title: '&#39;&lt;keyword&gt;&#39;は、インスタンス メソッド内でのみ有効です。'
ms.date: 07/20/2015
f1_keywords:
- bc30043
- vbc30043
helpviewer_keywords:
- BC30043
ms.assetid: 7973aa82-a681-440c-9bca-242627d7ba86
ms.openlocfilehash: a464a059aa2d13e3472b9770960384b6be398092
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54595943"
---
# <a name="39ltkeywordgt39-is-valid-only-within-an-instance-method"></a><span data-ttu-id="2615f-102">&#39;&lt;keyword&gt;&#39;は、インスタンス メソッド内でのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="2615f-102">&#39;&lt;keyword&gt;&#39; is valid only within an instance method</span></span>
<span data-ttu-id="2615f-103">`Me`、 `MyClass`、および`MyBase`キーワードは、特定のクラスのインスタンスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2615f-103">The `Me`, `MyClass`, and `MyBase` keywords refer to specific class instances.</span></span> <span data-ttu-id="2615f-104">共有内で使用することはできません`Function`または`Sub`プロシージャ。</span><span class="sxs-lookup"><span data-stu-id="2615f-104">You cannot use them inside a shared `Function` or `Sub` procedure.</span></span>  
  
 <span data-ttu-id="2615f-105">**エラー ID:** BC30043</span><span class="sxs-lookup"><span data-stu-id="2615f-105">**Error ID:** BC30043</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="2615f-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="2615f-106">To correct this error</span></span>  
  
-   <span data-ttu-id="2615f-107">プロシージャからキーワードを削除または削除、`Shared`プロシージャ宣言からキーワード。</span><span class="sxs-lookup"><span data-stu-id="2615f-107">Remove the keyword from the procedure, or remove the `Shared` keyword from the procedure declaration.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2615f-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="2615f-108">See also</span></span>
- [<span data-ttu-id="2615f-109">オブジェクト変数の代入</span><span class="sxs-lookup"><span data-stu-id="2615f-109">Object Variable Assignment</span></span>](../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)
- [<span data-ttu-id="2615f-110">Me、My、MyBase、および MyClass</span><span class="sxs-lookup"><span data-stu-id="2615f-110">Me, My, MyBase, and MyClass</span></span>](../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [<span data-ttu-id="2615f-111">継承の基本</span><span class="sxs-lookup"><span data-stu-id="2615f-111">Inheritance Basics</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
