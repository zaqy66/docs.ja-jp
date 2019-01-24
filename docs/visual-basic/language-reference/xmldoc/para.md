---
title: '&lt;para&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <para> XML tag
- para XML tag
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
ms.openlocfilehash: 5932ddb55a4dab48267cdd9b9f321cec8660d77a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54662323"
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
  
## <a name="remarks"></a>コメント  
 `<para>`などは、タグの内側で使用するタグ[\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md)、 [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md)、または[\<returns>](../../../visual-basic/language-reference/xmldoc/returns.md)、テキストに構造を追加することができます。    
  
 コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。  
  
## <a name="example"></a>例  
 この例では、`<para>`の「解説」セクションに分割するタグ、`UpdateRecord`メソッドが 2 つの段落にします。  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/para_1.vb)]  
  
## <a name="see-also"></a>関連項目
- [XML のコメント用タグ](../../../visual-basic/language-reference/xmldoc/index.md)
