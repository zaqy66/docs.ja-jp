---
title: '>> 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- '>>_CSharpKeyword'
helpviewer_keywords:
- '>> operator [C#]'
- right shift operator (>>) [C#]
ms.assetid: a07f8679-d318-4ef8-b38b-65903efb8056
ms.openlocfilehash: 809cd2cab29d3378892ea224cf846e9d0909b073
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219725"
---
# <a name="-operator-c-reference"></a>>> 演算子 (C# リファレンス)

右シフト演算子 `>>` では、最初のオペランドが 2 番目のオペランドで定義されたビット数だけ右にシフトされます。 すべての整数型で `>>` 演算子がサポートされます。 ただし、2 番目のオペランドの型は、[int](../keywords/int.md) または[事前に定義された `int` への暗黙的な数値変換](../keywords/implicit-numeric-conversions-table.md)を持つ型にする必要があります。

右シフト演算では、下位ビットが破棄されます。 空の上位ビット位置は、最初のオペランドの型に基づいて次のように設定されます。

- 最初のオペランドの型が [int](../keywords/int.md) または [long](../keywords/long.md) である場合、右シフト演算子では、**算術**シフトが実行されます: 最初のオペランドの最上位ビット (符号ビット) の値が空の上位ビット位置に反映されます。 つまり、最初のオペランドが負でない場合は空の上位ビット位置が 0 に設定され、負の場合は 1 に設定されます。

- 最初のオペランドの型が [uint](../keywords/uint.md) または [ulong](../keywords/ulong.md) である場合、右シフト演算子では、**論理**シフトが実行されます: 空の上位ビット位置は常に 0 に設定されます。

次の例は、その動作を示します。

[!code-csharp-interactive[right shift example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShift)]

## <a name="shift-count"></a>シフト数

式 `x >> count` では、実際のシフト数は次のように `x` の型によって異なります。

- `x` の型が [int](../keywords/int.md) または [uint](../keywords/uint.md) である場合、シフト数は、2 番目のオペランドの下位 *5* ビットで指定されます。 つまり、シフト数は `count & 0x1F` (または `count & 0b_1_1111`) から計算されます。

- `x` の型が [long](../keywords/long.md) または [ulong](../keywords/ulong.md) である場合、シフト数は、2 番目のオペランドの下位 *6* ビットで指定されます。 つまり、シフト数は `count & 0x3F` (または `count & 0b_11_1111`) から計算されます。

次の例は、その動作を示します。

[!code-csharp-interactive[shift count example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShiftByLargeCount)]

## <a name="remarks"></a>解説

シフト演算が原因でオーバーフローが発生することはなく、[checked と unchecked](../keywords/checked-and-unchecked.md) のコンテキストで同じ結果が生成されることはありません。

## <a name="operator-overloadability"></a>演算子のオーバーロード可/不可

ユーザー定義型は `>>` 演算子を[オーバーロード](../keywords/operator.md)できます。 ユーザー定義型 `T` では、`>>` 演算子がオーバーロードされます。最初のオペランドの型は `T` である必要があり、2 番目のオペランドの型は `int` である必要があります。 `>>` 演算子がオーバーロードされると、[右シフト代入演算子](right-shift-assignment-operator.md) `>>=` も暗黙的にオーバーロードされます。

## <a name="c-language-specification"></a>C# 言語仕様

詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[シフト演算子](~/_csharplang/spec/expressions.md#shift-operators)」セクションを参照してください。

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミング ガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
- [<< 演算子](left-shift-operator.md)