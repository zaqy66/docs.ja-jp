---
title: -> 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- ->_CSharpKeyword
helpviewer_keywords:
- member access operator (->) [C#]
- -> operator [C#]
ms.assetid: e39ccdc1-f1ff-4a92-bf1d-ac2c8c11316a
ms.openlocfilehash: be74f02a85aa05cdab32768ed38222fc4d9289b1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255368"
---
# <a name="--operator-c-reference"></a><span data-ttu-id="d6723-102">-> 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="d6723-102">-> Operator (C# Reference)</span></span>

<span data-ttu-id="d6723-103">ポインター メンバー アクセス演算子 `->` は、ポインターの間接アクセスとメンバー アクセスを結合したものです。</span><span class="sxs-lookup"><span data-stu-id="d6723-103">The pointer member access operator `->` combines pointer indirection and member access.</span></span>

<span data-ttu-id="d6723-104">`x`が型 `T*` のポインターであり、`y` が `T` のアクセス可能なメンバーである場合、フォームの式</span><span class="sxs-lookup"><span data-stu-id="d6723-104">If `x` is a pointer of the type `T*` and `y` is an accessible member of `T`, an expression of the form</span></span>

```csharp
x->y
```

<span data-ttu-id="d6723-105">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="d6723-105">is equivalent to</span></span>

```csharp
(*x).y
```

<span data-ttu-id="d6723-106">`->` 演算子には [unsafe](../keywords/unsafe.md) コンテキストが必要です。</span><span class="sxs-lookup"><span data-stu-id="d6723-106">The `->` operator requires [unsafe](../keywords/unsafe.md) context.</span></span>

<span data-ttu-id="d6723-107">詳細については、「[方法 : ポインターを使用してメンバーにアクセスする](../../programming-guide/unsafe-code-pointers/how-to-access-a-member-with-a-pointer.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d6723-107">For more information, see [How to: access a member with a pointer](../../programming-guide/unsafe-code-pointers/how-to-access-a-member-with-a-pointer.md).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="d6723-108">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="d6723-108">Operator overloadability</span></span>

<span data-ttu-id="d6723-109">`->` 演算子はオーバーロードできません。</span><span class="sxs-lookup"><span data-stu-id="d6723-109">The `->` operator cannot be overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="d6723-110">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="d6723-110">C# language specification</span></span>

<span data-ttu-id="d6723-111">詳細については、「[C# 言語仕様](../language-specification/index.md)」の「[ポインターのメンバー アクセス](~/_csharplang/spec/unsafe-code.md#pointer-member-access)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d6723-111">For more information, see the [Pointer member access](~/_csharplang/spec/unsafe-code.md#pointer-member-access) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d6723-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="d6723-112">See also</span></span>

- [<span data-ttu-id="d6723-113">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="d6723-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="d6723-114">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="d6723-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="d6723-115">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="d6723-115">C# Operators</span></span>](index.md)
- [<span data-ttu-id="d6723-116">ポインター型</span><span class="sxs-lookup"><span data-stu-id="d6723-116">Pointer types</span></span>](../../programming-guide/unsafe-code-pointers/pointer-types.md)
