---
title: 明示的な数値変換の一覧表 (C# リファレンス)
ms.date: 09/06/2018
helpviewer_keywords:
- conversions [C#], explicit numeric
- numeric conversions [C#], explicit
- explicit numeric conversion [C#]
- numeric data types [C#]
- types [C#], explicit numeric conversions
- type conversion [C#], explicit numeric
ms.assetid: f3bb9e76-6b92-4df7-bc36-f866c24e1dfd
ms.openlocfilehash: 22bb2117e7b78596e1fb6af63584f51b066564c9
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2018
ms.locfileid: "44211789"
---
# <a name="explicit-numeric-conversions-table-c-reference"></a>明示的な数値変換の一覧表 (C# リファレンス)

次の表では、[暗黙的な変換](implicit-numeric-conversions-table.md)がない .NET 数値型間で事前定義されている明示的変換がまとめてあります。

|From|終了|  
|----------|--------|  
|[sbyte](sbyte.md)|`byte`、`ushort`、`uint`、`ulong`、または `char`|  
|[byte](byte.md)|`sbyte` または `char`|  
|[short](short.md)|`sbyte`、`byte`、`ushort`、`uint`、`ulong`、または `char`|  
|[ushort](ushort.md)|`sbyte`、`byte`、`short`、または `char`|  
|[int](int.md)|`sbyte`、`byte`、`short`、`ushort`、`uint`、`ulong`、または `char`|  
|[uint](uint.md)|`sbyte`、`byte`、`short`、`ushort`、`int`、または `char`|  
|[long](long.md)|`sbyte`、`byte`、`short`、`ushort`、`int`、`uint`、`ulong`、または `char`|  
|[ulong](ulong.md)|`sbyte`、`byte`、`short`、`ushort`、`int`、`uint`、`long`、または `char`|  
|[char](char.md)|`sbyte`、 `byte`、または `short`|  
|[float](float.md)|`sbyte`、`byte`、`short`、`ushort`、`int`、`uint`、`long`、`ulong`、`char`、または `decimal`|  
|[double](double.md)|`sbyte`、`byte`、`short`、`ushort`、`int`、`uint`、`long`、`ulong`、`char`、`float`、または `decimal`|  
|[decimal](decimal.md)|`sbyte`、`byte`、`short`、`ushort`、`int`、`uint`、`long`、`ulong`、`char`、`float`、または `double`|  
  
## <a name="remarks"></a>コメント  
  
- 明示的な数値変換では、精度が失われたり、例外 (通常、<xref:System.OverflowException>) がスローされることがあります。  

- ある整数型の値を別の整数型に変換するとき、その結果は、オーバーフロー [チェック コンテキスト](checked-and-unchecked.md)によって変わります。 checked コンテキストでは、変換元の値が変換先の型の範囲内にあるとき、変換に成功します。 それ以外の場合は、<xref:System.OverflowException> がスローされます。 unchecked コンテキストでは、変換は常に成功し、次のように続行されます。

  - 変換元の型が変換先の型より大きい場合、変換元の値はその "余分な" 最上位ビットを破棄することで切り詰められます。 結果は変換先の型の値として扱われます。

  - 変換元の型が変換先の型より小さい場合、変換元の値は変換先の型と同じサイズになるように符号かゼロが拡張されます。 変換元の型に符号が付いている場合は符号拡張が利用され、符号が付いていない場合はゼロ拡張が利用されます。 結果は変換先の型の値として扱われます。

  - 変換元の型が変換先の型と同じサイズの場合、変換元の値は変換先の型の値として扱われます。
  
- `decimal` 値を整数型に変換するとき、この値は 0 方向に最も近い整数値に丸められます。 結果的に生成される整数値が変換先の型の範囲外になった場合、<xref:System.OverflowException> がスローされます。  
  
- `double` または `float` 値を整数型に変換するとき、この値は 0 方向に最も近い整数値に丸められます。 結果的に生成される整数値が変換先の型の範囲外になる場合、結果はオーバーフロー [チェック コンテキスト](checked-and-unchecked.md)によって変わります。 チェック済みコンテキストの場合、<xref:System.OverflowException> がスローされます。未チェック コンテキストの場合、結果は変換先の型の未指定値になります。  
  
- `double` を `float` に変換すると、`double` 値は最も近い `float` 値に丸められます。 `double` 値が小さすぎるか、大きすぎて変換先の型に合わない場合、結果は 0 か無限になります。  
  
- `float` または `double` を `decimal` に変換するとき、変換元の値は `decimal` 表現に変換され、必要であれば、28 番目の小数位の後に最も近い数字に丸められます。 変換元の値によっては、結果は次のいずれかになります。  

  - 変換元の値が小さすぎて `decimal` として表現できない場合、結果は 0 になります。  

  - 変換元の値が NaN (Not a Number/数字ではない) か、無限か、大きすぎて `decimal` として表現できない場合、<xref:System.OverflowException> がスローされます。  
  
- `decimal` を `float` または `double` に変換すると、`decimal` 値は最も近い `double` または `float` 値に丸められます。  
  
 明示的な変換に関する詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[Explicit conversions](/dotnet/csharp/language-reference/language-specification/conversions#explicit-conversions)」(明示的な変換) セクションをご覧ください。
  
## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミング ガイド](../../programming-guide/index.md)
- [キャストと型変換](../../programming-guide/types/casting-and-type-conversions.md)
- [() 演算子](../operators/invocation-operator.md)
- [整数型の一覧表](integral-types-table.md)
- [浮動小数点型の一覧表](floating-point-types-table.md)
- [組み込み型の一覧表](built-in-types-table.md)
- [暗黙的な数値変換の一覧表](implicit-numeric-conversions-table.md)
