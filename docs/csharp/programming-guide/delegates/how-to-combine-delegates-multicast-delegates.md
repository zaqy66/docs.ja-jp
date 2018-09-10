---
title: '方法 : デリゲートを結合する (マルチキャスト デリゲート) (C# プログラミング ガイド)'
ms.date: 07/20/2015
helpviewer_keywords:
- delegates [C#], combining
- multicast delegates [C#]
ms.assetid: 4e689450-6d0c-46de-acfd-f961018ae5dd
ms.openlocfilehash: e3cc3f9082bd86004a7821b64c01253408c07641
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44083278"
---
# <a name="how-to-combine-delegates-multicast-delegatesc-programming-guide"></a><span data-ttu-id="23fd4-102">方法 : デリゲートを結合する (マルチキャスト デリゲート) (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="23fd4-102">How to: Combine Delegates (Multicast Delegates)(C# Programming Guide)</span></span>
<span data-ttu-id="23fd4-103">ここでは、マルチキャスト デリゲートを作成する例について説明します。</span><span class="sxs-lookup"><span data-stu-id="23fd4-103">This example demonstrates how to create multicast delegates.</span></span> <span data-ttu-id="23fd4-104">[デリゲート](../../../csharp/language-reference/keywords/delegate.md) オブジェクトの便利な性質の 1 つは、`+` 演算子を使用して、複数のオブジェクトを 1 つのデリゲート インスタンスに割り当てられることです。</span><span class="sxs-lookup"><span data-stu-id="23fd4-104">A useful property of [delegate](../../../csharp/language-reference/keywords/delegate.md) objects is that multiple objects can be assigned to one delegate instance by using the `+` operator.</span></span> <span data-ttu-id="23fd4-105">マルチキャスト デリゲートには、割り当てられたデリゲートの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="23fd4-105">The multicast delegate contains a list of the assigned delegates.</span></span> <span data-ttu-id="23fd4-106">マルチキャスト デリゲートを呼び出すと、一覧内のデリゲートが順に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="23fd4-106">When the multicast delegate is called, it invokes the delegates in the list, in order.</span></span> <span data-ttu-id="23fd4-107">結合できるのは、同じ型のデリゲートのみです。</span><span class="sxs-lookup"><span data-stu-id="23fd4-107">Only delegates of the same type can be combined.</span></span>  
  
 <span data-ttu-id="23fd4-108">`-` 演算子を使用して、マルチキャスト デリゲートからコンポーネント デリゲートを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="23fd4-108">The `-` operator can be used to remove a component delegate from a multicast delegate.</span></span>  
  
## <a name="example"></a><span data-ttu-id="23fd4-109">例</span><span class="sxs-lookup"><span data-stu-id="23fd4-109">Example</span></span>  
 [!code-csharp[csProgGuideDelegates#11](../../../csharp/programming-guide/delegates/codesnippet/CSharp/how-to-combine-delegates-multicast-delegates_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="23fd4-110">参照</span><span class="sxs-lookup"><span data-stu-id="23fd4-110">See Also</span></span>

- <xref:System.MulticastDelegate>  
- [<span data-ttu-id="23fd4-111">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="23fd4-111">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="23fd4-112">イベント</span><span class="sxs-lookup"><span data-stu-id="23fd4-112">Events</span></span>](../../../csharp/programming-guide/events/index.md)
