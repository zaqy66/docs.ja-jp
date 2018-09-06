---
title: '&lt;param&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- param XML tag
- <param> XML tag
ms.assetid: 4e32e86f-f6f3-4301-b7fc-2f321fb54368
ms.openlocfilehash: 4cb3de06d574f8b9abb3e3e11641a6ada750b56a
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43856492"
---
# <a name="ltparamgt-visual-basic"></a><span data-ttu-id="9ec7e-102">&lt;param&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9ec7e-102">&lt;param&gt; (Visual Basic)</span></span>
<span data-ttu-id="9ec7e-103">パラメーターの名前と説明を定義します。</span><span class="sxs-lookup"><span data-stu-id="9ec7e-103">Defines a parameter name and description.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ec7e-104">構文</span><span class="sxs-lookup"><span data-stu-id="9ec7e-104">Syntax</span></span>  
  
```xml  
<param name="name">description</param>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9ec7e-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9ec7e-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="9ec7e-106">メソッド パラメーターの名前です。</span><span class="sxs-lookup"><span data-stu-id="9ec7e-106">The name of a method parameter.</span></span> <span data-ttu-id="9ec7e-107">名前は二重引用符 (" ") で囲みます。</span><span class="sxs-lookup"><span data-stu-id="9ec7e-107">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="9ec7e-108">パラメーターの説明です。</span><span class="sxs-lookup"><span data-stu-id="9ec7e-108">A description for the parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9ec7e-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="9ec7e-109">Remarks</span></span>  
 <span data-ttu-id="9ec7e-110">`<param>`タグは、メソッドのパラメーターのいずれかを説明するメソッド宣言のコメントで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ec7e-110">The `<param>` tag should be used in the comment for a method declaration to describe one of the parameters for the method.</span></span>  
  
 <span data-ttu-id="9ec7e-111">テキスト、`<param>`タグは、次の場所に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9ec7e-111">The text for the `<param>` tag will appear in the following locations:</span></span>  
  
-   <span data-ttu-id="9ec7e-112">IntelliSense のパラメーター情報。</span><span class="sxs-lookup"><span data-stu-id="9ec7e-112">Parameter Info of IntelliSense.</span></span> <span data-ttu-id="9ec7e-113">詳細については、「[IntelliSense の使用](/visualstudio/ide/using-intellisense)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ec7e-113">For more information, see [Using IntelliSense](/visualstudio/ide/using-intellisense).</span></span>  
  
-   <span data-ttu-id="9ec7e-114">オブジェクト ブラウザー。</span><span class="sxs-lookup"><span data-stu-id="9ec7e-114">Object Browser.</span></span> <span data-ttu-id="9ec7e-115">詳細については、「[コードの構造の表示](/visualstudio/ide/viewing-the-structure-of-code)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ec7e-115">For more information, see [Viewing the Structure of Code](/visualstudio/ide/viewing-the-structure-of-code).</span></span>  
  
 <span data-ttu-id="9ec7e-116">コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="9ec7e-116">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9ec7e-117">例</span><span class="sxs-lookup"><span data-stu-id="9ec7e-117">Example</span></span>  
 <span data-ttu-id="9ec7e-118">この例では、`<param>`を記述するタグ、`id`パラメーター。</span><span class="sxs-lookup"><span data-stu-id="9ec7e-118">This example uses the `<param>` tag to describe the `id` parameter.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/param_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="9ec7e-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="9ec7e-119">See Also</span></span>  
 [<span data-ttu-id="9ec7e-120">XML のコメント用タグ</span><span class="sxs-lookup"><span data-stu-id="9ec7e-120">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
