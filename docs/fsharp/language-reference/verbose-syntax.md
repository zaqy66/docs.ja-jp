---
title: 冗語構文 (F#)
description: F# プログラミング言語の詳細であり、軽量構文の違いについて説明します。
ms.date: 05/16/2016
ms.openlocfilehash: b4f2354738da4692cb444e5e7dd9531d80d26664
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44063119"
---
# <a name="verbose-syntax"></a><span data-ttu-id="e50c9-103">冗語構文</span><span class="sxs-lookup"><span data-stu-id="e50c9-103">Verbose Syntax</span></span>

<span data-ttu-id="e50c9-104">F# 言語で多くの構成要素に使用できる 2 つの形式の構文は:*冗語構文*と*軽量構文*します。</span><span class="sxs-lookup"><span data-stu-id="e50c9-104">There are two forms of syntax available for many constructs in the F# language: *verbose syntax* and *lightweight syntax*.</span></span> <span data-ttu-id="e50c9-105">冗語構文は、一般的に使用されませんが、インデントを受けにくくなるという利点があります。</span><span class="sxs-lookup"><span data-stu-id="e50c9-105">The verbose syntax is not as commonly used, but has the advantage of being less sensitive to indentation.</span></span> <span data-ttu-id="e50c9-106">などの他のキーワード、軽量構文が短いとインデントを先頭と末尾、コンストラクトの使用ではなく`begin`、 `end`、`in`など。</span><span class="sxs-lookup"><span data-stu-id="e50c9-106">The lightweight syntax is shorter and uses indentation to signal the beginning and end of constructs, rather than additional keywords like `begin`, `end`, `in`, and so on.</span></span> <span data-ttu-id="e50c9-107">既定の構文は、軽量構文です。</span><span class="sxs-lookup"><span data-stu-id="e50c9-107">The default syntax is the lightweight syntax.</span></span> <span data-ttu-id="e50c9-108">このトピックでは、軽量構文が有効でない場合、f# の構成要素の構文をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e50c9-108">This topic describes the syntax for F# constructs when lightweight syntax is not enabled.</span></span> <span data-ttu-id="e50c9-109">冗語構文はのでまま一部のコンストラクトの冗語構文を使用することができる場合でも、軽量構文を有効にすると、常に有効です。</span><span class="sxs-lookup"><span data-stu-id="e50c9-109">Verbose syntax is always enabled, so even if you enable lightweight syntax, you can still use verbose syntax for some constructs.</span></span> <span data-ttu-id="e50c9-110">使用して軽量構文を無効にすることができます、`#light "off"`ディレクティブ。</span><span class="sxs-lookup"><span data-stu-id="e50c9-110">You can disable lightweight syntax by using the `#light "off"` directive.</span></span>

## <a name="table-of-constructs"></a><span data-ttu-id="e50c9-111">テーブルの構成体</span><span class="sxs-lookup"><span data-stu-id="e50c9-111">Table of Constructs</span></span>

<span data-ttu-id="e50c9-112">次の表では、f# 言語コンストラクトの軽量と詳細な構文を示しますのコンテキストで 2 つの形式の違いがあります。</span><span class="sxs-lookup"><span data-stu-id="e50c9-112">The following table shows the lightweight and verbose syntax for F# language constructs in contexts where there is a difference between the two forms.</span></span> <span data-ttu-id="e50c9-113">この表では、角度を角かっこ (&lt;&gt;) 構文のユーザーが指定した要素で囲みます。</span><span class="sxs-lookup"><span data-stu-id="e50c9-113">In this table, angle brackets (&lt;&gt;) enclose user-supplied syntax elements.</span></span> <span data-ttu-id="e50c9-114">これらのコンストラクト内で使用される構文の詳細情報の各言語構成要素は、ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e50c9-114">Refer to the documentation for each language construct for more detailed information about the syntax used within these constructs.</span></span>

<table>
<tr>
<th><span data-ttu-id="e50c9-115">言語構成要素</span><span class="sxs-lookup"><span data-stu-id="e50c9-115">Language construct</span></span></th>
<th><span data-ttu-id="e50c9-116">軽量構文</span><span class="sxs-lookup"><span data-stu-id="e50c9-116">Lightweight syntax</span></span></th>
<th><span data-ttu-id="e50c9-117">冗語構文</span><span class="sxs-lookup"><span data-stu-id="e50c9-117">Verbose syntax</span></span></th>
</tr>
<tr>
<td>
<span data-ttu-id="e50c9-118">複合式</span><span class="sxs-lookup"><span data-stu-id="e50c9-118">compound expressions</span></span>
</td>
<td>

```xml
<expression1>
<expression2>
```
</td><td>

```
<expression1>; <expression2>
```

</td>
</tr>
<tr><td>


<span data-ttu-id="e50c9-119">入れ子になった`let`バインド</span><span class="sxs-lookup"><span data-stu-id="e50c9-119">nested `let` bindings</span></span>

</td><td>
```
let f x =
    let a = 1
    let b = 2
    x + a + b
```

</td><td>

```
let f x =
    let a = 1 in
    let b = 2 in
    x + a + b
```

</td>
</tr>
<tr><td>
<span data-ttu-id="e50c9-120">コード ブロック</span><span class="sxs-lookup"><span data-stu-id="e50c9-120">code block</span></span>
</td><td>

```
(
    <expression1>
    <expression2>
)
```

</td><td>

```
begin
    <expression1>;
    <expression2>;
end
```
</td>
</tr>
<tr><td>
`for...do`
</td><td>

```
for counter = start to finish do
    ...
```

</td><td>

```
for counter = start to finish do
    ...
done
```

</td>
</tr>
<tr><td>
`while...do`
</td><td>

```
while <condition> do
    ...
```

</td><td>

```
while <condition> do
    ...
done
```

</td>
</tr>
<tr><td>
`for...in`
</td><td>

```
for var in start .. finish do
    ...
```

</td><td>

```
for var in start .. finish do
    ...
done
```

</td>
</tr>
<tr><td>
`do`
</td><td>

```
do
    ...
```

</td><td>

```
do
    ...
in
```

</td>
</tr>
<tr><td><span data-ttu-id="e50c9-121">レコード</span><span class="sxs-lookup"><span data-stu-id="e50c9-121">record</span></span>
</td><td>

```
type <record-name> =
    {
        <field-declarations>
    }
    <value-or-member-definitions>
```

</td><td>

```
type <record-name> =
    {
        <field-declarations>
    }
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="e50c9-122">class</span><span class="sxs-lookup"><span data-stu-id="e50c9-122">class</span></span>
</td><td><span data-ttu-id="e50c9-123">
```
type <class-name>(<params>) = ... ```

</span><span class="sxs-lookup"><span data-stu-id="e50c9-123">
```
type <class-name>(<params>) = ... ```

</span></span></td><td>

```
type <class-name>(<params>) =
    class
        ...
    end
```
</td>
</tr>
<tr><td><span data-ttu-id="e50c9-124">構造体</span><span class="sxs-lookup"><span data-stu-id="e50c9-124">structure</span></span></td><td>

```
[<StructAttribute>]
type <structure-name> =
    ...
```
</td><td>

```
type <structure-name> =
    struct
        ...
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="e50c9-125">判別共用体</span><span class="sxs-lookup"><span data-stu-id="e50c9-125">discriminated union</span></span></td><td>

```
type <union-name> =
    | ...
    | ...
    ...
    <value-or-member definitions>
```
</td><td>

```
type <union-name> =
    | ...
    | ...
    ...
    with
        <value-or-member-definitions>
    end    
```

</td>
</tr>
<tr><td><span data-ttu-id="e50c9-126">interface</span><span class="sxs-lookup"><span data-stu-id="e50c9-126">interface</span></span></td><td>

```
type <interface-name> =
    ...
```
</td><td>

```
type <interface-name> =
    interface
        ...
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="e50c9-127">オブジェクト式</span><span class="sxs-lookup"><span data-stu-id="e50c9-127">object expression</span></span></td><td>

```
{ new <type-name>
    with
        <value-or-member-definitions>
        <interface-implementations>
}
```

</td><td>

```
{ new <type-name>
    with
        <value-or-member-definitions>
    end
    <interface-implementations>
}
```

</td>
</tr>
<tr><td><span data-ttu-id="e50c9-128">インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="e50c9-128">interface implementation</span></span></td><td>

```
interface <interface-name>
    with
        <value-or-member-definitions>
```

</td><td>

```
interface <interface-name>
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="e50c9-129">型の拡張機能</span><span class="sxs-lookup"><span data-stu-id="e50c9-129">type extension</span></span></td><td>

```
type <type-name>
    with
        <value-or-member-definitions>
```

</td><td>

```
type <type-name>
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="e50c9-130">name</span><span class="sxs-lookup"><span data-stu-id="e50c9-130">module</span></span></td><td>

```
module <module-name> =
    ...
```

</td><td>

```
module <module-name> =
    begin
        ...
    end
```

</td>
</tr>
</table>

## <a name="see-also"></a><span data-ttu-id="e50c9-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="e50c9-131">See also</span></span>

- [<span data-ttu-id="e50c9-132">F# 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="e50c9-132">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="e50c9-133">コンパイラ ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="e50c9-133">Compiler Directives</span></span>](compiler-directives.md)
- [<span data-ttu-id="e50c9-134">コードのフォーマットに関するガイドライン</span><span class="sxs-lookup"><span data-stu-id="e50c9-134">Code Formatting Guidelines</span></span>](code-formatting-guidelines.md)
