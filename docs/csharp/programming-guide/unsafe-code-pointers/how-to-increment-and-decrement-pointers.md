---
title: '方法 : ポインターのインクリメントとデクリメント (C# プログラミング ガイド)'
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], increment and decrement
- pointer expressions [C#], increment and decrement
ms.assetid: 1b8b9281-44ee-485a-9045-3db38a4b4b89
ms.openlocfilehash: 39cefc5dcebf1331a5e0ac0fadb8284e9041eb27
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2018
ms.locfileid: "44206472"
---
# <a name="how-to-increment-and-decrement-pointers-c-programming-guide"></a>方法 : ポインターのインクリメントとデクリメント (C# プログラミング ガイド)
pointer-type* 型のポインターの [sizeof](../../../csharp/language-reference/keywords/sizeof.md) (`pointer-type`) でポインターの位置を変更するには、インクリメント演算子 (`++`) とデクリメント演算子 (`--`) を使用します。 インクリメント式とデクリメント式には、次の書式を使用します。  
  
```  
++p;  
p++;  
--p;  
p--;  
```  
  
 インクリメント演算子とデクリメント演算子は、`void*` 以外のすべての型のポインターに適用できます。  
  
 `pointer-type` 型のポインターにインクリメント演算子を適用すると、ポインター変数に格納されているアドレスに [sizeof](../../../csharp/language-reference/keywords/sizeof.md) (`pointer-type`) が加算されます。  
  
 `pointer-type` 型のポインターにデクリメント演算子を適用すると、ポインター変数に格納されているアドレスから `sizeof` (`pointer-type`) が減算されます。  
  
 演算がポインターのドメインをオーバーフローしても例外は生成されません。生じる結果は実装によって異なります。  
  
## <a name="example"></a>例  
 この例では、ポインターを `int` のサイズだけインクリメントして、配列をステップ実行します。 ステップごとに、配列要素のアドレスと内容を表示します。  
  
 [!code-csharp[csProgGuidePointers#3](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-increment-and-decrement-pointers_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#13](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-increment-and-decrement-pointers_2.cs)]  
  
**値:0 @ アドレス:12860272**
**値:1 @ アドレス:12860276**
**値:2 @ アドレス:12860280**
**値:3 @ アドレス:12860284**
**値:4 @ アドレス:12860288**

## <a name="see-also"></a>参照

- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [ポインター式](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)  
- [C# 演算子](../../../csharp/language-reference/operators/index.md)  
- [ポインターの操作](../../../csharp/programming-guide/unsafe-code-pointers/manipulating-pointers.md)  
- [ポインター型](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)  
- [型](../../../csharp/language-reference/keywords/types.md)  
- [unsafe](../../../csharp/language-reference/keywords/unsafe.md)  
- [fixed ステートメント](../../../csharp/language-reference/keywords/fixed-statement.md)  
- [stackalloc](../../../csharp/language-reference/keywords/stackalloc.md)
