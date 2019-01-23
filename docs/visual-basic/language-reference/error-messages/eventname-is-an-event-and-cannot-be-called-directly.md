---
title: '&#39;&lt;eventname&gt; &#39;イベントは、直接呼び出すことはできません'
ms.date: 07/20/2015
f1_keywords:
- bc32022
- vbc32022
helpviewer_keywords:
- BC32022
ms.assetid: 4dcfcb8d-a9fa-46a7-a034-29d9ff3a59b3
ms.openlocfilehash: 3efd8c18497ce288e16659db4ca4693d5a3e6acc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54581997"
---
# <a name="39lteventnamegt39-is-an-event-and-cannot-be-called-directly"></a><span data-ttu-id="89753-102">&#39;&lt;eventname&gt; &#39;イベントは、直接呼び出すことはできません</span><span class="sxs-lookup"><span data-stu-id="89753-102">&#39;&lt;eventname&gt;&#39; is an event, and cannot be called directly</span></span>
<span data-ttu-id="89753-103">' <`eventname`>' は、イベントで、これは直接呼び出すことができません。</span><span class="sxs-lookup"><span data-stu-id="89753-103">'<`eventname`>' is an event, and so cannot be called directly.</span></span> <span data-ttu-id="89753-104">使用して、`RaiseEvent`イベントを発生させるステートメントです。</span><span class="sxs-lookup"><span data-stu-id="89753-104">Use a `RaiseEvent` statement to raise an event.</span></span>  
  
 <span data-ttu-id="89753-105">プロシージャ呼び出しでは、イベント プロシージャ名を指定します。</span><span class="sxs-lookup"><span data-stu-id="89753-105">A procedure call specifies an event for the procedure name.</span></span> <span data-ttu-id="89753-106">イベント ハンドラーは、プロシージャが、イベント自体はシグナル デバイスで発生して処理する必要がありますが、です。</span><span class="sxs-lookup"><span data-stu-id="89753-106">An event handler is a procedure, but the event itself is a signaling device, which must be raised and handled.</span></span>  
  
 <span data-ttu-id="89753-107">**エラー ID:** BC32022</span><span class="sxs-lookup"><span data-stu-id="89753-107">**Error ID:** BC32022</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="89753-108">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="89753-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="89753-109">使用して、`RaiseEvent`イベントを通知し、それを処理する手順を起動するステートメント。</span><span class="sxs-lookup"><span data-stu-id="89753-109">Use a `RaiseEvent` statement to signal an event and invoke the procedure or procedures that handle it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="89753-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="89753-110">See also</span></span>
- [<span data-ttu-id="89753-111">RaiseEvent ステートメント</span><span class="sxs-lookup"><span data-stu-id="89753-111">RaiseEvent Statement</span></span>](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
