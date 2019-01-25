---
title: 遅延実行の例 (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 9a22bea1-c755-4aac-800a-fcd9e5107ace
ms.openlocfilehash: e9247c89d46cc7705ef4297868739ba85d993eec
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54614173"
---
# <a name="deferred-execution-example-visual-basic"></a>遅延実行の例 (Visual Basic)
このトピックでは、遅延実行とレイジー評価が LINQ to XML クエリの実行にどのように影響するかについて説明します。  
  
## <a name="example"></a>例  
 遅延実行を利用する拡張メソッドの使用時における実行順序の例を次に示します。 この例では、3 つの文字列の配列を宣言します。 次に、`ConvertCollectionToUpperCase` によって返されるコレクションを反復処理します。  
  
```vb  
Imports System.Runtime.CompilerServices  
  
Module Module1  
  
    <Extension()>  
    Private Iterator Function ConvertCollectionToUpperCase(  
    ByVal source As IEnumerable(Of String)) _  
    As IEnumerable(Of String)   
        For Each str As String In source  
            Console.WriteLine("ToUpper: source {0}", str)   
            Yield str.ToUpper()  
        Next  
    End Function  
  
    Sub Main()  
        Dim stringArray = New String() {"abc", "def", "ghi"}  
  
        Dim q = From str In stringArray.ConvertCollectionToUpperCase()  
                Select str  
  
        For Each Str As String In q  
            Console.WriteLine("Main: str {0}", Str)   
        Next  
    End Sub  
  
End Module  
```  
  
 この例を実行すると、次の出力が生成されます。  
  
```  
ToUpper: source abc  
Main: str ABC  
ToUpper: source def  
Main: str DEF  
ToUpper: source ghi  
Main: str GHI  
```  
  
 `ConvertCollectionToUpperCase` によって返されるコレクションの反復処理時、各アイテムはソース文字列の配列から取得され、次のアイテムがソース文字列の配列から取得される前に大文字に変換されることに注意してください。  
  
 返されるコレクションの各アイテムが `foreach` の `Main` ループで処理されるまで、文字列の配列全体は大文字に変換されないことを確認できます。  
  
## <a name="see-also"></a>関連項目
- [チュートリアル: 遅延実行 (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/tutorial-deferred-execution.md)
