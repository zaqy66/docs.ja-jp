---
title: '&lt;seealso&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <seealso> XML tag
- seealso XML tag
ms.assetid: 36050c95-1af2-4284-b9b6-1a70691ed978
ms.openlocfilehash: a792bbea108bcdf33d430c47773466ef3dccdb0c
ms.sourcegitcommit: daa8788af67ac2d1cecd24f9f3409babb2f978c9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47862147"
---
# <a name="ltseealsogt-visual-basic"></a>&lt;seealso&gt; (Visual Basic)
「参照」セクションに表示されるリンクを指定します。  
  
## <a name="syntax"></a>構文  
  
```xml  
<seealso cref="member"/>  
```  
  
#### <a name="parameters"></a>パラメーター  
 `member`  
 現在のコンパイル環境からの呼び出しに利用できる、メンバーまたはフィールドへの参照。 コンパイラは、指定されたコード要素が存在し、渡すことを確認します。`member`出力 XML 内の要素名にします。 `member` は、二重引用符 (" ") で囲む必要があります。  
  
## <a name="remarks"></a>Remarks  
 使用して、 `<seealso>` 「参照」セクションに表示するテキストを指定するタグ。 [\<see>](../../../visual-basic/language-reference/xmldoc/see.md) タグを使用すると、テキスト内からリンクを指定できます。  
  
 コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。  
  
## <a name="example"></a>例  
 この例では、`<seealso>`にタグを付ける、`DoesRecordExist`解説セクションを参照する、`UpdateRecord`メソッド。  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/seealso_1.vb)]  
  
## <a name="see-also"></a>関連項目  
 [XML のコメント用タグ](../../../visual-basic/language-reference/xmldoc/index.md)
