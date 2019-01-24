---
title: '&#39;&lt;membername&gt;&#39; は型 &#39;&lt;typename&gt;&#39; を &lt;containertype&gt; &#39;&lt;containertypename&gt;&#39; 経由でプロジェクトの外側に公開できない'
ms.date: 07/20/2015
f1_keywords:
- bc30909
- vbc30909
helpviewer_keywords:
- BC30909
ms.assetid: ffa7395d-e182-4087-8ce8-079810fdae54
ms.openlocfilehash: 39d316aca5ec306de4b1e43e2eb2d1495f5525d9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672345"
---
# <a name="39ltmembernamegt39-cannot-expose-type-39lttypenamegt39-outside-the-project-through-ltcontainertypegt-39ltcontainertypenamegt39"></a><span data-ttu-id="afab7-102">&#39;&lt;membername&gt;&#39; は型 &#39;&lt;typename&gt;&#39; を &lt;containertype&gt; &#39;&lt;containertypename&gt;&#39; 経由でプロジェクトの外側に公開できない</span><span class="sxs-lookup"><span data-stu-id="afab7-102">&#39;&lt;membername&gt;&#39; cannot expose type &#39;&lt;typename&gt;&#39; outside the project through &lt;containertype&gt; &#39;&lt;containertypename&gt;&#39;</span></span>
<span data-ttu-id="afab7-103">変数、プロシージャのパラメーター、または関数の戻り値が、そのコンテナーの外部に公開されているが、コンテナーの外に必ず公開しない型として宣言されています。</span><span class="sxs-lookup"><span data-stu-id="afab7-103">A variable, procedure parameter, or function return is exposed outside its container, but it is declared as a type that must not be exposed outside the container.</span></span>  
  
 <span data-ttu-id="afab7-104">次のスケルトン コードは、このエラーが発生する状況を示しています。</span><span class="sxs-lookup"><span data-stu-id="afab7-104">The following skeleton code shows a situation that generates this error.</span></span>  
  
```  
Private Class privateClass  
End Class  
Public Class mainClass  
    Public exposedVar As New privateClass  
End Class  
```  
  
 <span data-ttu-id="afab7-105">宣言されている型`Protected`、 `Friend`、 `Protected Friend`、または`Private`その宣言コンテキストの外部アクセスを制限するためのものです。</span><span class="sxs-lookup"><span data-stu-id="afab7-105">A type that is declared `Protected`, `Friend`, `Protected Friend`, or `Private` is intended to have limited access outside its declaration context.</span></span> <span data-ttu-id="afab7-106">データとして使用制限の少ない方のアクセス権を持つ変数の型はこの目的を倒すとします。</span><span class="sxs-lookup"><span data-stu-id="afab7-106">Using it as the data type of a variable with less restricted access would defeat this purpose.</span></span> <span data-ttu-id="afab7-107">上記のスケルトン コード`exposedVar`は`Public`公開と`privateClass`にアクセス権のないコードにします。</span><span class="sxs-lookup"><span data-stu-id="afab7-107">In the preceding skeleton code, `exposedVar` is `Public` and would expose `privateClass` to code that should not have access to it.</span></span>  
  
 <span data-ttu-id="afab7-108">**エラー ID:** BC30909</span><span class="sxs-lookup"><span data-stu-id="afab7-108">**Error ID:** BC30909</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="afab7-109">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="afab7-109">To correct this error</span></span>  
  
-   <span data-ttu-id="afab7-110">変数、プロシージャのパラメーター、または関数のアクセス レベルの変更は、少なくともそのデータ型のアクセス レベルと同程度に制限するように返します。</span><span class="sxs-lookup"><span data-stu-id="afab7-110">Change the access level of the variable, procedure parameter, or function return to be at least as restrictive as the access level of its data type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="afab7-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="afab7-111">See also</span></span>
- [<span data-ttu-id="afab7-112">Visual Basic でのアクセス レベル</span><span class="sxs-lookup"><span data-stu-id="afab7-112">Access levels in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
