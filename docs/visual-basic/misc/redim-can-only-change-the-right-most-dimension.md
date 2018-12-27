---
title: "'ReDim' では最も右にある次元のみ変更できます"
ms.date: 07/20/2015
f1_keywords:
- vbrArray_TypeMismatch
ms.assetid: d53cf41b-7a7a-466c-a29a-920d99698fa9
ms.openlocfilehash: 5b4f054c5d1dfad52ce19e1a9f9d246945866703
ms.sourcegitcommit: 0888d7b24f475c346a3f444de8d83ec1ca7cd234
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/22/2018
ms.locfileid: "53767396"
---
# <a name="redim-can-only-change-the-right-most-dimension"></a><span data-ttu-id="4b875-102">'ReDim' では最も右にある次元のみ変更できます</span><span class="sxs-lookup"><span data-stu-id="4b875-102">'ReDim' can only change the right-most dimension</span></span>
<span data-ttu-id="4b875-103">`ReDim` ステートメントが `Preserve` キーワードを使用して、最後のディメンションではない配列のディメンションを変更しようとしました。</span><span class="sxs-lookup"><span data-stu-id="4b875-103">A `ReDim` statement attempted to use the `Preserve` keyword to change a dimension of an array that is not the last dimension.</span></span> <span data-ttu-id="4b875-104">`Preserve`を使用すると、配列の最後のディメンションについてのみ、サイズを変更できます。</span><span class="sxs-lookup"><span data-stu-id="4b875-104">When using `Preserve`, you can resize only the last dimension of an array.</span></span> <span data-ttu-id="4b875-105">他のすべてのディメンションに対しては、既存の配列と同じサイズを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b875-105">For all other dimensions, you must specify the same size as for the existing array.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="4b875-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="4b875-106">To correct this error</span></span>  
  
-   <span data-ttu-id="4b875-107">`Preserve` キーワードを削除します。</span><span class="sxs-lookup"><span data-stu-id="4b875-107">Remove the `Preserve` keyword.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b875-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b875-108">See Also</span></span>  
 [<span data-ttu-id="4b875-109">Visual Basic における配列</span><span class="sxs-lookup"><span data-stu-id="4b875-109">Arrays in Visual Basic</span></span>](~/docs/visual-basic/programming-guide/language-features/arrays/index.md)  
 [<span data-ttu-id="4b875-110">Visual Basic で配列の次元</span><span class="sxs-lookup"><span data-stu-id="4b875-110">Array dimensions in Visual Basic</span></span>](~/docs/visual-basic/programming-guide/language-features/arrays/array-dimensions.md)  
 [<span data-ttu-id="4b875-111">ReDim ステートメント</span><span class="sxs-lookup"><span data-stu-id="4b875-111">ReDim Statement</span></span>](../../visual-basic/language-reference/statements/redim-statement.md)  
 [<span data-ttu-id="4b875-112">Dim ステートメント</span><span class="sxs-lookup"><span data-stu-id="4b875-112">Dim Statement</span></span>](../../visual-basic/language-reference/statements/dim-statement.md)  
 [<span data-ttu-id="4b875-113">保存 - 削除</span><span class="sxs-lookup"><span data-stu-id="4b875-113">Preserve - delete</span></span>](https://msdn.microsoft.com/library/91badeab-b4e0-48b6-92c9-9f0c8f995d81)
