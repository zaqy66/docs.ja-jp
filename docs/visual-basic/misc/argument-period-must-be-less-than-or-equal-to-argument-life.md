---
title: 引数 'Period' は 'Life' 引数以下でなければなりません
ms.date: 07/20/2015
f1_keywords:
- vbrFinancial_PeriodLELife
ms.assetid: dc575d41-b376-4b05-bbbe-6de1e98385f1
ms.openlocfilehash: d647f5c86beafb7d6a914945ffeac05271c86a72
ms.sourcegitcommit: 0888d7b24f475c346a3f444de8d83ec1ca7cd234
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/22/2018
ms.locfileid: "53762955"
---
# <a name="argument-period-must-be-less-than-or-equal-to-argument-life"></a><span data-ttu-id="4257a-102">引数 'Period' は 'Life' 引数以下でなければなりません</span><span class="sxs-lookup"><span data-stu-id="4257a-102">Argument 'Period' must be less than or equal to argument 'Life'</span></span>
<span data-ttu-id="4257a-103">資産の減価償却費計算の対象期間を指定する `Period` 引数の値が `Life` 引数の値より大きくなっています。</span><span class="sxs-lookup"><span data-stu-id="4257a-103">The value of the `Period` argument, which specifies the period for which asset depreciation is calculated, is greater than the value of the `Life` argument.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="4257a-104">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="4257a-104">To correct this error</span></span>  
  
-   <span data-ttu-id="4257a-105">`Life` 引数と `Period` 引数の両方が同じ単位で指定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4257a-105">Ensure that the `Life` and `Period` arguments are expressed in the same units.</span></span> <span data-ttu-id="4257a-106">たとえば、 `Life` を月単位で指定する場合は、 `Period` も月単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="4257a-106">For example, if `Life` is measured in months, `Period` should be as well.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4257a-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="4257a-107">See Also</span></span>  
   
   
 [<span data-ttu-id="4257a-108">引数の値渡しと参照渡し</span><span class="sxs-lookup"><span data-stu-id="4257a-108">Passing Arguments by Value and by Reference</span></span>](../../visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
