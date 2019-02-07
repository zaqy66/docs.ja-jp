---
title: <typeparamref> - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- typeparamref
helpviewer_keywords:
- typeparamref C# XML tag
- <typeparamref> C# XML tag
ms.assetid: 6d8ffc58-12c5-4688-8db6-833a7ded5886
ms.openlocfilehash: 834aff6e4673a306559daa1b9517e11538e90ad0
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55273349"
---
# <a name="typeparamref-c-programming-guide"></a><span data-ttu-id="11ea4-102">\<typeparamref> (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="11ea4-102">\<typeparamref> (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="11ea4-103">構文</span><span class="sxs-lookup"><span data-stu-id="11ea4-103">Syntax</span></span>  
  
```xml  
<typeparamref name="name"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="11ea4-104">パラメーター</span><span class="sxs-lookup"><span data-stu-id="11ea4-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="11ea4-105">型パラメーターの名前。</span><span class="sxs-lookup"><span data-stu-id="11ea4-105">The name of the type parameter.</span></span> <span data-ttu-id="11ea4-106">名前は二重引用符 (" ") で囲みます。</span><span class="sxs-lookup"><span data-stu-id="11ea4-106">Enclose the name in double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="11ea4-107">コメント</span><span class="sxs-lookup"><span data-stu-id="11ea4-107">Remarks</span></span>  
 <span data-ttu-id="11ea4-108">ジェネリック型およびメソッドの型パラメーターの詳細については、「[ジェネリック (C# プログラミング ガイド)](../../../csharp/programming-guide/generics/index.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11ea4-108">For more information on type parameters in generic types and methods, see [Generics](../../../csharp/programming-guide/generics/index.md).</span></span>  
  
 <span data-ttu-id="11ea4-109">ドキュメント ファイルを使用するときに何らかの方法で単語の書式 (斜体など) を指定するには、このタグを使用します。</span><span class="sxs-lookup"><span data-stu-id="11ea4-109">Use this tag to enable consumers of the documentation file to format the word in some distinct way, for example in italics.</span></span>  
  
 <span data-ttu-id="11ea4-110">コンパイル時に [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="11ea4-110">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="11ea4-111">例</span><span class="sxs-lookup"><span data-stu-id="11ea4-111">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#13](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/typeparamref_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="11ea4-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="11ea4-112">See also</span></span>

- [<span data-ttu-id="11ea4-113">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="11ea4-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="11ea4-114">ドキュメント コメントとして推奨されるタグ</span><span class="sxs-lookup"><span data-stu-id="11ea4-114">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
