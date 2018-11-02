---
title: 構造体 (F#)
description: F# 構造、多くの場合、コンパクトなオブジェクト型について説明しますと少量のデータと動作が単純な型のクラスよりも効率的です。
ms.date: 05/16/2016
ms.openlocfilehash: 08af88132dda28883e246b94585ff4ed8bd2f16a
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "48845301"
---
# <a name="structures"></a><span data-ttu-id="66abc-103">構造体</span><span class="sxs-lookup"><span data-stu-id="66abc-103">Structures</span></span>

<span data-ttu-id="66abc-104">A*構造*は少量のデータと動作が単純ながある型のクラスよりも効率的にできるコンパクトなオブジェクト型です。</span><span class="sxs-lookup"><span data-stu-id="66abc-104">A *structure* is a compact object type that can be more efficient than a class for types that have a small amount of data and simple behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="66abc-105">構文</span><span class="sxs-lookup"><span data-stu-id="66abc-105">Syntax</span></span>

```fsharp
[ attributes ]
type [accessibility-modifier] type-name =
    struct
        type-definition-elements-and-members
    end
// or
[ attributes ]
[<StructAttribute>]
type [accessibility-modifier] type-name =
    type-definition-elements-and-members
```

## <a name="remarks"></a><span data-ttu-id="66abc-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="66abc-106">Remarks</span></span>

<span data-ttu-id="66abc-107">構造体が*値の型*、つまりスタック上で直接、または、として使用している場合、それらが保存されるフィールドまたは配列要素では、親のインラインを入力します。</span><span class="sxs-lookup"><span data-stu-id="66abc-107">Structures are *value types*, which means that they are stored directly on the stack or, when they are used as fields or array elements, inline in the parent type.</span></span> <span data-ttu-id="66abc-108">クラスやレコードとは異なり、構造体のセマンティクスは値渡しです。</span><span class="sxs-lookup"><span data-stu-id="66abc-108">Unlike classes and records, structures have pass-by-value semantics.</span></span> <span data-ttu-id="66abc-109">これは、主にアクセスおよびコピーが頻繁に行われるデータの小規模な集約に有用であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="66abc-109">This means that they are useful primarily for small aggregates of data that are accessed and copied frequently.</span></span>

<span data-ttu-id="66abc-110">上記の構文では、2 つの形式が示されています。</span><span class="sxs-lookup"><span data-stu-id="66abc-110">In the previous syntax, two forms are shown.</span></span> <span data-ttu-id="66abc-111">1 番目のものは軽量構文ではないものの、頻繁に使用されます。これは、`struct` キーワードと `end` キーワードを使用する場合に、2 番目のものに出現する `StructAttribute` 属性を省略できるためです。</span><span class="sxs-lookup"><span data-stu-id="66abc-111">The first is not the lightweight syntax, but it is nevertheless frequently used because, when you use the `struct` and `end` keywords, you can omit the `StructAttribute` attribute, which appears in the second form.</span></span> <span data-ttu-id="66abc-112">`StructAttribute` は省略して単に `Struct` とすることができます。</span><span class="sxs-lookup"><span data-stu-id="66abc-112">You can abbreviate `StructAttribute` to just `Struct`.</span></span>

<span data-ttu-id="66abc-113">*型定義の要素-と-メンバー*前の構文でメンバーの宣言と定義を表します。</span><span class="sxs-lookup"><span data-stu-id="66abc-113">The *type-definition-elements-and-members* in the previous syntax represents member declarations and definitions.</span></span> <span data-ttu-id="66abc-114">構造体にはコンス トラクター、可変フィールド、および不変フィールドを含めることができ、メンバーとインターフェイス実装を宣言できます。</span><span class="sxs-lookup"><span data-stu-id="66abc-114">Structures can have constructors and mutable and immutable fields, and they can declare members and interface implementations.</span></span> <span data-ttu-id="66abc-115">詳細については、次を参照してください。[メンバー](members/index.md)します。</span><span class="sxs-lookup"><span data-stu-id="66abc-115">For more information, see [Members](members/index.md).</span></span>

<span data-ttu-id="66abc-116">構造体は、継承に参加することも、`let` または `do` バインディングを含めることも、それ自身の型のフィールドを再帰的に含めることもできません (ただし、それ自身の型を参照する参照セルを含めることができます)。</span><span class="sxs-lookup"><span data-stu-id="66abc-116">Structures cannot participate in inheritance, cannot contain `let` or `do` bindings, and cannot recursively contain fields of their own type (although they can contain reference cells that reference their own type).</span></span>

<span data-ttu-id="66abc-117">構造体では `let` バインディングは使用できないため、`val` キーワードを使用して構造体のフィールドを宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66abc-117">Because structures do not allow `let` bindings, you must declare fields in structures by using the `val` keyword.</span></span> <span data-ttu-id="66abc-118">`val` キーワードではフィールドとその型が定義されますが、初期化は実行できません。</span><span class="sxs-lookup"><span data-stu-id="66abc-118">The `val` keyword defines a field and its type but does not allow initialization.</span></span> <span data-ttu-id="66abc-119">代わりに、`val` 宣言がゼロまたは null に初期化されます。</span><span class="sxs-lookup"><span data-stu-id="66abc-119">Instead, `val` declarations are initialized to zero or null.</span></span> <span data-ttu-id="66abc-120">このため、暗黙のコンストラクター (宣言で構造体名の直後に指定されるパラメーター) を含む構造体では、`val` 宣言に `DefaultValue` 属性で注釈を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="66abc-120">For this reason, structures that have an implicit constructor (that is, parameters that are given immediately after the structure name in the declaration) require that `val` declarations be annotated with the `DefaultValue` attribute.</span></span> <span data-ttu-id="66abc-121">定義されたコンストラクターを含む構造体でも、ゼロ初期化がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="66abc-121">Structures that have a defined constructor still support zero-initialization.</span></span> <span data-ttu-id="66abc-122">したがって、`DefaultValue` 属性は、このようなゼロ値がフィールドに対して有効であることの宣言になります。</span><span class="sxs-lookup"><span data-stu-id="66abc-122">Therefore, the `DefaultValue` attribute is a declaration that such a zero value is valid for the field.</span></span> <span data-ttu-id="66abc-123">構造体の暗黙的なコンストラクターでは動作は実行されません。これは、`let` バインディングと `do` バインディングがその型では許可されていないためですが、渡された暗黙のコンストラクターのパラメーター値はプライベート フィールドとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="66abc-123">Implicit constructors for structures do not perform any actions because `let` and `do` bindings aren’t allowed on the type, but the implicit constructor parameter values passed in are available as private fields.</span></span>

<span data-ttu-id="66abc-124">明示的なコンストラクターにフィールド値の初期化が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="66abc-124">Explicit constructors might involve initialization of field values.</span></span> <span data-ttu-id="66abc-125">明示的なコンストラクターを含む構造体がある場合も、ゼロ初期化がサポートされます。ただし、明示的なコンストラクターと競合するため、`DefaultValue` 宣言では `val` 属性を使用しません。</span><span class="sxs-lookup"><span data-stu-id="66abc-125">When you have a structure that has an explicit constructor, it still supports zero-initialization; however, you do not use the `DefaultValue` attribute on the `val` declarations because it conflicts with the explicit constructor.</span></span> <span data-ttu-id="66abc-126">詳細については`val`宣言を参照してください[明示的なフィールド:`val`キーワード](members/explicit-fields-the-val-keyword.md)します。</span><span class="sxs-lookup"><span data-stu-id="66abc-126">For more information about `val` declarations, see [Explicit Fields: The `val` Keyword](members/explicit-fields-the-val-keyword.md).</span></span>

<span data-ttu-id="66abc-127">構造体では属性およびアクセシビリティ修飾子が許可されており、その他の型と同じ規則に従います。</span><span class="sxs-lookup"><span data-stu-id="66abc-127">Attributes and accessibility modifiers are allowed on structures, and follow the same rules as those for other types.</span></span> <span data-ttu-id="66abc-128">詳細については、次を参照してください。[属性](attributes.md)と[アクセス制御](access-control.md)します。</span><span class="sxs-lookup"><span data-stu-id="66abc-128">For more information, see [Attributes](attributes.md) and [Access Control](access-control.md).</span></span>

<span data-ttu-id="66abc-129">次のコード例は構造体の定義を示しています。</span><span class="sxs-lookup"><span data-stu-id="66abc-129">The following code examples illustrate structure definitions.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2501.fs)]

## <a name="byreflike-structs"></a><span data-ttu-id="66abc-130">ByRefLike 構造体</span><span class="sxs-lookup"><span data-stu-id="66abc-130">ByRefLike structs</span></span>

<span data-ttu-id="66abc-131">従うことができます独自の構造体を定義する`byref`-などのセマンティクス: を参照してください[Byref](byrefs.md)詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="66abc-131">You can define your own structs that can adhere to `byref`-like semantics: see [Byrefs](byrefs.md) for more information.</span></span> <span data-ttu-id="66abc-132">これは、<xref:System.Runtime.CompilerServices.IsByRefLikeAttribute>属性。</span><span class="sxs-lookup"><span data-stu-id="66abc-132">This is done with the <xref:System.Runtime.CompilerServices.IsByRefLikeAttribute> attribute:</span></span>

```fsharp
open System
open System.Runtime.CompilerServices

[<IsByRefLike; Struct>]
type S(count1: Span<int>, count2: Span<int>) =
    member x.Count1 = count1
    member x.Count2 = count2
```

<span data-ttu-id="66abc-133">`IsByRefLike` 限りません`Struct`します。</span><span class="sxs-lookup"><span data-stu-id="66abc-133">`IsByRefLike` does not imply `Struct`.</span></span> <span data-ttu-id="66abc-134">両方は、型に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66abc-134">Both must be present on the type.</span></span>

<span data-ttu-id="66abc-135">A"`byref`のような"F# の構造体はスタック バインド値の型。</span><span class="sxs-lookup"><span data-stu-id="66abc-135">A "`byref`-like" struct in F# is a stack-bound value type.</span></span> <span data-ttu-id="66abc-136">マネージ ヒープに割り当てられることはありません。</span><span class="sxs-lookup"><span data-stu-id="66abc-136">It is never allocated on the managed heap.</span></span> <span data-ttu-id="66abc-137">A `byref`-と同様に、強力な確認については、有効期間と非キャプチャのセットをそのポリシーが適用されて、構造体です、高性能なプログラミングに便利です。</span><span class="sxs-lookup"><span data-stu-id="66abc-137">A `byref`-like struct is useful for high-performance programming, as it is enforced with set of strong checks about lifetime and non-capture.</span></span> <span data-ttu-id="66abc-138">規則は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="66abc-138">The rules are:</span></span>

* <span data-ttu-id="66abc-139">メソッドを返します関数パラメーター、メソッド パラメーター、ローカル変数を使用ができます。</span><span class="sxs-lookup"><span data-stu-id="66abc-139">They can be used as function parameters, method parameters, local variables, method returns.</span></span>
* <span data-ttu-id="66abc-140">静的またはインスタンス クラスまたは構造体を通常のメンバーができません。</span><span class="sxs-lookup"><span data-stu-id="66abc-140">They cannot be static or instance members of a class or normal struct.</span></span>
* <span data-ttu-id="66abc-141">任意のクロージャ コンストラクトをキャプチャできない (`async`メソッドまたはラムダ式)。</span><span class="sxs-lookup"><span data-stu-id="66abc-141">They cannot be captured by any closure construct (`async` methods or lambda expressions).</span></span>
* <span data-ttu-id="66abc-142">これらは、ジェネリック パラメーターとして使用できません。</span><span class="sxs-lookup"><span data-stu-id="66abc-142">They cannot be used as a generic parameter.</span></span>

<span data-ttu-id="66abc-143">これらの規則は、使用状況を制限する非常に強く、それによって、安全な方法でのハイ パフォーマンス コンピューティングの約束を実行するためにします。</span><span class="sxs-lookup"><span data-stu-id="66abc-143">Although these rules very strongly restrict usage, they do so to fulfill the promise of high-performance computing in a safe manner.</span></span>

## <a name="readonly-structs"></a><span data-ttu-id="66abc-144">読み取り専用の構造体</span><span class="sxs-lookup"><span data-stu-id="66abc-144">ReadOnly structs</span></span>

<span data-ttu-id="66abc-145">構造体での注釈を付けることができます、<xref:System.Runtime.CompilerServices.IsReadOnlyAttribute>属性。</span><span class="sxs-lookup"><span data-stu-id="66abc-145">You can annotate structs with the <xref:System.Runtime.CompilerServices.IsReadOnlyAttribute> attribute.</span></span> <span data-ttu-id="66abc-146">例えば:</span><span class="sxs-lookup"><span data-stu-id="66abc-146">For example:</span></span>

```fsharp
[<IsReadOnly; Struct>]
type S(count1: int, count2: int) =
    member x.Count1 = count1
    member x.Count2 = count2
```

<span data-ttu-id="66abc-147">`IsReadOnly` 限りません`Struct`します。</span><span class="sxs-lookup"><span data-stu-id="66abc-147">`IsReadOnly` does not imply `Struct`.</span></span> <span data-ttu-id="66abc-148">両方に追加する必要があります、`IsReadOnly`構造体。</span><span class="sxs-lookup"><span data-stu-id="66abc-148">You must add both to have an `IsReadOnly` struct.</span></span>

<span data-ttu-id="66abc-149">この属性の使用は、F# と c# として扱い、他人に把握できるようにすることのメタデータを出力`inref<'T>`と`in ref`、それぞれします。</span><span class="sxs-lookup"><span data-stu-id="66abc-149">Use of this attribute emits metadata letting F# and C# know to treat it as `inref<'T>` and `in ref`, respectively.</span></span>

<span data-ttu-id="66abc-150">読み取り専用の構造体の内部で変更可能な値を定義するには、エラーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="66abc-150">Defining a mutable value inside of a readonly struct produces an error.</span></span>

## <a name="struct-records-and-discriminated-unions"></a><span data-ttu-id="66abc-151">構造体のレコード、判別共用体</span><span class="sxs-lookup"><span data-stu-id="66abc-151">Struct Records and Discriminated Unions</span></span>

<span data-ttu-id="66abc-152">表すことができます[レコード](records.md)と[判別共用体](discriminated-unions.md)と構造体として、`[<Struct>]`属性。</span><span class="sxs-lookup"><span data-stu-id="66abc-152">You can represent [Records](records.md) and [Discriminated Unions](discriminated-unions.md) as structs with the `[<Struct>]` attribute.</span></span>  <span data-ttu-id="66abc-153">詳細については、各記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66abc-153">See each article to learn more.</span></span>

## <a name="see-also"></a><span data-ttu-id="66abc-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="66abc-154">See also</span></span>

- [<span data-ttu-id="66abc-155">F# 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="66abc-155">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="66abc-156">クラス</span><span class="sxs-lookup"><span data-stu-id="66abc-156">Classes</span></span>](classes.md)
- [<span data-ttu-id="66abc-157">レコード</span><span class="sxs-lookup"><span data-stu-id="66abc-157">Records</span></span>](records.md)
- [<span data-ttu-id="66abc-158">メンバー</span><span class="sxs-lookup"><span data-stu-id="66abc-158">Members</span></span>](members/index.md)
