---
title: 参照セル (F#)
description: F# の参照セルの参照セマンティクスを持つ変更可能な値を作成するための記憶域の場所の方法について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: 133aec6b162a13306a05c9afa172f859890565eb
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43892423"
---
# <a name="reference-cells"></a>参照セル

*参照セル*参照セマンティクスを持つ変更可能な値を作成するための記憶域の場所します。

## <a name="syntax"></a>構文

```fsharp
ref expression
```

## <a name="remarks"></a>Remarks

値をカプセル化する新しい参照セルを作成するには、値の前に `ref` 演算子を指定します。 基になる値は変更可能なので、後で変更できます。

参照セルは、単なるアドレスではなく、実際の値を保持します。 `ref` 演算子を使用して参照セルを作成すると、基の値のコピーが、カプセル化された変更可能な値として作成されます。

参照セルを逆参照するには、`!` (感嘆符) 演算子を使用します。

次のコード例は、参照セルの宣言と使用方法を示しています。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2201.fs)]

出力は `50`になります。

参照セルは、次のように宣言される `Ref` ジェネリック レコード型のインスタンスです。

```fsharp
type Ref<'a> =
{ mutable contents: 'a }
```

`'a ref` 型は、`Ref<'a>` のシノニムです。 コンパイラと IDE の IntelliSense では、この型について前者が表示されますが、基になる定義は後者です。

`ref` 演算子は、新しい参照セルを作成します。 次のコードは、`ref` 演算子の宣言です。

```fsharp
let ref x = { contents = x }
```

次の表に、参照セルで使用できる機能を示します。

|演算子、メンバー、またはフィールド|説明|型|定義|
|--------------------------|-----------|----|----------|
|`!` (逆参照演算子)|基になる値を返します。|`'a ref -> 'a`|`let (!) r = r.contents`|
|`:=` (代入演算子)|基になる値を変更します。|`'a ref -> 'a -> unit`|`let (:=) r x = r.contents <- x`|
|`ref` (演算子)|新しい参照セルに値をカプセル化します。|`'a -> 'a ref`|`let ref x = { contents = x }`|
|`Value` (プロパティ)|基になる値を取得または設定します。|`unit -> 'a`|`member x.Value = x.contents`|
|`contents` (レコード フィールド)|基になる値を取得または設定します。|`'a`|`let ref x = { contents = x }`|
基になる値にアクセスする方法はいくつかあります。 逆参照演算子 (`!`) によって返される値は、代入可能な値ではありません。 したがって、基になる値を変更する場合は、代わりに代入演算子 (`:=`) を使用する必要があります。

`Value` プロパティと `contents` フィールドは、いずれも代入可能な値です。 したがって、次のコードに示すように、これらを使用して基になる値にアクセスしたり、基になる値を変更したりできます。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2203.fs)]

出力は次のとおりです。

```
10
10
11
12
```

`contents` フィールドは、他のバージョンの ML との互換性のために用意されており、コンパイル中に警告を生成します。 この警告を無効にするには、`--mlcompatibility` コンパイラ オプションを使用します。 詳細については、「[コンパイラ オプション](compiler-options.md)」を参照してください。

次のコードは、パラメーターの引き渡しでの参照セルの使用方法を示しています。 インクリメンタ型では、インクリメント、パラメーターの型に byref を含むパラメーターを受け取るメソッドがあります。 Byref パラメーター型で渡すことを示します呼び出しする必要があります参照セルまたは指定した型の典型的な変数のアドレスでこのケースの int です。残りのコードを両方の引数の型とインクリメントを呼び出す方法と参照セル (ref myDelta1) を作成する変数を ref 演算子の使用を示します。 次に、アドレス演算子 (&amp;) を使用して適切な引数を生成する方法を示しています。 最後に、インクリメント メソッドは、let バインドを使用して宣言されている参照セルを使用して、もう一度呼び出されます。 コードの最後の行がの使い方を説明します。 印刷用に参照セルを逆参照演算子。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2204.fs)]

参照渡しする方法の詳細については、次を参照してください。[パラメーターと引数](parameters-and-arguments.md)します。

>[!NOTE]
C# プログラマでは、その ref 異なる動作を f# で c# では、知っておく必要があります。 たとえば、引数を渡すときに、ref の使用はありませんと同じ効果 f# で c# では。

>[!NOTE]
`mutable` 変数に自動的に昇格`'a ref`; クロージャによってキャプチャされた場合は、次を参照してください。[値](values/index.md)します。

## <a name="consuming-c-ref-returns"></a>使用 (C#)`ref`を返します

使用できる f# 4.1 以降、`ref`生成 (C#) を返します。  このような呼び出しの結果は、`byref<_>`ポインター。

次の c# メソッド:

```csharp
namespace RefReturns
{
    public static class RefClass
    {
        public static ref int Find(int val, int[] vals)
        {
            for (int i = 0; i < vals.Length; i++)
            {
                if (vals[i] == val)
                {
                    return ref numbers[i]; // Returns the location, not the value
                }
            }

            throw new IndexOutOfRangeException($"{nameof(number)} not found");
        }
    }
}
```

透過的にで呼び出せるよう f# ない特殊な構文を使用します。

```fsharp
open RefReturns

let consumeRefReturn() =
    let result = RefClass.Find(3, [| 1; 2; 3; 4; 5 |]) // 'result' is of type 'byref<int>'.
    ()
```

かかる場合があります関数を宣言することもできます、`ref`など、入力として返します。

```fsharp
let f (x: byref<int>) = &x
```

現在生成する方法はありません、`ref`戻りで F# で c# で使用できます。

## <a name="see-also"></a>関連項目

- [F# 言語リファレンス](index.md)
- [パラメーターと引数](parameters-and-arguments.md)
- [シンボルと演算子のリファレンス](symbol-and-operator-reference/index.md)
- [値](values/index.md)
