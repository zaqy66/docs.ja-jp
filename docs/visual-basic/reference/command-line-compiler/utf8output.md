---
title: -utf8output (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- -utf8output compiler option [Visual Basic]
- utf8output compiler option [Visual Basic]
- /utf8output compiler option [Visual Basic]
ms.assetid: 8ab36b1e-027a-49ac-85b4-f48997d9e4d6
ms.openlocfilehash: e6bb04364c2f92129993e19c746fd7cb9c18dc8a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648535"
---
# <a name="-utf8output-visual-basic"></a>-utf8output (Visual Basic)
UTF-8 エンコードを使用してコンパイラ出力を表示します。  
  
## <a name="syntax"></a>構文  
  
```  
-utf8output[+ | -]  
```  
  
## <a name="arguments"></a>引数  
 `+` &#124; `-`  
 任意。 このオプションの既定値は`-utf8output-`、つまり、コンパイラの出力は utf-8 エンコードを使用しません。 `-utf8output` を指定することは、`-utf8output+` を指定することと同じです。  
  
## <a name="remarks"></a>Remarks  
 国際対応の構成によっては、コンパイラの出力は、コンソールで正常に表示できません。 このような状況では、次のように使用します。`-utf8output`してコンパイラ出力をファイルにリダイレクトします。  
  
> [!NOTE]
>  `-utf8output`オプションは、Visual Studio 開発環境内からは使用できません。 コマンドラインからコンパイルする場合にのみ使用可能なです。  
  
## <a name="example"></a>例  
 次のコードのコンパイル`In.vb`表示をコンパイラに指示して utf-8 エンコードを使用して出力します。  
  
```console  
vbc -utf8output in.vb  
```  
  
## <a name="see-also"></a>関連項目
- [Visual Basic のコマンド ライン コンパイラ](../../../visual-basic/reference/command-line-compiler/index.md)
- [コンパイル コマンド ラインのサンプル](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
