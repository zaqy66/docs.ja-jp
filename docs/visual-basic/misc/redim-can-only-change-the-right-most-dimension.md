---
title: '&#39;ReDim&#39;最も右にある次元のみ変更できます'
ms.date: 07/20/2015
f1_keywords:
- vbrArray_TypeMismatch
ms.assetid: d53cf41b-7a7a-466c-a29a-920d99698fa9
ms.openlocfilehash: 94e0fe81f7e750a67943b68f2db700e3a7831da1
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43482718"
---
# <a name="39redim39-can-only-change-the-right-most-dimension"></a>&#39;ReDim&#39;最も右にある次元のみ変更できます
`ReDim` ステートメントが `Preserve` キーワードを使用して、最後のディメンションではない配列のディメンションを変更しようとしました。 `Preserve`を使用すると、配列の最後のディメンションについてのみ、サイズを変更できます。 他のすべてのディメンションに対しては、既存の配列と同じサイズを指定する必要があります。  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   `Preserve` キーワードを削除します。  
  
## <a name="see-also"></a>関連項目  
 [Visual Basic における配列](~/docs/visual-basic/programming-guide/language-features/arrays/index.md)  
 [Visual Basic で配列の次元](~/docs/visual-basic/programming-guide/language-features/arrays/array-dimensions.md)  
 [ReDim ステートメント](../../visual-basic/language-reference/statements/redim-statement.md)  
 [Dim ステートメント](../../visual-basic/language-reference/statements/dim-statement.md)  
 [保存 - 削除](https://msdn.microsoft.com/library/91badeab-b4e0-48b6-92c9-9f0c8f995d81)
