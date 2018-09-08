---
title: '方法: デリゲート メソッドを呼び出す (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: b56866ae-abf9-4a5a-a855-486359455e9c
ms.openlocfilehash: c50a32d300aaf52efe0c55cef69d5793a98305ac
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44129215"
---
# <a name="how-to-invoke-a-delegate-method-visual-basic"></a><span data-ttu-id="dbe66-102">方法: デリゲート メソッドを呼び出す (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dbe66-102">How to: Invoke a Delegate Method (Visual Basic)</span></span>
<span data-ttu-id="dbe66-103">この例では、メソッドをデリゲートに関連付け、デリゲートからメソッドを呼び出す方法を示します。</span><span class="sxs-lookup"><span data-stu-id="dbe66-103">This example shows how to associate a method with a delegate and then invoke that method through the delegate.</span></span>  
  
### <a name="create-the-delegate-and-matching-procedures"></a><span data-ttu-id="dbe66-104">デリゲートと一致するプロシージャを作成します。</span><span class="sxs-lookup"><span data-stu-id="dbe66-104">Create the delegate and matching procedures</span></span>  
  
1.  <span data-ttu-id="dbe66-105">という名前のデリゲートを作成する`MySubDelegate`します。</span><span class="sxs-lookup"><span data-stu-id="dbe66-105">Create a delegate named `MySubDelegate`.</span></span>  
  
    ```  
    Delegate Sub MySubDelegate(ByVal x As Integer)  
    ```  
  
2.  <span data-ttu-id="dbe66-106">デリゲートと同じシグネチャを持つメソッドを含むクラスを宣言します。</span><span class="sxs-lookup"><span data-stu-id="dbe66-106">Declare a class that contains a method with the same signature as the delegate.</span></span>  
  
    ```  
    Class class1  
        Sub Sub1(ByVal x As Integer)  
            MsgBox("The value of x is: " & CStr(x))  
        End Sub  
    End Class  
    ```  
  
3.  <span data-ttu-id="dbe66-107">デリゲートのインスタンスを作成し、組み込みを呼び出すことによって、デリゲートに関連付けられているメソッドを呼び出し、メソッドを定義`Invoke`メソッド。</span><span class="sxs-lookup"><span data-stu-id="dbe66-107">Define a method that creates an instance of the delegate and invokes the method associated with the delegate by calling the built-in `Invoke` method.</span></span>  
  
    ```  
    Protected Sub DelegateTest()  
        Dim c1 As New class1  
        ' Create an instance of the delegate.  
        Dim msd As MySubDelegate = AddressOf c1.Sub1  
        ' Call the method.  
        msd.Invoke(10)  
    End Sub  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="dbe66-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="dbe66-108">See also</span></span>

- [<span data-ttu-id="dbe66-109">Delegate ステートメント</span><span class="sxs-lookup"><span data-stu-id="dbe66-109">Delegate Statement</span></span>](../../../../visual-basic/language-reference/statements/delegate-statement.md)  
- [<span data-ttu-id="dbe66-110">デリゲート</span><span class="sxs-lookup"><span data-stu-id="dbe66-110">Delegates</span></span>](../../../../visual-basic/programming-guide/language-features/delegates/index.md)  
- [<span data-ttu-id="dbe66-111">イベント</span><span class="sxs-lookup"><span data-stu-id="dbe66-111">Events</span></span>](../../../../visual-basic/programming-guide/language-features/events/index.md)  
- [<span data-ttu-id="dbe66-112">マルチスレッド アプリケーション</span><span class="sxs-lookup"><span data-stu-id="dbe66-112">Multithreaded Applications</span></span>](../../../../standard/threading/using-threads-and-threading.md)
