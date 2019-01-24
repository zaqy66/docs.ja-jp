---
title: 変数&#39; &lt;variablename&gt; &#39; 、値が割り当てられる前に使用されます
ms.date: 07/20/2015
f1_keywords:
- vbc42104
- BC42104
helpviewer_keywords:
- BC42104
ms.assetid: 6909aa0b-b4a1-46f5-a18c-ba3e565c1dd8
ms.openlocfilehash: f91343e850600c9e5f4b4b4eb2126798baf3d980
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54647024"
---
# <a name="variable-39ltvariablenamegt39-is-used-before-it-has-been-assigned-a-value"></a>変数&#39; &lt;variablename&gt; &#39; 、値が割り当てられる前に使用されます
変数 '\<variablename >' は、値が割り当てられる前に使用します。 結果として、実行時に null 参照の例外が発生する可能性があります。  
  
 アプリケーションでは、少なくとも 1 つのパスをそのコードを任意の値が割り当てられる前に変数を読み込むことがあります。  
  
 変数に値が割り当てられていない場合、変数はそのデータ型の既定値を保持します。 参照データ型の場合、その既定値は [Nothing](../../../visual-basic/language-reference/nothing.md)です。 値が `Nothing` である参照変数を読み取ると、状況によって <xref:System.NullReferenceException> が発生する可能性があります。  
  
 既定では、このメッセージは警告です。 警告を非表示にする方法や、警告をエラーとして扱う方法の詳細については、「 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)」を参照してください。  
  
 **エラー ID:** BC42104  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   制御フローのロジックを確認し、によって読み取られる任意のステートメントに制御が渡される前に、変数が有効な値を持つかどうかを確認します。  
  
-   変数が常に有効な値を持つことを保証するために 1 つの方法では、その宣言の一部として初期化します。 「初期化」を参照してください[Dim ステートメント](../../../visual-basic/language-reference/statements/dim-statement.md)します。  
  
## <a name="see-also"></a>関連項目
- [Dim ステートメント](../../../visual-basic/language-reference/statements/dim-statement.md)
- [変数宣言](../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [変数のトラブルシューティング](../../../visual-basic/programming-guide/language-features/variables/troubleshooting-variables.md)
