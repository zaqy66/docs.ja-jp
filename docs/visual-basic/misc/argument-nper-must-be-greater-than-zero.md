---
title: 引数 'NPer' は 0 より大きくなければなりません
ms.date: 07/20/2015
f1_keywords:
- vbrRate_NPerMustBeGTZero
ms.assetid: d49242df-dbd1-4b26-bd8c-ed56d24fdfcd
ms.openlocfilehash: 23e3f59236d30ee7293fa1784c5f0a0d1a087713
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54497473"
---
# <a name="argument-nper-must-be-greater-than-zero"></a>引数 'NPer' は 0 より大きくなければなりません
`NPer` 関数 (定期定額払いおよび固定金利に基づいて年金の期間を指定する `Double` を返します) には、0 を超える引数が必要です。  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   式の引数のスペルを確認します。 変数名のスペルが間違っていると、0 に初期化される数値型の変数が暗黙的に生成されることがあります。  
  
-   式の変数 (特に、他のプロシージャから引数としてプロシージャに渡されたもの) に対してこれまで実行した操作を確認します。  
  
## <a name="see-also"></a>関連項目
- [引数の値渡しと参照渡し](../../visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
