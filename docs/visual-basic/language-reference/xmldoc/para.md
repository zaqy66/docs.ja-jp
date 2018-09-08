---
title: '&lt;para&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <para> XML tag
- para XML tag
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
ms.openlocfilehash: fa11c713a5ed5793b50865753f8bcdeaabf56e83
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44132358"
---
# <a name="ltparagt-visual-basic"></a><span data-ttu-id="9c69b-102">&lt;para&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9c69b-102">&lt;para&gt; (Visual Basic)</span></span>
<span data-ttu-id="9c69b-103">コンテンツが文章としてフォーマットされているを指定します。</span><span class="sxs-lookup"><span data-stu-id="9c69b-103">Specifies that the content is formatted as a paragraph.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c69b-104">構文</span><span class="sxs-lookup"><span data-stu-id="9c69b-104">Syntax</span></span>  
  
```xml  
<para>content</para>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9c69b-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9c69b-105">Parameters</span></span>  
 `content`  
 <span data-ttu-id="9c69b-106">段落のテキストです。</span><span class="sxs-lookup"><span data-stu-id="9c69b-106">The text of the paragraph.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9c69b-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="9c69b-107">Remarks</span></span>  
 <span data-ttu-id="9c69b-108">`<para>`などは、タグの内側で使用するタグ[\<概要 >](../../../visual-basic/language-reference/xmldoc/summary.md)、 [\<解説 >](../../../visual-basic/language-reference/xmldoc/remarks.md)、または[\<返します >](../../../visual-basic/language-reference/xmldoc/returns.md)、テキストに構造を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="9c69b-108">The `<para>` tag is for use inside a tag, such as [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md), [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md), or [\<returns>](../../../visual-basic/language-reference/xmldoc/returns.md), and lets you add structure to the text.</span></span>  
  
 <span data-ttu-id="9c69b-109">コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="9c69b-109">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9c69b-110">例</span><span class="sxs-lookup"><span data-stu-id="9c69b-110">Example</span></span>  
 <span data-ttu-id="9c69b-111">この例では、`<para>`の「解説」セクションに分割するタグ、`UpdateRecord`メソッドが 2 つの段落にします。</span><span class="sxs-lookup"><span data-stu-id="9c69b-111">This example uses the `<para>` tag to split the remarks section for the `UpdateRecord` method into two paragraphs.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/para_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="9c69b-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c69b-112">See Also</span></span>  
 [<span data-ttu-id="9c69b-113">XML のコメント用タグ</span><span class="sxs-lookup"><span data-stu-id="9c69b-113">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
