---
title: '&lt;c&gt; - C# プログラミング ガイド'
ms.custom: seodec18
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
ms.openlocfilehash: 5ebdb275ffa9b735d0d68b3d9b4685880a849a7a
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236414"
---
# <a name="ltcgt-c-programming-guide"></a><span data-ttu-id="ffb5d-102">&lt;c&gt; (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="ffb5d-102">&lt;c&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="ffb5d-103">構文</span><span class="sxs-lookup"><span data-stu-id="ffb5d-103">Syntax</span></span>  
  
```xml  
<c>text</c>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ffb5d-104">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ffb5d-104">Parameters</span></span>  
 `text`  
 <span data-ttu-id="ffb5d-105">コードとして指定するテキストです。</span><span class="sxs-lookup"><span data-stu-id="ffb5d-105">The text you would like to indicate as code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ffb5d-106">コメント</span><span class="sxs-lookup"><span data-stu-id="ffb5d-106">Remarks</span></span>  
 <span data-ttu-id="ffb5d-107">\<c> タグを使用すると、説明内のテキストをコードとして指定できます。</span><span class="sxs-lookup"><span data-stu-id="ffb5d-107">The \<c> tag gives you a way to indicate that text within a description should be marked as code.</span></span> <span data-ttu-id="ffb5d-108">複数行をコードとして指定する場合は、[\<code>](../../../csharp/programming-guide/xmldoc/code.md) タグを使用します。</span><span class="sxs-lookup"><span data-stu-id="ffb5d-108">Use [\<code>](../../../csharp/programming-guide/xmldoc/code.md) to indicate multiple lines as code.</span></span>  
  
 <span data-ttu-id="ffb5d-109">コンパイル時に [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="ffb5d-109">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ffb5d-110">例</span><span class="sxs-lookup"><span data-stu-id="ffb5d-110">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#2](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/code-inline_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="ffb5d-111">参照</span><span class="sxs-lookup"><span data-stu-id="ffb5d-111">See Also</span></span>

- [<span data-ttu-id="ffb5d-112">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="ffb5d-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="ffb5d-113">ドキュメント コメントとして推奨されるタグ</span><span class="sxs-lookup"><span data-stu-id="ffb5d-113">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
