---
title: unsafe キーワード (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- unsafe_CSharpKeyword
- unsafe
helpviewer_keywords:
- unsafe keyword [C#]
ms.assetid: 7e818009-1c6e-4b9e-b769-3728a01586a0
ms.openlocfilehash: 79cb246c4094f02d1319d28fcc94d0d3d5bd9cb5
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53128428"
---
# <a name="unsafe-c-reference"></a><span data-ttu-id="b5c59-102">unsafe (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="b5c59-102">unsafe (C# Reference)</span></span>

<span data-ttu-id="b5c59-103">`unsafe` キーワードは、ポインターに関連するすべての操作に必要な、unsafe コンテキストを示します。</span><span class="sxs-lookup"><span data-stu-id="b5c59-103">The `unsafe` keyword denotes an unsafe context, which is required for any operation involving pointers.</span></span> <span data-ttu-id="b5c59-104">詳しくは、「[アンセーフ コードとポインター](../../programming-guide/unsafe-code-pointers/index.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b5c59-104">For more information, see [Unsafe Code and Pointers](../../programming-guide/unsafe-code-pointers/index.md).</span></span>

<span data-ttu-id="b5c59-105">`unsafe` 修飾子は、型またはメンバーの宣言で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b5c59-105">You can use the `unsafe` modifier in the declaration of a type or a member.</span></span> <span data-ttu-id="b5c59-106">そのため、型やメンバーの全体的なテキスト範囲が unsafe コンテキストと見なされます。</span><span class="sxs-lookup"><span data-stu-id="b5c59-106">The entire textual extent of the type or member is therefore considered an unsafe context.</span></span> <span data-ttu-id="b5c59-107">たとえば、次に示すのは、`unsafe` 修飾子を使用して宣言されたメソッドです。</span><span class="sxs-lookup"><span data-stu-id="b5c59-107">For example, the following is a method declared with the `unsafe` modifier:</span></span>

```csharp
unsafe static void FastCopy(byte[] src, byte[] dst, int count)
{
    // Unsafe context: can use pointers here.
}
```

<span data-ttu-id="b5c59-108">unsafe コンテキストのスコープはパラメーター リストからメソッドの末尾までなので、ポインターはパラメーター リストでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="b5c59-108">The scope of the unsafe context extends from the parameter list to the end of the method, so pointers can also be used in the parameter list:</span></span>

```csharp
unsafe static void FastCopy ( byte* ps, byte* pd, int count ) {...}
```

<span data-ttu-id="b5c59-109">また、unsafe ブロックを使用して、そのブロック内で unsafe コードを使用できるようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b5c59-109">You can also use an unsafe block to enable the use of an unsafe code inside this block.</span></span> <span data-ttu-id="b5c59-110">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b5c59-110">For example:</span></span>

```csharp
unsafe
{
    // Unsafe context: can use pointers here.
}
```

<span data-ttu-id="b5c59-111">unsafe コードをコンパイルするには、 [/unsafe](../compiler-options/unsafe-compiler-option.md) コンパイラ オプションを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5c59-111">To compile unsafe code, you must specify the [/unsafe](../compiler-options/unsafe-compiler-option.md) compiler option.</span></span> <span data-ttu-id="b5c59-112">unsafe コードは、共通言語ランタイムでは検証できません。</span><span class="sxs-lookup"><span data-stu-id="b5c59-112">Unsafe code is not verifiable by the common language runtime.</span></span>

## <a name="example"></a><span data-ttu-id="b5c59-113">例</span><span class="sxs-lookup"><span data-stu-id="b5c59-113">Example</span></span>

[!code-csharp[csrefKeywordsModifiers#22](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#22)]

## <a name="c-language-specification"></a><span data-ttu-id="b5c59-114">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="b5c59-114">C# language specification</span></span>

<span data-ttu-id="b5c59-115">詳細については、「[C# 言語の仕様](../language-specification/index.md)」の[アンセーフ コード](~/_csharplang/spec/unsafe-code.md)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5c59-115">For more information, see [Unsafe code](~/_csharplang/spec/unsafe-code.md) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="b5c59-116">言語仕様は、C# の構文と使用法に関する信頼性のある情報源です。</span><span class="sxs-lookup"><span data-stu-id="b5c59-116">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5c59-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="b5c59-117">See also</span></span>

- [<span data-ttu-id="b5c59-118">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="b5c59-118">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="b5c59-119">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="b5c59-119">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="b5c59-120">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="b5c59-120">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="b5c59-121">fixed ステートメント</span><span class="sxs-lookup"><span data-stu-id="b5c59-121">fixed Statement</span></span>](fixed-statement.md)
- [<span data-ttu-id="b5c59-122">アンセーフ コードとポインター</span><span class="sxs-lookup"><span data-stu-id="b5c59-122">Unsafe Code and Pointers</span></span>](../../programming-guide/unsafe-code-pointers/index.md)
- [<span data-ttu-id="b5c59-123">固定サイズ バッファー</span><span class="sxs-lookup"><span data-stu-id="b5c59-123">Fixed Size Buffers</span></span>](../../programming-guide/unsafe-code-pointers/fixed-size-buffers.md)