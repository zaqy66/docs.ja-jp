---
title: '#領域ディレクティブ (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.Region
- vb.#Region
helpviewer_keywords:
- Visual Basic compiler, compiler directives
- '#region directive'
- region directive (#region)
- '#Region keyword [Visual Basic]'
ms.assetid: 90a6a104-3cbf-47d0-bdc4-b585d0921b87
ms.openlocfilehash: 204b53751fce4f9a3e038ae7c44634522d54657c
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43385373"
---
# <a name="region-directive"></a>#Region ディレクティブ
Visual Basic ファイルのコードのセクションを折りたたんで非表示にします。  
  
## <a name="syntax"></a>構文  

```vb
#Region "identifier_string"  
#End Region  
```  
  
## <a name="parts"></a>指定項目  
  
|用語|定義|  
|---|---|  
|`identifier_string`|必須。 領域が折りたたまれたときにその領域のタイトルとして機能する文字列です。 既定では、領域は折りたたまれています。|  
|`#End Region`|`#Region` ブロックを終了します。|  
  
## <a name="remarks"></a>Remarks  
 Visual Studio コード エディターのアウトライン機能を使うときに展開または折りたたみの対象となるコード ブロックを指定するには、`#Region` ディレクティブを使用します。 に配置するまたは*入れ子*、類似した領域をグループ化するには、他のリージョン内のリージョン。  
  
## <a name="example"></a>例  
 `#Region` ディレクティブの使用例を次に示します。  
  
 [!code-vb[VbVbalrConditionalComp#4](../../../visual-basic/language-reference/directives/codesnippet/VisualBasic/region-directive_1.vb)]  
  
## <a name="see-also"></a>関連項目  
 [#If...Then...#Else ディレクティブ](../../../visual-basic/language-reference/directives/if-then-else-directives.md)  
 [アウトライン](/visualstudio/ide/outlining)  
 [方法 : コードのセクションを折りたたんで非表示にする](../../../visual-basic/programming-guide/program-structure/how-to-collapse-and-hide-sections-of-code.md)
