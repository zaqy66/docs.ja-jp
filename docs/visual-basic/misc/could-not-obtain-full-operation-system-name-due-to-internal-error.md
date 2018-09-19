---
title: 内部エラーのために完全な運用システム名を取得できませんでした
ms.date: 07/20/2015
f1_keywords:
- vbrDiagnosticInfo_FullOSName
ms.assetid: f69da02b-eb9a-4284-bb9e-3025517ae6c1
ms.openlocfilehash: 192033348a779591a54860505d5d707a802c415a
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/18/2018
ms.locfileid: "45972729"
---
# <a name="could-not-obtain-full-operation-system-name-due-to-internal-error"></a><span data-ttu-id="b7f7d-102">内部エラーのために完全な運用システム名を取得できませんでした</span><span class="sxs-lookup"><span data-stu-id="b7f7d-102">Could not obtain full operation system name due to internal error</span></span>
<span data-ttu-id="b7f7d-103">内部エラーのために完全な運用システム名を取得できませんでした。</span><span class="sxs-lookup"><span data-stu-id="b7f7d-103">Could not obtain full operation system name due to internal error.</span></span> <span data-ttu-id="b7f7d-104">これは、現在のコンピューターに WMI が存在しないことが原因である場合があります。</span><span class="sxs-lookup"><span data-stu-id="b7f7d-104">This might be caused by WMI not existing on the current machine.</span></span>  
  
 <span data-ttu-id="b7f7d-105">`My.Computer.Info.OSFullName` プロパティの呼び出しに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="b7f7d-105">A call to the `My.Computer.Info.OSFullName` property failed.</span></span> <span data-ttu-id="b7f7d-106">このエラーの考えられる原因は、Windows Management Instrumentation (WMI) が、現在のコンピューターにインストールされていないことです。</span><span class="sxs-lookup"><span data-stu-id="b7f7d-106">A possible cause for this failure is if Windows Management Instrumentation (WMI) is not installed on the current computer.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b7f7d-107">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="b7f7d-107">To correct this error</span></span>  
  
1.  <span data-ttu-id="b7f7d-108">`Try...Catch` プロパティの呼び出しの周囲に `My.Computer.Info.OSFullName` ブロックを追加します。</span><span class="sxs-lookup"><span data-stu-id="b7f7d-108">Add a `Try...Catch` block around the call to the `My.Computer.Info.OSFullName` property.</span></span>  
  
2.  <span data-ttu-id="b7f7d-109">WMI とそのインストール方法の詳細については、「Windows Management Instrumentation Core」を検索してに移動します。</span><span class="sxs-lookup"><span data-stu-id="b7f7d-109">For more information about WMI and how to install it, go to  and search for "Windows Management Instrumentation Core".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7f7d-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7f7d-110">See Also</span></span>  
 [<span data-ttu-id="b7f7d-111">My.Computer.Info.OSFullName</span><span class="sxs-lookup"><span data-stu-id="b7f7d-111">My.Computer.Info.OSFullName</span></span>](xref:Microsoft.VisualBasic.Devices.ComputerInfo.OSFullName)  
 [<span data-ttu-id="b7f7d-112">例外と Visual Basic でのエラー処理</span><span class="sxs-lookup"><span data-stu-id="b7f7d-112">Exception and Error Handling in Visual Basic</span></span>](https://msdn.microsoft.com/library/3e351e73-cf23-40ab-8b60-05794160529e)  
 [<span data-ttu-id="b7f7d-113">Try...Catch...Finally ステートメント</span><span class="sxs-lookup"><span data-stu-id="b7f7d-113">Try...Catch...Finally Statement</span></span>](../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
