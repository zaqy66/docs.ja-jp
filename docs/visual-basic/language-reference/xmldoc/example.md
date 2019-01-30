---
title: <example> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- example XML tag
- <example> XML tag
ms.assetid: 90eeda1c-3fc4-427c-879c-5046d265a97c
ms.openlocfilehash: 75e6f966f8baac2fd3c863c7caea939d80bfc41b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255525"
---
# <a name="example-visual-basic"></a>\<例 > (Visual Basic)
メンバーの例を指定します。  
  
## <a name="syntax"></a>構文  
  
```xml  
<example>description</example>  
```  
  
#### <a name="parameters"></a>パラメーター  
 `description`  
 コード例の説明です。  
  
## <a name="remarks"></a>コメント  
 `<example>`タグを使用して、メソッド、またはその他のライブラリ メンバーを使用する方法の例を指定できます。 一般的に、[\<code>](../../../visual-basic/language-reference/xmldoc/code.md) タグが使用されます。  
  
 コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。  
  
## <a name="example"></a>例  
 この例では、`<example>`タグを含める例を使用するために、`ID`フィールド。  
  
 [!code-vb[VbVbcnXmlDocComments#2](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/example_1.vb)]  
  
## <a name="see-also"></a>関連項目
- [XML のコメント用タグ](../../../visual-basic/language-reference/xmldoc/index.md)
