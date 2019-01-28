---
title: '方法 : ポインターのインクリメントとデクリメント - C# プログラミング ガイド'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], increment and decrement
- pointer expressions [C#], increment and decrement
ms.assetid: 1b8b9281-44ee-485a-9045-3db38a4b4b89
ms.openlocfilehash: ead179c3711a5e63bbdc2ec2b5644d5991b82ee7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54573271"
---
# <a name="how-to-increment-and-decrement-pointers-c-programming-guide"></a><span data-ttu-id="fe9dd-102">方法 : ポインターのインクリメントとデクリメント (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="fe9dd-102">How to: increment and decrement pointers (C# Programming Guide)</span></span>

<span data-ttu-id="fe9dd-103">`pointer-type*` 型のポインターの `sizeof(pointer-type)` によってポインターの位置を変更するには、インクリメント演算子 (`++`) とデクリメント演算子 (`--`) を使用します。</span><span class="sxs-lookup"><span data-stu-id="fe9dd-103">Use the increment and the decrement operators, `++` and `--`, to change the pointer location by `sizeof(pointer-type)` for a pointer of the type `pointer-type*`.</span></span> <span data-ttu-id="fe9dd-104">インクリメント式とデクリメント式には、次の書式を使用します。</span><span class="sxs-lookup"><span data-stu-id="fe9dd-104">The increment and decrement expressions take the following form:</span></span>  
  
```csharp
++p;  
p++;  
--p;  
p--;  
```  
  
 <span data-ttu-id="fe9dd-105">インクリメント演算子とデクリメント演算子は、`void*` 以外のすべての型のポインターに適用できます。</span><span class="sxs-lookup"><span data-stu-id="fe9dd-105">The increment and decrement operators can be applied to pointers of any type except the type `void*`.</span></span>  
  
 <span data-ttu-id="fe9dd-106">`pointer-type*` 型のポインターにインクリメント演算子を適用すると、ポインター変数に格納されているアドレスに `sizeof(pointer-type)` が加算されます。</span><span class="sxs-lookup"><span data-stu-id="fe9dd-106">The effect of applying the increment operator to a pointer of the type `pointer-type*` is to add `sizeof(pointer-type)` to the address that is contained in the pointer variable.</span></span>  
  
 <span data-ttu-id="fe9dd-107">`pointer-type*` 型のポインターにデクリメント演算子を適用すると、ポインター変数に格納されているアドレスから `sizeof(pointer-type)` が減算されます。</span><span class="sxs-lookup"><span data-stu-id="fe9dd-107">The effect of applying the decrement operator to a pointer of the type `pointer-type*` is to subtract `sizeof(pointer-type)` from the address that is contained in the pointer variable.</span></span>  
  
 <span data-ttu-id="fe9dd-108">演算がポインターのドメインをオーバーフローしても例外は生成されません。生じる結果は実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="fe9dd-108">No exceptions are generated when the operation overflows the domain of the pointer, and the result depends on the implementation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fe9dd-109">例</span><span class="sxs-lookup"><span data-stu-id="fe9dd-109">Example</span></span>  
 <span data-ttu-id="fe9dd-110">この例では、ポインターを `int` のサイズだけインクリメントして、配列をステップ実行します。</span><span class="sxs-lookup"><span data-stu-id="fe9dd-110">In this example, you step through an array by incrementing the pointer by the size of `int`.</span></span> <span data-ttu-id="fe9dd-111">ステップごとに、配列要素のアドレスと内容を表示します。</span><span class="sxs-lookup"><span data-stu-id="fe9dd-111">With each step, you display the address and the content of the array element.</span></span>  
  
 [!code-csharp[csProgGuidePointers#3](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-increment-and-decrement-pointers_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#13](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-increment-and-decrement-pointers_2.cs)]  
  
<span data-ttu-id="fe9dd-112">**値:0 @ アドレス:12860272**
**値:1 @ アドレス:12860276**
**値:2 @ アドレス:12860280**
**値:3 @ アドレス:12860284**
**値:4 @ アドレス:12860288**</span><span class="sxs-lookup"><span data-stu-id="fe9dd-112">**Value:0 @ Address:12860272**
**Value:1 @ Address:12860276**
**Value:2 @ Address:12860280**
**Value:3 @ Address:12860284**
**Value:4 @ Address:12860288**</span></span>

## <a name="see-also"></a><span data-ttu-id="fe9dd-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe9dd-113">See also</span></span>

- [<span data-ttu-id="fe9dd-114">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="fe9dd-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="fe9dd-115">ポインター式</span><span class="sxs-lookup"><span data-stu-id="fe9dd-115">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)
- [<span data-ttu-id="fe9dd-116">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="fe9dd-116">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
- [<span data-ttu-id="fe9dd-117">ポインターの操作</span><span class="sxs-lookup"><span data-stu-id="fe9dd-117">Manipulating Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/manipulating-pointers.md)
- [<span data-ttu-id="fe9dd-118">ポインター型</span><span class="sxs-lookup"><span data-stu-id="fe9dd-118">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [<span data-ttu-id="fe9dd-119">型</span><span class="sxs-lookup"><span data-stu-id="fe9dd-119">Types</span></span>](../../../csharp/language-reference/keywords/types.md)
- [<span data-ttu-id="fe9dd-120">unsafe</span><span class="sxs-lookup"><span data-stu-id="fe9dd-120">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)
- [<span data-ttu-id="fe9dd-121">fixed ステートメント</span><span class="sxs-lookup"><span data-stu-id="fe9dd-121">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)
- [<span data-ttu-id="fe9dd-122">stackalloc</span><span class="sxs-lookup"><span data-stu-id="fe9dd-122">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
- [<span data-ttu-id="fe9dd-123">sizeof</span><span class="sxs-lookup"><span data-stu-id="fe9dd-123">sizeof</span></span>](../../../csharp/language-reference/keywords/sizeof.md)
