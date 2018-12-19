---
title: void - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- void_CSharpKeyword
- void
helpviewer_keywords:
- void keyword [C#]
ms.assetid: 0d2d8a95-fe20-4fbd-bf5d-c1e54bce71d4
ms.openlocfilehash: 87ccc3a18f0956ffe800ae97598e621e5ca72480
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53238378"
---
# <a name="void-c-reference"></a><span data-ttu-id="03738-102">void (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="03738-102">void (C# Reference)</span></span>
<span data-ttu-id="03738-103">メソッドの戻り値の型として使用した場合、`void` はメソッドが値を返さないことを指定します。</span><span class="sxs-lookup"><span data-stu-id="03738-103">When used as the return type for a method, `void` specifies that the method doesn't return a value.</span></span>

<span data-ttu-id="03738-104">`void` は、メソッドのパラメーター リストに含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="03738-104">`void` isn't allowed in the parameter list of a method.</span></span> <span data-ttu-id="03738-105">パラメーターを取らず、値を返さないメソッドは、次のように宣言されます。</span><span class="sxs-lookup"><span data-stu-id="03738-105">A method that takes no parameters and returns no value is declared as follows:</span></span>

```csharp
public void SampleMethod()
{
    // Body of the method.
}
```

<span data-ttu-id="03738-106">`void` は、不明な型へのポインターを宣言するために、unsafe コンテキストでも使用されます。</span><span class="sxs-lookup"><span data-stu-id="03738-106">`void` is also used in an unsafe context to declare a pointer to an unknown type.</span></span> <span data-ttu-id="03738-107">詳しくは、「[ポインター型](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="03738-107">For more information, see [Pointer types](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md).</span></span>

<span data-ttu-id="03738-108">`void` は、.NET Framework の <xref:System.Void?displayProperty=nameWithType> 型のエイリアスです。</span><span class="sxs-lookup"><span data-stu-id="03738-108">`void` is an alias for the .NET Framework <xref:System.Void?displayProperty=nameWithType> type.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="03738-109">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="03738-109">C# Language Specification</span></span>
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="03738-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="03738-110">See also</span></span>

- [<span data-ttu-id="03738-111">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="03738-111">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="03738-112">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="03738-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="03738-113">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="03738-113">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="03738-114">参照型</span><span class="sxs-lookup"><span data-stu-id="03738-114">Reference Types</span></span>](../../../csharp/language-reference/keywords/reference-types.md)  
- [<span data-ttu-id="03738-115">値型</span><span class="sxs-lookup"><span data-stu-id="03738-115">Value Types</span></span>](../../../csharp/language-reference/keywords/value-types.md)  
- [<span data-ttu-id="03738-116">メソッド</span><span class="sxs-lookup"><span data-stu-id="03738-116">Methods</span></span>](../../../csharp/programming-guide/classes-and-structs/methods.md)  
- [<span data-ttu-id="03738-117">アンセーフ コードとポインター</span><span class="sxs-lookup"><span data-stu-id="03738-117">Unsafe Code and Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/index.md)
