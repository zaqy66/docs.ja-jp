---
title: '&lt;c&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- c XML tag
- <c> XML tag
ms.assetid: 36ad5d1b-11f7-4012-8932-41962ac327d1
ms.openlocfilehash: 06c6899895f278fdf652725a05ecc7229805f4d4
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43455706"
---
# <a name="ltcgt-visual-basic"></a><span data-ttu-id="bc22c-102">&lt;c&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bc22c-102">&lt;c&gt; (Visual Basic)</span></span>
<span data-ttu-id="bc22c-103">説明内のテキストがコードであることを示します。</span><span class="sxs-lookup"><span data-stu-id="bc22c-103">Indicates that text within a description is code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bc22c-104">構文</span><span class="sxs-lookup"><span data-stu-id="bc22c-104">Syntax</span></span>  
  
```xml  
<c>text</c>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bc22c-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bc22c-105">Parameters</span></span>  
  
|<span data-ttu-id="bc22c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bc22c-106">Parameter</span></span>|<span data-ttu-id="bc22c-107">説明</span><span class="sxs-lookup"><span data-stu-id="bc22c-107">Description</span></span>|  
|---|---|  
|`text`|<span data-ttu-id="bc22c-108">コードとして指定するテキストです。</span><span class="sxs-lookup"><span data-stu-id="bc22c-108">The text you would like to indicate as code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bc22c-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="bc22c-109">Remarks</span></span>  
 <span data-ttu-id="bc22c-110">`<c>`タグを使用する方法を示す説明内のテキストをコードとしてマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc22c-110">The `<c>` tag gives you a way to indicate that text within a description should be marked as code.</span></span> <span data-ttu-id="bc22c-111">複数行をコードとして指定する場合は、[\<code>](../../../visual-basic/language-reference/xmldoc/code.md) タグを使用します。</span><span class="sxs-lookup"><span data-stu-id="bc22c-111">Use [\<code>](../../../visual-basic/language-reference/xmldoc/code.md) to indicate multiple lines as code.</span></span>  
  
 <span data-ttu-id="bc22c-112">コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="bc22c-112">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bc22c-113">例</span><span class="sxs-lookup"><span data-stu-id="bc22c-113">Example</span></span>  
 <span data-ttu-id="bc22c-114">この例では、`<c>`ことを示す [概要] セクションでタグ`Counter`コードに示します。</span><span class="sxs-lookup"><span data-stu-id="bc22c-114">This example uses the `<c>` tag in the summary section to indicate that `Counter` is code.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/c_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="bc22c-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="bc22c-115">See Also</span></span>  
 [<span data-ttu-id="bc22c-116">XML のコメント用タグ</span><span class="sxs-lookup"><span data-stu-id="bc22c-116">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
