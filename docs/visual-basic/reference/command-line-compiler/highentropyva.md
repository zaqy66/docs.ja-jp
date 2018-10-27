---
title: -highentropyva (Visual Basic)
ms.date: 03/10/2018
helpviewer_keywords:
- highentropyva compiler option (Visual Basic)
- /highentropyva compiler option (Visual Basic)
ms.assetid: ff25f20a-6ca2-467b-9e52-5cf439f5028e
ms.openlocfilehash: 5d948817d4bc71aa31c5890f6740248f4c309588
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50181502"
---
# <a name="-highentropyva-visual-basic"></a>-highentropyva (Visual Basic)
示す、64 ビット実行可能ファイルまたは実行可能ファイルでマークされているかどうか、 [/platform:anycpu](../../../visual-basic/reference/command-line-compiler/platform.md)コンパイラ オプションで高エントロピ アドレス空間レイアウト Randomization (ASLR) をサポートします。  
  
## <a name="syntax"></a>構文  
  
```  
-highentropyva[+ | -]  
```  
  
## <a name="arguments"></a>引数  
 `+` &#124; `-`  
 任意。 既定では、オプションはオフですまたは指定した`-highentropyva-`します。 指定したかどうかに、オプションは、`-highentropyva`または`-highentropyva+`します。  
  
## <a name="remarks"></a>Remarks  
 このオプションを指定する場合、互換性のあるバージョンの Windows カーネルはカーネル ASLR の一環として、プロセスのアドレス空間レイアウトをランダムにときに高いレベルのエントロピを使用できます。 カーネルは、高いレベルのエントロピを使用している場合、アドレスの数が多いがスタックやヒープといったメモリ領域に割り当てられたことができます。 これによって特定のメモリ領域の位置を推測しづらくなる効果が得られます。  
  
 オプションが、ターゲットの実行可能ファイルとすべてのモジュールでのこれらのモジュールは、64 ビット プロセスとして実行しているときに、4 ギガバイト (GB) を超えるポインター値を処理することに依存する必要があります。  
  
## <a name="see-also"></a>関連項目  
 [Visual Basic のコマンド ライン コンパイラ](../../../visual-basic/reference/command-line-compiler/index.md)  
 [コンパイル コマンド ラインのサンプル](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
