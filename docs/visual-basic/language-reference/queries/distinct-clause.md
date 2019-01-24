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
ms.openlocfilehash: 3761f6d6ba97e7f1a824b70b18a50dae820c7e51
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710041"
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
- [Visual Basic における LINQ の概要](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [クエリ](../../../visual-basic/language-reference/queries/index.md)
- [From 句](../../../visual-basic/language-reference/queries/from-clause.md)
- [Select 句](../../../visual-basic/language-reference/queries/select-clause.md)
- [Where 句](../../../visual-basic/language-reference/queries/where-clause.md)
