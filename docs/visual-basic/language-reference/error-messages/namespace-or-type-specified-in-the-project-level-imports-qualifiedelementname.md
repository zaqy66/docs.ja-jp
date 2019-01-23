---
title: プロジェクト レベル インポートで指定された Namespace または型&#39; &lt;qualifiedelementname&gt; &#39;は&#39;t は、パブリック メンバーを含めることがまたはが見つかりません
ms.date: 07/20/2015
f1_keywords:
- vbc40057
- bc40057
helpviewer_keywords:
- BC40057
ms.assetid: 4ae3506e-2ebe-4ff3-995d-14ac60db5e9f
ms.openlocfilehash: 215d8d301317f711aecb88167030e70ed01408aa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54552464"
---
# <a name="namespace-or-type-specified-in-the-project-level-imports-39ltqualifiedelementnamegt39-doesn39t-contain-any-public-member-or-cannot-be-found"></a>プロジェクト レベル インポートで指定された Namespace または型&#39; &lt;qualifiedelementname&gt; &#39;は&#39;t は、パブリック メンバーを含めることがまたはが見つかりません
プロジェクト レベル インポートで指定された Namespace または型\<qualifiedelementname >' のパブリック メンバーを含んでいないか、見つかりません。 確認して、名前空間または型が定義されているし、少なくとも 1 つのパブリック メンバーが含まれています。 エイリアス名には他のエイリアスが含まれていないことを確認します。  
  
 見つからないか、いずれかを一切定義しませんコンテナー要素を指定して、プロジェクトのインポート プロパティ`Public`メンバー。  
  
 A*要素を含む*名前空間、クラス、構造体、モジュール、インターフェイス、または列挙型にすることができます。 コンテナー要素には、変数、プロシージャ、または他のコンテナー要素などのメンバーが含まれています。  
  
 インポートの目的は、それらを修飾することがなくコードの名前空間または型メンバーにアクセスを許可します。 プロジェクトは、名前空間または型への参照を追加する必要もあります。 詳細については、「を格納している要素のインポート」を参照してください[References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)します。  
  
 コンパイラに指定されたコンテナー要素が見つからない場合、それを使用して参照を解決できません。 要素を検索しますが、いずれかの要素を公開しません`Public`メンバー、その参照はありませんが成功することができます。 いずれの場合も要素をインポートしても無意味です。  
  
 使用する、**プロジェクト デザイナー**をインポートする要素を指定します。 使用して、**インポートされた名前空間**のセクション、**参照**ページ。 取得する、**プロジェクト デザイナー**をダブルクリックして、 **My Project**アイコン**ソリューション エクスプ ローラー**します。  
  
 **エラー ID:** BC40057  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  開く、**プロジェクト デザイナー**に切り替えると、**参照**ページ。  
  
2.  **インポートされた名前空間**セクションで、コンテナーの要素がプロジェクトからアクセスできることを確認します。  
  
3.  コンテナーの要素が少なくとも 1 つを公開していることを確認します。`Public`メンバー。  
  
## <a name="see-also"></a>関連項目
- [[参照設定] ページ (プロジェクト デザイナー) (Visual Basic)](/visualstudio/ide/reference/references-page-project-designer-visual-basic)
- [プロジェクトおよびソリューションのプロパティの管理](/visualstudio/ide/managing-project-and-solution-properties)
- [Public](../../../visual-basic/language-reference/modifiers/public.md)
- [Visual Basic における名前空間](../../../visual-basic/programming-guide/program-structure/namespaces.md)
- [宣言された要素の参照](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
