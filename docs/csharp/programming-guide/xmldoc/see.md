---
title: '&lt;see&gt; - C# プログラミング ガイド'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <see>
- see
helpviewer_keywords:
- cref [C#], <see> tag
- <see> C# XML tag
- cross-references [C#]
- see C# XML tag
ms.assetid: 0200de01-7e2f-45c4-9094-829d61236383
ms.openlocfilehash: 1e799c975fe21dd2dd0354a9d658a271ded5fc2c
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235691"
---
# <a name="ltseegt-c-programming-guide"></a><span data-ttu-id="a4cb4-102">&lt;see&gt; (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="a4cb4-102">&lt;see&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="a4cb4-103">構文</span><span class="sxs-lookup"><span data-stu-id="a4cb4-103">Syntax</span></span>  
  
```xml  
<see cref="member"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a4cb4-104">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a4cb4-104">Parameters</span></span>  
 <span data-ttu-id="a4cb4-105">cref = "`member`"</span><span class="sxs-lookup"><span data-stu-id="a4cb4-105">cref = " `member`"</span></span>  
 <span data-ttu-id="a4cb4-106">現在のコンパイル環境からの呼び出しに利用できる、メンバーまたはフィールドへの参照。</span><span class="sxs-lookup"><span data-stu-id="a4cb4-106">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="a4cb4-107">コンパイラは、指定されたコード要素が存在するかどうかを確認し、`member` を出力 XML 内の要素名に渡します。*member* は二重引用符で囲んで配置します。</span><span class="sxs-lookup"><span data-stu-id="a4cb4-107">The compiler checks that the given code element exists and passes `member` to the element name in the output XML.Place *member* within double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a4cb4-108">コメント</span><span class="sxs-lookup"><span data-stu-id="a4cb4-108">Remarks</span></span>  
 <span data-ttu-id="a4cb4-109">\<see> タグを使用すると、テキスト内でリンクを指定できます。</span><span class="sxs-lookup"><span data-stu-id="a4cb4-109">The \<see> tag lets you specify a link from within text.</span></span> <span data-ttu-id="a4cb4-110">テキストが参照セクションに配置されていることを示すには、[\<seealso>](../../../csharp/programming-guide/xmldoc/seealso.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="a4cb4-110">Use [\<seealso>](../../../csharp/programming-guide/xmldoc/seealso.md) to indicate that text should be placed in a See Also section.</span></span> <span data-ttu-id="a4cb4-111">コード要素のドキュメント ページへの内部ハイパーリンクを作成するには、[cref 属性](../../../csharp/programming-guide/xmldoc/cref-attribute.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="a4cb4-111">Use the [cref Attribute](../../../csharp/programming-guide/xmldoc/cref-attribute.md) to create internal hyperlinks to documentation pages for code elements.</span></span>  
  
 <span data-ttu-id="a4cb4-112">コンパイル時に [-doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="a4cb4-112">Compile with [-doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
 <span data-ttu-id="a4cb4-113">次の例では、summary セクション内の \<see> タグを示しています。</span><span class="sxs-lookup"><span data-stu-id="a4cb4-113">The following example shows a \<see> tag within a summary section.</span></span>  
  
 [!code-csharp[csProgGuideDocComments#12](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/see_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="a4cb4-114">参照</span><span class="sxs-lookup"><span data-stu-id="a4cb4-114">See Also</span></span>

- [<span data-ttu-id="a4cb4-115">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="a4cb4-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="a4cb4-116">ドキュメント コメントとして推奨されるタグ</span><span class="sxs-lookup"><span data-stu-id="a4cb4-116">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
