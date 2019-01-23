---
title: インポートで指定された Namespace または型&#39; &lt;qualifiedelementname&gt; &#39;は&#39;t は、パブリック メンバーを含めることがまたはが見つかりません
ms.date: 07/20/2015
f1_keywords:
- bc40056
- vbc40056
helpviewer_keywords:
- BC40056
ms.assetid: b59f5754-444f-4378-9272-9678b437e84a
ms.openlocfilehash: 21c0794fb4ed6104204fba5d49e37394eff24865
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54552139"
---
# <a name="namespace-or-type-specified-in-the-imports-39ltqualifiedelementnamegt39-doesn39t-contain-any-public-member-or-cannot-be-found"></a>インポートで指定された Namespace または型&#39; &lt;qualifiedelementname&gt; &#39;は&#39;t は、パブリック メンバーを含めることがまたはが見つかりません
インポートで指定された Namespace または型\<qualifiedelementname >' のパブリック メンバーを含んでいないか、見つかりません。 確認して、名前空間または型が定義されているし、少なくとも 1 つのパブリック メンバーが含まれています。 エイリアス名には他のエイリアスが含まれていないことを確認します。  
  
 `Imports`ステートメントがコンテナー要素を検出することはできませんか、いずれかを定義していないいずれかを指定する`Public`メンバー。  
  
 A*要素を含む*名前空間、クラス、構造体、モジュール、インターフェイス、または列挙型にすることができます。 コンテナー要素には、変数、プロシージャ、または他のコンテナー要素などのメンバーが含まれています。  
  
 インポートの目的は、それらを修飾することがなくコードの名前空間または型メンバーにアクセスを許可します。 プロジェクトは、名前空間または型への参照を追加する必要もあります。 詳細については、「を格納している要素のインポート」を参照してください[References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)します。  
  
 コンパイラに指定されたコンテナー要素が見つからない場合、それを使用して参照を解決できません。 要素を検索しますが、いずれかの要素を公開しません`Public`メンバー、その参照はありませんが成功することができます。 いずれの場合も要素をインポートしても無意味です。  
  
 コンテナー要素をインポートしてインポート エイリアスを割り当てる場合、使用できないことそのインポート エイリアスを別の要素をインポートすることに留意してください。 次のコードでは、コンパイラ エラーを生成します。  
  
 `Imports`   `winfrm`   `= System.Windows.Forms`  
  
 `' The following statement is`   `INVALID`   `because it reuses an import alias.`  
  
 `Imports behav =`   `winfrm`  `.Design.Behavior`  
  
 **エラー ID:** BC40056  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  コンテナー要素がプロジェクトからアクセスできることを確認します。  
  
2.  別のインポートからのインポート エイリアスが含まれている要素の仕様に含まれていないことを確認します。  
  
3.  コンテナーの要素が少なくとも 1 つを公開していることを確認します。`Public`メンバー。  
  
## <a name="see-also"></a>関連項目
- [Imports ステートメント (.NET 名前空間および型)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)
- [Namespace ステートメント](../../../visual-basic/language-reference/statements/namespace-statement.md)
- [Public](../../../visual-basic/language-reference/modifiers/public.md)
- [Visual Basic における名前空間](../../../visual-basic/programming-guide/program-structure/namespaces.md)
- [宣言された要素の参照](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
