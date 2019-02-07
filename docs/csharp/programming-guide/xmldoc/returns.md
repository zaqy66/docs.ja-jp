---
title: <returns> - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- returns
- <returns>
helpviewer_keywords:
- <returns> C# XML tag
- returns C# XML tag
ms.assetid: bb2d9958-62fc-47c7-9511-6311171f119f
ms.openlocfilehash: 873f515830c072f31548bee84a8ca9eec83fde27
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55274134"
---
# <a name="returns-c-programming-guide"></a><span data-ttu-id="ef449-102">\<returns> (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="ef449-102">\<returns> (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="ef449-103">構文</span><span class="sxs-lookup"><span data-stu-id="ef449-103">Syntax</span></span>  
  
```xml  
<returns>description</returns>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ef449-104">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ef449-104">Parameters</span></span>  
 `description`  
 <span data-ttu-id="ef449-105">戻り値の説明。</span><span class="sxs-lookup"><span data-stu-id="ef449-105">A description of the return value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ef449-106">コメント</span><span class="sxs-lookup"><span data-stu-id="ef449-106">Remarks</span></span>  
 <span data-ttu-id="ef449-107">\<returns> タグは、戻り値を説明するためにメソッドの宣言のコメントで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef449-107">The \<returns> tag should be used in the comment for a method declaration to describe the return value.</span></span>  
  
 <span data-ttu-id="ef449-108">コンパイル時に [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="ef449-108">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ef449-109">例</span><span class="sxs-lookup"><span data-stu-id="ef449-109">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#10](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/returns_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="ef449-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="ef449-110">See also</span></span>

- [<span data-ttu-id="ef449-111">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="ef449-111">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="ef449-112">ドキュメント コメントとして推奨されるタグ</span><span class="sxs-lookup"><span data-stu-id="ef449-112">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
