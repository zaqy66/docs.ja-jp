---
title: '&lt;含める&gt;(Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- include XML tag
- <include> XML tag
ms.assetid: ba8e9173-82cd-460b-8938-a075a2dfb36d
ms.openlocfilehash: da7a6c15c558fc56dbc6a874d4a28c4434f67668
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43482705"
---
# <a name="ltincludegt-visual-basic"></a>&lt;含める&gt;(Visual Basic)
型と、ソース コード内のメンバーを記述する別のファイルを参照します。  
  
## <a name="syntax"></a>構文  
  
```xml  
<include file="filename" path="tagpath[@name='id']" />  
```  
  
#### <a name="parameters"></a>パラメーター  
 `filename`  
 必須。 文書を含むファイルの名前。 ファイル名をパスで修飾することができます。 囲む`filename`で二重引用符 ("")。  
  
 `tagpath`  
 必須。 タグ `name` につながる `filename` 内のタグのパス。 パスを二重引用符で囲みます ("")。  
  
 `name`  
 必須。 コメントの前にあるタグの名前指定子。 `Name` 必要があります、`id`します。  
  
 `id`  
 必須。 コメントの前に配置するタグの ID。 ID を単一引用符で囲みます (' ')。  
  
## <a name="remarks"></a>Remarks  
 使用して、`<include>`タグをソース コード内のメンバーと型を記述する別のファイル内のコメントを参照してください。 これは文書化のコメントをソース コード ファイル内に直接配置する方法の代替です。  
  
 `<include>`タグは、W3C XML Path Language (XPath) Version 1.0 』 を使用します。 カスタマイズする方法の詳細については、`<include>`使用については、「 http://www.w3.org/TR/xpathします。  
  
## <a name="example"></a>例  
 この例では、`<include>`メンバー ドキュメントのコメントをという名前のファイルからインポートするタグ`commentFile.xml`します。  
  
 [!code-vb[VbVbcnXmlDocComments#4](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/include_1.vb)]  
  
 形式、`commentFile.xml`のとおりです。  
  
```xml  
<Docs>  
<Members name="Open">  
<summary>Opens a file.</summary>  
<param name="filename">File name to open.</param>  
</Members>  
<Members name="Close">  
<summary>Closes a file.</summary>  
<param name="filename">File name to close.</param>  
</Members>  
</Docs>  
```  
  
## <a name="see-also"></a>関連項目  
 [XML のコメント用タグ](../../../visual-basic/language-reference/xmldoc/index.md)
