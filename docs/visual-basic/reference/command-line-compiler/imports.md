---
title: -インポート (Visual Basic)
ms.date: 03/10/2018
helpviewer_keywords:
- /imports compiler option [Visual Basic]
- imports compiler option [Visual Basic]
- -imports compiler option [Visual Basic]
ms.assetid: 9a93fb53-c080-497b-bf9b-441022dbbc39
ms.openlocfilehash: 9e5adcce85c4ca4863d28784a7d7f61c441a06c8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54588445"
---
# <a name="-imports-visual-basic"></a>-インポート (Visual Basic)
指定したアセンブリから名前空間をインポートします。  
  
## <a name="syntax"></a>構文  
  
```  
-imports:namespaceList  
```  
  
## <a name="arguments"></a>引数  
  
|用語|定義|  
|---|---|  
|`namespaceList`|必須。 インポートする名前空間のコンマ区切りリスト。|  
  
## <a name="remarks"></a>Remarks  
 `-imports`オプションは、現在のソース ファイルまたは参照先アセンブリのセット内で定義されている任意の名前空間をインポートします。  
  
 指定された名前空間内のメンバー`-imports`コンパイルですべてのソース コード ファイルを利用できます。 使用して、 [Imports ステートメント (.NET Namespace よぶ型)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)を 1 つのソース コード ファイルの名前空間を使用します。  
  
|設定する]、[Visual Studio 統合開発環境のインポート|  
|---|  
|1.**ソリューション エクスプローラー**でプロジェクトを選択します。 **[プロジェクト]** メニューの **[プロパティ]** をクリックします。 <br />2.**[参照]** タブをクリックします。<br />3.横にあるボックスに名前空間の名前を入力、**ユーザー インポートの追加**ボタンをクリックします。<br />4.をクリックして、**ユーザー インポートの追加**ボタンをクリックします。|  
  
## <a name="example"></a>例  
 ときに、次のコードがコンパイル`/imports:system.globalization`を指定します。 それなしに正常にコンパイルする必要がありますか、`Imports System.Globalization`ステートメントは、ソース コード ファイルの先頭に必ず、またはプロパティとして完全修飾`System.Globalization.CultureInfo.CurrentCulture.Name`します。 
  
 [!code-vb[imports example](codesnippet/VisualBasic/imports_2.vb)]  
  
## <a name="see-also"></a>関連項目
- [Visual Basic のコマンド ライン コンパイラ](../../../visual-basic/reference/command-line-compiler/index.md)
- [参照と Imports ステートメント](../../../visual-basic/programming-guide/program-structure/references-and-the-imports-statement.md)
- [コンパイル コマンド ラインのサンプル](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
