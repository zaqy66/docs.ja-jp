---
title: -nowin32manifest (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- /nowin32manifest compiler option [Visual Basic]
- nowin32manifest compiler option [Visual Basic]
- -nowin32manifest compiler option [Visual Basic]
ms.assetid: c0528aae-83b3-4425-99f0-19448e9843e3
ms.openlocfilehash: 382e8fd089211f6d23a1e6baff93bf08f19248c8
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2018
ms.locfileid: "50035762"
---
# <a name="-nowin32manifest-visual-basic"></a><span data-ttu-id="af15a-102">-nowin32manifest (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="af15a-102">-nowin32manifest (Visual Basic)</span></span>
<span data-ttu-id="af15a-103">アプリケーション マニフェストを実行可能ファイルに埋め込まないようコンパイラに指定します。</span><span class="sxs-lookup"><span data-stu-id="af15a-103">Instructs the compiler not to embed any application manifest into the executable file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="af15a-104">構文</span><span class="sxs-lookup"><span data-stu-id="af15a-104">Syntax</span></span>  
  
```  
-nowin32manifest  
```  
  
## <a name="remarks"></a><span data-ttu-id="af15a-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="af15a-105">Remarks</span></span>  
 <span data-ttu-id="af15a-106">このオプションを使用すると、Win32 リソース ファイルに、あるいは後のビルド ステップでアプリケーション マニフェストを指定しない限り、 Windows Vista で仮想化に従います。</span><span class="sxs-lookup"><span data-stu-id="af15a-106">When this option is used, the application will be subject to virtualization on Windows Vista unless you provide an application manifest in a Win32 Resource file or during a later build step.</span></span> <span data-ttu-id="af15a-107">仮想化の詳細については、次を参照してください。 [Windows Vista の ClickOnce 配置](/visualstudio/deployment/clickonce-deployment-on-windows-vista)します。</span><span class="sxs-lookup"><span data-stu-id="af15a-107">For more information about virtualization, see [ClickOnce Deployment on Windows Vista](/visualstudio/deployment/clickonce-deployment-on-windows-vista).</span></span>  
  
 <span data-ttu-id="af15a-108">マニフェスト作成の詳細については、次を参照してください。 [-win32manifest (Visual Basic)](../../../visual-basic/reference/command-line-compiler/win32manifest.md)します。</span><span class="sxs-lookup"><span data-stu-id="af15a-108">For more information about manifest creation, see [-win32manifest (Visual Basic)](../../../visual-basic/reference/command-line-compiler/win32manifest.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="af15a-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="af15a-109">See Also</span></span>  
 [<span data-ttu-id="af15a-110">Visual Basic のコマンド ライン コンパイラ</span><span class="sxs-lookup"><span data-stu-id="af15a-110">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 <span data-ttu-id="af15a-111">[[アプリケーション] ページ (プロジェクト デザイナー)](/visualstudio/ide/reference/application-page-project-designer-visual-basic)</span><span class="sxs-lookup"><span data-stu-id="af15a-111">[Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic)</span></span>
