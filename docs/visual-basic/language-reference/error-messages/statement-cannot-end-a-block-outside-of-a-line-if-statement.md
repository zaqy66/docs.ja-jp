---
title: ステートメント行の外部でブロックを終了することはできません&#39;場合&#39;ステートメント
ms.date: 07/20/2015
f1_keywords:
- vbc32005
- bc32005
helpviewer_keywords:
- BC32005
ms.assetid: 4039f51b-e0ee-4789-a89b-45d06de06b5d
ms.openlocfilehash: 78fe136acbd09e202b1daeb16dd540cf42ada390
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574717"
---
# <a name="statement-cannot-end-a-block-outside-of-a-line-39if39-statement"></a>ステートメント行の外部でブロックを終了することはできません&#39;場合&#39;ステートメント
単一行`If`ステートメントには、コロン (:) のうちの 1 つで区切られた複数のステートメントが含まれています、`End`単一行の外側のコントロール ブロックのステートメント`If`します。 単一行`If`ステートメントは使用しないでください、`End If`ステートメント。  
  
 **エラー ID:** BC32005  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   単一行を移動`If`ステートメントを含むコントロール ブロックの外側、`End If`ステートメント。  
  
## <a name="see-also"></a>関連項目
- [If...Then...Else ステートメント](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
