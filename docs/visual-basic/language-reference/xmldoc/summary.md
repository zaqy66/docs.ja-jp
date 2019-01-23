---
title: '&lt;summary&gt;(Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <summary> XML tag
- summary XML tag
ms.assetid: 861c847d-dd94-478a-aa23-bf4899cdc848
ms.openlocfilehash: 899a3343d9758aab79f5aaa77ede26e92f8c07ae
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54551009"
---
# <a name="ltsummarygt-visual-basic"></a><span data-ttu-id="dfd4f-102">&lt;summary&gt;(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dfd4f-102">&lt;summary&gt; (Visual Basic)</span></span>
<span data-ttu-id="dfd4f-103">メンバーの概要を指定します。</span><span class="sxs-lookup"><span data-stu-id="dfd4f-103">Specifies the summary of the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dfd4f-104">構文</span><span class="sxs-lookup"><span data-stu-id="dfd4f-104">Syntax</span></span>  
  
```xml  
<summary>description</summary>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="dfd4f-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dfd4f-105">Parameters</span></span>  
 `description`  
 <span data-ttu-id="dfd4f-106">オブジェクトの概要。</span><span class="sxs-lookup"><span data-stu-id="dfd4f-106">A summary of the object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dfd4f-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="dfd4f-107">Remarks</span></span>  
 <span data-ttu-id="dfd4f-108">使用して、`<summary>`型または型のメンバーを記述するタグ。</span><span class="sxs-lookup"><span data-stu-id="dfd4f-108">Use the `<summary>` tag to describe a type or a type member.</span></span> <span data-ttu-id="dfd4f-109">型の説明に補足情報を追加するには、[\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md) タグを使用します。</span><span class="sxs-lookup"><span data-stu-id="dfd4f-109">Use [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md) to add supplemental information to a type description.</span></span>  
  
 <span data-ttu-id="dfd4f-110">テキスト、`<summary>`タグは IntelliSense の型に関する情報の唯一のソースであり、オブジェクト ブラウザーにも表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfd4f-110">The text for the `<summary>` tag is the only source of information about the type in IntelliSense, and is also displayed in the Object Browser.</span></span> <span data-ttu-id="dfd4f-111">オブジェクト ブラウザーの詳細については、次を参照してください。[コードの構造を表示する](/visualstudio/ide/viewing-the-structure-of-code)します。</span><span class="sxs-lookup"><span data-stu-id="dfd4f-111">For information about the Object Browser, see [Viewing the Structure of Code](/visualstudio/ide/viewing-the-structure-of-code).</span></span>  
  
 <span data-ttu-id="dfd4f-112">コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="dfd4f-112">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dfd4f-113">例</span><span class="sxs-lookup"><span data-stu-id="dfd4f-113">Example</span></span>  
 <span data-ttu-id="dfd4f-114">この例では、`<summary>`を記述するタグ、`ResetCounter`メソッドと`Counter`プロパティ。</span><span class="sxs-lookup"><span data-stu-id="dfd4f-114">This example uses the `<summary>` tag to describe the `ResetCounter` method and `Counter` property.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/summary_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="dfd4f-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="dfd4f-115">See also</span></span>
- [<span data-ttu-id="dfd4f-116">XML のコメント用タグ</span><span class="sxs-lookup"><span data-stu-id="dfd4f-116">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
