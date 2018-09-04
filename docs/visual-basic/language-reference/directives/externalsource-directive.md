---
title: '#ExternalSource ディレクティブ (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- '#Externalsource'
- '#ExternalSource'
- vb.ExternalSource
- Externalsource
- vb.#ExternalSource
- ExternalSource
helpviewer_keywords:
- ExternalSource directive (#ExternalSource)
- '#ExternalSource directive'
ms.assetid: 243bc6a2-34c3-4eeb-a776-9fd2bf988149
ms.openlocfilehash: dcde8507eb033d0a47d5c5d3fa36176cd63b0856
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43556319"
---
# <a name="externalsource-directive"></a><span data-ttu-id="e0bd9-102">#ExternalSource ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="e0bd9-102">#ExternalSource Directive</span></span>
<span data-ttu-id="e0bd9-103">ソース コードの特定の行とソース外部のテキスト間のマッピングを示します。</span><span class="sxs-lookup"><span data-stu-id="e0bd9-103">Indicates a mapping between specific lines of source code and text external to the source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0bd9-104">構文</span><span class="sxs-lookup"><span data-stu-id="e0bd9-104">Syntax</span></span>  
  
```  
#ExternalSource( StringLiteral , IntLiteral )  
    [ LogicalLine+ ]  
#End ExternalSource  
```  
  
## <a name="parts"></a><span data-ttu-id="e0bd9-105">指定項目</span><span class="sxs-lookup"><span data-stu-id="e0bd9-105">Parts</span></span>  
 `StringLiteral`  
 <span data-ttu-id="e0bd9-106">外部ソースへのパス。</span><span class="sxs-lookup"><span data-stu-id="e0bd9-106">The path to the external source.</span></span>  
  
 `IntLiteral`  
 <span data-ttu-id="e0bd9-107">外部ソースの最初の行の行番号。</span><span class="sxs-lookup"><span data-stu-id="e0bd9-107">The line number of the first line of the external source.</span></span>  
  
 `LogicalLine`  
 <span data-ttu-id="e0bd9-108">行を外部ソースでエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e0bd9-108">The line where the error occurs in the external source.</span></span>  
  
 `#End ExternalSource`  
 <span data-ttu-id="e0bd9-109">`#ExternalSource` ブロックを終了します。</span><span class="sxs-lookup"><span data-stu-id="e0bd9-109">Terminates the `#ExternalSource` block.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e0bd9-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="e0bd9-110">Remarks</span></span>  
 <span data-ttu-id="e0bd9-111">このディレクティブは、コンパイラと、デバッガーでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="e0bd9-111">This directive is used only by the compiler and the debugger.</span></span>  
  
 <span data-ttu-id="e0bd9-112">ソース ファイルには、ソース ファイル内のコードの特定の行と、.aspx ファイルなど、ソースの外部のテキスト間のマッピングを示す外部ソース ディレクティブを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="e0bd9-112">A source file may include external source directives, which indicate a mapping between specific lines of code in the source file and text external to the source, such as an .aspx file.</span></span> <span data-ttu-id="e0bd9-113">指定されたソース コードでは、コンパイル中にエラーが発生する場合は、外部ソースからのものとして識別されます。</span><span class="sxs-lookup"><span data-stu-id="e0bd9-113">If errors are encountered in the designated source code during compilation, they are identified as coming from the external source.</span></span>  
  
 <span data-ttu-id="e0bd9-114">外部ソース ディレクティブは、コンパイルに影響を与えるありませんし、入れ子にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e0bd9-114">External source directives have no effect on compilation and cannot be nested.</span></span> <span data-ttu-id="e0bd9-115">内部使用のアプリケーションのみが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e0bd9-115">They are intended for internal use by the application only.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0bd9-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="e0bd9-116">See Also</span></span>  
 [<span data-ttu-id="e0bd9-117">条件付きコンパイル</span><span class="sxs-lookup"><span data-stu-id="e0bd9-117">Conditional Compilation</span></span>](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
