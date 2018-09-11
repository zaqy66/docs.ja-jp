---
title: '#領域ディレクティブ (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.Region
- vb.#Region
helpviewer_keywords:
- Visual Basic compiler, compiler directives
- '#region directive'
- region directive (#region)
- '#Region keyword [Visual Basic]'
ms.assetid: 90a6a104-3cbf-47d0-bdc4-b585d0921b87
ms.openlocfilehash: 204b53751fce4f9a3e038ae7c44634522d54657c
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/10/2018
ms.locfileid: "44264182"
---
# <a name="region-directive"></a><span data-ttu-id="751c9-102">#Region ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="751c9-102">#Region Directive</span></span>
<span data-ttu-id="751c9-103">Visual Basic ファイルのコードのセクションを折りたたんで非表示にします。</span><span class="sxs-lookup"><span data-stu-id="751c9-103">Collapses and hides sections of code in Visual Basic files.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="751c9-104">構文</span><span class="sxs-lookup"><span data-stu-id="751c9-104">Syntax</span></span>  

```vb
#Region "identifier_string"  
#End Region  
```  
  
## <a name="parts"></a><span data-ttu-id="751c9-105">指定項目</span><span class="sxs-lookup"><span data-stu-id="751c9-105">Parts</span></span>  
  
|<span data-ttu-id="751c9-106">用語</span><span class="sxs-lookup"><span data-stu-id="751c9-106">Term</span></span>|<span data-ttu-id="751c9-107">定義</span><span class="sxs-lookup"><span data-stu-id="751c9-107">Definition</span></span>|  
|---|---|  
|`identifier_string`|<span data-ttu-id="751c9-108">必須。</span><span class="sxs-lookup"><span data-stu-id="751c9-108">Required.</span></span> <span data-ttu-id="751c9-109">領域が折りたたまれたときにその領域のタイトルとして機能する文字列です。</span><span class="sxs-lookup"><span data-stu-id="751c9-109">String that acts as the title of a region when it is collapsed.</span></span> <span data-ttu-id="751c9-110">既定では、領域は折りたたまれています。</span><span class="sxs-lookup"><span data-stu-id="751c9-110">Regions are collapsed by default.</span></span>|  
|`#End Region`|<span data-ttu-id="751c9-111">`#Region` ブロックを終了します。</span><span class="sxs-lookup"><span data-stu-id="751c9-111">Terminates the `#Region` block.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="751c9-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="751c9-112">Remarks</span></span>  
 <span data-ttu-id="751c9-113">Visual Studio コード エディターのアウトライン機能を使うときに展開または折りたたみの対象となるコード ブロックを指定するには、`#Region` ディレクティブを使用します。</span><span class="sxs-lookup"><span data-stu-id="751c9-113">Use the `#Region` directive to specify a block of code to expand or collapse when using the outlining feature of the Visual Studio Code Editor.</span></span> <span data-ttu-id="751c9-114">に配置するまたは*入れ子*、類似した領域をグループ化するには、他のリージョン内のリージョン。</span><span class="sxs-lookup"><span data-stu-id="751c9-114">You can place, or *nest*, regions within other regions to group similar regions together.</span></span>  
  
## <a name="example"></a><span data-ttu-id="751c9-115">例</span><span class="sxs-lookup"><span data-stu-id="751c9-115">Example</span></span>  
 <span data-ttu-id="751c9-116">`#Region` ディレクティブの使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="751c9-116">This example uses the `#Region` directive.</span></span>  
  
 [!code-vb[VbVbalrConditionalComp#4](../../../visual-basic/language-reference/directives/codesnippet/VisualBasic/region-directive_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="751c9-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="751c9-117">See Also</span></span>  
 [<span data-ttu-id="751c9-118">#If...Then...#Else ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="751c9-118">#If...Then...#Else Directives</span></span>](../../../visual-basic/language-reference/directives/if-then-else-directives.md)  
 [<span data-ttu-id="751c9-119">アウトライン</span><span class="sxs-lookup"><span data-stu-id="751c9-119">Outlining</span></span>](/visualstudio/ide/outlining)  
 [<span data-ttu-id="751c9-120">方法 : コードのセクションを折りたたんで非表示にする</span><span class="sxs-lookup"><span data-stu-id="751c9-120">How to: Collapse and Hide Sections of Code</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-collapse-and-hide-sections-of-code.md)
