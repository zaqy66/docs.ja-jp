---
title: Unicode (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Unicode
helpviewer_keywords:
- Unicode, external references
- Declare statement [Visual Basic], marshaling strings
- Unicode keyword [Visual Basic]
- Unicode, marshaling strings
ms.assetid: 0021d5ff-3209-444e-8497-420f3e6ee075
ms.openlocfilehash: 491bbb24be8e6a3044b0a433c5ad262596ae00d8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54655284"
---
# <a name="unicode-visual-basic"></a><span data-ttu-id="33158-102">Unicode (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="33158-102">Unicode (Visual Basic)</span></span>
<span data-ttu-id="33158-103">Visual Basic に宣言されている外部プロシージャの名前に関係なく Unicode 値にすべての文字列がマーシャ リングする必要がありますを指定します。</span><span class="sxs-lookup"><span data-stu-id="33158-103">Specifies that Visual Basic should marshal all strings to Unicode values regardless of the name of the external procedure being declared.</span></span>  
  
 <span data-ttu-id="33158-104">プロジェクトの外部で定義されたプロシージャを呼び出すときに、Visual Basic コンパイラには、手順を正しく呼び出すために必要があります情報へのアクセスはありません。</span><span class="sxs-lookup"><span data-stu-id="33158-104">When you call a procedure defined outside your project, the Visual Basic compiler does not have access to the information it must have in order to call the procedure correctly.</span></span> <span data-ttu-id="33158-105">この情報には、プロシージャがある場所は、識別方法、その呼び出し元のシーケンスおよび戻り値の型が含まれます。 して、使用する文字列の文字セットします。</span><span class="sxs-lookup"><span data-stu-id="33158-105">This information includes where the procedure is located, how it is identified, its calling sequence and return type, and the string character set it uses.</span></span> <span data-ttu-id="33158-106">[Declare ステートメント](../../../visual-basic/language-reference/statements/declare-statement.md)外部プロシージャへの参照を作成し、このために必要な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="33158-106">The [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md) creates a reference to an external procedure and supplies this necessary information.</span></span>  
  
 <span data-ttu-id="33158-107">`charsetmodifier`パーツ、`Declare`ステートメントが外部プロシージャの呼び出し中に文字列をマーシャ リングする、文字セット情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="33158-107">The `charsetmodifier` part in the `Declare` statement supplies the character set information to marshal strings during a call to the external procedure.</span></span> <span data-ttu-id="33158-108">また、Visual Basic が外部プロシージャ名の外部のファイルを検索する方法も影響します。</span><span class="sxs-lookup"><span data-stu-id="33158-108">It also affects how Visual Basic searches the external file for the external procedure name.</span></span> <span data-ttu-id="33158-109">`Unicode`修飾子は、Visual Basic を Unicode 値のすべての文字列をマーシャ リングする必要があり、検索中にその名前を変更することがなく、プロシージャを検索することを指定します。</span><span class="sxs-lookup"><span data-stu-id="33158-109">The `Unicode` modifier specifies that Visual Basic should marshal all strings to Unicode values and should look up the procedure without modifying its name during the search.</span></span>  
  
 <span data-ttu-id="33158-110">文字セットに修飾子が指定されていない場合`Ansi`既定値です。</span><span class="sxs-lookup"><span data-stu-id="33158-110">If no character set modifier is specified, `Ansi` is the default.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="33158-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="33158-111">Remarks</span></span>  
 <span data-ttu-id="33158-112">`Unicode`修飾子は、このコンテキストで使用できます。</span><span class="sxs-lookup"><span data-stu-id="33158-112">The `Unicode` modifier can be used in this context:</span></span>  
  
 [<span data-ttu-id="33158-113">Declare ステートメント</span><span class="sxs-lookup"><span data-stu-id="33158-113">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
## <a name="smart-device-developer-notes"></a><span data-ttu-id="33158-114">スマート デバイスの開発者向け注意事項</span><span class="sxs-lookup"><span data-stu-id="33158-114">Smart Device Developer Notes</span></span>  
 <span data-ttu-id="33158-115">このキーワードはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="33158-115">This keyword is not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33158-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="33158-116">See also</span></span>
- [<span data-ttu-id="33158-117">Ansi</span><span class="sxs-lookup"><span data-stu-id="33158-117">Ansi</span></span>](../../../visual-basic/language-reference/modifiers/ansi.md)
- [<span data-ttu-id="33158-118">Auto</span><span class="sxs-lookup"><span data-stu-id="33158-118">Auto</span></span>](../../../visual-basic/language-reference/modifiers/auto.md)
- [<span data-ttu-id="33158-119">キーワード</span><span class="sxs-lookup"><span data-stu-id="33158-119">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
