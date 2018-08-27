---
title: 値のオプション (f#)
description: オプションの種類の構造体のバージョンでは、f# の値のオプションの種類について説明します。
ms.date: 06/16/2018
ms.openlocfilehash: 4c255cbbcfd9cb480230de09cd370a401c87343a
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42936577"
---
# <a name="value-options"></a><span data-ttu-id="34784-103">値のオプション</span><span class="sxs-lookup"><span data-stu-id="34784-103">Value Options</span></span>

<span data-ttu-id="34784-104">F# の値のオプションの種類は、次の 2 つの状況を保持しているときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="34784-104">The Value Option type in F# is used when the following two circumstances hold:</span></span>

1. <span data-ttu-id="34784-105">シナリオに適した、 [f# オプション](options.md)します。</span><span class="sxs-lookup"><span data-stu-id="34784-105">A scenario is appropriate for an [F# Option](options.md).</span></span>
2. <span data-ttu-id="34784-106">構造体を使用して自分のシナリオでパフォーマンス上の利点を提供します。</span><span class="sxs-lookup"><span data-stu-id="34784-106">Using a struct provides a performance benefit in your scenario.</span></span>

<span data-ttu-id="34784-107">すべてのパフォーマンスが重視されるシナリオは、構造体を使用して、「解決」されます。</span><span class="sxs-lookup"><span data-stu-id="34784-107">Not all performance-sensitive scenarios are "solved" by using structs.</span></span> <span data-ttu-id="34784-108">参照型の代わりに使用するときに、コピーの追加のコストを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34784-108">You must consider the additional cost of copying when using them instead of reference types.</span></span> <span data-ttu-id="34784-109">ただし、構造体は、プログラムの有効期間の全体的なパフォーマンスが向上を得場合がありますので、大規模な f# プログラムによってホット パスを通過する多くの省略可能な型がよくインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="34784-109">However, large F# programs commonly instantiate many optional types that flow through hot paths, because structs can sometimes yield better overall performance over the lifetime of a program.</span></span>

## <a name="definition"></a><span data-ttu-id="34784-110">定義</span><span class="sxs-lookup"><span data-stu-id="34784-110">Definition</span></span>

<span data-ttu-id="34784-111">として値オプションが定義されている、[構造体の判別共用体](discriminated-unions.md#struct-discriminated-unions)参照オプションの種類に似ています。</span><span class="sxs-lookup"><span data-stu-id="34784-111">Value Option is defined as a [struct discriminated union](discriminated-unions.md#struct-discriminated-unions) that is similar to the reference option type:</span></span>

```fsharp
[<StructuralEquality; StructuralComparison>]
[<CompiledName("FSharpValueOption`1")>]
[<Struct>]
type ValueOption<'T> =
    | ValueNone: 'T voption
    | ValueSome: 'T -> 'T voption

    member Value : 'T

and 'T voption = ValueOption<'T>
```

<span data-ttu-id="34784-112">構造の等値と比較する値のオプションが準拠しています。</span><span class="sxs-lookup"><span data-stu-id="34784-112">Value Option conforms to structural equality and comparison.</span></span> <span data-ttu-id="34784-113">主な違いは、あるコンパイル済みの名前、型名、および大文字と小文字の名前を示す値型であります。</span><span class="sxs-lookup"><span data-stu-id="34784-113">The main difference is that the compiled name, type name, and case names all indicate that it is a value type.</span></span>

## <a name="using-value-options"></a><span data-ttu-id="34784-114">値のオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="34784-114">Using Value Options</span></span>

<span data-ttu-id="34784-115">値のオプションを使用して同様[オプション](options.md)します。</span><span class="sxs-lookup"><span data-stu-id="34784-115">Value Options are used just like [Options](options.md).</span></span> <span data-ttu-id="34784-116">`ValueSome` 値が存在することを示すために使用し、`ValueNone`値が存在しない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="34784-116">`ValueSome` is used to indicate that a value is present, and `ValueNone` is used when a value is not present:</span></span>

```fsharp
let tryParseDateTime (s: string) =
    match System.DateTime.TryParse(s) with
    | (true, dt) -> ValueSome dt
    | (false, _) -> ValueNone

let possibleDateString1 = "1990-12-25"
let possibleDateString2 = "This is not a date"

let result1 = tryParseDateTime possibleDateString1
let result2 = tryParseDateTime possibleDateString2

match (result1, result2) with
| ValueSome d1, ValueSome d2 -> printfn "Both are dates!"
| ValueSome d1, ValueNone -> printfn "Only the first is a date!"
| ValueNone, ValueSome d2 -> printfn "Only the second is a date!"
| ValueNone, ValueNone -> printfn "None of them are dates!"
```

<span data-ttu-id="34784-117">同様[オプション](options.md)を返す関数の名前付け規則`ValueOption`の前にプレフィックスが、`try`します。</span><span class="sxs-lookup"><span data-stu-id="34784-117">As with [Options](options.md), the naming convention for a function that returns `ValueOption` is to prefix it with `try`.</span></span>

## <a name="value-option-properties-and-methods"></a><span data-ttu-id="34784-118">オプションの値のプロパティとメソッド</span><span class="sxs-lookup"><span data-stu-id="34784-118">Value Option properties and methods</span></span>

<span data-ttu-id="34784-119">この時点で値のオプションの 1 つのプロパティがある:`Value`します。</span><span class="sxs-lookup"><span data-stu-id="34784-119">There is one property for Value Options at this time: `Value`.</span></span> <span data-ttu-id="34784-120"><xref:System.InvalidOperationException>値には、このプロパティの呼び出し時に存在するがない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="34784-120">An <xref:System.InvalidOperationException> is raised if no value is present when this property is invoked.</span></span>

## <a name="value-option-functions"></a><span data-ttu-id="34784-121">オプションの値関数</span><span class="sxs-lookup"><span data-stu-id="34784-121">Value Option functions</span></span>

<span data-ttu-id="34784-122">値のオプションの 1 つのモジュール連結関数が現在`defaultValueArg`:</span><span class="sxs-lookup"><span data-stu-id="34784-122">There is currently one module-bound function for Value Options, `defaultValueArg`:</span></span>

```fsharp
val defaultValueArg : arg:'T voption -> defaultValue:'T -> 'T 
```

<span data-ttu-id="34784-123">同様、`defaultArg`関数、`defaultValueArg`特定値オプションの基になる値を返しますが存在する。 それ以外の場合、指定した既定値を返します。</span><span class="sxs-lookup"><span data-stu-id="34784-123">As with the `defaultArg` function, `defaultValueArg` returns the underlying value of the given Value Option if it exists; otherwise, it returns the specified default value.</span></span>

<span data-ttu-id="34784-124">この時点では、値のオプションの場合は、他のモジュール連結関数はありません。</span><span class="sxs-lookup"><span data-stu-id="34784-124">At this time, there are no other module-bound functions for Value Options.</span></span>

## <a name="see-also"></a><span data-ttu-id="34784-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="34784-125">See also</span></span>

[<span data-ttu-id="34784-126">オプション</span><span class="sxs-lookup"><span data-stu-id="34784-126">Options</span></span>](options.md)