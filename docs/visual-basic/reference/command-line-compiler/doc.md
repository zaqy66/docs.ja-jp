---
title: -ドキュメント
ms.date: 03/10/2018
helpviewer_keywords:
- doc compiler option [Visual Basic]
- -doc compiler option [Visual Basic]
- /doc compiler option [Visual Basic]
ms.assetid: 5fc32ec9-a149-4648-994c-a8d0cccd0a65
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4c77d063d64354bf4693ce82509f36be9d2e5b0c
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42934480"
---
# <a name="-doc"></a>-ドキュメント
ドキュメント コメントを XML ファイルに出力します。  
  
## <a name="syntax"></a>構文  
  
```  
-doc[+ | -]  
' -or-  
-doc:file  
```  
  
## <a name="arguments"></a>引数  
  
|用語|定義|  
|---|---|  
|`+` &#124; `-`|任意。 指定する +、または単`-doc`、コンパイラが、ドキュメント情報を生成し、XML ファイル内に配置します。 指定する`-`指定しない場合のと同じ`-doc`、なり、ドキュメントの情報を作成します。|  
|`file`|`-doc:` を使用する場合に、必ず指定します。 コンパイルのソース コード ファイルからのコメントが設定されている出力 XML ファイルを指定します。 ファイル名にスペースが含まれている場合は、引用符で名を囲む ("")。|  
  
## <a name="remarks"></a>Remarks  
 `-doc`オプションでは、コンパイラは、ドキュメント コメントを含む XML ファイルを生成するかどうかを制御します。 使用する場合、 `-doc:file` 、構文、`file`パラメーターを XML ファイルの名前を指定します。 使用する場合`-doc`または`-doc+`コンパイラは、実行可能ファイルまたはコンパイラを作成しているライブラリから XML ファイルの名前を取得します。 使用する場合`-doc-`を指定しないか、`-doc`オプション、コンパイラは、XML ファイルを作成しません。  
  
 ソース コード ファイル、ドキュメントのコメントは以下の定義の前にことができます。  
  
-   ユーザー定義型の場合など、[クラス](../../../visual-basic/language-reference/statements/class-statement.md)または[インターフェイス](../../../visual-basic/language-reference/statements/interface-statement.md)  
  
-   など、フィールド メンバー[イベント](../../../visual-basic/language-reference/statements/event-statement.md)、[プロパティ](../../../visual-basic/language-reference/statements/property-statement.md)、[関数](../../../visual-basic/language-reference/statements/function-statement.md)、または[サブルーチン](../../../visual-basic/language-reference/statements/sub-statement.md)します。  
  
 Visual Studio で生成された XML ファイルを使用する[IntelliSense](/visualstudio/ide/using-intellisense)機能をサポートするアセンブリと同じである XML ファイルのファイル名を使用します。 .Xml ファイルにも見つかるアセンブリは、Visual Studio プロジェクトで参照されるとき、に、アセンブリと同じディレクトリに XML ファイルが確認します。 XML ドキュメント ファイルは、コード プロジェクト内、またはプロジェクトによって参照されているプロジェクト内で動作する IntelliSense の必要はありません。  
  
 コンパイルしない限り`/target:module`、XML ファイルには、タグが含まれています。`<assembly></assembly>`します。 これらのタグは、コンパイルの出力ファイルのアセンブリ マニフェストを含むファイルの名前を指定します。  
  
 参照してください[XML コメント タグ](../../../visual-basic/language-reference/xmldoc/index.md)コードのコメントからドキュメントを生成する方法について。  
  
|設定されているドキュメントは、Visual studio 統合開発環境|  
|---|  
|1.**ソリューション エクスプローラー**でプロジェクトを選択します。 **[プロジェクト]** メニューの **[プロパティ]** をクリックします。 <br />2.**[コンパイル]** タブをクリックします。<br />3.値を設定、**生成 XML ドキュメント ファイル**ボックス。|  
  
## <a name="example"></a>例  
 参照してください[xml コードの文書化](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md)サンプルについては、します。  
  
## <a name="see-also"></a>関連項目  
 [Visual Basic のコマンド ライン コンパイラ](../../../visual-basic/reference/command-line-compiler/index.md)  
 [XML の使用によるコードのドキュメントの作成](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md)
