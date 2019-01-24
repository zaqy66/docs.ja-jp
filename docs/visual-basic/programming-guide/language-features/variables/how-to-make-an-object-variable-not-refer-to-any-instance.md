---
title: '方法: オブジェクトが変数になる任意のインスタンス (Visual Basic) を参照していません'
ms.date: 07/20/2015
helpviewer_keywords:
- Nothing keyword [Visual Basic], variable assignment
- object variables [Visual Basic], null reference
ms.assetid: e6d30578-bdae-4142-a3ac-a10697bf696a
ms.openlocfilehash: 1199fa4e126c3d15e56a6c895aecf6afcae17f0b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54678513"
---
# <a name="how-to-make-an-object-variable-not-refer-to-any-instance-visual-basic"></a>方法: オブジェクトが変数になる任意のインスタンス (Visual Basic) を参照していません
任意のオブジェクトのインスタンスからオブジェクト変数設定することで関連付けを解除することができます[Nothing](../../../../visual-basic/language-reference/nothing.md)します。  
  
### <a name="to-disassociate-an-object-variable-from-any-object-instance"></a>任意のオブジェクトのインスタンスからオブジェクト変数の関連付けを解除するには  
  
-   変数を設定します`Nothing`代入ステートメントでします。  
  
    ```  
    ' Assume account is a defined class  
    Dim currentAccount As account  
    currentAccount = Nothing  
    ```  
  
## <a name="robust-programming"></a>信頼性の高いプログラミング  
 設定されているオブジェクト変数のメンバーにアクセスしようとすると、コード`Nothing`、<xref:System.NullReferenceException>に発生します。 オブジェクト変数を設定した場合`Nothing`多くの場合、またはのメンバーへのアクセスを囲むことをお勧め、変数が初期化されていないが可能ですが場合、は、`Try...Catch...Finally`ブロックします。  
  
## <a name="net-framework-security"></a>.NET Framework セキュリティ  
 機密情報や機密データを格納するオブジェクトをオブジェクト変数を使用する場合変数を設定することができます`Nothing`ときにアクティブに処理するいないとそれらのオブジェクトのいずれか。 これにより、悪意のあるコードがデータにアクセスする可能性が減少します。  
  
## <a name="see-also"></a>関連項目
- <xref:System.NullReferenceException>
- [オブジェクト変数](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [オブジェクト変数の代入](../../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)
- [Nothing](../../../../visual-basic/language-reference/nothing.md)
- [Try...Catch...Finally ステートメント](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
- [例外のトラブルシューティング。System.NullReferenceException](https://msdn.microsoft.com/library/4822b0b4-8105-43fb-887a-3cc51ff02899)
