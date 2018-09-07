---
title: Distinct 句 (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryDistinct
helpviewer_keywords:
- Distinct clause [Visual Basic]
- Distinct statement [Visual Basic]
- queries [Visual Basic], Distinct
ms.assetid: 86f42614-0d8f-4ffc-b888-ce8a37a8d36a
ms.openlocfilehash: 18d09d8018303aab6a69801c84c7ec9c6ea19ca9
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44083833"
---
# <a name="distinct-clause-visual-basic"></a>Distinct 句 (Visual Basic)
次のクエリ句で、重複を排除する現在の範囲変数の値を制限します。  
  
## <a name="syntax"></a>構文  
  
```  
Distinct  
```  
  
## <a name="remarks"></a>Remarks  
 使用することができます、`Distinct`句を一意の項目の一覧を返します。 `Distinct`句によって重複するクエリの結果を無視するクエリ。 `Distinct`句は、すべての戻り値で指定されたフィールドの重複する値を適用、`Select`句。 ない場合は`Select`句が指定されて、`Distinct`で特定されたクエリの範囲変数に句が適用される、`From`句。 クエリは、範囲変数が変更不可の型でない場合、既存のクエリ結果に一致する型のすべてのメンバーである場合は、クエリ結果を無視してはのみです。  
  
## <a name="example"></a>例  
 次のクエリ式では、顧客の一覧と顧客の注文のリストを結合します。 `Distinct`句は、一意の顧客名のリストを返し、注文日に含まれています。  
  
 [!code-vb[VbSimpleQuerySamples#20](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/distinct-clause_1.vb)]  
  
## <a name="see-also"></a>関連項目  
 [Visual Basic における LINQ の概要](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [クエリ](../../../visual-basic/language-reference/queries/index.md)  
 [From 句](../../../visual-basic/language-reference/queries/from-clause.md)  
 [Select 句](../../../visual-basic/language-reference/queries/select-clause.md)  
 [WHERE 句](../../../visual-basic/language-reference/queries/where-clause.md)
