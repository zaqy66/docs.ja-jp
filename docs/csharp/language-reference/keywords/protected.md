---
title: protected キーワード (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- protected
- protected_CSharpKeyword
helpviewer_keywords:
- protected keyword [C#]
ms.assetid: 05ce3794-6675-4025-bddb-eaaa0ec22892
ms.openlocfilehash: 6e3f72226d10910152f7a2139a5a1be35e681ec7
ms.sourcegitcommit: 3b1cb8467bd73dee854b604e306c0e7e3882d91a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "50183179"
---
# <a name="protected-c-reference"></a><span data-ttu-id="856df-102">protected (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="856df-102">protected (C# Reference)</span></span>

<span data-ttu-id="856df-103">`protected` キーワードはメンバー アクセス修飾子です。</span><span class="sxs-lookup"><span data-stu-id="856df-103">The `protected` keyword is a member access modifier.</span></span>

 > <span data-ttu-id="856df-104">このページでは、`protected` アクセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="856df-104">This page covers `protected` access.</span></span> <span data-ttu-id="856df-105">`protected` キーワードもアクセス修飾子の [`protected internal`](protected-internal.md) と [`private protected`](private-protected.md) に含まれます。</span><span class="sxs-lookup"><span data-stu-id="856df-105">The `protected` keyword is also part of the [`protected internal`](protected-internal.md) and [`private protected`](private-protected.md) access modifiers.</span></span>

<span data-ttu-id="856df-106">protected メンバーは、そのクラス内部と、派生クラスのインスタンスからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="856df-106">A protected member is accessible within its class and by derived class instances.</span></span>

<span data-ttu-id="856df-107">`protected` と他のアクセス修飾子の比較については、「[アクセシビリティ レベル](accessibility-levels.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="856df-107">For a comparison of `protected` with the other access modifiers, see [Accessibility Levels](accessibility-levels.md).</span></span>

## <a name="example"></a><span data-ttu-id="856df-108">例</span><span class="sxs-lookup"><span data-stu-id="856df-108">Example</span></span>

<span data-ttu-id="856df-109">派生クラス内で基底クラスの protected メンバーにアクセスできるのは、派生クラスの型を通してアクセスした場合のみです。</span><span class="sxs-lookup"><span data-stu-id="856df-109">A protected member of a base class is accessible in a derived class only if the access occurs through the derived class type.</span></span> <span data-ttu-id="856df-110">たとえば、次のコード セグメントを考えてみます。</span><span class="sxs-lookup"><span data-stu-id="856df-110">For example, consider the following code segment:</span></span>

[!code-csharp[csrefKeywordsModifiers#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#11)]

<span data-ttu-id="856df-111">ステートメント `a.x = 10` でエラーが発生します。これは、クラス B のインスタンスではなく、静的メソッド Main 内にあるためです。</span><span class="sxs-lookup"><span data-stu-id="856df-111">The statement `a.x = 10` generates an error because it is made within the static method Main, and not an instance of class B.</span></span>

<span data-ttu-id="856df-112">構造体は継承できないため、構造体のメンバーを protected にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="856df-112">Struct members cannot be protected because the struct cannot be inherited.</span></span>

## <a name="example"></a><span data-ttu-id="856df-113">例</span><span class="sxs-lookup"><span data-stu-id="856df-113">Example</span></span>

<span data-ttu-id="856df-114">この例では、`DerivedPoint` クラスは `Point` から派生しています。</span><span class="sxs-lookup"><span data-stu-id="856df-114">In this example, the class `DerivedPoint` is derived from `Point`.</span></span> <span data-ttu-id="856df-115">そのため、基底クラスの protected メンバーに、派生クラスから直接アクセスできます。</span><span class="sxs-lookup"><span data-stu-id="856df-115">Therefore, you can access the protected members of the base class directly from the derived class.</span></span>

[!code-csharp[csrefKeywordsModifiers#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#12)]  

<span data-ttu-id="856df-116">`x` と `y` のアクセス レベルを [private](private.md) に変更すると、コンパイラによってエラー メッセージが生成されます。</span><span class="sxs-lookup"><span data-stu-id="856df-116">If you change the access levels of `x` and `y` to [private](private.md), the compiler will issue the error messages:</span></span>

`'Point.y' is inaccessible due to its protection level.`

`'Point.x' is inaccessible due to its protection level.`

## <a name="c-language-specification"></a><span data-ttu-id="856df-117">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="856df-117">C# language specification</span></span>  

<span data-ttu-id="856df-118">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[宣言されたアクセシビリティ](~/_csharplang/spec/basic-concepts.md#declared-accessibility)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="856df-118">For more information, see [Declared accessibility](~/_csharplang/spec/basic-concepts.md#declared-accessibility) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="856df-119">言語仕様は、C# の構文と使用法に関する信頼性のある情報源です。</span><span class="sxs-lookup"><span data-stu-id="856df-119">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="856df-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="856df-120">See also</span></span>

- [<span data-ttu-id="856df-121">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="856df-121">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="856df-122">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="856df-122">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="856df-123">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="856df-123">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="856df-124">アクセス修飾子</span><span class="sxs-lookup"><span data-stu-id="856df-124">Access Modifiers</span></span>](access-modifiers.md)
- [<span data-ttu-id="856df-125">アクセシビリティ レベル</span><span class="sxs-lookup"><span data-stu-id="856df-125">Accessibility Levels</span></span>](accessibility-levels.md)
- [<span data-ttu-id="856df-126">修飾子</span><span class="sxs-lookup"><span data-stu-id="856df-126">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="856df-127">public</span><span class="sxs-lookup"><span data-stu-id="856df-127">public</span></span>](public.md)
- [<span data-ttu-id="856df-128">private</span><span class="sxs-lookup"><span data-stu-id="856df-128">private</span></span>](private.md)
- [<span data-ttu-id="856df-129">internal</span><span class="sxs-lookup"><span data-stu-id="856df-129">internal</span></span>](internal.md)
- <span data-ttu-id="856df-130">[Internal Virtual キーワードのセキュリティ関連事項](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/heyd8kky(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="856df-130">[Security concerns for internal virtual keywords](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/heyd8kky(v=vs.100))</span></span>