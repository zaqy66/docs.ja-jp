---
title: '&lt;「解説」&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <remarks> XML tag
- remarks XML tag
ms.assetid: c6241773-a7ed-41c9-9a8b-9722a0c606a9
ms.openlocfilehash: 97fca8758d9c21ac0b8f15bf9d5831750fbabe77
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43746968"
---
# <a name="ltremarksgt-visual-basic"></a><span data-ttu-id="b1ecb-102">&lt;「解説」&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b1ecb-102">&lt;remarks&gt; (Visual Basic)</span></span>
<span data-ttu-id="b1ecb-103">メンバーの「解説」セクションをを指定します。</span><span class="sxs-lookup"><span data-stu-id="b1ecb-103">Specifies a remarks section for the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1ecb-104">構文</span><span class="sxs-lookup"><span data-stu-id="b1ecb-104">Syntax</span></span>  
  
```xml  
<remarks>description</remarks>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b1ecb-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1ecb-105">Parameters</span></span>  
 `description`  
 <span data-ttu-id="b1ecb-106">メンバーの説明。</span><span class="sxs-lookup"><span data-stu-id="b1ecb-106">A description of the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b1ecb-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="b1ecb-107">Remarks</span></span>  
 <span data-ttu-id="b1ecb-108">使用して、`<remarks>`で指定された情報を補うため、型に関する情報を追加するタグ[\<概要 >](../../../visual-basic/language-reference/xmldoc/summary.md)します。</span><span class="sxs-lookup"><span data-stu-id="b1ecb-108">Use the `<remarks>` tag to add information about a type, supplementing the information specified with [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md).</span></span>  
  
 <span data-ttu-id="b1ecb-109">この情報は、オブジェクト ブラウザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b1ecb-109">This information appears in the Object Browser.</span></span> <span data-ttu-id="b1ecb-110">オブジェクト ブラウザーの詳細については、次を参照してください。[コードの構造を表示する](/visualstudio/ide/viewing-the-structure-of-code)します。</span><span class="sxs-lookup"><span data-stu-id="b1ecb-110">For information about the Object Browser, see [Viewing the Structure of Code](/visualstudio/ide/viewing-the-structure-of-code).</span></span>  
  
 <span data-ttu-id="b1ecb-111">コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="b1ecb-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b1ecb-112">例</span><span class="sxs-lookup"><span data-stu-id="b1ecb-112">Example</span></span>  
 <span data-ttu-id="b1ecb-113">この例では、`<remarks>`何かを説明するタグ、`UpdateRecord`メソッドします。</span><span class="sxs-lookup"><span data-stu-id="b1ecb-113">This example uses the `<remarks>` tag to explain what the `UpdateRecord` method does.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/remarks_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="b1ecb-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1ecb-114">See Also</span></span>  
 [<span data-ttu-id="b1ecb-115">XML のコメント用タグ</span><span class="sxs-lookup"><span data-stu-id="b1ecb-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
