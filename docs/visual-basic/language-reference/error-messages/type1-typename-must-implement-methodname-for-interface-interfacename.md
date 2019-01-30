---
title: <type1>'<typename>' は、インターフェイス '<methodname>' に対して '<interfacename>' を実装しなければなりません。
ms.date: 07/20/2015
f1_keywords:
- vbc30149
- bc30149
helpviewer_keywords:
- BC30149
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
ms.openlocfilehash: c5dd7c6889a3fb5344142ee9914f98e8922d748b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55264436"
---
# <a name="type1typename-must-implement-methodname-for-interface-interfacename"></a><span data-ttu-id="ea5d3-102">\<type1 >'\<typename >' を実装する必要があります '\<methodname >' のインターフェイス'\<interfacename >'</span><span class="sxs-lookup"><span data-stu-id="ea5d3-102">\<type1>'\<typename>' must implement '\<methodname>' for interface '\<interfacename>'</span></span>
<span data-ttu-id="ea5d3-103">クラスまたは構造体がインターフェイスを実装するために要求しているインターフェイスによって定義されたプロシージャを実装していません。</span><span class="sxs-lookup"><span data-stu-id="ea5d3-103">A class or structure claims to implement an interface but does not implement a procedure defined by the interface.</span></span> <span data-ttu-id="ea5d3-104">インターフェイスのすべてのメンバーを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea5d3-104">Every member of the interface must be implemented.</span></span>  
  
 <span data-ttu-id="ea5d3-105">**エラー ID:** BC30149</span><span class="sxs-lookup"><span data-stu-id="ea5d3-105">**Error ID:** BC30149</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ea5d3-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="ea5d3-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="ea5d3-107">同じ名前と、インターフェイスで定義されたシグネチャを持つプロシージャを宣言します。</span><span class="sxs-lookup"><span data-stu-id="ea5d3-107">Declare a procedure with the same name and signature as defined in the interface.</span></span> <span data-ttu-id="ea5d3-108">必ず含めて、少なくとも`End Function`または`End Sub`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="ea5d3-108">Be sure to include at least the `End Function` or `End Sub` statement.</span></span>  
  
2.  <span data-ttu-id="ea5d3-109">追加、`Implements`句の末尾に、`Function`または`Sub`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="ea5d3-109">Add an `Implements` clause to the end of the `Function` or `Sub` statement.</span></span> <span data-ttu-id="ea5d3-110">例:</span><span class="sxs-lookup"><span data-stu-id="ea5d3-110">For example:</span></span>  
  
    ```  
    Public Sub DoSomething() Implements IBaseInterface.DoSomething  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="ea5d3-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="ea5d3-111">See also</span></span>
- [<span data-ttu-id="ea5d3-112">Implements ステートメント</span><span class="sxs-lookup"><span data-stu-id="ea5d3-112">Implements Statement</span></span>](../../../visual-basic/language-reference/statements/implements-statement.md)
- [<span data-ttu-id="ea5d3-113">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ea5d3-113">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
