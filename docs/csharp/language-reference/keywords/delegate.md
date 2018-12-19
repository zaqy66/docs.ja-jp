---
title: delegate - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- delegate_CSharpKeyword
- delegate
- CS0123
helpviewer_keywords:
- delegate keyword [C#]
- function pointers [C#]
ms.assetid: 0bb8cb6d-2f87-47c7-9d1f-d65c1cd01e9f
ms.openlocfilehash: 233b0255121cf6e7a5283041d594e2d843f105fb
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286469"
---
# <a name="delegate-c-reference"></a><span data-ttu-id="de907-102">delegate (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="de907-102">delegate (C# Reference)</span></span>

<span data-ttu-id="de907-103">デリゲート型の宣言は、メソッド シグネチャに似ています。</span><span class="sxs-lookup"><span data-stu-id="de907-103">The declaration of a delegate type is similar to a method signature.</span></span> <span data-ttu-id="de907-104">戻り値 1 つのほか、任意の型のパラメーターをいくつでも指定することができます。</span><span class="sxs-lookup"><span data-stu-id="de907-104">It has a return value and any number of parameters of any type:</span></span>

```csharp
public delegate void TestDelegate(string message);
public delegate int TestDelegate(MyType m, long num);
```

<span data-ttu-id="de907-105">`delegate` は、名前付きメソッドまたは匿名メソッドをカプセル化することができる参照型です。</span><span class="sxs-lookup"><span data-stu-id="de907-105">A `delegate` is a reference type that can be used to encapsulate a named or an anonymous method.</span></span> <span data-ttu-id="de907-106">デリゲートは C++ の関数ポインターに似ていますが、タイプ セーフであり安全です。</span><span class="sxs-lookup"><span data-stu-id="de907-106">Delegates are similar to function pointers in C++; however, delegates are type-safe and secure.</span></span> <span data-ttu-id="de907-107">デリゲートの使い方については、[デリゲート](../../../csharp/programming-guide/delegates/index.md)と[汎用デリゲート](../../../csharp/programming-guide/generics/generic-delegates.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de907-107">For applications of delegates, see [Delegates](../../../csharp/programming-guide/delegates/index.md) and [Generic Delegates](../../../csharp/programming-guide/generics/generic-delegates.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="de907-108">コメント</span><span class="sxs-lookup"><span data-stu-id="de907-108">Remarks</span></span>

<span data-ttu-id="de907-109">デリゲートは[イベント](../../../csharp/programming-guide/events/index.md)の土台となる働きをします。</span><span class="sxs-lookup"><span data-stu-id="de907-109">Delegates are the basis for [Events](../../../csharp/programming-guide/events/index.md).</span></span>

<span data-ttu-id="de907-110">デリゲートは名前付きメソッドまたは匿名メソッドに関連付けることによって、インスタンス化することができます。</span><span class="sxs-lookup"><span data-stu-id="de907-110">A delegate can be instantiated by associating it either with a named or anonymous method.</span></span> <span data-ttu-id="de907-111">詳細については、[名前付きメソッド](../../../csharp/programming-guide/delegates/delegates-with-named-vs-anonymous-methods.md)と[匿名メソッド](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de907-111">For more information, see [Named Methods](../../../csharp/programming-guide/delegates/delegates-with-named-vs-anonymous-methods.md) and [Anonymous Methods](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md).</span></span>

<span data-ttu-id="de907-112">デリゲートは、適合する入力パラメーターと戻り値の型を持ったメソッドまたはラムダ式でインスタンス化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de907-112">The delegate must be instantiated with a method or lambda expression that has a compatible return type and input parameters.</span></span> <span data-ttu-id="de907-113">メソッドのシグネチャでどの程度の変性が許容されるかについて詳しくは、[デリゲートの変性](../../programming-guide/concepts/covariance-contravariance/using-variance-in-delegates.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de907-113">For more information on the degree of variance that is allowed in the method signature, see [Variance in Delegates](../../programming-guide/concepts/covariance-contravariance/using-variance-in-delegates.md).</span></span> <span data-ttu-id="de907-114">匿名メソッドで使用する場合は、デリゲートとそれに関連付けるコードとを一緒に宣言します。</span><span class="sxs-lookup"><span data-stu-id="de907-114">For use with anonymous methods, the delegate and the code to be associated with it are declared together.</span></span> <span data-ttu-id="de907-115">このセクションでは、その両方の方法でデリゲートをインスタンス化しています。</span><span class="sxs-lookup"><span data-stu-id="de907-115">Both ways of instantiating delegates are discussed in this section.</span></span>

## <a name="example"></a><span data-ttu-id="de907-116">例</span><span class="sxs-lookup"><span data-stu-id="de907-116">Example</span></span>

[!code-csharp[csrefKeywordsTypes#8](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#8)]

## <a name="c-language-specification"></a><span data-ttu-id="de907-117">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="de907-117">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="de907-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="de907-118">See also</span></span>

- [<span data-ttu-id="de907-119">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="de907-119">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="de907-120">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="de907-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="de907-121">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="de907-121">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="de907-122">参照型</span><span class="sxs-lookup"><span data-stu-id="de907-122">Reference Types</span></span>](../../../csharp/language-reference/keywords/reference-types.md)  
- [<span data-ttu-id="de907-123">デリゲート</span><span class="sxs-lookup"><span data-stu-id="de907-123">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)  
- [<span data-ttu-id="de907-124">イベント</span><span class="sxs-lookup"><span data-stu-id="de907-124">Events</span></span>](../../../csharp/programming-guide/events/index.md)  
- [<span data-ttu-id="de907-125">名前付きメソッドを使用したデリゲートと匿名メソッドを使用したデリゲート</span><span class="sxs-lookup"><span data-stu-id="de907-125">Delegates with Named vs. Anonymous Methods</span></span>](../../../csharp/programming-guide/delegates/delegates-with-named-vs-anonymous-methods.md) 
- [<span data-ttu-id="de907-126">匿名メソッド</span><span class="sxs-lookup"><span data-stu-id="de907-126">Anonymous Methods</span></span>](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md)
- [<span data-ttu-id="de907-127">ラムダ式</span><span class="sxs-lookup"><span data-stu-id="de907-127">Lambda Expressions</span></span>](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)
