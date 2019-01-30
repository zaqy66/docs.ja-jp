---
title: 型 'type1' の値を 'type2' に変換できません
ms.date: 07/20/2015
f1_keywords:
- vbc31194
- bc31194
helpviewer_keywords:
- BC31194
ms.assetid: 03d50c31-addd-4c90-9c53-725b84f9782e
ms.openlocfilehash: eb30d63e83452e75f353c44a9d0445c7dbb1013a
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55287509"
---
# <a name="value-of-type-type1-cannot-be-converted-to-type2"></a>型 'type1' の値を 'type2' に変換できません
型 'type1' の値は、'type2' へ変換できません。 最初の要素の文字列値を取得する、'Value' プロパティを使用することができます '\<parentElement >'。  
  
 XML リテラルを特定の型を暗黙的にキャストしようとしました。 XML リテラルは、指定した型に暗黙的にキャストできません。  
  
 **エラー ID:** BC31194  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   XML リテラルの `Value` プロパティを使用して、その値を `String`として参照します。 `CType` 関数、別の型変換関数、または <xref:System.Convert> クラスを使用して、指定した型として値をキャストします。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Convert>
- [データ型変換関数](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [XML リテラル](../../../visual-basic/language-reference/xml-literals/index.md)
- [XML](../../../visual-basic/programming-guide/language-features/xml/index.md)
