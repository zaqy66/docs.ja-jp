---
title: '方法: Char 値 (Visual Basic) の配列から文字列を作成します。'
ms.date: 07/20/2015
helpviewer_keywords:
- examples [Visual Basic], arrays
- examples [Visual Basic], Char data type
ms.assetid: 69f94e85-d57c-4ccc-a62a-426e829f5c5e
ms.openlocfilehash: a067474d6b32589a34b031d5c3ea4e5a4be55834
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54611463"
---
# <a name="how-to-create-a-string-from-an-array-of-char-values-visual-basic"></a>方法: Char 値 (Visual Basic) の配列から文字列を作成します。
この例では、個々 の文字から文字列"abcd"を作成します。  
  
## <a name="example"></a>例  
 [!code-vb[VbVbalrStrings#61](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-create-a-string-from-an-array-of-char-values_1.vb)]  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 このメソッドには、特別な要件はありません。  
  
 構文`"a"c`がある場合、1 つ、`c`引用符内の 1 文字に依存して、文字リテラルを作成するために使用します。  
  
## <a name="robust-programming"></a>信頼性の高いプログラミング  
 Null 文字 (に相当`Chr(0)`) 文字列の結果が発生する予期しない文字列を使用する場合。 Null 文字は文字列で含まれますが、状況によっては、null 文字に続く文字は表示されません。  
  
## <a name="see-also"></a>関連項目
- <xref:System.String>
- [Char データ型](../../../../visual-basic/language-reference/data-types/char-data-type.md)
- [データの種類](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
