---
title: "'<expression>' を型制約として使用することはできません。"
ms.date: 07/20/2015
f1_keywords:
- bc32061
- vbc32061
helpviewer_keywords:
- BC32061
ms.assetid: b17821b7-fa14-4397-a211-6e2a14079f09
ms.openlocfilehash: 02d5035daa1ff3da4d7d3bac7c95ef8e8379b3f7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55264675"
---
# <a name="expression-cannot-be-used-as-a-type-constraint"></a>'\<式 >' を型制約として使用することはできません
制約リストに、型パラメーターについて有効な制約を表していない式が含まれています。  
  
 制約リストでは、型パラメーターに渡される型引数の要件が適用されます。 次の要件を任意の組み合わせで指定できます。  
  
-   型引数が 1 つまたは複数のインターフェイスを実装する必要があります  
  
-   型引数は、最大で 1 つのクラスから継承する必要があります  
  
-   型引数は、作成元のコードがアクセスできるパラメーターなしのコンストラクターを公開する必要があります ( `New` 制約を含む)  
  
 制約リストに特定のクラスまたはインターフェイスを何も含めない場合は、次のいずれかを指定することによって一般的な要件を設定できます。  
  
-   型引数は値型である必要があります ( `Structure` 制約を含む)  
  
-   型引数は参照型である必要があります ( `Class` 制約を含む)  
  
 同じ型パラメーターに `Structure` と `Class` の両方を指定することはできません。また、どちらも複数回指定することはできません。  
  
 **エラー ID:** BC32061  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   式とその要素のスペルが正しいことを確認します。  
  
-   式が上記の要件リストを満たしていない場合は、制約リストから削除します。  
  
-   式でインターフェイスまたはクラスを参照する場合、コンパイラにそのインターフェイスまたはクラスへのアクセス権があることを確認します。 その名前を修飾し、プロジェクトに参照を追加することが必要な場合があります。 詳細についてを参照してください「の参照をプロジェクト」 [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)します。  
  
## <a name="see-also"></a>関連項目
- [Visual Basic におけるジェネリック型](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
- [値型と参照型](../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
- [宣言された要素の参照](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)

