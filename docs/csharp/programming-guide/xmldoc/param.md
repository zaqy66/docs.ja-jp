---
title: <param> - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- param
- <param>
helpviewer_keywords:
- <param> C# XML tag
- param C# XML tag
ms.assetid: 46d329b1-5b84-4537-9e17-73ca97313e4e
ms.openlocfilehash: 3f1099da6a43ed7f48389a16e3be6a3b6b98a148
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271578"
---
# <a name="param-c-programming-guide"></a><span data-ttu-id="3d6d5-102">\<param> (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="3d6d5-102">\<param> (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="3d6d5-103">構文</span><span class="sxs-lookup"><span data-stu-id="3d6d5-103">Syntax</span></span>  
  
```xml  
<param name="name">description</param>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3d6d5-104">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3d6d5-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="3d6d5-105">メソッド パラメーターの名前です。</span><span class="sxs-lookup"><span data-stu-id="3d6d5-105">The name of a method parameter.</span></span> <span data-ttu-id="3d6d5-106">名前は二重引用符 (" ") で囲みます。</span><span class="sxs-lookup"><span data-stu-id="3d6d5-106">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="3d6d5-107">パラメーターの説明です。</span><span class="sxs-lookup"><span data-stu-id="3d6d5-107">A description for the parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3d6d5-108">コメント</span><span class="sxs-lookup"><span data-stu-id="3d6d5-108">Remarks</span></span>  
 <span data-ttu-id="3d6d5-109">\<param> タグは、メソッドのいずれか 1 つのパラメーターを説明するためにメソッドの宣言のコメントで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d6d5-109">The \<param> tag should be used in the comment for a method declaration to describe one of the parameters for the method.</span></span> <span data-ttu-id="3d6d5-110">複数のパラメーターをドキュメント化するには、複数の \<param> タグを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d6d5-110">To document multiple parameters, use multiple \<param> tags.</span></span>  
  
 <span data-ttu-id="3d6d5-111">\<param> タグのテキストは、IntelliSense、オブジェクト ブラウザー、コード コメント Web レポートに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d6d5-111">The text for the \<param> tag will be displayed in IntelliSense, the Object Browser, and in the Code Comment Web Report.</span></span>  
  
 <span data-ttu-id="3d6d5-112">コンパイル時に [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="3d6d5-112">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3d6d5-113">例</span><span class="sxs-lookup"><span data-stu-id="3d6d5-113">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#1](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/param_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="3d6d5-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d6d5-114">See also</span></span>

- [<span data-ttu-id="3d6d5-115">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="3d6d5-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="3d6d5-116">ドキュメント コメントとして推奨されるタグ</span><span class="sxs-lookup"><span data-stu-id="3d6d5-116">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
