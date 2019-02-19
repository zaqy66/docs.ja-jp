---
title: 暗黙的な数値変換の一覧表 - C# リファレンス
ms.custom: seodec18
ms.date: 09/05/2018
helpviewer_keywords:
- conversions [C#], implicit numeric
- implicit numeric conversions [C#]
- numeric conversions [C#], implicit
- types [C#], implicit numeric conversions
ms.assetid: 72eb5a94-0491-48bf-8032-d7ebfdfeb8d8
ms.openlocfilehash: 703f60f48e1e569e0ffcab66ff7ccc91d4a49514
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2019
ms.locfileid: "56093555"
---
# <a name="implicit-numeric-conversions-table-c-reference"></a>暗黙的な数値変換の一覧表 (C# リファレンス)

.NET 数値型間の定義済みの暗黙的な変換を次の表に示します。
  
|変換元|終了|  
|----------|--------|  
|[sbyte](sbyte.md)|`short`、`int`、`long`、`float`、`double`、または `decimal`|  
|[byte](byte.md)|`short`、`ushort`、`int`、`uint`、`long`、`ulong`、`float`、`double`、または `decimal`|  
|[char](char.md)|`ushort`、`int`、`uint`、`long`、`ulong`、`float`、`double`、または `decimal`|  
|[short](short.md)|`int`、`long`、`float`、`double`、または `decimal`|  
|[ushort](ushort.md)|`int`、`uint`、`long`、`ulong`、`float`、`double`、または `decimal`|  
|[int](int.md)|`long`、`float`、`double`、または `decimal`|  
|[uint](uint.md)|`long`、`ulong`、`float`、`double`、または `decimal`|  
|[long](long.md)|`float`、 `double`、または `decimal`|  
|[ulong](ulong.md)|`float`、 `double`、または `decimal`|  
|[float](float.md)|`double`|  
  
## <a name="remarks"></a>解説  

- [整数型](integral-types-table.md)はすべて、あらゆる[浮動小数点型](floating-point-types-table.md)に暗黙的に変換できます。

- `int`、`uint`、`long`、または `ulong` から `float` への変換と `long` から `ulong` または `double` への変換では、有効桁数が失われる場合があります (絶対値ではありません)。  
  
- `char`、`byte`、`sbyte` 型への暗黙的な変換はありません。  

- `double` および `decimal` 型からの暗黙的な変換はありません。
  
- `decimal` 型と `float` 型または `double` 型の間に暗黙的な変換はありません。  
  
- 型 `int` の定数式の値 (整数リテラルで表される値など) は、それが変換先の型の範囲内にある場合、`sbyte`、`byte`、`short`、`ushort`、`uint`、`ulong` に変換できます。

  ```csharp
  byte a = 13;    // Compiles
  byte b = 300;   // CS0031: Constant value '300' cannot be converted to a 'byte'
  ```

明示的な変換に関する詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[Implicit conversions](~/_csharplang/spec/conversions.md#implicit-conversions)」 (明示的な変換) セクションをご覧ください。
  
## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミング ガイド](../../programming-guide/index.md)
- [整数型の一覧表](integral-types-table.md)
- [浮動小数点型の一覧表](floating-point-types-table.md)
- [組み込み型の一覧表](built-in-types-table.md)
- [明示的な数値変換の一覧表](explicit-numeric-conversions-table.md)
- [キャストと型変換](../../programming-guide/types/casting-and-type-conversions.md)
