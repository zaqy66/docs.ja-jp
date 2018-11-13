---
title: ?? 演算子 (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- ??_CSharpKeyword
helpviewer_keywords:
- coalesce operator [C#]
- ?? operator [C#]
- conditional-AND operator (&&) [C#]
ms.assetid: 088b1f0d-c1af-4fe1-b4b8-196fd5ea9132
ms.openlocfilehash: fbcfda07cc55628aeed82eb7561516f7012bc4fe
ms.sourcegitcommit: b5cd9d5d3b75a5537fc9ad8a3f085f0bb1845ee0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "50980675"
---
# <a name="-operator-c-reference"></a>?? 演算子 (C# リファレンス)
`??` 演算子は、null 合体演算子と呼ばれます。  左側のオペランドが null 値でない場合には左側のオペランドを返し、null 値である場合には右側のオペランドを返します。  
  
## <a name="remarks"></a>コメント  
 null 許容型は、型のドメインの値を表すことができ、値は未定義でもかまいません (その場合、値は null になります)。 `??` 演算子の構文を使用して、左側のオペランドが null 許容型でその値が null である場合に、適切な値 (右側のオペランド) を返すことができます。 `??` 演算子を使用せずに、null 非許容値型に対して null 許容値型を割り当てると、コンパイル時にエラーが発生します。 null 許容値型が定義されていない場合にキャストを使用すると、`InvalidOperationException` 例外がスローされます。  
  
 詳細については、「[Null 許容型](../../../csharp/programming-guide/nullable-types/index.md)」を参照してください。  
  
 ?? の結果は、 たとえ両方の引数が定数であった場合でも、定数とは見なされません。  
  
## <a name="example"></a>例  
 [!code-csharp[csRefOperators#53](../../../csharp/language-reference/operators/codesnippet/CSharp/null-conditional-operator_1.cs)]  
  
## <a name="c-language-specification"></a>C# 言語仕様  

詳細については、「[C# 言語仕様](../language-specification/index.md)」の [null 合体演算子](~/_csharplang/spec/expressions.md#the-null-coalescing-operator)に関するセクションを参照してください。 言語仕様は、C# の構文と使用法に関する信頼性のある情報源です。
  
## <a name="see-also"></a>参照

- [C# リファレンス](../../../csharp/language-reference/index.md)  
- [C# プログラミングガイド](../../../csharp/programming-guide/index.md)  
- [C# 演算子](../../../csharp/language-reference/operators/index.md)  
- [Null 許容型](../../../csharp/programming-guide/nullable-types/index.md)  
- ['Lifted' の正確な意味](https://blogs.msdn.microsoft.com/ericlippert/2007/06/27/what-exactly-does-lifted-mean/)
