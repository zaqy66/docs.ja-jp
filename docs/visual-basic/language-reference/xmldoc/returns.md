---
title: '&lt;returns&gt;(Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- returns XML tag
- <returns> XML tag
ms.assetid: a03a6469-d907-425d-882f-083187950e7e
ms.openlocfilehash: 47debcef2c6ce56fda4c4a0818c8e813b41ebad1
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/25/2018
ms.locfileid: "42925019"
---
# <a name="ltreturnsgt-visual-basic"></a>&lt;returns&gt;(Visual Basic)
プロパティまたは関数の戻り値を指定します。  
  
## <a name="syntax"></a>構文  
  
```xml  
<returns>description</returns>  
```  
  
#### <a name="parameters"></a>パラメーター  
 `description`  
 戻り値の説明。  
  
## <a name="remarks"></a>Remarks  
 使用して、`<returns>`戻り値を記述するメソッド宣言のコメント内のタグ。  
  
 コンパイル時に [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) を指定して、ドキュメント コメントをファイルに出力します。  
  
## <a name="example"></a>例  
 この例では、`<returns>`何かを説明するタグ、`DoesRecordExist`関数が返される。  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/returns_1.vb)]  
  
## <a name="see-also"></a>関連項目  
 [XML のコメント用タグ](../../../visual-basic/language-reference/xmldoc/index.md)
