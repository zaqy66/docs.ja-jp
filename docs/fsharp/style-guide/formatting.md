---
title: F# コードの書式設定のガイドライン
description: F# コードの書式設定するためのガイドラインについて説明します。
ms.date: 05/14/2018
ms.openlocfilehash: 9c6e80509e9a5654e6514674d38c02e2a6b44e37
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42935938"
---
# <a name="f-code-formatting-guidelines"></a>F# コードの書式設定のガイドライン

この記事では、f# コードが実行されるように、コードを書式設定する方法に関するガイドラインを提供します。

* 一般に読みやすくとして表示
* Visual Studio のツールとその他のエディターの書式設定が適用される規則に従って、します。
* その他のコードをオンラインに似ています

これらのガイドラインに基づいています[f# の書式設定規則に包括的なガイド](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md)によって[Anh 協力 Phan](https://github.com/dungpa)します。

## <a name="general-rules-for-indentation"></a>インデントの一般的な規則

F# で既定では、有意の空白を使用します。 次のガイドラインはこれをかけることがいくつかの課題を使い分ける方法についてのガイダンスを提供するためのものです。

### <a name="using-spaces"></a>スペースを使用します。

インデントが必要な場合は、スペース、タブではなくを使用する必要があります。 少なくとも 1 つの領域が必要です。 組織がインデントに使用する空白文字の数を指定するコーディング規則を作成できます。各レベルのインデントを設定するインデントの 2 つ、3 つまたは 4 つのスペースが一般的です。

**インデントあたり 4 つのスペースをお勧めします。**

ただし、プログラムのインデントは主観的な問題。 バリエーションが [ok] が最初の規則に従う必要がありますが、*インデントの一貫性*します。 インデントの一般的に受け入れられるスタイルを選択し、コードベース全体で体系的に使用します。

## <a name="formatting-blank-lines"></a>空白行を書式設定

* 独立したトップレベル関数やクラスの定義 2 つの空白行を含む。
* クラス内でメソッドの定義は、単一の空白行で区切られます。
* 余分な空白行は、関連する関数のグループを区切る (控えめ) に使用する可能性があります。 一連の関連困ら (たとえば、ダミーの実装のセット) の間の空白行は省略できます。
* 論理的なセクションを示すために、関数では、空白行を使用します。

## <a name="formatting-comments"></a>コメントの書式設定

一般に ML スタイル ブロックのコメントを複数のコメントをダブル スラッシュを好みます。

```fsharp
// Prefer this style of comments when you want
// to express written ideas on multiple lines.

(*
    ML-style comments are fine, but not a .NET-ism.
    They are useful when needing to modify multi-line comments, though.
*)
```

インライン コメントは、最初の文字を大文字にする必要があります。

```fsharp
let f x = x + 1 // Increment by one.
```

## <a name="naming-conventions"></a>名前付け規則

### <a name="use-camelcase-for-class-bound-expression-bound-and-pattern-bound-values-and-functions"></a>キャメル ケースを使用して、クラス バインド、バインド式とパターン バインドの値と関数

一般的な camelCase を使用して、すべての名前を指定できる f# スタイルには、ローカル変数として、またはパターン マッチと関数定義がバインドされています。

```fsharp
// OK
let addIAndJ i j = i + j

// Bad
let addIAndJ I J = I+J

// Bad
let AddIAndJ i j = i + j
```

クラスのローカルにバインドされた関数は、camelCase を使用してもする必要があります。

```fsharp
type MyClass() =

    let doSomething () =

    let firstResult = ...

    let secondResult = ...

    member x.Result = doSomething()
```

### <a name="use-camelcase-for-module-bound-public-functions"></a>キャメル ケースを使用してバインド モジュールのパブリック関数

モジュール連結関数は、パブリック API の一部が、camelCase を使用します。

```fsharp
module MyAPI =
    let publicFunctionOne param1 param2 param2 = ...

    let publicFunctionTwo param1 param2 param3 = ...
```

### <a name="use-camelcase-for-internal-and-private-module-bound-values-and-functions"></a>キャメル ケースを使用して、内部、プライベート モジュール連結値および関数

プライベート モジュール連結値は、次のようには、camelCase を使用します。

* スクリプトでアドホック関数

* モジュールまたは型の内部実装を作成する値

```fsharp
let emailMyBossTheLatestResults =
    ...
```

### <a name="use-camelcase-for-parameters"></a>パラメーターにキャメル ケースを使用します。

すべてのパラメーターは、.NET の名前付け規則に従って、camelCase を使用してください。

```fsharp
module MyModule =
    let myFunction paramOne paramTwo = ...

type MyClass() =
    member this.MyMethod(paramOne, paramTwo) = ...
```

### <a name="use-pascalcase-for-modules"></a>PascalCase モジュールを使用します。

(最上位レベル、内部、プライベートの入れ子になった) のすべてのモジュールは PascalCase を使用する必要があります。

```fsharp
module MyTopLevelModule

module Helpers =
    module private SuperHelpers =
        ...

    ...
```

### <a name="use-pascalcase-for-type-declarations-members-and-labels"></a>PascalCase を使用して、型宣言、メンバー、およびラベル

クラス、インターフェイス、構造体、列挙、デリゲート、レコード、および判別共用体がすべての名前は PascalCase です。 型およびレコード、判別共用体のラベル内のメンバーは、PascalCase を使用してもする必要があります。

```fsharp
type IMyInterface =
    abstract Something: int

type MyClass() =
    member this.MyMethod(x, y) = x + y

type MyRecord = { IntVal: int; StringVal: string }

type SchoolPerson =
    | Professor
    | Student
    | Advisor
    | Administrator
```

### <a name="use-pascalcase-for-constructs-intrinsic-to-net"></a>PascalCase を使用して、.NET に固有の構成要素

名前空間、例外、イベント、およびプロジェクト/`.dll`名も PascalCase を使用します。 だけでなく、これにより、コンシューマーに自然に感じられる他の .NET 言語から消費も発生する可能性がある .NET の名前付け規則と一致します。

### <a name="avoid-underscores-in-names"></a>名前にアンダー スコアを回避します。

従来、一部の f# ライブラリは、名前にアンダー スコアを使用するが。 ただし、これが不要になった広く受け入れられて .NET の名前付け規則と衝突ためです。 ただし、f# プログラマによってアンダー スコアは使用頻度の高い、一部の歴史的な理由と許容範囲と点が重要です。 ただし、スタイルが使用するかどうかの選択肢を持つ他のユーザーによって多くの場合、我慢しなければならないこともあります。

いくつかの例外には、アンダー スコアが非常に一般的であるネイティブのコンポーネントとの相互運用が含まれています。

### <a name="use-standard-f-operators"></a>標準的な f# 演算子を使用します。

次の演算子は、f# の標準ライブラリで定義され、対応を定義する代わりに使用する必要があります。 読みやすく、慣用コードを作成する傾向が、これらの演算子の使用をお勧めします。 OCaml またはその他の関数型プログラミング言語の背景を持つ開発者は、さまざまな表現方法に慣れて可能性があります。 次の一覧は、推奨の f# 演算子をまとめたものです。

```fsharp
x |> f // Forward pipeline
f >> g // Forward composition
x |> ignore // Discard away a value
x + y // Overloaded addition (including string concatenation)
x - y // Overloaded subtraction
x * y // Overloaded multiplication
x / y // Overloaded division
x % y // Overloaded modulus
x && y // Lazy/short-cut "and"
x || y // Lazy/short-cut "or"
x <<< y // Bitwise left shift
x >>> y // Bitwise right shift
x ||| y // Bitwise or, also for working with “flags” enumeration
x &&& y // Bitwise and, also for working with “flags” enumeration
x ^^^ y // Bitwise xor, also for working with “flags” enumeration
```

### <a name="use-prefix-syntax-for-generics-foot-in-preference-to-postfix-syntax-t-foo"></a>ジェネリックのプレフィックスの構文を使用して (`Foo<T>`) 方が優先的後置構文 (`T Foo`)

F# ジェネリック型の名前付けの両方、後置 ML スタイルを継承する (たとえば、 `int list`) .NET スタイルのプレフィックスと (たとえば、 `list<int>`)。 次の 4 つの特定の型を除く、.NET スタイルを優先するには。

1. F# リストは、後置形式を使用:`int list`なく`list<int>`します。
2. F# オプションについては、後置形式を使用:`int option`なく`option<int>`します。
3. F# の配列、構文の名前を使用`int[]`なく`int array`または`array<int>`します。
4. 参照セルを使用して`int ref`なく`ref<int>`または`Ref<int>`します。

他のすべての種類では、前置形式を使用します。

## <a name="formatting-tuples"></a>タプルの書式設定

タプル インスタンス化はかっこで囲まれた、する必要があり、内で使用する区切りコンマをたとえば、1 つのスペースで従う必要が: `(1, 2)`、`(x, y, z)`します。

タプルのパターン マッチングでは、かっこを省略することがよく受け入れられます。

```fsharp
let (x, y) = z // Destructuring
let x, y = z // OK

// OK
match x, y with
| 1, _ -> 0
| x, 1 -> 0
| x, y -> 1
```

## <a name="formatting-discriminated-union-declarations"></a>判別共用体の宣言の書式設定

インデント`|`によって 4 つのスペースの種類の定義。

```fsharp
// OK
type Volume =
    | Liter of float
    | FluidOunce of float
    | ImperialPint of float

// Not OK
type Volume =
| Liter of float
| USPint of float
| ImperialPint of float
```

## <a name="formatting-discriminated-unions"></a>判別共用体の書式設定

複数行にわたって判別の共用体はインスタンス化されたはインデントで新しいスコープに含まれているデータを提供する必要があります。

```fsharp
let tree1 =
    BinaryNode
        (BinaryNode(BinaryValue 1, BinaryValue 2),
         BinaryNode(BinaryValue 3, BinaryValue 4))
```

新しい行の終わりかっこのこともできます。

```fsharp
let tree1 =
    BinaryNode(
        BinaryNode(BinaryValue 1, BinaryValue 2),
        BinaryNode(BinaryValue 3, BinaryValue 4)
    )
```

## <a name="formatting-record-declarations"></a>レコードの宣言を書式設定

インデント`{`4 で定義型で空白し、同じ行にフィールド リストの先頭します。

```fsharp
// OK
type PostalAddress =
    { Address : string
      City : string
      Zip : string }
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City

// Not OK
type PostalAddress =
  { Address : string
    City : string
    Zip : string }
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City
    
// Unusual in F#
type PostalAddress =
    { 
        Address : string
        City : string
        Zip : string
    }
```

問題でも、同じ行で、新しい行に終了トークン開始トークンを配置することですを使用する必要があることに注意してください、[冗語構文](../language-reference/verbose-syntax.md)メンバーを定義する (、`with`キーワード)。

```fsharp
//  OK, but verbose syntax required
type PostalAddress = { 
    Address : string
    City : string
    Zip : string
} with
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City
```

## <a name="formatting-records"></a>レコードを書式設定

1 行では、短いレコードを記述することができます。

```fsharp
let point = { X = 1.0; Y = 0.0 }
```

長いレコードは、新しい行を使用して、ラベルの必要があります。

```fsharp
let rainbow =
    { Boss = "Jeffrey"
      Lackeys = ["Zippy"; "George"; "Bungle"] }
```

開始トークンを同じ行で、新しい行に終了トークン配置することは問題もです。

```fsharp
let rainbow = {
    Boss1 = "Jeffrey"
    Boss2 = "Jeffrey"
    Boss3 = "Jeffrey"
    Boss4 = "Jeffrey"
    Boss5 = "Jeffrey"
    Boss6 = "Jeffrey"
    Boss7 = "Jeffrey"
    Boss8 = "Jeffrey"
    Lackeys = ["Zippy"; "George"; "Bungle"]
}
```

リストと配列の要素の場合と同じ規則が適用されます。

## <a name="formatting-lists-and-arrays"></a>書式設定のリストと配列

書き込み`x :: l`の前後のスペースで、`::`演算子 (`::`が空白で囲まれたため、挿入演算子) と`[1; 2; 3]`(`;`はその後にスペースを区切り記号) です。

常に 2 つの個別の中かっこのような演算子の間に少なくとも 1 つの領域を使用します。 たとえば、間に空白のままに、`[`と`{`します。

```fsharp
// OK
[ { IngredientName = "Green beans"; Quantity = 250 }
  { IngredientName = "Pine nuts"; Quantity = 250 }
  { IngredientName = "Feta cheese"; Quantity = 250 }
  { IngredientName = "Olive oil"; Quantity = 10 }
  { IngredientName = "Lemon"; Quantity = 1 } ]

// Not OK
[{ IngredientName = "Green beans"; Quantity = 250 }
 { IngredientName = "Pine nuts"; Quantity = 250 }
 { IngredientName = "Feta cheese"; Quantity = 250 }
 { IngredientName = "Olive oil"; Quantity = 10 }
 { IngredientName = "Lemon"; Quantity = 1 }]
```

リストと複数行にわたって配列は、同様のルール、レコードと同様に従います。

```fsharp
let pascalsTriangle = [|
    [|1|]
    [|1; 1|]
    [|1; 2; 1|]
    [|1; 3; 3; 1|]
    [|1; 4; 6; 4; 1|]
    [|1; 5; 10; 10; 5; 1|]
    [|1; 6; 15; 20; 15; 6; 1|]
    [|1; 7; 21; 35; 35; 21; 7; 1|]
    [|1; 8; 28; 56; 70; 56; 28; 8; 1|]
|]
```

## <a name="formatting-if-expressions"></a>書式設定の if 式

条件文のインデントは、それらを構成する式のサイズによって異なります。 場合`cond`、`e1`と`e2`短く、単純に 1 行に書き込むには。

```fsharp
if cond then e1 else e2
```

いずれか`cond`、`e1`または`e2`は長くなりますが、複数行にありません。

```fsharp
if cond
then e1
else e2
```

複数行の式のいずれかの場合。

```fsharp
if cond then
    e1
else
    e2
```

複数の条件で`elif`と`else`と同じスコープでインデントは、 `if`:

```fsharp
if cond1 then e1
elif cond2 then e2
elif cond3 then e3
else e4
```

### <a name="pattern-matching-constructs"></a>パターン マッチング

使用して、`|`インデントなしの一致の各句。 式が短い場合は、各部分式が単純でもある場合は、1 行を使用を検討できます。

```fsharp
// OK
match l with
| { him = x; her = "Posh" } :: tail -> _
| _ :: tail -> findDavid tail
| [] -> failwith "Couldn't find David"

// Not OK
match l with
    | { him = x; her = "Posh" } :: tail -> _
    | _ :: tail -> findDavid tail
    | [] -> failwith "Couldn't find David"
```

パターン マッチングの矢印の右側の式が大きすぎる場合は、次の行のインデントが設定された 1 つの手順に移動、 `match` /`|`します。

```fsharp
match lam with
| Var v -> 1
| Abs(x, body) ->
    1 + sizeLambda body
| App(lam1, lam2) ->
    sizeLambda lam1 + sizeLambda lam2

```

パターン マッチングして以降、匿名関数の`function`、遠すぎていないインデントする必要があります一般にします。 たとえば、次のように 1 つのスコープをインデントも可能です。

```fsharp
lambdaList
|> List.map (function
    | Abs(x, body) -> 1 + sizeLambda 0 body
    | App(lam1, lam2) -> sizeLambda (sizeLambda 0 lam1) lam2
    | Var v -> 1)
```

パターン マッチングで定義されている関数に`let`または`let rec`の開始後にインデントが設定された 4 つのスペースにする必要があります`let`場合でも、`function`キーワードの使用します。

```fsharp
let rec sizeLambda acc = function
    | Abs(x, body) -> sizeLambda (succ acc) body
    | App(lam1, lam2) -> sizeLambda (sizeLambda acc lam1) lam2
    | Var v -> succ acc
```

矢印の整列はお勧めしません。

## <a name="formatting-trywith-expressions"></a>書式設定してみてください/式を

例外の種類に一致するパターンと同じレベルでインデントする`with`します。

```fsharp
try
    if System.DateTime.Now.Second % 3 = 0 then
        raise (new System.Exception())
    else
        raise (new System.ApplicationException())
with
| :? System.ApplicationException ->
    printfn "A second that was not a multiple of 3"
| _ ->
    printfn "A second that was a multiple of 3"
```

## <a name="formatting-function-parameter-application"></a>関数パラメーターのアプリケーションを書式設定

一般に、関数パラメーターのほとんどのアプリケーションは、同じ行に行われます。

新しい行に関数にパラメーターを適用する場合は、1 つのスコープでインデントします。

```fsharp
// OK
sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
sprintf
     "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
let printVolumes x =
    printf "Volume in liters = %f, in us pints = %f, in imperial = %f"
        (convertVolumeToLiter x)
        (convertVolumeUSPint x)
        (convertVolumeImperialPint x)
```

関数の引数としてラムダ式と同じガイドラインが適用されます。 ラムダ式の本体の本文には別の行を設定できる場合は、1 つのスコープでインデント

```fsharp
let printListWithOffset a list1 =
    List.iter
        (fun elem -> printfn "%d" (a + elem))
        list1

// OK if lambda body is long enough
let printListWithOffset a list1 =
    List.iter
        (fun elem ->
            printfn "%d" (a + elem))
        list1
```

ただし、ラムダ式の本体が 1 つ以上の行の場合は、別の関数にファクタリング アウトを検討してくださいではなく 1 つの引数として関数に適用される複数行の構築します。

### <a name="formatting-infix-operators"></a>挿入演算子を書式設定

スペースで別の演算子。 このルールの明確な例外は、`!`と`.`演算子。

挿入辞の式では、[ok] を同じ列に編成します。

```fsharp
acc +
(sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity)

let function1 arg1 arg2 arg3 arg4 =
    arg1 + arg2 +
    arg3 + arg4
```

### <a name="formatting-pipeline-operators"></a>パイプライン演算子を書式設定

パイプライン`|>`演算子は、上で動作する式の下に移動する必要があります。

```fsharp
// Preferred approach
let methods2 =
    System.AppDomain.CurrentDomain.GetAssemblies()
    |> List.ofArray
    |> List.map (fun assm -> assm.GetTypes())
    |> Array.concat
    |> List.ofArray
    |> List.map (fun t -> t.GetMethods())
    |> Array.concat

// Not OK
let methods2 = System.AppDomain.CurrentDomain.GetAssemblies()
            |> List.ofArray
            |> List.map (fun assm -> assm.GetTypes())
            |> Array.concat
            |> List.ofArray
            |> List.map (fun t -> t.GetMethods())
            |> Array.concat
```

### <a name="formatting-modules"></a>モジュールの書式設定

モジュールの基準としたローカル モジュール内のコードのインデントを設定する必要がありますが、最上位レベルのモジュール内のコードはインデントされませんする必要があります。 Namespace 要素は、インデントを設定するのにはありません。

```fsharp
// A is a top-level module.
module A

let function1 a b = a - b * b
```

```fsharp
// A1 and A2 are local modules.
module A1 =
    let function1 a b = a*a + b*b

module A2 =
    let function2 a b = a*a - b*b
```

### <a name="formatting-object-expressions-and-interfaces"></a>オブジェクトの式とインターフェイスの書式設定

同じ方法では、オブジェクトの式とインターフェイスを配置する必要があります`member`される 4 つのスペース後の分だけインデントされます。

```fsharp
let comparer =
    { new IComparer<string> with
          member x.Compare(s1, s2) =
              let rev (s : String) =
                  new String (Array.rev (s.ToCharArray()))
              let reversed = rev s1
              reversed.CompareTo (rev s2) }
```

### <a name="formatting-white-space-in-expressions"></a>式内の空白の書式設定

F# の式で余分な空白文字を避けてください。

```fsharp
// OK
spam (ham.[1])

// Not OK
spam ( ham.[ 1 ] )
```

名前付き引数も必要はありません領域を囲む、 `=`:

```fsharp
// OK
let makeStreamReader x = new System.IO.StreamReader(path=x)

// Not OK
let makeStreamReader x = new System.IO.StreamReader(path = x)
```
