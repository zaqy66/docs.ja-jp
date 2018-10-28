---
title: -定義 (Visual Basic)
ms.date: 03/10/2018
helpviewer_keywords:
- -d compiler option [Visual Basic]
- /d compiler option [Visual Basic]
- -define compiler option [Visual Basic]
- d compiler option [Visual Basic]
- /define compiler option [Visual Basic]
- define compiler option [Visual Basic]
ms.assetid: f735c57d-1cf9-4f2f-a26f-0de630fd4077
ms.openlocfilehash: 4cab6bc968275bc12af4365fd3da5e3b5ff417f2
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50195178"
---
# <a name="-define-visual-basic"></a>-定義 (Visual Basic)
条件付きコンパイル定数を定義します。  
  
## <a name="syntax"></a>構文  
  
```  
-define:["]symbol[=value][,symbol[=value]]["]  
' -or-  
-d:["]symbol[=value][,symbol[=value]]["]  
```  
  
## <a name="arguments"></a>引数  
  
|用語|定義|  
|---|---|  
|`symbol`|必ず指定します。 定義する記号。|  
|`value`|省略可能です。 `symbol` に代入する値。 場合`value`文字列で、シーケンスのバック スラッシュ/引用符で囲みます (\\") 引用符の代わりにします。 値が指定されていない場合は、True として処理されます。|  
  
## <a name="remarks"></a>Remarks  
 `-define`オプションを使用すると同様の効果には、`#Const`プリプロセッサ ディレクティブで定義された定数を除く、ソース ファイル内`-define`をパブリックにして、プロジェクト内のすべてのファイルに適用されます。  
  
 このオプションで作成される記号を `#If`...`Then`...`#Else` ディレクティブで使用すると、ソース ファイルを条件付きでコンパイルできます。  
  
 `-d` は `-define` の省略形です。  
  
 記号の定義をコンマで区切ると、`-define` を使用して複数の記号を定義できます。  
  
|Visual Studio 統合開発環境で /define を設定するには|  
|---|  
|1.**ソリューション エクスプローラー**でプロジェクトを選択します。 **[プロジェクト]** メニューの **[プロパティ]** をクリックします。 <br />2.**[コンパイル]** タブをクリックします。<br />3.**[詳細設定]** をクリックします。<br />4.値を変更、**カスタム定数**ボックス。|  
  
## <a name="example"></a>例  
 2 つの条件付きコンパイル定数を定義して使用する場合のコード例を次に示します。  
  
 [!code-vb[VbVbalrCompiler#45](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/define_1.vb)]  
  
## <a name="see-also"></a>関連項目  
 [Visual Basic のコマンド ライン コンパイラ](../../../visual-basic/reference/command-line-compiler/index.md)  
 [#If...Then...#Else ディレクティブ](../../../visual-basic/language-reference/directives/if-then-else-directives.md)  
 [#Const ディレクティブ](../../../visual-basic/language-reference/directives/const-directive.md)  
 [コンパイル コマンド ラインのサンプル](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
