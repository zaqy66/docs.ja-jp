---
title: 名前空間 (F#)
description: F# 名前空間を使用すると、プログラム要素のグループに名前を追加することによって関連する機能の領域にコードを整理する方法について説明します。
ms.date: 04/24/2017
ms.openlocfilehash: 769a1241f76ac32d3a6a80bd637078493119bb3c
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44178257"
---
# <a name="namespaces"></a>名前空間

名前空間を使用すると、プログラム要素のグループに名前を割り当てて、関連する機能の区分にコードを編成することができます。

## <a name="syntax"></a>構文

```fsharp
namespace [parent-namespaces.]identifier
```

## <a name="remarks"></a>Remarks

名前空間にコードを配置する場合は、ファイル内の最初の宣言は名前空間を宣言する必要があります。 全体のファイルの内容は、名前空間の一部になります。

値および関数、名前空間を含める直接ことはできません。 代わりに、モジュールでは、値および関数を含める必要があるし、モジュールの名前空間に含まれます。 名前空間は、モジュールの種類を含めることができます。

名前空間は明示的に宣言する名前空間キーワード、または暗黙的にモジュールを宣言するときに。 名前空間を明示的に宣言するには、名前空間キーワードの後に名前空間の名前を使用します。 次の例では、型とその名前空間に含まれるモジュールのウィジェットの名前空間を宣言するコード ファイルを示します。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6406.fs)]

ファイルの内容全体が 1 つのモジュールである場合は、宣言することも名前空間に暗黙的を使用して、`module`キーワードとモジュールの完全修飾名で新しい名前空間名を指定します。 次の例では、名前空間を宣言するコード ファイル`Widgets`とモジュール`WidgetsModule`関数が含まれています。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6401.fs)]

次のコードは上記のコードと同じですが、モジュールがローカル モジュールの宣言。 その場合は、名前空間は、独自の行に表示する必要があります。

[!code-fsharp[Main](../../../samples/snippets/fsharp/namespaces/snippet6402.fs)]

1 つ以上のモジュールが 1 つまたは複数の名前空間で同じファイルで必要に応じて、ローカル モジュール宣言を使用する必要があります。 モジュールのローカル宣言を使用する場合は、モジュール宣言で修飾名前空間を使用できません。 次のコードでは、名前空間の宣言と 2 つのモジュールのローカル宣言を持つファイルを示します。 この場合、モジュールが、名前空間で直接に含まれるファイルと同じ名前を持つ、暗黙的に作成されたモジュールはありません。 などのファイルで、コードの他の`do`モジュール メンバーを修飾する必要があるため、内部のモジュールではなく、名前空間には、バインド、`widgetFunction`モジュール名を使用しています。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6403.fs)]

この例の出力は次のとおりです。

```fsharp
Module1 10 20
Module2 5 6
```

詳細については、次を参照してください。[モジュール](modules.md)します。

## <a name="nested-namespaces"></a>入れ子になった名前空間

入れ子になった名前空間を作成するときに、完全修飾する必要があります。 それ以外の場合、新しい最上位レベルの名前空間を作成します。 インデントは、名前空間の宣言では無視されます。

次の例では、入れ子になった名前空間を宣言する方法を示します。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6404.fs)]

## <a name="namespaces-in-files-and-assemblies"></a>ファイルとアセンブリの名前空間

名前空間は、1 つのプロジェクトやコンパイルで複数のファイルにまたがることができます。 用語*名前空間のフラグメント*1 つのファイルに含まれている名前空間の一部について説明します。 名前空間は、複数のアセンブリをまたがることもできます。 たとえば、`System`名前空間に多数のアセンブリにまたがり、多数の入れ子になった名前空間が含まれていますが、全体の .NET Framework が含まれています。

## <a name="global-namespace"></a>グローバル Namespace

定義済みの名前空間を使用する`global`に最上位レベルの .NET 名前空間に名前を格納します。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6407.fs)]

使用することできますもグローバル他の名前空間と名前が競合を解決するのには、たとえば最上位レベルの .NET 名前空間を参照します。

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6408.fs)]

## <a name="recursive-namespaces"></a>再帰的な名前空間

F# 4.1 には、再帰的に相互に含まれているすべてのコードでは、名前空間の概念が導入されています。  使用してこれには`namespace rec`します。  使用`namespace rec`されない型とモジュール間の相互参照コードを記述することでいくつかの問題を軽減することができます。  この例を次に示します。

```fsharp
namespace rec MutualReferences

type Orientation = Up | Down
type PeelState = Peeled | Unpeeled

// This exception depends on the type below.
exception DontSqueezeTheBananaException of Banana

type BananaPeel() = class end

type Banana(orientation : Orientation) =
    member val IsPeeled = false with get, set
    member val Orientation = orientation with get, set
    member val Sides: PeelState list = [ Unpeeled; Unpeeled; Unpeeled; Unpeeled] with get, set

    member self.Peel() = BananaHelpers.peel self // Note the dependency on the BananaHelpers module.
    member self.SqueezeJuiceOut() = raise (DontSqueezeTheBananaException self) // This member depends on the exception above.

module BananaHelpers =
    let peel (b: Banana) =
        let flip (banana: Banana) =
            match banana.Orientation with
            | Up -> 
                banana.Orientation <- Down
                banana
            | Down -> banana

        let peelSides (banana: Banana) =
            banana.Sides
            |> List.map (function
                         | Unpeeled -> Peeled
                         | Peeled -> Peeled)

        match b.Orientation with
        | Up ->   b |> flip |> peelSides
        | Down -> b |> peelSides
```

なお、例外`DontSqueezeTheBananaException`とクラス`Banana`両方には、互いを参照してください。  モジュールではさらに、`BananaHelpers`とクラス`Banana`も互いに参照してください。  これは、削除した場合、f# で表現できませんが、`rec`からキーワード、`MutualReferences`名前空間。

この機能は使用できる最上位[モジュール](modules.md)f# 4.1 またはそれ以降。

## <a name="see-also"></a>関連項目

- [F# 言語リファレンス](index.md)
- [モジュール](modules.md)
- [F# RFC FS-1009 - ファイル内でより大きな範囲経由で相互に参照型とモジュールを許可します。](https://github.com/fsharp/fslang-design/blob/master/FSharp-4.1/FS-1009-mutually-referential-types-and-modules-single-scope.md)
