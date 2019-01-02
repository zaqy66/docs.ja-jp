---
title: '&lt;returns&gt;(Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- returns XML tag
- <returns> XML tag
ms.assetid: a03a6469-d907-425d-882f-083187950e7e
ms.openlocfilehash: 47debcef2c6ce56fda4c4a0818c8e813b41ebad1
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/25/2018
ms.locfileid: "42925019"
---
# <a name="ltreturnsgt-visual-basic"></a><span data-ttu-id="57a41-102">&lt;returns&gt;(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="57a41-102">&lt;returns&gt; (Visual Basic)</span></span>
<span data-ttu-id="57a41-103">プロパティまたは関数の戻り値を指定します。</span><span class="sxs-lookup"><span data-stu-id="57a41-103">Specifies the return value of the property or function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57a41-104">構文</span><span class="sxs-lookup"><span data-stu-id="57a41-104">Syntax</span></span>  
  
```xml  
<returns>description</returns>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="57a41-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="57a41-105">Parameters</span></span>  
 `description`  
 <span data-ttu-id="57a41-106">戻り値の説明。</span><span class="sxs-lookup"><span data-stu-id="57a41-106">A description of the return value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="57a41-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="57a41-107">Remarks</span></span>  
 <span data-ttu-id="57a41-108">使用して、`<returns>`戻り値を記述するメソッド宣言のコメント内のタグ。</span><span class="sxs-lookup"><span data-stu-id="57a41-108">Use the `<returns>` tag in the comment for a method declaration to describe the return value.</span></span>  
  
 <span data-ttu-id="57a41-109">コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="57a41-109">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="57a41-110">例</span><span class="sxs-lookup"><span data-stu-id="57a41-110">Example</span></span>  
 <span data-ttu-id="57a41-111">この例では、`<returns>`何かを説明するタグ、`DoesRecordExist`関数が返される。</span><span class="sxs-lookup"><span data-stu-id="57a41-111">This example uses the `<returns>` tag to explain what the `DoesRecordExist` function returns.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/returns_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="57a41-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="57a41-112">See Also</span></span>  
 [<span data-ttu-id="57a41-113">XML のコメント用タグ</span><span class="sxs-lookup"><span data-stu-id="57a41-113">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
