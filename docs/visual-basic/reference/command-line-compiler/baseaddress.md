---
title: -baseaddress
ms.date: 08/09/2018
f1_keywords:
- /baseaddress
- baseaddress
helpviewer_keywords:
- -baseaddress compiler option [Visual Basic]
- /baseaddress compiler option [Visual Basic]
- baseaddress compiler option [Visual Basic]
ms.assetid: c982bcf2-46e5-47a2-bc8f-a5cc32b7dc47
ms.openlocfilehash: 733013c8eca75bad0dc0bdf1d76f1468b1d903a8
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2019
ms.locfileid: "55759393"
---
# <a name="-baseaddress"></a>-baseaddress
DLL を作成するときに、既定のベース アドレスを指定します。  
  
## <a name="syntax"></a>構文  
  
```  
-baseaddress:address  
```  
  
## <a name="arguments"></a>引数  
  
|用語|定義|  
|---|---|  
|`address`|必須。 DLL のベース アドレス。 このアドレスは、16 進数として指定する必要があります。|  
  
## <a name="remarks"></a>Remarks  
 DLL の既定のベース アドレスの設定、[!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]します。  
  
 このアドレスの下位ワードは丸められますことに注意します。 たとえば、0x11110001 とを指定する場合は丸められて 0x11110000 に丸められます。  
  
 DLL の署名プロセスを完了するには使用、`–R`厳密名ツール (Sn.exe) のオプション。  
  
 このオプションには、ターゲットが DLL ではない場合は無視されます。  
  
|Visual Studio IDE で-baseaddress を設定するには|  
|---|  
|1.**ソリューション エクスプローラー**でプロジェクトを選択します。 **[プロジェクト]** メニューの **[プロパティ]** をクリックします。 <br />2.**[コンパイル]** タブをクリックします。<br />3.**[詳細設定]** をクリックします。<br />4.値を変更、 **DLL ベース アドレス:** ボックス。 **注:**    **DLL ベース アドレス:** ターゲットが DLL でない限り、ボックスは読み取り専用です。|  
  
## <a name="see-also"></a>関連項目
- [Visual Basic のコマンド ライン コンパイラ](../../../visual-basic/reference/command-line-compiler/index.md)
- [-ターゲット (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md)
- [コンパイル コマンド ラインのサンプル](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [Sn.exe (厳密名ツール)](../../../framework/tools/sn-exe-strong-name-tool.md))
