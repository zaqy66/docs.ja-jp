---
title: '方法: LINQ 以外でラムダ式を使用する - C# プログラミング ガイド'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- lambda expressions [C#], outside LINQ
ms.assetid: 2b519274-6ee4-4455-ab2e-aed67dbfd07c
ms.openlocfilehash: d4dc0375552ef1fe00f629c22b5296399b4cc99d
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243934"
---
# <a name="how-to-use-lambda-expressions-outside-linq-c-programming-guide"></a>方法: LINQ 以外でラムダ式を使用する (C# プログラミング ガイド)
ラムダ式の使用は [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] クエリに限定されているわけではありません。 デリゲート値が想定される場面、すなわち匿名メソッドを使用できる場面であれば、どこでもラムダ式を使用できます。 次の例では、Windows フォームのイベント ハンドラーでラムダ式を使用する方法を示します。 なお、入力 (<xref:System.Object> と <xref:System.Windows.Forms.MouseEventArgs>) の型はコンパイラによって推論されるため、ラムダ入力パラメーターで明示的に指定する必要がありません。  
  
## <a name="example"></a>例  
  
```csharp  
public partial class Form1 : Form  
{  
    public Form1()  
    {  
        InitializeComponent();  
        // Use a lambda expression to define an event handler.  
       this.Click += (s, e) => { MessageBox.Show(((MouseEventArgs)e).Location.ToString());};  
    }  
}  
```  
  
## <a name="see-also"></a>参照

- [ラムダ式](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)  
- [匿名メソッド](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md)  
- [統合言語クエリ (LINQ)](../../../csharp/programming-guide/concepts/linq/index.md)
