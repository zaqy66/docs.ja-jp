---
title: <value> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <value> XML tag
- value XML tag
ms.assetid: 0b84b02e-9e6d-41b5-a926-0d5dc76dacb5
ms.openlocfilehash: 5aab2307a1967ea660282c7b324eaddfe798a155
ms.sourcegitcommit: 5dcfeb59179e81071f54840d4902cbe00b184294
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/24/2019
ms.locfileid: "54857880"
---
# <a name="value-visual-basic"></a>\<値 > (Visual Basic)
プロパティの説明を指定します。  
  
## <a name="syntax"></a>構文  
  
```xml  
<value>property-description</value>  
```  
  
#### <a name="parameters"></a>パラメーター  
 `property-description`  
 プロパティの説明。  
  
## <a name="remarks"></a>Remarks  
 使用して、`<value>`プロパティを説明するタグ。 Visual Studio 開発環境で、コード ウィザードを使用してプロパティを追加すると、追加されることに注意してください、 [\<概要 >](../../../visual-basic/language-reference/xmldoc/summary.md)新しいプロパティのタグ。 手動で追加する必要がありますし、`<value>`プロパティを表す値を記述するタグ。  
  
 コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。  
  
## <a name="example"></a>例  
 この例では、`<value>`どのような値を記述するタグ、`Counter`プロパティを保持します。  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/value_1.vb)]  
  
## <a name="see-also"></a>関連項目
- [XML のコメント用タグ](../../../visual-basic/language-reference/xmldoc/index.md)
