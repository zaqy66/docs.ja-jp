---
title: private キーワード (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- private_CSharpKeyword
- private
helpviewer_keywords:
- private keyword [C#]
ms.assetid: 654c0bb8-e6ac-4086-bf96-7474fa6aa1c8
ms.openlocfilehash: a817f3f60b76b51868c5cacd8e648ec10497f64a
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53131002"
---
# <a name="private-c-reference"></a><span data-ttu-id="e21be-102">private (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="e21be-102">private (C# Reference)</span></span>

<span data-ttu-id="e21be-103">`private` キーワードはメンバー アクセス修飾子です。</span><span class="sxs-lookup"><span data-stu-id="e21be-103">The `private` keyword is a member access modifier.</span></span>

> <span data-ttu-id="e21be-104">このページでは、`private` アクセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e21be-104">This page covers `private` access.</span></span> <span data-ttu-id="e21be-105">`private` キーワードも [`private protected`](./private-protected.md) アクセス修飾子に含まれます。</span><span class="sxs-lookup"><span data-stu-id="e21be-105">The `private` keyword is also part of the [`private protected`](./private-protected.md) access modifier.</span></span>

<span data-ttu-id="e21be-106">プライベート アクセスは、最も制限の多いアクセス レベルです。</span><span class="sxs-lookup"><span data-stu-id="e21be-106">Private access is the least permissive access level.</span></span> <span data-ttu-id="e21be-107">次の例に示すように、プライベート メンバーは、宣言されているクラスまたは構造体の本体内でのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e21be-107">Private members are accessible only within the body of the class or the struct in which they are declared, as in this example:</span></span>

```csharp
class Employee
{
    private int i;
    double d;   // private access by default
}
```

<span data-ttu-id="e21be-108">同じ本体にある入れ子にされた型も、プライベート メンバーにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e21be-108">Nested types in the same body can also access those private members.</span></span>

<span data-ttu-id="e21be-109">プライベート メンバーへの参照を、クラスの外側やメンバーが宣言されているクラスの外側から行った場合は、コンパイル時のエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e21be-109">It is a compile-time error to reference a private member outside the class or the struct in which it is declared.</span></span>

<span data-ttu-id="e21be-110">`private` とその他のアクセス修飾子の比較については、「[アクセシビリティ レベル](accessibility-levels.md)」と「[アクセス修飾子](../../programming-guide/classes-and-structs/access-modifiers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e21be-110">For a comparison of `private` with the other access modifiers, see [Accessibility Levels](accessibility-levels.md) and [Access Modifiers](../../programming-guide/classes-and-structs/access-modifiers.md).</span></span>

## <a name="example"></a><span data-ttu-id="e21be-111">例</span><span class="sxs-lookup"><span data-stu-id="e21be-111">Example</span></span>

<span data-ttu-id="e21be-112">この例では、`Employee` クラスに `name` と `salary` という 2 つのプライベート データ メンバーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e21be-112">In this example, the `Employee` class contains two private data members, `name` and `salary`.</span></span> <span data-ttu-id="e21be-113">これらのメンバーは、プライベート メンバーであり、メンバー メソッド以外からはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="e21be-113">As private members, they cannot be accessed except by member methods.</span></span> <span data-ttu-id="e21be-114">`GetName` と `Salary` というパブリック メソッドが追加されており、プライベート メンバーへの制御されたアクセスが許可されています。</span><span class="sxs-lookup"><span data-stu-id="e21be-114">Public methods named `GetName` and `Salary` are added to allow controlled access to the private members.</span></span> <span data-ttu-id="e21be-115">`name` メンバーはパブリック メソッドを通してアクセスされ、`salary` メンバーはパブリックな読み取り専用プロパティを通してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="e21be-115">The `name` member is accessed by way of a public method, and the `salary` member is accessed by way of a public read-only property.</span></span> <span data-ttu-id="e21be-116">(詳細については、「[プロパティ](../../programming-guide/classes-and-structs/properties.md)」を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="e21be-116">(See [Properties](../../programming-guide/classes-and-structs/properties.md) for more information.)</span></span>

[!code-csharp[csrefKeywordsModifiers#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#10)]

## <a name="c-language-specification"></a><span data-ttu-id="e21be-117">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="e21be-117">C# language specification</span></span>  

<span data-ttu-id="e21be-118">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[宣言されたアクセシビリティ](~/_csharplang/spec/basic-concepts.md#declared-accessibility)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e21be-118">For more information, see [Declared accessibility](~/_csharplang/spec/basic-concepts.md#declared-accessibility) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="e21be-119">言語仕様は、C# の構文と使用法に関する信頼性のある情報源です。</span><span class="sxs-lookup"><span data-stu-id="e21be-119">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="e21be-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="e21be-120">See also</span></span>

- [<span data-ttu-id="e21be-121">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="e21be-121">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="e21be-122">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="e21be-122">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="e21be-123">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="e21be-123">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="e21be-124">アクセス修飾子</span><span class="sxs-lookup"><span data-stu-id="e21be-124">Access Modifiers</span></span>](access-modifiers.md)
- [<span data-ttu-id="e21be-125">アクセシビリティ レベル</span><span class="sxs-lookup"><span data-stu-id="e21be-125">Accessibility Levels</span></span>](accessibility-levels.md)
- [<span data-ttu-id="e21be-126">修飾子</span><span class="sxs-lookup"><span data-stu-id="e21be-126">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="e21be-127">public</span><span class="sxs-lookup"><span data-stu-id="e21be-127">public</span></span>](public.md)
- [<span data-ttu-id="e21be-128">protected</span><span class="sxs-lookup"><span data-stu-id="e21be-128">protected</span></span>](protected.md)
- [<span data-ttu-id="e21be-129">internal</span><span class="sxs-lookup"><span data-stu-id="e21be-129">internal</span></span>](internal.md)