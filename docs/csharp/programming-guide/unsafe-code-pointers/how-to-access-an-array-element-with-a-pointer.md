---
title: ポインターを使用して配列要素にアクセスする方法 - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], array access
ms.assetid: 6c46f2af-a730-4855-8638-f136d9abaa12
ms.openlocfilehash: 57b1bebb95c1b3f24e550d554fe369d931d6f6b4
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53241802"
---
# <a name="how-to-access-an-array-element-with-a-pointer-c-programming-guide"></a><span data-ttu-id="4efbe-102">ポインターを使用して配列要素にアクセスする方法 (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="4efbe-102">How to access an array element with a pointer (C# Programming Guide)</span></span>

<span data-ttu-id="4efbe-103">安全ではないコンテキストでは、次の例のように、ポインターを利用してメモリ内の要素にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="4efbe-103">In an unsafe context, you can access an element in memory by using pointer element access, as shown in the following example:</span></span>

```csharp
char* charPointer = stackalloc char[123];
for (int i = 65; i < 123; i++)
{
    charPointer[i] = (char)i; //access array elements
}
```

<span data-ttu-id="4efbe-104">角かっこ内の式は `int`、`uint`、`long`、`ulong` に暗黙的に変換できるものでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4efbe-104">The expression in square brackets must be implicitly convertible to `int`, `uint`, `long`, or `ulong`.</span></span> <span data-ttu-id="4efbe-105">演算 p[e] は \*(p+e) と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="4efbe-105">The operation p[e] is equivalent to \*(p+e).</span></span> <span data-ttu-id="4efbe-106">C や C++ と同様に、ポインターで要素にアクセスする行為では、範囲外のエラーがチェックされません。</span><span class="sxs-lookup"><span data-stu-id="4efbe-106">Like C and C++, the pointer element access does not check for out-of-bounds errors.</span></span>

## <a name="example"></a><span data-ttu-id="4efbe-107">例</span><span class="sxs-lookup"><span data-stu-id="4efbe-107">Example</span></span>

<span data-ttu-id="4efbe-108">この例では、123 のメモリ場所が文字配列 `charPointer` に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="4efbe-108">In this example, 123 memory locations are allocated to a character array, `charPointer`.</span></span> <span data-ttu-id="4efbe-109">この配列を利用し、2 つの [for](../../../csharp/language-reference/keywords/for.md) ループの小文字と大文字が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4efbe-109">The array is used to display the lowercase letters and the uppercase letters in two [for](../../../csharp/language-reference/keywords/for.md) loops.</span></span>

<span data-ttu-id="4efbe-110">式 `charPointer[i]` は式 `*(charPointer + i)` と等しく、2 つの式のいずれを利用しても同じ結果が得られることに注目してください。</span><span class="sxs-lookup"><span data-stu-id="4efbe-110">Notice that the expression `charPointer[i]` is equivalent to the expression `*(charPointer + i)`, and you can obtain the same result by using either of the two expressions.</span></span>

[!code-csharp[csProgGuidePointers#11](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-access-an-array-element-with-a-pointer_1.cs)]

[!code-csharp[csProgGuidePointers#12](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-access-an-array-element-with-a-pointer_2.cs)]

<span data-ttu-id="4efbe-111">**大文字:**
**ABCDEFGHIJKLMNOPQRSTUVWXYZ**
**小文字:**
**abcdefghijklmnopqrstuvwxyz**</span><span class="sxs-lookup"><span data-stu-id="4efbe-111">**Uppercase letters:**
**ABCDEFGHIJKLMNOPQRSTUVWXYZ**
**Lowercase letters:**
**abcdefghijklmnopqrstuvwxyz**</span></span>

## <a name="see-also"></a><span data-ttu-id="4efbe-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="4efbe-112">See also</span></span>

- [<span data-ttu-id="4efbe-113">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="4efbe-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="4efbe-114">ポインター式</span><span class="sxs-lookup"><span data-stu-id="4efbe-114">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)
- [<span data-ttu-id="4efbe-115">ポインター型</span><span class="sxs-lookup"><span data-stu-id="4efbe-115">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [<span data-ttu-id="4efbe-116">型</span><span class="sxs-lookup"><span data-stu-id="4efbe-116">Types</span></span>](../../../csharp/language-reference/keywords/types.md)
- [<span data-ttu-id="4efbe-117">unsafe</span><span class="sxs-lookup"><span data-stu-id="4efbe-117">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)
- [<span data-ttu-id="4efbe-118">fixed ステートメント</span><span class="sxs-lookup"><span data-stu-id="4efbe-118">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)
- [<span data-ttu-id="4efbe-119">stackalloc</span><span class="sxs-lookup"><span data-stu-id="4efbe-119">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
