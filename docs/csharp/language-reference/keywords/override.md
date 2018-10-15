---
title: override 修飾子 (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- override
- override_CSharpKeyword
helpviewer_keywords:
- override keyword [C#]
ms.assetid: dd1907a8-acf8-46d3-80b9-c2ca4febada8
ms.openlocfilehash: cbd5e21e7ca71a4986099a0386c684a6db37c3e8
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44187008"
---
# <a name="override-c-reference"></a><span data-ttu-id="fd211-102">override (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="fd211-102">override (C# Reference)</span></span>

<span data-ttu-id="fd211-103">`override` 修飾子は、継承したメソッド、プロパティ、インデクサー、またはイベントの抽象実装または仮想実装を拡張したり修飾したりする際に必要です。</span><span class="sxs-lookup"><span data-stu-id="fd211-103">The `override` modifier is required to extend or modify the abstract or virtual implementation of an inherited method, property, indexer, or event.</span></span>

## <a name="example"></a><span data-ttu-id="fd211-104">例</span><span class="sxs-lookup"><span data-stu-id="fd211-104">Example</span></span>

<span data-ttu-id="fd211-105">この例では、`Square` クラスが `Area` のオーバーライドされる実装を提供する必要があります。これは、`Area` が抽象 `ShapesClass` から継承されているためです。</span><span class="sxs-lookup"><span data-stu-id="fd211-105">In this example, the `Square` class must provide an overridden implementation of `Area` because `Area` is inherited from the abstract `ShapesClass`:</span></span>

[!code-csharp[csrefKeywordsModifiers#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#1)]

<span data-ttu-id="fd211-106">`override` メソッドは、基底クラスから継承されるメンバーの新しい実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="fd211-106">An `override` method provides a new implementation of a member that is inherited from a base class.</span></span> <span data-ttu-id="fd211-107">`override` 宣言によってオーバーライドされるメソッドを、オーバーライドされる基本メソッドと言います。</span><span class="sxs-lookup"><span data-stu-id="fd211-107">The method that is overridden by an `override` declaration is known as the overridden base method.</span></span> <span data-ttu-id="fd211-108">オーバーライドされる基本メソッドには、`override` メソッドと同じシグネチャが必要です。</span><span class="sxs-lookup"><span data-stu-id="fd211-108">The overridden base method must have the same signature as the `override` method.</span></span> <span data-ttu-id="fd211-109">継承については、「[継承](../../programming-guide/classes-and-structs/inheritance.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd211-109">For information about inheritance, see [Inheritance](../../programming-guide/classes-and-structs/inheritance.md).</span></span>

<span data-ttu-id="fd211-110">非仮想メソッドまたは静的メソッドをオーバーライドすることはできません。</span><span class="sxs-lookup"><span data-stu-id="fd211-110">You cannot override a non-virtual or static method.</span></span> <span data-ttu-id="fd211-111">オーバーライドされる基本メソッドは、`virtual`、`abstract`、`override` のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd211-111">The overridden base method must be `virtual`, `abstract`, or `override`.</span></span>

<span data-ttu-id="fd211-112">`override` 宣言は、`virtual` メソッドのアクセシビリティを変更できません。</span><span class="sxs-lookup"><span data-stu-id="fd211-112">An `override` declaration cannot change the accessibility of the `virtual` method.</span></span> <span data-ttu-id="fd211-113">`override` メソッドと `virtual` メソッドの両方に、同じ[アクセス レベル修飾子](access-modifiers.md)が必要です。</span><span class="sxs-lookup"><span data-stu-id="fd211-113">Both the `override` method and the `virtual` method must have the same [access level modifier](access-modifiers.md).</span></span>

<span data-ttu-id="fd211-114">`override` メソッドの修飾に、修飾子 `new`、`static`、または `virtual` は使用できません。</span><span class="sxs-lookup"><span data-stu-id="fd211-114">You cannot use the `new`, `static`, or `virtual` modifiers to modify an `override` method.</span></span>

<span data-ttu-id="fd211-115">オーバーライドするプロパティの宣言では、継承されるプロパティとまったく同じアクセス修飾子、型、および名前を指定する必要があります。オーバーライドされるプロパティは、`virtual`、`abstract`、または `override` である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd211-115">An overriding property declaration must specify exactly the same access modifier, type, and name as the inherited property, and the overridden property must be `virtual`, `abstract`, or `override`.</span></span>

<span data-ttu-id="fd211-116">`override` キーワードの使い方の詳細については、「[Override キーワードと New キーワードによるバージョン管理](../../programming-guide/classes-and-structs/versioning-with-the-override-and-new-keywords.md)」および「[Override キーワードと New キーワードを使用する場合について](../../programming-guide/classes-and-structs/knowing-when-to-use-override-and-new-keywords.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd211-116">For more information about how to use the `override` keyword, see [Versioning with the Override and New Keywords](../../programming-guide/classes-and-structs/versioning-with-the-override-and-new-keywords.md) and [Knowing when to use Override and New Keywords](../../programming-guide/classes-and-structs/knowing-when-to-use-override-and-new-keywords.md).</span></span>

## <a name="example"></a><span data-ttu-id="fd211-117">例</span><span class="sxs-lookup"><span data-stu-id="fd211-117">Example</span></span>

<span data-ttu-id="fd211-118">この例では、`Employee` という基底クラスと、`SalesEmployee` という派生クラスを定義します。</span><span class="sxs-lookup"><span data-stu-id="fd211-118">This example defines a base class named `Employee`, and a derived class named `SalesEmployee`.</span></span> <span data-ttu-id="fd211-119">`SalesEmployee` クラスには追加のフィールド `salesbonus` があり、このフィールドを処理に含めるために、`CalculatePay` メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="fd211-119">The `SalesEmployee` class includes an extra field, `salesbonus`, and overrides the method `CalculatePay` in order to take it into account.</span></span>

[!code-csharp[csrefKeywordsModifiers#9](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#9)]

## <a name="c-language-specification"></a><span data-ttu-id="fd211-120">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="fd211-120">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="fd211-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="fd211-121">See also</span></span>

- [<span data-ttu-id="fd211-122">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="fd211-122">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="fd211-123">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="fd211-123">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="fd211-124">継承</span><span class="sxs-lookup"><span data-stu-id="fd211-124">Inheritance</span></span>](../../programming-guide/classes-and-structs/inheritance.md)
- [<span data-ttu-id="fd211-125">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="fd211-125">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="fd211-126">修飾子</span><span class="sxs-lookup"><span data-stu-id="fd211-126">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="fd211-127">abstract</span><span class="sxs-lookup"><span data-stu-id="fd211-127">abstract</span></span>](abstract.md)
- [<span data-ttu-id="fd211-128">virtual</span><span class="sxs-lookup"><span data-stu-id="fd211-128">virtual</span></span>](virtual.md)
- [<span data-ttu-id="fd211-129">new</span><span class="sxs-lookup"><span data-stu-id="fd211-129">new</span></span>](new.md)
- [<span data-ttu-id="fd211-130">ポリモーフィズム</span><span class="sxs-lookup"><span data-stu-id="fd211-130">Polymorphism</span></span>](../../programming-guide/classes-and-structs/polymorphism.md)
