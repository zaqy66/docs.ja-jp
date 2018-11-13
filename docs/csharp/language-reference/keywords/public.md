---
title: public キーワード (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- public
- public_CSharpKeyword
helpviewer_keywords:
- public keyword [C#]
ms.assetid: 0ae45d16-a551-4b74-9845-57208de1328e
ms.openlocfilehash: b2e09bdb16d6128d69a3eb33cf2cffd4cba60376
ms.sourcegitcommit: 3b1cb8467bd73dee854b604e306c0e7e3882d91a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "43518187"
---
# <a name="public-c-reference"></a><span data-ttu-id="e38fe-102">public (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="e38fe-102">public (C# Reference)</span></span>

<span data-ttu-id="e38fe-103">`public` キーワードは、型と型のメンバーを示すアクセス修飾子です。</span><span class="sxs-lookup"><span data-stu-id="e38fe-103">The `public` keyword is an access modifier for types and type members.</span></span> <span data-ttu-id="e38fe-104">パブリック アクセスは、最も制限の少ないアクセス レベルです。</span><span class="sxs-lookup"><span data-stu-id="e38fe-104">Public access is the most permissive access level.</span></span> <span data-ttu-id="e38fe-105">次の例のように、パブリック メンバーへのアクセスには制限がありません。</span><span class="sxs-lookup"><span data-stu-id="e38fe-105">There are no restrictions on accessing public members, as in this example:</span></span>

```csharp
class SampleClass
{
    public int x; // No access restrictions.
}
```

<span data-ttu-id="e38fe-106">詳しくは、「[アクセス修飾子](../../programming-guide/classes-and-structs/access-modifiers.md)」および「[アクセシビリティ レベル](accessibility-levels.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="e38fe-106">See [Access Modifiers](../../programming-guide/classes-and-structs/access-modifiers.md) and [Accessibility Levels](accessibility-levels.md) for more information.</span></span>

## <a name="example"></a><span data-ttu-id="e38fe-107">例</span><span class="sxs-lookup"><span data-stu-id="e38fe-107">Example</span></span>

<span data-ttu-id="e38fe-108">次の例では、2 つのクラス (`PointTest` と `MainClass`) が宣言されています。</span><span class="sxs-lookup"><span data-stu-id="e38fe-108">In the following example, two classes are declared, `PointTest` and `MainClass`.</span></span> <span data-ttu-id="e38fe-109">`PointTest` のパブリック メンバー `x` および `y` は、`MainClass` から直接アクセスされます。</span><span class="sxs-lookup"><span data-stu-id="e38fe-109">The public members `x` and `y` of `PointTest` are accessed directly from `MainClass`.</span></span>

[!code-csharp[csrefKeywordsModifiers#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#13)]

<span data-ttu-id="e38fe-110">`public` アクセス レベルを [private](private.md) または [protected](protected.md) に変更すると、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e38fe-110">If you change the `public` access level to [private](private.md) or [protected](protected.md), you will get the error message:</span></span>

<span data-ttu-id="e38fe-111">'PointTest.y' はアクセスできない保護レベルになっています。</span><span class="sxs-lookup"><span data-stu-id="e38fe-111">'PointTest.y' is inaccessible due to its protection level.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="e38fe-112">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="e38fe-112">C# language specification</span></span>  

<span data-ttu-id="e38fe-113">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[宣言されたアクセシビリティ](~/_csharplang/spec/basic-concepts.md#declared-accessibility)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e38fe-113">For more information, see [Declared accessibility](~/_csharplang/spec/basic-concepts.md#declared-accessibility) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="e38fe-114">言語仕様は、C# の構文と使用法に関する信頼性のある情報源です。</span><span class="sxs-lookup"><span data-stu-id="e38fe-114">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="e38fe-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="e38fe-115">See also</span></span>

- [<span data-ttu-id="e38fe-116">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="e38fe-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="e38fe-117">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="e38fe-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="e38fe-118">アクセス修飾子</span><span class="sxs-lookup"><span data-stu-id="e38fe-118">Access Modifiers</span></span>](../../programming-guide/classes-and-structs/access-modifiers.md)
- [<span data-ttu-id="e38fe-119">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="e38fe-119">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="e38fe-120">アクセス修飾子</span><span class="sxs-lookup"><span data-stu-id="e38fe-120">Access Modifiers</span></span>](access-modifiers.md)
- [<span data-ttu-id="e38fe-121">アクセシビリティ レベル</span><span class="sxs-lookup"><span data-stu-id="e38fe-121">Accessibility Levels</span></span>](accessibility-levels.md)
- [<span data-ttu-id="e38fe-122">修飾子</span><span class="sxs-lookup"><span data-stu-id="e38fe-122">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="e38fe-123">private</span><span class="sxs-lookup"><span data-stu-id="e38fe-123">private</span></span>](private.md)
- [<span data-ttu-id="e38fe-124">protected</span><span class="sxs-lookup"><span data-stu-id="e38fe-124">protected</span></span>](protected.md)
- [<span data-ttu-id="e38fe-125">internal</span><span class="sxs-lookup"><span data-stu-id="e38fe-125">internal</span></span>](internal.md)