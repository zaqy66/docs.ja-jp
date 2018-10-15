---
title: '方法 : ポインター変数の値を取得する (C# プログラミング ガイド)'
ms.date: 07/20/2015
helpviewer_keywords:
- pointer expressions [C#], indirection
- pointers [C#], indirection
- variables [C#], pointers
- pointers [C#], * operator
ms.assetid: 460a813a-4995-44c1-9de2-213b91dc7668
ms.openlocfilehash: 66f341e193a0f018adb76a40617f85266519e602
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/18/2018
ms.locfileid: "45746589"
---
# <a name="how-to-obtain-the-value-of-a-pointer-variable-c-programming-guide"></a><span data-ttu-id="2cac4-102">方法 : ポインター変数の値を取得する (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="2cac4-102">How to: Obtain the Value of a Pointer Variable (C# Programming Guide)</span></span>
<span data-ttu-id="2cac4-103">ポインターが指す位置にある変数を取得するには、ポインター間接演算子を使用します。</span><span class="sxs-lookup"><span data-stu-id="2cac4-103">Use the pointer indirection operator to obtain the variable at the location pointed to by a pointer.</span></span> <span data-ttu-id="2cac4-104">この式は次の形式になります。`p` はポインター型です。</span><span class="sxs-lookup"><span data-stu-id="2cac4-104">The expression takes the following form, where `p` is a pointer type:</span></span>  
  
```  
*p;  
```  
  
 <span data-ttu-id="2cac4-105">ポインター型以外の型の式では、単項間接演算子を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="2cac4-105">You cannot use the unary indirection operator on an expression of any type other than the pointer type.</span></span> <span data-ttu-id="2cac4-106">また、[void](../../../csharp/language-reference/keywords/void.md) ポインターに適用することもできません。</span><span class="sxs-lookup"><span data-stu-id="2cac4-106">Also, you cannot apply it to a [void](../../../csharp/language-reference/keywords/void.md) pointer.</span></span>  
  
 <span data-ttu-id="2cac4-107">間接演算子を [null](../../../csharp/language-reference/keywords/null.md) ポインターに適用すると、結果は実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="2cac4-107">When you apply the indirection operator to a [null](../../../csharp/language-reference/keywords/null.md) pointer, the result depends on the implementation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2cac4-108">例</span><span class="sxs-lookup"><span data-stu-id="2cac4-108">Example</span></span>  
 <span data-ttu-id="2cac4-109">次の例では、`char` 型の変数に、さまざまな型のポインターを使用してアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2cac4-109">In the following example, a variable of the type `char` is accessed by using pointers of different types.</span></span> <span data-ttu-id="2cac4-110">変数に割り当てられる物理アドレスが変更できるため、`theChar` のアドレスが実行ごとに異なることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2cac4-110">Note that the address of `theChar` will vary from run to run, because the physical address allocated to a variable can change.</span></span>  
  
 [!code-csharp[csProgGuidePointers#5](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-obtain-the-value-of-a-pointer-variable_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#6](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-obtain-the-value-of-a-pointer-variable_2.cs)]  
  
<span data-ttu-id="2cac4-111">**theChar の値 = Z**
**theChar のアドレス = 12F718**
**pChar の値 = Z**
**pInt の値 = 90**</span><span class="sxs-lookup"><span data-stu-id="2cac4-111">**Value of theChar = Z**
**Address of theChar = 12F718**
**Value of pChar = Z**
**Value of pInt = 90**</span></span>

## <a name="see-also"></a><span data-ttu-id="2cac4-112">参照</span><span class="sxs-lookup"><span data-stu-id="2cac4-112">See Also</span></span>

- [<span data-ttu-id="2cac4-113">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="2cac4-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="2cac4-114">ポインター式</span><span class="sxs-lookup"><span data-stu-id="2cac4-114">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)  
- [<span data-ttu-id="2cac4-115">ポインター型</span><span class="sxs-lookup"><span data-stu-id="2cac4-115">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)  
- [<span data-ttu-id="2cac4-116">型</span><span class="sxs-lookup"><span data-stu-id="2cac4-116">Types</span></span>](../../../csharp/language-reference/keywords/types.md)  
- [<span data-ttu-id="2cac4-117">unsafe</span><span class="sxs-lookup"><span data-stu-id="2cac4-117">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)  
- [<span data-ttu-id="2cac4-118">fixed ステートメント</span><span class="sxs-lookup"><span data-stu-id="2cac4-118">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)  
- [<span data-ttu-id="2cac4-119">stackalloc</span><span class="sxs-lookup"><span data-stu-id="2cac4-119">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
