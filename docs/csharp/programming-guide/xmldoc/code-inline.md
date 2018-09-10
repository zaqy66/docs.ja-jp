---
title: '&lt;c&gt; (C# プログラミング ガイド)'
ms.date: 07/20/2015
f1_keywords:
- c
- <c>
helpviewer_keywords:
- text, marking as code [C#]
- code, marking text as [C#]
- c C# XML tag
- <c> C# XML tag
ms.assetid: aad5b16e-a29e-445e-bd0d-eea0b138d7b2
ms.openlocfilehash: 2220c42485674eaa4ba4e3b2dfb03865ad8013cb
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43508148"
---
# <a name="ltcgt-c-programming-guide"></a><span data-ttu-id="8f119-102">&lt;c&gt; (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="8f119-102">&lt;c&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="8f119-103">構文</span><span class="sxs-lookup"><span data-stu-id="8f119-103">Syntax</span></span>  
  
```xml  
<c>text</c>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8f119-104">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8f119-104">Parameters</span></span>  
 `text`  
 <span data-ttu-id="8f119-105">コードとして指定するテキストです。</span><span class="sxs-lookup"><span data-stu-id="8f119-105">The text you would like to indicate as code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8f119-106">コメント</span><span class="sxs-lookup"><span data-stu-id="8f119-106">Remarks</span></span>  
 <span data-ttu-id="8f119-107">\<c> タグを使用すると、説明内のテキストをコードとして指定できます。</span><span class="sxs-lookup"><span data-stu-id="8f119-107">The \<c> tag gives you a way to indicate that text within a description should be marked as code.</span></span> <span data-ttu-id="8f119-108">複数行をコードとして指定する場合は、[\<code>](../../../csharp/programming-guide/xmldoc/code.md) タグを使用します。</span><span class="sxs-lookup"><span data-stu-id="8f119-108">Use [\<code>](../../../csharp/programming-guide/xmldoc/code.md) to indicate multiple lines as code.</span></span>  
  
 <span data-ttu-id="8f119-109">コンパイル時に [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="8f119-109">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8f119-110">例</span><span class="sxs-lookup"><span data-stu-id="8f119-110">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#2](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/code-inline_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="8f119-111">参照</span><span class="sxs-lookup"><span data-stu-id="8f119-111">See Also</span></span>

- [<span data-ttu-id="8f119-112">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="8f119-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="8f119-113">ドキュメント コメントとして推奨されるタグ</span><span class="sxs-lookup"><span data-stu-id="8f119-113">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
