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
# <a name="39ltmembernamegt39-cannot-expose-type-39lttypenamegt39-outside-the-project-through-ltcontainertypegt-39ltcontainertypenamegt39"></a>&#39;&lt;membername&gt;&#39; は型 &#39;&lt;typename&gt;&#39; を &lt;containertype&gt; &#39;&lt;containertypename&gt;&#39; 経由でプロジェクトの外側に公開できない
変数、プロシージャのパラメーター、または関数の戻り値が、そのコンテナーの外部に公開されているが、コンテナーの外に必ず公開しない型として宣言されています。  
  
 次のスケルトン コードは、このエラーが発生する状況を示しています。  
  
```  
Private Class privateClass  
End Class  
Public Class mainClass  
    Public exposedVar As New privateClass  
End Class  
```  
  
 宣言されている型`Protected`、 `Friend`、 `Protected Friend`、または`Private`その宣言コンテキストの外部アクセスを制限するためのものです。 データとして使用制限の少ない方のアクセス権を持つ変数の型はこの目的を倒すとします。 上記のスケルトン コード`exposedVar`は`Public`公開と`privateClass`にアクセス権のないコードにします。  
  
 **エラー ID:** BC30909  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   変数、プロシージャのパラメーター、または関数のアクセス レベルの変更は、少なくともそのデータ型のアクセス レベルと同程度に制限するように返します。  
  
## <a name="see-also"></a>関連項目
- [Visual Basic でのアクセス レベル](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
