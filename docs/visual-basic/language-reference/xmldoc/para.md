---
title: '&lt;para&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <para> XML tag
- para XML tag
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
ms.openlocfilehash: fa11c713a5ed5793b50865753f8bcdeaabf56e83
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/18/2018
ms.locfileid: "45994287"
---
# <a name="ltparagt-visual-basic"></a>&lt;para&gt; (Visual Basic)
コンテンツが文章としてフォーマットされているを指定します。  
  
## <a name="syntax"></a>構文  
  
```xml  
<para>content</para>  
```  
  
#### <a name="parameters"></a>パラメーター  
 `content`  
 段落のテキストです。  
  
## <a name="remarks"></a>Remarks  
 `<para>`などは、タグの内側で使用するタグ[\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md)、 [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md)、または[\<returns>](../../../visual-basic/language-reference/xmldoc/returns.md)、テキストに構造を追加することができます。  
  
 コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。  
  
## <a name="example"></a>例  
 この例では、`<para>`の「解説」セクションに分割するタグ、`UpdateRecord`メソッドが 2 つの段落にします。  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/para_1.vb)]  
  
## <a name="see-also"></a>関連項目  
 [XML のコメント用タグ](../../../visual-basic/language-reference/xmldoc/index.md)
