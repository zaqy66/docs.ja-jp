---
title: '方法 : Visual Basic で XML ドキュメントを作成する'
ms.date: 07/20/2015
helpviewer_keywords:
- XML comments
- XML documentation [Visual Basic], creating
ms.assetid: 27b5b06c-09b9-496a-8245-f9542d846230
ms.openlocfilehash: 7fb56da8a28367a6dcd5e28f208b4519510d7d95
ms.sourcegitcommit: 70c76a12449439bac0f7a359866be5a0311ce960
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/25/2018
ms.locfileid: "39243880"
---
# <a name="how-to-create-xml-documentation-in-visual-basic"></a><span data-ttu-id="d30da-102">方法 : Visual Basic で XML ドキュメントを作成する</span><span class="sxs-lookup"><span data-stu-id="d30da-102">How to: Create XML Documentation in Visual Basic</span></span>
<span data-ttu-id="d30da-103">この例では、コードに XML ドキュメントのコメントを追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d30da-103">This example shows how to add XML documentation comments to your code.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-xml-documentation-for-a-type-or-member"></a><span data-ttu-id="d30da-104">型またはメンバーの XML ドキュメントを作成するには</span><span class="sxs-lookup"><span data-stu-id="d30da-104">To create XML documentation for a type or member</span></span>  
  
1.  <span data-ttu-id="d30da-105">**コード エディター**ドキュメントを作成する型またはメンバー上の行にカーソルを置きます。</span><span class="sxs-lookup"><span data-stu-id="d30da-105">In the **Code Editor**, position your cursor on the line above the type or member for which you want to create documentation.</span></span>  
  
2.  <span data-ttu-id="d30da-106">型`'''`(3 つ単一引用符は含みません)。</span><span class="sxs-lookup"><span data-stu-id="d30da-106">Type `'''` (three single-quotation marks).</span></span>  
  
     <span data-ttu-id="d30da-107">型またはメンバーの XML スケルトンが追加された、**コード エディター**します。</span><span class="sxs-lookup"><span data-stu-id="d30da-107">An XML skeleton for the type or member is added in the **Code Editor**.</span></span>  
  
3.  <span data-ttu-id="d30da-108">適切なタグの間のわかりやすい情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="d30da-108">Add descriptive information between the appropriate tags.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="d30da-109">それぞれの行が始まる必要があります、XML ドキュメントのブロック内で行を追加する場合`'''`します。</span><span class="sxs-lookup"><span data-stu-id="d30da-109">If you add additional lines within the XML documentation block, each line must begin with `'''`.</span></span>  
  
4.  <span data-ttu-id="d30da-110">新しい XML ドキュメント コメントを含む型またはメンバーを使用する追加のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d30da-110">Add additional code that uses the type or member with the new XML documentation comments.</span></span>  
  
     <span data-ttu-id="d30da-111">テキストを表示する IntelliSense、\<概要 > 型またはメンバーのタグ。</span><span class="sxs-lookup"><span data-stu-id="d30da-111">IntelliSense displays the text from the \<summary> tag for the type or member.</span></span>  
  
5.  <span data-ttu-id="d30da-112">ドキュメントのコメントを含む XML ファイルを生成するコードをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="d30da-112">Compile the code to generate an XML file containing the documentation comments.</span></span> <span data-ttu-id="d30da-113">詳細については、「[/doc](../../../visual-basic/reference/command-line-compiler/doc.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d30da-113">For more information, see [/doc](../../../visual-basic/reference/command-line-compiler/doc.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d30da-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="d30da-114">See Also</span></span>  
 [<span data-ttu-id="d30da-115">XML の使用によるコードのドキュメントの作成</span><span class="sxs-lookup"><span data-stu-id="d30da-115">Documenting Your Code with XML</span></span>](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md)  
 [<span data-ttu-id="d30da-116">XML のコメント用タグ</span><span class="sxs-lookup"><span data-stu-id="d30da-116">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)  
 [<span data-ttu-id="d30da-117">/doc</span><span class="sxs-lookup"><span data-stu-id="d30da-117">/doc</span></span>](../../../visual-basic/reference/command-line-compiler/doc.md)
