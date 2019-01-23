---
title: 序数が有効ではありません。
ms.date: 07/20/2015
f1_keywords:
- vbrID452
ms.assetid: 7459562b-cd4f-4590-95e0-6126ae3589a5
ms.openlocfilehash: 351b7ee7f1cfc5199d878c33965770693227ccc4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54618962"
---
# <a name="ordinal-is-not-valid"></a>序数が有効ではありません。
プロシージャ名ではなく番号を使用するダイナミック リンク ライブラリ (DLL) への呼び出しが示されるを使用して、`#num`構文。 このエラーは、次の考えられる原因があります。  
  
-   変換、`#num`序数が失敗する式。  
  
-   `#num`指定された DLL で任意の関数を指定できません。  
  
-   タイプ ライブラリには、無効な序数の内部使用の無効な宣言があります。  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  名前でプロシージャを呼び出す、または式が有効な数値を表すかどうかを確認します。  
  
2.  必ず`#num`DLL 内の有効な関数を識別します。  
  
3.  問題の原因で、コードのコメント アウト、プロシージャの呼び出しを分離します。 書き込みを`Declare`プロシージャと、タイプ ライブラリのベンダーの問題の報告ステートメント。  
  
## <a name="see-also"></a>関連項目
- [Declare ステートメント](../../../visual-basic/language-reference/statements/declare-statement.md)
