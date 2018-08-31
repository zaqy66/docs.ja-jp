---
title: '&lt;参照してください&gt;(Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- see XML tag
- <see> XML tag
ms.assetid: 7e18f60b-ef4a-4678-a797-5eb918635ca9
ms.openlocfilehash: 78311651593d3d4a47c723f64a9a74d4660f7c90
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/30/2018
ms.locfileid: "43254063"
---
# <a name="ltseegt-visual-basic"></a>&lt;参照してください&gt;(Visual Basic)
別のメンバーへのリンクを指定します。  
  
## <a name="syntax"></a>構文  
  
```xml  
<see cref="member"/>  
```  
  
#### <a name="parameters"></a>パラメーター  
 `member`  
 現在のコンパイル環境からの呼び出しに利用できる、メンバーまたはフィールドへの参照。 コンパイラは、指定されたコード要素が存在し、渡すことを確認します。`member`出力 XML 内の要素名にします。 `member` は、二重引用符 (" ") で囲む必要があります。  
  
## <a name="remarks"></a>Remarks  
 使用して、`<see>`タグからテキスト内のリンクを指定します。 使用[ \<seealso >](../../../visual-basic/language-reference/xmldoc/seealso.md) 「「参照」セクションに表示するテキストを示します。  
  
 コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。  
  
## <a name="example"></a>例  
 この例では、`<see>`にタグを付ける、`UpdateRecord`解説セクションを参照する、`DoesRecordExist`メソッド。  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/see_1.vb)]  
  
## <a name="see-also"></a>関連項目  
 [XML のコメント用タグ](../../../visual-basic/language-reference/xmldoc/index.md)
