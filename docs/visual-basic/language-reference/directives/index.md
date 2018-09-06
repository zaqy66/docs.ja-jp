---
title: ディレクティブ (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- directives, Visual Basic compiler
- Visual Basic code, directives
- directives
ms.assetid: 20d5fe65-490a-4c23-88c2-ee4f490ed762
ms.openlocfilehash: 38d54feae5cf7bf41a825d1f6000811e2b56f319
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "44032058"
---
# <a name="directives-visual-basic"></a><span data-ttu-id="20931-102">ディレクティブ (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="20931-102">Directives (Visual Basic)</span></span>
<span data-ttu-id="20931-103">このセクションのトピックでは、Visual Basic ソース コードのコンパイラ ディレクティブについて説明します。</span><span class="sxs-lookup"><span data-stu-id="20931-103">The topics in this section document the Visual Basic source code compiler directives.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="20931-104">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="20931-104">In This Section</span></span>  
 <span data-ttu-id="20931-105">[#Const ディレクティブ](../../../visual-basic/language-reference/directives/const-directive.md)--コンパイラ定数の定義</span><span class="sxs-lookup"><span data-stu-id="20931-105">[#Const Directive](../../../visual-basic/language-reference/directives/const-directive.md) -- Define a compiler constant</span></span>  
  
 <span data-ttu-id="20931-106">[#ExternalSource ディレクティブ](../../../visual-basic/language-reference/directives/externalsource-directive.md)--ソース行とソース外部のテキストの間のマッピングを示します</span><span class="sxs-lookup"><span data-stu-id="20931-106">[#ExternalSource Directive](../../../visual-basic/language-reference/directives/externalsource-directive.md) -- Indicate a mapping between source lines and text external to the source</span></span>  
  
 <span data-ttu-id="20931-107">[#If.Then... #Else ディレクティブ](../../../visual-basic/language-reference/directives/if-then-else-directives.md)--選択したコード ブロックのコンパイル</span><span class="sxs-lookup"><span data-stu-id="20931-107">[#If...Then...#Else Directives](../../../visual-basic/language-reference/directives/if-then-else-directives.md) -- Compile selected blocks of code</span></span>  
  
 <span data-ttu-id="20931-108">[#Region ディレクティブ](../../../visual-basic/language-reference/directives/region-directive.md): 折りたたむし、Visual Studio エディターでコードのセクションを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="20931-108">[#Region Directive](../../../visual-basic/language-reference/directives/region-directive.md) -- Collapse and hide sections of code in the Visual Studio editor</span></span>  
  
 <span data-ttu-id="20931-109">**#Disable、#Enable** : 無効にして、コードの領域の特定の警告を有効にします。</span><span class="sxs-lookup"><span data-stu-id="20931-109">**#Disable, #Enable** -- Disable and enable specific warnings for regions of code.</span></span>  
  
```vb  
#Disable Warning BC42356 ' suppress warning about no awaits in this method  
    Async Function TestAsync() As Task  
        Console.WriteLine("testing")  
    End Function  
#Enable Warning BC42356  
```  
  
 <span data-ttu-id="20931-110">警告コードのコンマ区切りリストを無効および有効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="20931-110">You can disable and enable a comma-separated list of warning codes too.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="20931-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="20931-111">Related Sections</span></span>  
 [<span data-ttu-id="20931-112">Visual Basic の言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="20931-112">Visual Basic Language Reference</span></span>](../../../visual-basic/language-reference/index.md)  
  
 [<span data-ttu-id="20931-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="20931-113">Visual Basic</span></span>](../../../visual-basic/index.md)
