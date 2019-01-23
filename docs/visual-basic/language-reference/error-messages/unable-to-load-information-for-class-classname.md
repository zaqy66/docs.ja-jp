---
title: クラスの情報を読み込めません&#39; &lt;classname&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- vbc30712
- bc30712
helpviewer_keywords:
- BC30712
ms.assetid: c7ffbd6d-05c6-4261-b44b-1bcd521bb350
ms.openlocfilehash: 368484d9138d1ae10efb8c63f6cfaa6bcefa6ed8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54528963"
---
# <a name="unable-to-load-information-for-class-39ltclassnamegt39"></a><span data-ttu-id="bf4fd-102">クラスの情報を読み込めません&#39; &lt;classname&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="bf4fd-102">Unable to load information for class &#39;&lt;classname&gt;&#39;</span></span>
<span data-ttu-id="bf4fd-103">無効なクラスに参照が行われました。</span><span class="sxs-lookup"><span data-stu-id="bf4fd-103">A reference was made to a class that is not available.</span></span>  
  
 <span data-ttu-id="bf4fd-104">**エラー ID:** BC30712</span><span class="sxs-lookup"><span data-stu-id="bf4fd-104">**Error ID:** BC30712</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="bf4fd-105">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="bf4fd-105">To correct this error</span></span>  
  
1.  <span data-ttu-id="bf4fd-106">クラスが定義されていると、名前のスペルが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="bf4fd-106">Verify that the class is defined and that you spelled the name correctly.</span></span>  
  
2.  <span data-ttu-id="bf4fd-107">モジュールで宣言されたいずれかのメンバーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="bf4fd-107">Try accessing one of the members declared in the module.</span></span> <span data-ttu-id="bf4fd-108">宣言されているモジュールがまだ読み込まれていないために、デバッグ環境ではメンバーを特定できないという場合もあります。</span><span class="sxs-lookup"><span data-stu-id="bf4fd-108">In some cases, the debugging environment cannot locate members because the modules where they are declared have not been loaded yet.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bf4fd-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf4fd-109">See also</span></span>
- [<span data-ttu-id="bf4fd-110">Visual Studio でのデバッグ</span><span class="sxs-lookup"><span data-stu-id="bf4fd-110">Debugging in Visual Studio</span></span>](/visualstudio/debugger/debugging-in-visual-studio)
