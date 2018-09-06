---
title: ターゲット ディレクトリがソース ディレクトリ内にあるため、操作を完了できませんでした
ms.date: 07/20/2015
f1_keywords:
- vbrIO_CyclicOperation
ms.assetid: 850d3a24-5d51-4ac8-a912-630efcd75278
ms.openlocfilehash: b821034731514362a3725c390e02542b536f0a59
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43890805"
---
# <a name="could-not-complete-operation-since-target-directory-is-under-source-directory"></a><span data-ttu-id="dff33-102">ターゲット ディレクトリがソース ディレクトリ内にあるため、操作を完了できませんでした</span><span class="sxs-lookup"><span data-stu-id="dff33-102">Could not complete operation since target directory is under source directory</span></span>
<span data-ttu-id="dff33-103">循環操作が失敗しました。</span><span class="sxs-lookup"><span data-stu-id="dff33-103">A cyclic operation has failed.</span></span> <span data-ttu-id="dff33-104">循環操作は循環しているため、完了できません。</span><span class="sxs-lookup"><span data-stu-id="dff33-104">Cyclic operations cycle and therefore cannot complete.</span></span> <span data-ttu-id="dff33-105">たとえば、オブジェクト A がオブジェクト B の継承を試行し、同様にオブジェクト B がオブジェクト A の継承を試行するような場合です。</span><span class="sxs-lookup"><span data-stu-id="dff33-105">For example, Object A may attempt to inherit from Object B, which in turn inherits from Object A.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="dff33-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="dff33-106">To correct this error</span></span>  
  
-   <span data-ttu-id="dff33-107">継承を行うときには、参照の循環がないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="dff33-107">When inheriting, make sure that there are no cyclic references.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dff33-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="dff33-108">See Also</span></span>  
 [<span data-ttu-id="dff33-109">エラーの種類</span><span class="sxs-lookup"><span data-stu-id="dff33-109">Error Types</span></span>](../../visual-basic/programming-guide/language-features/error-types.md)  
 [<span data-ttu-id="dff33-110">デバッグの基礎: ブレークポイント</span><span class="sxs-lookup"><span data-stu-id="dff33-110">Debugging Basics: Breakpoints</span></span>](https://msdn.microsoft.com/library/752a02c2-0ac7-4c8b-aa1b-4b2b3b21152e)
