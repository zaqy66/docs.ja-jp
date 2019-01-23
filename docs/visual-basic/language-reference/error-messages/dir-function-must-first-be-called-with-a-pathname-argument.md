---
title: '&#39;Dir&#39;で関数を呼び出すことがまず必要があります、 &#39;PathName&#39;引数'
ms.date: 07/20/2015
f1_keywords:
- vbrDIR_IllegalCall
ms.assetid: 7b5d149f-be91-4ac3-8262-86a360894e7d
ms.openlocfilehash: f7e9ef9cc6309f24ae9f8963e910b41180c029b7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54518489"
---
# <a name="39dir39-function-must-first-be-called-with-a-39pathname39-argument"></a><span data-ttu-id="7a209-102">&#39;Dir&#39;で関数を呼び出すことがまず必要があります、 &#39;PathName&#39;引数</span><span class="sxs-lookup"><span data-stu-id="7a209-102">&#39;Dir&#39; function must first be called with a &#39;PathName&#39; argument</span></span>
<span data-ttu-id="7a209-103">最初に呼び出すとき、`Dir`関数には含まれません、`PathName`引数。</span><span class="sxs-lookup"><span data-stu-id="7a209-103">An initial call to the `Dir` function does not include the `PathName` argument.</span></span> <span data-ttu-id="7a209-104">最初の呼び出し`Dir`含める必要があります、`PathName`が後続の呼び出し`Dir`次の項目を取得するパラメーターを含める必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7a209-104">The first call to `Dir` must include a `PathName`, but subsequent calls to `Dir` do not need to include parameters to retrieve the next item.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="7a209-105">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="7a209-105">To correct this error</span></span>  
  
1.  <span data-ttu-id="7a209-106">指定、`PathName`関数呼び出しの引数。</span><span class="sxs-lookup"><span data-stu-id="7a209-106">Supply a `PathName` argument in the function call.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a209-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a209-107">See also</span></span>
- <xref:Microsoft.VisualBasic.FileSystem.Dir%2A>
