---
title: '&lt;typeparam&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- typeparam XML tag
- <typeparam> XML tag
ms.assetid: 1bb5ba78-f060-478c-905c-77a2e43639af
ms.openlocfilehash: d362f181921a39d274eaee78e85976522ce4fc15
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43863190"
---
# <a name="lttypeparamgt-visual-basic"></a>&lt;typeparam&gt; (Visual Basic)
型パラメーターの名前と説明を定義します。  
  
## <a name="syntax"></a>構文  
  
```xml  
<typeparam name="name">description</typeparam>  
```  
  
#### <a name="parameters"></a>パラメーター  
 `name`  
 型パラメーターの名前。 名前は二重引用符 (" ") で囲みます。  
  
 `description`  
 型パラメーターの説明。  
  
## <a name="remarks"></a>Remarks  
 使用して、`<typeparam>`型パラメーターのいずれかを記述するには、ジェネリック型またはジェネリック メンバー宣言のコメント内のタグ。  
  
 コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。  
  
## <a name="example"></a>例  
 この例では、`<typeparam>`を記述するタグ、`id`パラメーター。  
  
 [!code-vb[VbVbcnXmlDocComments#8](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/typeparam_1.vb)]  
  
## <a name="see-also"></a>関連項目  
 [XML のコメント用タグ](../../../visual-basic/language-reference/xmldoc/index.md)
