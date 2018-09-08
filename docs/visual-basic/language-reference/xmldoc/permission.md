---
title: '&lt;アクセス許可&gt;(Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <permission> XML tag
- permission XML tag
ms.assetid: 0edf0500-5cd7-49c0-9255-64c48f972b77
ms.openlocfilehash: bcec5d968f5d0c5400c28e772df151b164888a47
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44191847"
---
# <a name="ltpermissiongt-visual-basic"></a><span data-ttu-id="27a06-102">&lt;アクセス許可&gt;(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="27a06-102">&lt;permission&gt; (Visual Basic)</span></span>
<span data-ttu-id="27a06-103">メンバーの必要なアクセス許可を指定します。</span><span class="sxs-lookup"><span data-stu-id="27a06-103">Specifies a required permission for the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="27a06-104">構文</span><span class="sxs-lookup"><span data-stu-id="27a06-104">Syntax</span></span>  
  
```xml  
<permission cref="member">description</permission>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="27a06-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="27a06-105">Parameters</span></span>  
 `member`  
 <span data-ttu-id="27a06-106">現在のコンパイル環境からの呼び出しに利用できる、メンバーまたはフィールドへの参照。</span><span class="sxs-lookup"><span data-stu-id="27a06-106">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="27a06-107">コンパイラは、指定されたコード要素が存在し、出力の XML で `member` が正規要素名に変換されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="27a06-107">The compiler checks that the given code element exists and translates `member` to the canonical element name in the output XML.</span></span> <span data-ttu-id="27a06-108">囲む`member`引用符 ("")。</span><span class="sxs-lookup"><span data-stu-id="27a06-108">Enclose `member` in quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="27a06-109">メンバーへのアクセスの説明です。</span><span class="sxs-lookup"><span data-stu-id="27a06-109">A description of the access to the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="27a06-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="27a06-110">Remarks</span></span>  
 <span data-ttu-id="27a06-111">使用して、`<permission>`メンバーへのアクセスを文書化タグ。</span><span class="sxs-lookup"><span data-stu-id="27a06-111">Use the `<permission>` tag to document the access of a member.</span></span> <span data-ttu-id="27a06-112">使用して、<xref:System.Security.PermissionSet>クラス メンバーへのアクセスを指定します。</span><span class="sxs-lookup"><span data-stu-id="27a06-112">Use the <xref:System.Security.PermissionSet> class to specify access to a member.</span></span>  
  
 <span data-ttu-id="27a06-113">コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="27a06-113">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="27a06-114">例</span><span class="sxs-lookup"><span data-stu-id="27a06-114">Example</span></span>  
 <span data-ttu-id="27a06-115">この例では、`<permission>`を記述するタグ、<xref:System.Security.Permissions.FileIOPermission>に必要な`ReadFile`メソッド。</span><span class="sxs-lookup"><span data-stu-id="27a06-115">This example uses the `<permission>` tag to describe that the <xref:System.Security.Permissions.FileIOPermission> is required by the `ReadFile` method.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#7](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/permission_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="27a06-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="27a06-116">See Also</span></span>  
 [<span data-ttu-id="27a06-117">XML のコメント用タグ</span><span class="sxs-lookup"><span data-stu-id="27a06-117">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
