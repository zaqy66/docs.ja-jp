---
title: '&#39;AddressOf&#39;オペランドは (かっこ) を使用せず、メソッドの名前を指定する必要があります'
ms.date: 07/20/2015
f1_keywords:
- vbc30577
- bc30577
helpviewer_keywords:
- BC30577
ms.assetid: c2c55640-5c61-4e66-97a4-4322020c6001
ms.openlocfilehash: 6f9827d885996ffab8bdab91d0f774a57073e4a3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54565151"
---
# <a name="39addressof39-operand-must-be-the-name-of-a-method-without-parentheses"></a>&#39;AddressOf&#39;オペランドは (かっこ) を使用せず、メソッドの名前を指定する必要があります
`AddressOf` 演算子は、特定のプロシージャを参照するプロシージャ デリゲート インスタンスを作成します。 構文は次のとおりです。  
  
 `AddressOf` `procedurename`  
  
 かっこで囲んで引数以下を挿入した`AddressOf`none は必要に応じて、します。  
  
 **エラー ID:** BC30577  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  次の引数を囲むかっこを削除`AddressOf`します。  
  
2.  引数がメソッド名を確認します。  
  
## <a name="see-also"></a>関連項目
- [AddressOf 演算子](../../../visual-basic/language-reference/operators/addressof-operator.md)
- [デリゲート](../../../visual-basic/programming-guide/language-features/delegates/index.md)
