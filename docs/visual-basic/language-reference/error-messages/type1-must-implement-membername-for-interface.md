---
title: '&lt;type1&gt;&#39;&lt;typename&gt; &#39;実装する必要があります&#39; &lt;membername&gt; &#39;インターフェイス&#39; &lt;interfacename&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30154
- bc30154
helpviewer_keywords:
- BC30154
ms.assetid: 259afdfa-3608-4760-adcb-88ec0da5020d
ms.openlocfilehash: 14e7bd199215764676a4b563eafc68bd6dabadc7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574743"
---
# <a name="lttype1gt39lttypenamegt39-must-implement-39ltmembernamegt39-for-interface-39ltinterfacenamegt39"></a><span data-ttu-id="7aae1-102">&lt;type1&gt;&#39;&lt;typename&gt; &#39;実装する必要があります&#39; &lt;membername&gt; &#39;インターフェイス&#39; &lt;interfacename&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="7aae1-102">&lt;type1&gt;&#39;&lt;typename&gt;&#39; must implement &#39;&lt;membername&gt;&#39; for interface &#39;&lt;interfacename&gt;&#39;</span></span>
<span data-ttu-id="7aae1-103">'\<typename >' を実装する必要があります'\<membername >' のインターフェイス '\<interfacename >'。</span><span class="sxs-lookup"><span data-stu-id="7aae1-103">'\<typename>' must implement '\<membername>' for interface '\<interfacename>'.</span></span> <span data-ttu-id="7aae1-104">'ReadOnly' を持つプロパティを実装する/'WriteOnly' 指定子。</span><span class="sxs-lookup"><span data-stu-id="7aae1-104">Implementing property must have matching 'ReadOnly'/'WriteOnly' specifiers.</span></span>  
  
 <span data-ttu-id="7aae1-105">クラスまたは構造体、インターフェイスを実装する要求が、プロシージャ、プロパティ、またはインターフェイスで定義したイベントを実装しません。</span><span class="sxs-lookup"><span data-stu-id="7aae1-105">A class or structure claims to implement an interface but does not implement a procedure, property, or event defined by the interface.</span></span> <span data-ttu-id="7aae1-106">インターフェイスのすべてのメンバーを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7aae1-106">Every member of the interface must be implemented.</span></span>  
  
 <span data-ttu-id="7aae1-107">**エラー ID:** BC30154</span><span class="sxs-lookup"><span data-stu-id="7aae1-107">**Error ID:** BC30154</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="7aae1-108">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="7aae1-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="7aae1-109">同じ名前と、インターフェイスで定義されたシグネチャを持つメンバーを宣言します。</span><span class="sxs-lookup"><span data-stu-id="7aae1-109">Declare a member with the same name and signature as defined in the interface.</span></span> <span data-ttu-id="7aae1-110">必ず含めて、少なくとも`End Function`、 `End Sub`、または`End Property`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="7aae1-110">Be sure to include at least the `End Function`, `End Sub`, or `End Property` statement.</span></span>  
  
2.  <span data-ttu-id="7aae1-111">追加、`Implements`句の末尾に、 `Function`、 `Sub`、 `Property`、または`Event`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="7aae1-111">Add an `Implements` clause to the end of the `Function`, `Sub`, `Property`, or `Event` statement.</span></span> <span data-ttu-id="7aae1-112">例:</span><span class="sxs-lookup"><span data-stu-id="7aae1-112">For example:</span></span>  
  
    ```  
    Public Event ItHappened() Implements IBaseInterface.ItHappened  
    ```  
  
3.  <span data-ttu-id="7aae1-113">プロパティを実装する場合、以下のことを確認`ReadOnly`または`WriteOnly`インターフェイスの定義と同じ方法で使用されます。</span><span class="sxs-lookup"><span data-stu-id="7aae1-113">When implementing a property, make sure that `ReadOnly` or `WriteOnly` is used in the same way as in the interface definition.</span></span>  
  
4.  <span data-ttu-id="7aae1-114">プロパティを実装する場合は、宣言`Get`と`Set`プロシージャに、必要に応じて。</span><span class="sxs-lookup"><span data-stu-id="7aae1-114">When implementing a property, declare `Get` and `Set` procedures, as appropriate.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7aae1-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="7aae1-115">See also</span></span>
- [<span data-ttu-id="7aae1-116">Implements ステートメント</span><span class="sxs-lookup"><span data-stu-id="7aae1-116">Implements Statement</span></span>](../../../visual-basic/language-reference/statements/implements-statement.md)
- [<span data-ttu-id="7aae1-117">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="7aae1-117">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
