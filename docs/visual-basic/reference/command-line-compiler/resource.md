---
title: -リソース (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- /resource compiler option [Visual Basic]
- -resource compiler option [Visual Basic]
- /res compiler option [Visual Basic]
- res compiler option [Visual Basic]
- -res compiler option [Visual Basic]
- resource compiler option [Visual Basic]
ms.assetid: eee2f227-91f2-4f2b-a9d6-1c51c5320858
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ab5593455546e65bdd760d9e60532031dc1f12a9
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42931447"
---
# <a name="-resource-visual-basic"></a>-リソース (Visual Basic)
マネージド リソースをアセンブリに埋め込みます。  
  
## <a name="syntax"></a>構文  
  
```  
-resource:filename[,identifier[,public|private]]  
' -or-  
-res:filename[,identifier[,public|private]]  
```  
  
## <a name="arguments"></a>引数  
  
|用語|定義|  
|---|---|  
|`filename`|必須。 出力ファイルに埋め込むリソース ファイルの名前。 既定では、`filename`アセンブリ内でパブリックです。 ファイル名を引用符で囲みます ("")、スペースが含まれている場合。|  
|`identifier`|任意。 リソースの論理名ファイルを読み込むための名前。 既定値は、ファイルの名前です。 必要に応じて、次のようには、パブリックまたはプライベート アセンブリ マニフェストでにリソースかどうかを指定できます。 `-res:filename.res, myname.res, public`|  
  
## <a name="remarks"></a>Remarks  
 使用`-linkresource`出力ファイルにリソース ファイルを配置することがなく、アセンブリにリソースをリンクします。  
  
 場合`filename`は、[!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]リソース ファイルの作成例については、によって、 [Resgen.exe (リソース ファイル ジェネレーター)](http://msdn.microsoft.com/library/8ef159de-b660-4bec-9213-c3fbc4d1c6f4)または開発環境でアクセスできるメンバー間で、 <xref:System.Resources> (参照名前空間<xref:System.Resources.ResourceManager>詳細については)。 実行時にその他のすべてのリソースにアクセスするには、次のいずれかを使用: <xref:System.Reflection.Assembly.GetManifestResourceInfo%2A>、 <xref:System.Reflection.Assembly.GetManifestResourceNames%2A>、または<xref:System.Reflection.Assembly.GetManifestResourceStream%2A>します。  
  
 `-resource` の省略形は `-res` です。  
  
 設定する方法については`-resource`、Visual Studio IDE で、次を参照してください。[アプリケーション リソースの管理 (.NET)](/visualstudio/ide/managing-application-resources-dotnet)します。  
  
## <a name="example"></a>例  
 次のコードのコンパイル`In.vb`とリソース ファイルのアタッチ`Rf.resource`します。  
  
```console
vbc -res:rf.resource in.vb  
```  
  
## <a name="see-also"></a>関連項目  
 [Visual Basic のコマンド ライン コンパイラ](../../../visual-basic/reference/command-line-compiler/index.md)  
 [-win32resource](../../../visual-basic/reference/command-line-compiler/win32resource.md)  
 [-linkresource (Visual Basic)](../../../visual-basic/reference/command-line-compiler/linkresource.md)  
 [-ターゲット (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md)  
 [コンパイル コマンド ラインのサンプル](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
