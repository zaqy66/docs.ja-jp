---
title: ~ 演算子 (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- ~_CSharpKeyword
helpviewer_keywords:
- tilde (~) one's complement operator [C#]
- ~ operator [C#]
- ~ [C#], bitwise complement operator
- bitwise complement operator [C#]
ms.assetid: 11bc078a-50e2-4d7e-9896-67ef669dc602
ms.openlocfilehash: 8af25217f9e7e66796192783a0b8e3415604dc90
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42933183"
---
# <a name="-operator-c-reference"></a>~ 演算子 (C# リファレンス)
`~` 演算子は、ビット単位の補数演算をオペランドに実行します。これにより、各ビットが反転します。 ビット単位の補数演算は [int](../../../csharp/language-reference/keywords/int.md)、[uint](../../../csharp/language-reference/keywords/uint.md)、[long](../../../csharp/language-reference/keywords/long.md)、[ulong](../../../csharp/language-reference/keywords/ulong.md) に事前定義されています。  
  
> [!NOTE]
>  `~` シンボルもファイナライザーの宣言に使用されます。 詳細については、「[Finalizers](../../../csharp/programming-guide/classes-and-structs/destructors.md)」 (ファイナライザー) を参照してください。  
  
## <a name="remarks"></a>コメント  
 ユーザー定義型は `~` 演算子をオーバーロードできます。 詳細については、「[operator](../../../csharp/language-reference/keywords/operator.md)」を参照してください。 整数型に対する演算は、通常、列挙型で使用できます。  
  
## <a name="example"></a>例  
 [!code-csharp[csRefOperators#25](../../../csharp/language-reference/operators/codesnippet/CSharp/bitwise-complement-operator_1.cs)]  
  
## <a name="see-also"></a>参照

- [C# リファレンス](../../../csharp/language-reference/index.md)  
- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [C# 演算子](../../../csharp/language-reference/operators/index.md)  
- [ファイナライザー](../../../csharp/programming-guide/classes-and-structs/destructors.md)
