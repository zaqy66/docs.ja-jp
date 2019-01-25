---
title: '方法: ポインターを使用して配列要素にアクセスする - C# プログラミング ガイド'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], array access
ms.assetid: 6c46f2af-a730-4855-8638-f136d9abaa12
ms.openlocfilehash: 59765dbcad6c28cf2ad9f3df2052df19cafd08f1
ms.sourcegitcommit: 75567a3cb437009db55949c6092f4e77ed1a9da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2019
ms.locfileid: "54307280"
---
# <a name="how-to-access-an-array-element-with-a-pointer-c-programming-guide"></a>方法: ポインターを使用して配列要素にアクセスする (C# プログラミング ガイド)

安全ではないコンテキストでは、次の例のように、ポインターを利用してメモリ内の要素にアクセスできます。

```csharp
char* charPointer = stackalloc char[123];
for (int i = 65; i < 123; i++)
{
    charPointer[i] = (char)i; //access array elements
}
```

角かっこ内の式は `int`、`uint`、`long`、`ulong` に暗黙的に変換できるものでなければなりません。 演算 `p[e]` は `*(p+e)` と等しくなります。 C や C++ と同様に、ポインターで要素にアクセスする行為では、範囲外のエラーがチェックされません。

## <a name="example"></a>例

この例では、123 のメモリ場所が文字配列 `charPointer` に割り当てられます。 この配列を利用し、2 つの [for](../../../csharp/language-reference/keywords/for.md) ループの小文字と大文字が表示されます。

式 `charPointer[i]` は式 `*(charPointer + i)` と等しく、2 つの式のいずれを利用しても同じ結果が得られることに注目してください。

[!code-csharp[csProgGuidePointers#11](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-access-an-array-element-with-a-pointer_1.cs)]

[!code-csharp[csProgGuidePointers#12](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-access-an-array-element-with-a-pointer_2.cs)]

**大文字:**  
**ABCDEFGHIJKLMNOPQRSTUVWXYZ**  
**小文字:**  
**abcdefghijklmnopqrstuvwxyz**  

## <a name="see-also"></a>関連項目

- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)
- [ポインター式](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)
- [ポインター型](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [型](../../../csharp/language-reference/keywords/types.md)
- [unsafe](../../../csharp/language-reference/keywords/unsafe.md)
- [fixed ステートメント](../../../csharp/language-reference/keywords/fixed-statement.md)
- [stackalloc](../../../csharp/language-reference/keywords/stackalloc.md)
