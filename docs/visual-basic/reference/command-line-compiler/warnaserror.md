---
title: -warnaserror (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- warnaserror compiler option [Visual Basic]
- /warnaserror compiler option [Visual Basic]
- -warnaserror compiler option [Visual Basic]
ms.assetid: 49819f1d-a1bd-4201-affe-5afe6d9712e1
ms.openlocfilehash: 89f6566bd733ff92d464c026102429d3fc5cf0c1
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2018
ms.locfileid: "50047853"
---
# <a name="-warnaserror-visual-basic"></a>-warnaserror (Visual Basic)
コンパイラで最初に発生した警告をエラーとして扱います。  
  
## <a name="syntax"></a>構文  
  
```  
-warnaserror[+ | -][:numberList]  
```  
  
## <a name="arguments"></a>引数  
  
|用語|定義|  
|---|---|  
|+ &#124; -|任意。 既定では、`-warnaserror-`が有効にします。 警告が妨げられないコンパイラ出力ファイルを生成します。 `-warnaserror`オプションは、同じとして`-warnaserror+`、警告をエラーとして扱うことです。|  
|`numberList`|任意。 警告 ID のコンマ区切りの一覧の番号を`-warnaserror`オプションが適用されます。 警告 ID が指定されていない場合、`-warnaserror`オプションは、すべての警告に適用されます。|  
  
## <a name="remarks"></a>Remarks  
 `-warnaserror`オプションは、すべての警告をエラーとして扱います。 警告をエラーとしてレポートされる代わりに、報告される通常メッセージ。 コンパイラは警告として同じ警告の後続の出現箇所を報告します。  
  
 既定では、`-warnaserror-`情報のみを指定するには、警告により、有効です。 `-warnaserror`オプションは、同じとして`-warnaserror+`、警告をエラーとして扱うことです。  
  
 いくつかの特定の警告のみを実行する場合に、エラーとして扱う警告番号のコンマ区切りの一覧を指定することがあります。  
  
> [!NOTE]
>  `-warnaserror`オプションでは、警告を表示する方法は制御しません。 使用して、 [-nowarn](../../../visual-basic/reference/command-line-compiler/nowarn.md)警告を無効にするオプション。  
  
|すべての警告を Visual Studio IDE のエラーとして扱う-warnaserror を設定するには|  
|---|  
|1.**ソリューション エクスプローラー**でプロジェクトを選択します。 **[プロジェクト]** メニューの **[プロパティ]** をクリックします。 <br />2.**[コンパイル]** タブをクリックします。<br />3.確認、**すべての警告を無効にする** チェック ボックスがオフになっています。<br />4.チェック、**すべての警告をエラーとして扱う**チェック ボックスをオンします。|  
  
|特定の警告を Visual Studio IDE のエラーとして扱う-warnaserror を設定するには|  
|---|  
|1.**ソリューション エクスプローラー**でプロジェクトを選択します。 **[プロジェクト]** メニューの **[プロパティ]** をクリックします。<br />2.**[コンパイル]** タブをクリックします。<br />3.確認、**すべての警告を無効にする** チェック ボックスがオフになっています。<br />4.確認、**すべての警告をエラーとして扱う** チェック ボックスがオフになっています。<br />5.選択**エラー**から、**通知**列隣に警告をエラーとして扱う必要があります。|  
  
## <a name="example"></a>例  
 次のコードのコンパイル`In.vb`し、最初に見つかった位置が見つかるすべての警告をエラーとして表示することをコンパイラに指示します。  
  
```console
vbc -warnaserror in.vb  
```  
  
## <a name="example"></a>例  
 次のコードのコンパイル`T2.vb`未使用のローカル変数 (42024) の警告のみをエラーとして扱います。  
  
```console
vbc -warnaserror:42024 t2.vb  
```  
  
## <a name="see-also"></a>関連項目  
 [Visual Basic のコマンド ライン コンパイラ](../../../visual-basic/reference/command-line-compiler/index.md)  
 [コンパイル コマンド ラインのサンプル](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)
