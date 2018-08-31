---
title: '&lt;参照してください&gt;(Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- see XML tag
- <see> XML tag
ms.assetid: 7e18f60b-ef4a-4678-a797-5eb918635ca9
ms.openlocfilehash: 78311651593d3d4a47c723f64a9a74d4660f7c90
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/30/2018
ms.locfileid: "43254063"
---
# <a name="ltseegt-visual-basic"></a><span data-ttu-id="1261b-102">&lt;参照してください&gt;(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1261b-102">&lt;see&gt; (Visual Basic)</span></span>
<span data-ttu-id="1261b-103">別のメンバーへのリンクを指定します。</span><span class="sxs-lookup"><span data-stu-id="1261b-103">Specifies a link to another member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1261b-104">構文</span><span class="sxs-lookup"><span data-stu-id="1261b-104">Syntax</span></span>  
  
```xml  
<see cref="member"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1261b-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1261b-105">Parameters</span></span>  
 `member`  
 <span data-ttu-id="1261b-106">現在のコンパイル環境からの呼び出しに利用できる、メンバーまたはフィールドへの参照。</span><span class="sxs-lookup"><span data-stu-id="1261b-106">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="1261b-107">コンパイラは、指定されたコード要素が存在し、渡すことを確認します。`member`出力 XML 内の要素名にします。</span><span class="sxs-lookup"><span data-stu-id="1261b-107">The compiler checks that the given code element exists and passes `member` to the element name in the output XML.</span></span> <span data-ttu-id="1261b-108">`member` は、二重引用符 (" ") で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="1261b-108">`member` must appear within double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1261b-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="1261b-109">Remarks</span></span>  
 <span data-ttu-id="1261b-110">使用して、`<see>`タグからテキスト内のリンクを指定します。</span><span class="sxs-lookup"><span data-stu-id="1261b-110">Use the `<see>` tag to specify a link from within text.</span></span> <span data-ttu-id="1261b-111">使用[ \<seealso >](../../../visual-basic/language-reference/xmldoc/seealso.md) 「「参照」セクションに表示するテキストを示します。</span><span class="sxs-lookup"><span data-stu-id="1261b-111">Use [\<seealso>](../../../visual-basic/language-reference/xmldoc/seealso.md) to indicate text that you might want to appear in a "See Also" section.</span></span>  
  
 <span data-ttu-id="1261b-112">コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="1261b-112">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1261b-113">例</span><span class="sxs-lookup"><span data-stu-id="1261b-113">Example</span></span>  
 <span data-ttu-id="1261b-114">この例では、`<see>`にタグを付ける、`UpdateRecord`解説セクションを参照する、`DoesRecordExist`メソッド。</span><span class="sxs-lookup"><span data-stu-id="1261b-114">This example uses the `<see>` tag in the `UpdateRecord` remarks section to refer to the `DoesRecordExist` method.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/see_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="1261b-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="1261b-115">See Also</span></span>  
 [<span data-ttu-id="1261b-116">XML のコメント用タグ</span><span class="sxs-lookup"><span data-stu-id="1261b-116">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
