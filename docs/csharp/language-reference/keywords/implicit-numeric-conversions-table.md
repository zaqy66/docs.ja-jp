---
title: 暗黙的な数値変換の一覧表 (C# リファレンス)
ms.date: 09/05/2018
helpviewer_keywords:
- conversions [C#], implicit numeric
- implicit numeric conversions [C#]
- numeric conversions [C#], implicit
- types [C#], implicit numeric conversions
ms.assetid: 72eb5a94-0491-48bf-8032-d7ebfdfeb8d8
ms.openlocfilehash: c3c0153a0ae3e07839822c8bb978b1a09277bd53
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188704"
---
# <a name="implicit-numeric-conversions-table-c-reference"></a>暗黙的な数値変換の一覧表 (C# リファレンス)

.NET 数値型間の定義済みの暗黙的な変換を次の表に示します。
  
|変換元|変換先|  
|----------|--------|  
|[sbyte](sbyte.md)|`short`、`int`、`long`、`float`、`double`、または `decimal`|  
|[byte](byte.md)|`short`、`ushort`、`int`、`uint`、`long`、`ulong`、`float`、`double`、または `decimal`|  
|[short](short.md)|`int`、`long`、`float`、`double`、または `decimal`|  
|[ushort](ushort.md)|`int`、`uint`、`long`、`ulong`、`float`、`double`、または `decimal`|  
|[int](int.md)|`long`、`float`、`double`、または `decimal`|  
|[uint](uint.md)|`long`、`ulong`、`float`、`double`、または `decimal`|  
|[long](long.md)|`float`、 `double`、または `decimal`|  
|[char](char.md)|`ushort`、`int`、`uint`、`long`、`ulong`、`float`、`double`、または `decimal`|  
|[float](float.md)|`double`|  
|[ulong](ulong.md)|`float`、 `double`、または `decimal`|  
  
## <a name="remarks"></a>コメント  

- [整数型](integral-types-table.md)はすべて、あらゆる[浮動小数点型](floating-point-types-table.md)に暗黙的に変換できます。

- `int`、`uint`、`long`、または `ulong` から `float` への変換と `long` から `ulong` または `double` への変換では、有効桁数が失われる場合があります (絶対値ではありません)。  
  
- `char` 型への暗黙的な変換はありません。  
  
- `float` 型、`double` 型、`decimal` 型の間に暗黙的な変換はありません。  
  
- 型 `int` の定数式の値 (整数リテラルで表される値など) は、それが変換先の型の範囲内にある場合、`sbyte`、`byte`、`short`、`ushort`、`uint`、`ulong` に変換できます。

  ```csharp
  byte a = 13;    // コンパイル可能
  byte b = 300;   // CS0031: 定数値 '300' を 'byte' に変換できません
  ```

明示的な変換に関する詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[Implicit conversions](~/_csharplang/spec/conversions.md#implicit-conversions)」 (明示的な変換) セクションをご覧ください。
  
## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [整数型の一覧表](integral-types-table.md)
- [浮動小数点型の一覧表](floating-point-types-table.md)
- [組み込み型の一覧表](built-in-types-table.md)
- [明示的な数値変換の一覧表](explicit-numeric-conversions-table.md)
- [キャストと型変換](../../programming-guide/types/casting-and-type-conversions.md)
