---
title: Sub または Function が定義されていません。(Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vbrID35
ms.assetid: 661fdb90-ee7d-40ce-b30b-5e7267bd957a
ms.openlocfilehash: 4627f8ddb979780481feadbef06225baf6a7c0ca
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54532176"
---
# <a name="sub-or-function-not-defined-visual-basic"></a>Sub または Function が定義されていません。(Visual Basic)
A`Sub`または`Function`呼び出すには定義する必要があります。 このエラーでは以下の原因が考えられます。  
  
-   プロシージャ名のスペルが間違っています。  
  
-   別のプロジェクトからでは、そのプロジェクトへの参照を明示的に追加せず、プロシージャを呼び出そうとしている、**参照** ダイアログ ボックス。  
  
-   呼び出し元のプロシージャには表示されないプロシージャを指定します。  
  
-   Windows ダイナミック リンク ライブラリ (DLL) のルーチンまたは指定したライブラリまたはコード リソース内にない Macintosh コード リソースのルーチンを宣言します。  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  プロシージャ名のスペルが正しいことを確認します。  
  
2.  呼び出そうとプロシージャを含むプロジェクトの名前を検索、**参照** ダイアログ ボックス。 表示されない場合は、クリックして、**参照**検索ボタンをクリックします。 プロジェクト名の左側にチェック ボックスを選択し、クリックして**OK**します。  
  
3.  ルーチンの名前を確認します。  
  
## <a name="see-also"></a>関連項目
- [エラーの種類](../../../visual-basic/programming-guide/language-features/error-types.md)
- [プロジェクト内の参照の管理](/visualstudio/ide/managing-references-in-a-project)
- [Sub ステートメント](../../../visual-basic/language-reference/statements/sub-statement.md)
- [Function ステートメント](../../../visual-basic/language-reference/statements/function-statement.md)
