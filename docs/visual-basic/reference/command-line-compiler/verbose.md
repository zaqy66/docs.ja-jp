---
title: -詳細
ms.date: 03/13/2018
helpviewer_keywords:
- verbose compiler option [Visual Basic]
- -verbose compiler option [Visual Basic]
- /verbose compiler option [Visual Basic]
ms.assetid: d1aec0c1-0261-421d-9adc-5b13756100be
ms.openlocfilehash: e70496b552ced8e07cbe3cde34cda377d94da9f4
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188418"
---
# <a name="-verbose"></a>-詳細
詳細なステータスおよびエラー メッセージを生成するためにコンパイラ ボックスをオンにします。  
  
## <a name="syntax"></a>構文  
  
```  
-verbose[+ | -]  
```  
  
## <a name="arguments"></a>引数  
 `+` &#124; `-`  
 任意。 指定する`-verbose`は指定した場合と同じ`-verbose+`、これにより、コンパイラから詳細なメッセージを出力します。 このオプションの既定値は`-verbose-`します。  
  
## <a name="remarks"></a>Remarks  
 `-verbose`オプションについては、コンパイラによって発行されたエラーの総数が表示されます、アセンブリ、モジュールから読み込んでいるおよびファイルがコンパイルされている現在が表示されます。  
  
> [!NOTE]
>  `-verbose`オプションは、Visual Studio 開発環境内からは使用できません。 コマンドラインからコンパイルする場合にのみ使用可能なです。  
  
## <a name="example"></a>例  
 次のコードのコンパイル`In.vb`し、詳細なステータス情報を表示することをコンパイラに指示します。  
  
```console  
vbc -verbose in.vb  
```  
  
## <a name="see-also"></a>関連項目  
 [Visual Basic のコマンド ライン コンパイラ](../../../visual-basic/reference/command-line-compiler/index.md)  
 [コンパイル コマンド ラインのサンプル](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
