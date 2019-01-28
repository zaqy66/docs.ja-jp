---
title: '&lt;permission&gt; - C# プログラミング ガイド'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- permission
- <permission>
helpviewer_keywords:
- <permission> C# XML tag
- permission C# XML tag
ms.assetid: 769e93fe-8404-443f-bf99-577aa42b6a49
ms.openlocfilehash: 5d78261807ab06bd5f89b5438648c5eb0dc56ad9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54739460"
---
# <a name="ltpermissiongt-c-programming-guide"></a><span data-ttu-id="d1bcb-102">&lt;permission&gt; (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="d1bcb-102">&lt;permission&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="d1bcb-103">構文</span><span class="sxs-lookup"><span data-stu-id="d1bcb-103">Syntax</span></span>  
  
```xml  
<permission cref="member">description</permission>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d1bcb-104">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d1bcb-104">Parameters</span></span>  
 <span data-ttu-id="d1bcb-105">cref = "`member`"</span><span class="sxs-lookup"><span data-stu-id="d1bcb-105">cref = " `member`"</span></span>  
 <span data-ttu-id="d1bcb-106">現在のコンパイル環境からの呼び出しに利用できる、メンバーまたはフィールドへの参照。</span><span class="sxs-lookup"><span data-stu-id="d1bcb-106">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="d1bcb-107">コンパイラは、指定されたコード要素が存在し、出力の XML で `member` が正規要素名に変換されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d1bcb-107">The compiler checks that the given code element exists and translates `member` to the canonical element name in the output XML.</span></span> <span data-ttu-id="d1bcb-108">*member* は、二重引用符 (" ") で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1bcb-108">*member* must appear within double quotation marks (" ").</span></span>  
  
 <span data-ttu-id="d1bcb-109">ジェネリック型への cref 参照を作成する方法については、「[\<see>](../../../csharp/programming-guide/xmldoc/see.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1bcb-109">For information on how to create a cref reference to a generic type, see [\<see>](../../../csharp/programming-guide/xmldoc/see.md).</span></span>  
  
 `description`  
 <span data-ttu-id="d1bcb-110">メンバーへのアクセスの説明です。</span><span class="sxs-lookup"><span data-stu-id="d1bcb-110">A description of the access to the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d1bcb-111">コメント</span><span class="sxs-lookup"><span data-stu-id="d1bcb-111">Remarks</span></span>  
 <span data-ttu-id="d1bcb-112">\<permission> タグを使用すると、メンバーのアクセスを文書化できます。</span><span class="sxs-lookup"><span data-stu-id="d1bcb-112">The \<permission> tag lets you document the access of a member.</span></span> <span data-ttu-id="d1bcb-113"><xref:System.Security.PermissionSet> クラスを使用すると、メンバーへのアクセスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="d1bcb-113">The <xref:System.Security.PermissionSet> class lets you specify access to a member.</span></span>  
  
 <span data-ttu-id="d1bcb-114">コンパイル時に [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="d1bcb-114">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d1bcb-115">例</span><span class="sxs-lookup"><span data-stu-id="d1bcb-115">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#8](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/permission_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="d1bcb-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1bcb-116">See also</span></span>

- [<span data-ttu-id="d1bcb-117">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="d1bcb-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="d1bcb-118">ドキュメント コメントとして推奨されるタグ</span><span class="sxs-lookup"><span data-stu-id="d1bcb-118">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
