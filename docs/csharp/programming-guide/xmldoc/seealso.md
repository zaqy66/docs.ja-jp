---
title: '&lt;seealso&gt; - C# プログラミング ガイド'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- cref
- <seealso>
- seealso
helpviewer_keywords:
- cref [C#], see also
- seealso C# XML tag
- cref [C#]
- cross-references [C#], tags
- <seealso> C# XML tag
ms.assetid: 8e157f3f-f220-4fcf-9010-88905b080b18
ms.openlocfilehash: e75480db9aebdeb2199694168abf4f774773b9c8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54543553"
---
# <a name="ltseealsogt-c-programming-guide"></a><span data-ttu-id="d6ff4-102">&lt;seealso&gt; (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="d6ff4-102">&lt;seealso&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="d6ff4-103">構文</span><span class="sxs-lookup"><span data-stu-id="d6ff4-103">Syntax</span></span>  
  
```xml  
<seealso cref="member"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d6ff4-104">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d6ff4-104">Parameters</span></span>  
 <span data-ttu-id="d6ff4-105">cref = "`member`"</span><span class="sxs-lookup"><span data-stu-id="d6ff4-105">cref = " `member`"</span></span>  
 <span data-ttu-id="d6ff4-106">現在のコンパイル環境からの呼び出しに利用できる、メンバーまたはフィールドへの参照。</span><span class="sxs-lookup"><span data-stu-id="d6ff4-106">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="d6ff4-107">コンパイラは、指定されたコード要素が存在するかどうかを確認し、`member` を出力 XML 内の要素名に渡します。`member`</span><span class="sxs-lookup"><span data-stu-id="d6ff4-107">The compiler checks that the given code element exists and passes `member` to the element name in the output XML.`member`</span></span> <span data-ttu-id="d6ff4-108"> は二重引用符 (" ") で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6ff4-108">must appear within double quotation marks (" ").</span></span>  
  
 <span data-ttu-id="d6ff4-109">ジェネリック型への cref 参照を作成する方法については、「[\<see>](../../../csharp/programming-guide/xmldoc/see.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d6ff4-109">For information on how to create a cref reference to a generic type, see [\<see>](../../../csharp/programming-guide/xmldoc/see.md).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d6ff4-110">コメント</span><span class="sxs-lookup"><span data-stu-id="d6ff4-110">Remarks</span></span>  
 <span data-ttu-id="d6ff4-111">\<seealso > タグを使用して、「See Also」セクションに表示するテキストを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="d6ff4-111">The \<seealso> tag lets you specify the text that you might want to appear in a See Also section.</span></span> <span data-ttu-id="d6ff4-112">[\<see>](../../../csharp/programming-guide/xmldoc/see.md) タグを使用すると、テキスト内からリンクを指定できます。</span><span class="sxs-lookup"><span data-stu-id="d6ff4-112">Use [\<see>](../../../csharp/programming-guide/xmldoc/see.md) to specify a link from within text.</span></span>  
  
 <span data-ttu-id="d6ff4-113">コンパイル時に [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="d6ff4-113">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d6ff4-114">例</span><span class="sxs-lookup"><span data-stu-id="d6ff4-114">Example</span></span>  
 <span data-ttu-id="d6ff4-115">\<seealso> の使用例については、[\<summary>](../../../csharp/programming-guide/xmldoc/summary.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d6ff4-115">See [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md) for an example of using \<seealso>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6ff4-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="d6ff4-116">See also</span></span>

- [<span data-ttu-id="d6ff4-117">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="d6ff4-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="d6ff4-118">ドキュメント コメントとして推奨されるタグ</span><span class="sxs-lookup"><span data-stu-id="d6ff4-118">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
