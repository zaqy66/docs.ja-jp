---
title: ジェネリックと配列 (C# プログラミング ガイド)
ms.date: 07/20/2015
helpviewer_keywords:
- generics [C#], arrays
- arrays [C#], generics
ms.assetid: 7d956536-3851-41b5-94ad-3e7c0a5fe485
ms.openlocfilehash: 6cb205d90d4b6de329a179c5969e2d3b543bfb35
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43528501"
---
# <a name="generics-and-arrays-c-programming-guide"></a>ジェネリックと配列 (C# プログラミング ガイド)
C# 2.0 以降、下限が 0 の一次元配列は自動的に <xref:System.Collections.Generic.IList%601> を実装します。 これにより、同じコードで配列や他のコレクション型を反復処理できるジェネリック メソッドを作成できます。 この手法は主に、コレクションのデータを読み込むときに便利です。 <xref:System.Collections.Generic.IList%601> インターフェイスを使用して配列の要素を追加したり、削除したりすることはできません。 このコンテキストの配列で、<xref:System.Collections.Generic.IList%601.RemoveAt%2A> のような、<xref:System.Collections.Generic.IList%601> メソッドを呼び出そうとすると、例外がスローされます。  
  
 次のコード例からは、<xref:System.Collections.Generic.IList%601> 入力パラメーターを受け取る単一のジェネリック メソッドがリストと配列 (この例では、整数の配列) の両方を反復処理できることがわかります。  
  
 [!code-csharp[csProgGuideGenerics#35](../../../csharp/programming-guide/generics/codesnippet/CSharp/generics-and-arrays_1.cs)]  
  
## <a name="see-also"></a>参照

- <xref:System.Collections.Generic>  
- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [ジェネリック](../../../csharp/programming-guide/generics/index.md)  
- [配列](../../../csharp/programming-guide/arrays/index.md)  
- [ジェネリック](~/docs/standard/generics/index.md)
