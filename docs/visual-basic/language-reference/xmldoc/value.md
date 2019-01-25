---
title: <value> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <value> XML tag
- value XML tag
ms.assetid: 0b84b02e-9e6d-41b5-a926-0d5dc76dacb5
ms.openlocfilehash: 5aab2307a1967ea660282c7b324eaddfe798a155
ms.sourcegitcommit: 5dcfeb59179e81071f54840d4902cbe00b184294
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/24/2019
ms.locfileid: "54857880"
---
# <a name="value-visual-basic"></a><span data-ttu-id="63c8f-102">\<値 > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="63c8f-102">\<value> (Visual Basic)</span></span>
<span data-ttu-id="63c8f-103">プロパティの説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="63c8f-103">Specifies the description of a property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63c8f-104">構文</span><span class="sxs-lookup"><span data-stu-id="63c8f-104">Syntax</span></span>  
  
```xml  
<value>property-description</value>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="63c8f-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63c8f-105">Parameters</span></span>  
 `property-description`  
 <span data-ttu-id="63c8f-106">プロパティの説明。</span><span class="sxs-lookup"><span data-stu-id="63c8f-106">A description for the property.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="63c8f-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="63c8f-107">Remarks</span></span>  
 <span data-ttu-id="63c8f-108">使用して、`<value>`プロパティを説明するタグ。</span><span class="sxs-lookup"><span data-stu-id="63c8f-108">Use the `<value>` tag to describe a property.</span></span> <span data-ttu-id="63c8f-109">Visual Studio 開発環境で、コード ウィザードを使用してプロパティを追加すると、追加されることに注意してください、 [\<概要 >](../../../visual-basic/language-reference/xmldoc/summary.md)新しいプロパティのタグ。</span><span class="sxs-lookup"><span data-stu-id="63c8f-109">Note that when you add a property using the code wizard in the Visual Studio development environment, it will add a [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md) tag for the new property.</span></span> <span data-ttu-id="63c8f-110">手動で追加する必要がありますし、`<value>`プロパティを表す値を記述するタグ。</span><span class="sxs-lookup"><span data-stu-id="63c8f-110">You should then manually add a `<value>` tag to describe the value that the property represents.</span></span>  
  
 <span data-ttu-id="63c8f-111">コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="63c8f-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="63c8f-112">例</span><span class="sxs-lookup"><span data-stu-id="63c8f-112">Example</span></span>  
 <span data-ttu-id="63c8f-113">この例では、`<value>`どのような値を記述するタグ、`Counter`プロパティを保持します。</span><span class="sxs-lookup"><span data-stu-id="63c8f-113">This example uses the `<value>` tag to describe what value the `Counter` property holds.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/value_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="63c8f-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="63c8f-114">See also</span></span>
- [<span data-ttu-id="63c8f-115">XML のコメント用タグ</span><span class="sxs-lookup"><span data-stu-id="63c8f-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
