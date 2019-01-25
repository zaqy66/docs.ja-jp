---
title: '&gt;&gt; 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '>>_CSharpKeyword'
helpviewer_keywords:
- '>> operator [C#]'
- right shift operator (>>) [C#]
ms.assetid: a07f8679-d318-4ef8-b38b-65903efb8056
ms.openlocfilehash: 80e38d8e75b9ad573b635d544d6381950f107583
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333688"
---
# <a name="gtgt-operator-c-reference"></a>&gt;&gt; 演算子 (C# リファレンス)

右シフト演算子 (`>>`) は、最初のオペランドを 2 番目のオペランドで指定されたビット数だけ右にシフトします。

## <a name="remarks"></a>コメント

最初のオペランドが [int](../keywords/int.md) または [uint](../keywords/uint.md) (32 ビット値) である場合、シフト数は、2 番目のオペランド (2 番目のオペランドと 0x1f) の下位 5 ビットで指定されます。

最初のオペランドが [long](../keywords/long.md) または [ulong](../keywords/ulong.md) (64 ビット値) である場合、シフト数は、2 番目のオペランド (2 番目のオペランドと 0x3f) の下位 6 ビットで指定されます。

最初のオペランドが [int](../keywords/int.md) または [long](../keywords/long.md) である場合、右シフトは算術演算シフトになります (空の上位ビットが符号ビットに設定されます)。 最初のオペランドの型が [uint](../keywords/uint.md) または [ulong](../keywords/ulong.md) である場合、右シフトは論理シフトになります (上位ビットはゼロで埋められます)。

ユーザー定義型は、`>>` 演算子をオーバーロードすることができます。最初のオペランドの型は、ユーザー定義型である必要があり、2 番目のオペランドの型は [int](../keywords/int.md) でなければなりません。詳細については、「[operator](../keywords/operator.md)」を参照してください。 二項演算子をオーバーロードすると、対応する代入演算子がある場合、これも暗黙的にオーバーロードされます。

## <a name="example"></a>例

[!code-csharp[csRefOperators#26](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#26)]

## <a name="see-also"></a>参照

- [C# リファレンス](../index.md)
- [C# プログラミング ガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)