---
title: '方法: コレクション初期化子 (Visual Basic) を使用してコレクションを作成します。'
ms.date: 07/20/2015
helpviewer_keywords:
- collection initializers [Visual Basic]
ms.assetid: c858db10-424d-47e0-92cd-e08087cc5ebc
ms.openlocfilehash: aaa367e5a1739f26e9b0458d8f2fc44462b73b7b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631725"
---
# <a name="how-to-create-a-collection-used-by-a-collection-initializer-visual-basic"></a><span data-ttu-id="e601c-102">方法: コレクション初期化子 (Visual Basic) を使用してコレクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="e601c-102">How to: Create a Collection Used by a Collection Initializer (Visual Basic)</span></span>
<span data-ttu-id="e601c-103">コレクション初期化子を使用してコレクションを作成するときに、Visual Basic コンパイラ検索、`Add`対象のコレクション型のメソッドのパラメーター、`Add`メソッド コレクション初期化子の値の型に一致します。</span><span class="sxs-lookup"><span data-stu-id="e601c-103">When you use a collection initializer to create a collection, the Visual Basic compiler searches for an `Add` method of the collection type for which the parameters for the `Add` method match the types of the values in the collection initializer.</span></span> <span data-ttu-id="e601c-104">これは、`Add`メソッドを使用して、コレクション、コレクション初期化子の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="e601c-104">This `Add` method is used to populate the collection with the values from the collection initializer.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e601c-105">例</span><span class="sxs-lookup"><span data-stu-id="e601c-105">Example</span></span>  
 <span data-ttu-id="e601c-106">次の例は、`OrderCollection`パブリックを含むコレクション`Add`コレクション初期化子を使用して型のオブジェクトの追加メソッド`Order`します。</span><span class="sxs-lookup"><span data-stu-id="e601c-106">The following example shows an `OrderCollection` collection that contains a public `Add` method that a collection initializer can use to add objects of type `Order`.</span></span> <span data-ttu-id="e601c-107">`Add`メソッドでは、簡略化されたコレクションの初期化子構文を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="e601c-107">The `Add` method enables you to use the shortened collection initializer syntax.</span></span>  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#4](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_1.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#1](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_2.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#2](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_3.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#3](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_4.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="e601c-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="e601c-108">See also</span></span>
- [<span data-ttu-id="e601c-109">コレクション初期化子</span><span class="sxs-lookup"><span data-stu-id="e601c-109">Collection Initializers</span></span>](../../../../visual-basic/programming-guide/language-features/collection-initializers/index.md)
- [<span data-ttu-id="e601c-110">方法: 作成、コレクション初期化子によって使用される拡張メソッドを追加</span><span class="sxs-lookup"><span data-stu-id="e601c-110">How to: Create an Add Extension Method Used by a Collection Initializer</span></span>](../../../../visual-basic/programming-guide/language-features/collection-initializers/how-to-create-an-add-extension-method-used-by-a-collection-initializer.md)
