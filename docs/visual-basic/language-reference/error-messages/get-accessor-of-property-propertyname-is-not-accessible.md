---
title: プロパティ '<propertyname>' の 'Get' アクセサーにアクセスできません。
ms.date: 07/20/2015
f1_keywords:
- vbc31103
- bc31103
helpviewer_keywords:
- BC31103
ms.assetid: 3c346c32-7669-4b04-841d-7a9df9cb703e
ms.openlocfilehash: 72675f882676d3ded9ccc9ff245a1d757fa4393a
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55257786"
---
# <a name="get-accessor-of-property-propertyname-is-not-accessible"></a><span data-ttu-id="aa3a1-102">プロパティのアクセサーを 'get''\<propertyname >' にアクセスできません</span><span class="sxs-lookup"><span data-stu-id="aa3a1-102">'Get' accessor of property '\<propertyname>' is not accessible</span></span>
<span data-ttu-id="aa3a1-103">ステートメントが、プロパティへのアクセスがあるない場合は、プロパティの値を取得しようとしています。`Get`プロシージャ。</span><span class="sxs-lookup"><span data-stu-id="aa3a1-103">A statement attempts to retrieve the value of a property when it does not have access to the property's `Get` procedure.</span></span>  
  
 <span data-ttu-id="aa3a1-104">場合、 [Get ステートメント](../../../visual-basic/language-reference/statements/get-statement.md)レベルよりもより制限の厳しいアクセスでマークされたその[Property ステートメント](../../../visual-basic/language-reference/statements/property-statement.md)プロパティの値を読み取ろうとしてが失敗する、次の場合。</span><span class="sxs-lookup"><span data-stu-id="aa3a1-104">If the [Get Statement](../../../visual-basic/language-reference/statements/get-statement.md) is marked with a more restrictive access level than its [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md), an attempt to read the property value could fail in the following cases:</span></span>  
  
-   <span data-ttu-id="aa3a1-105">`Get`ステートメントがマークされている[プライベート](../../../visual-basic/language-reference/modifiers/private.md)呼び出し元のコードとそれには、クラスまたは構造体のプロパティが定義されているとします。</span><span class="sxs-lookup"><span data-stu-id="aa3a1-105">The `Get` statement is marked [Private](../../../visual-basic/language-reference/modifiers/private.md) and the calling code is outside the class or structure in which the property is defined.</span></span>  
  
-   <span data-ttu-id="aa3a1-106">`Get`ステートメントがマークされている[Protected](../../../visual-basic/language-reference/modifiers/protected.md)呼び出し元のコードは、クラスまたはプロパティが定義されている構造体ではなく、派生クラスでも。</span><span class="sxs-lookup"><span data-stu-id="aa3a1-106">The `Get` statement is marked [Protected](../../../visual-basic/language-reference/modifiers/protected.md) and the calling code is not in the class or structure in which the property is defined, nor in a derived class.</span></span>  
  
-   <span data-ttu-id="aa3a1-107">`Get`ステートメントがマークされている[フレンド](../../../visual-basic/language-reference/modifiers/friend.md)プロパティが定義されている同じアセンブリに呼び出し元のコードがないとします。</span><span class="sxs-lookup"><span data-stu-id="aa3a1-107">The `Get` statement is marked [Friend](../../../visual-basic/language-reference/modifiers/friend.md) and the calling code is not in the same assembly in which the property is defined.</span></span>  
  
 <span data-ttu-id="aa3a1-108">**エラー ID:** BC31103</span><span class="sxs-lookup"><span data-stu-id="aa3a1-108">**Error ID:** BC31103</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="aa3a1-109">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="aa3a1-109">To correct this error</span></span>  
  
-   <span data-ttu-id="aa3a1-110">コントロールのプロパティを定義するソース コードを使っている場合を宣言することを検討してください、`Get`プロパティ自体と同じアクセス レベルを持つプロシージャ。</span><span class="sxs-lookup"><span data-stu-id="aa3a1-110">If you have control of the source code defining the property, consider declaring the `Get` procedure with the same access level as the property itself.</span></span>  
  
-   <span data-ttu-id="aa3a1-111">場合は、プロパティを定義するソース コードがないか、または制限する必要があります、`Get`プロパティ自体へのアクセス性のあるコードの領域にプロパティ値を読み取るステートメントに移動しようとする複数のプロシージャ アクセス レベル、プロパティ。</span><span class="sxs-lookup"><span data-stu-id="aa3a1-111">If you do not have control of the source code defining the property, or you must restrict the `Get` procedure access level more than the property itself, try to move the statement that reads the property value to a region of code that has better access to the property.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa3a1-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa3a1-112">See also</span></span>
- [<span data-ttu-id="aa3a1-113">Property プロシージャ</span><span class="sxs-lookup"><span data-stu-id="aa3a1-113">Property Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/property-procedures.md)
- [<span data-ttu-id="aa3a1-114">方法: 混合アクセス レベルを持つプロパティを宣言します。</span><span class="sxs-lookup"><span data-stu-id="aa3a1-114">How to: Declare a Property with Mixed Access Levels</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-a-property-with-mixed-access-levels.md)
