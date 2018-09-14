---
title: '&lt;概要&gt;(Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <summary> XML tag
- summary XML tag
ms.assetid: 861c847d-dd94-478a-aa23-bf4899cdc848
ms.openlocfilehash: 5ef9b7a98503ff36174de4418ca7d599c365f5aa
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/14/2018
ms.locfileid: "45593782"
---
# <a name="ltsummarygt-visual-basic"></a>&lt;概要&gt;(Visual Basic)
メンバーの概要を指定します。  
  
## <a name="syntax"></a>構文  
  
```xml  
<summary>description</summary>  
```  
  
#### <a name="parameters"></a>パラメーター  
 `description`  
 オブジェクトの概要。  
  
## <a name="remarks"></a>Remarks  
 使用して、`<summary>`型または型のメンバーを記述するタグ。 型の説明に補足情報を追加するには、[\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md) タグを使用します。  
  
 テキスト、`<summary>`タグは IntelliSense の型に関する情報の唯一のソースであり、オブジェクト ブラウザーにも表示されます。 オブジェクト ブラウザーの詳細については、次を参照してください。[コードの構造を表示する](/visualstudio/ide/viewing-the-structure-of-code)します。  
  
 コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。  
  
## <a name="example"></a>例  
 この例では、`<summary>`を記述するタグ、`ResetCounter`メソッドと`Counter`プロパティ。  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/summary_1.vb)]  
  
## <a name="see-also"></a>関連項目  
 [XML のコメント用タグ](../../../visual-basic/language-reference/xmldoc/index.md)
