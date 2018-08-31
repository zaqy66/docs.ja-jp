---
title: XML コメントの例外があります、 &#39;cref&#39;属性
ms.date: 07/20/2015
f1_keywords:
- bc42319
- vbc42319
helpviewer_keywords:
- BC42319
ms.assetid: 62eeeba3-6811-48be-b1ef-c2e4feda3177
ms.openlocfilehash: abe9fe0f6216f81fa223fe83a122b580577e1c32
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/30/2018
ms.locfileid: "43255646"
---
# <a name="xml-comment-exception-must-have-a-39cref39-attribute"></a><span data-ttu-id="40451-102">XML コメントの例外があります、 &#39;cref&#39;属性</span><span class="sxs-lookup"><span data-stu-id="40451-102">XML comment exception must have a &#39;cref&#39; attribute</span></span>
<span data-ttu-id="40451-103">\<例外 > タグは、メソッドによってスローされる可能性が例外を文書化する方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="40451-103">The \<exception> tag provides a way to document the exceptions that may be thrown by a method.</span></span> <span data-ttu-id="40451-104">必要な`cref`属性は、ドキュメントのジェネレーターがチェックされているメンバーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="40451-104">The required `cref` attribute designates the name of a member, which is checked by the documentation generator.</span></span> <span data-ttu-id="40451-105">メンバーが存在する場合は、ドキュメント ファイルで正規要素名に変換されます。</span><span class="sxs-lookup"><span data-stu-id="40451-105">If the member exists, it is translated to the canonical element name in the documentation file.</span></span>  
  
 <span data-ttu-id="40451-106">**エラー ID:** BC42319</span><span class="sxs-lookup"><span data-stu-id="40451-106">**Error ID:** BC42319</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="40451-107">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="40451-107">To correct this error</span></span>  
  
-   <span data-ttu-id="40451-108">追加、`cref`属性、例外を次のようにします。</span><span class="sxs-lookup"><span data-stu-id="40451-108">Add the `cref` attribute to the exception as follows:</span></span>  
  
    ```  
    '''<exception cref="member">description</exception>  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="40451-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="40451-109">See Also</span></span>  
 [<span data-ttu-id="40451-110">\<exception></span><span class="sxs-lookup"><span data-stu-id="40451-110">\<exception></span></span>](../../../visual-basic/language-reference/xmldoc/exception.md)  
 [<span data-ttu-id="40451-111">方法: XML ドキュメントを作成する</span><span class="sxs-lookup"><span data-stu-id="40451-111">How to: Create XML Documentation</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)  
 [<span data-ttu-id="40451-112">XML のコメント用タグ</span><span class="sxs-lookup"><span data-stu-id="40451-112">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
