---
title: '&lt;code&gt;(Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- code XML tag
- <code> XML tag
ms.assetid: 925e5342-be05-45f2-bf66-7398bbd6710e
ms.openlocfilehash: e66aebe35dd8f6443fefe3b07842b37270159e6e
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43858640"
---
# <a name="ltcodegt-visual-basic"></a><span data-ttu-id="1c608-102">&lt;code&gt;(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1c608-102">&lt;code&gt; (Visual Basic)</span></span>
<span data-ttu-id="1c608-103">テキストが複数行のコードであることを示します。</span><span class="sxs-lookup"><span data-stu-id="1c608-103">Indicates that the text is multiple lines of code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1c608-104">構文</span><span class="sxs-lookup"><span data-stu-id="1c608-104">Syntax</span></span>  
  
```xml  
<code>content</code>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1c608-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1c608-105">Parameters</span></span>  
 `content`  
 <span data-ttu-id="1c608-106">コードとしてマークするテキスト。</span><span class="sxs-lookup"><span data-stu-id="1c608-106">The text to mark as code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1c608-107">コメント</span><span class="sxs-lookup"><span data-stu-id="1c608-107">Remarks</span></span>  
 <span data-ttu-id="1c608-108">コードとして複数の行を示すには、`<code>`タグを使用します。</span><span class="sxs-lookup"><span data-stu-id="1c608-108">Use the `<code>` tag to indicate multiple lines as code.</span></span> <span data-ttu-id="1c608-109">説明内のテキストをコードとしてマークする場合は、[\<c](../../../visual-basic/language-reference/xmldoc/c.md) タグを使用します。  </span><span class="sxs-lookup"><span data-stu-id="1c608-109">Use [\<c>](../../../visual-basic/language-reference/xmldoc/c.md) to indicate that text within a description should be marked as code.</span></span>  
  
 <span data-ttu-id="1c608-110">コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="1c608-110">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1c608-111">例</span><span class="sxs-lookup"><span data-stu-id="1c608-111">Example</span></span>  
 <span data-ttu-id="1c608-112">この例では、\<code> タグを使用するためのサンプル コードを`ID`フィールド。</span><span class="sxs-lookup"><span data-stu-id="1c608-112">This example uses the \<code> tag to include example code for using the `ID` field.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#2](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/code_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="1c608-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="1c608-113">See Also</span></span>  
 [<span data-ttu-id="1c608-114">XML のコメント用タグ</span><span class="sxs-lookup"><span data-stu-id="1c608-114">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
