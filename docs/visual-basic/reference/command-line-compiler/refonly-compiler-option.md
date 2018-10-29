---
title: -refonly (Visual Basic)
ms.date: 03/16/2018
f1_keywords:
- -refonly
helpviewer_keywords:
- /refonly compiler option [Visual Basic]
- -refonly compiler option [Visual Basic]
- refonly compiler option [Visual Basic]
ms.openlocfilehash: b22fb9ae24a04d9fe530811bf764352199c31813
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50200811"
---
# <a name="-refonly-visual-basic"></a>-refonly (Visual Basic)

**-Refonly**オプションでは、コンパイルのプライマリ出力で実装アセンブリではなく、参照アセンブリがあることを示します。 `-refonly` パラメーターは、参照アセンブリを実行できない場合に、PDB の出力を暗黙的に無効にします。

[!INCLUDE[compiler-options](~/includes/compiler-options.md)]

## <a name="syntax"></a>構文

```console
-refonly
```

## <a name="remarks"></a>Remarks

Visual Basic は、`-refout`バージョン 15.3 以降を切り替えます。

参照アセンブリは、実装コードではなくメタデータが含まれているメタデータのみアセンブリです。 匿名型を除くすべての型およびメンバーの情報が含まれます。 (本体なしではなく) `throw null` 本体を使用する理由は、PEVerify を実行して渡せるようにするためです (そのためにメタデータの完全性を検証します)。

参照アセンブリは、アセンブリ レベル[ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute)属性。 この属性は、ソースで指定できます (指定すると、コンパイラではこれを合成する必要がなくなります)。 この属性により、ランタイムは、実行の参照アセンブリの読み込みが拒否されます (ただしリフレクション専用コンテキストに読み込まれていることがあります)。 アセンブリにリフレクションするツールは、リフレクション専用として参照アセンブリが読み込まれることを確認する必要があります。それ以外の場合、ランタイム、<xref:System.BadImageFormatException>します。

`-refonly` オプションと [`-refout`](refout-compiler-option.md) オプションは同時に指定できません。

## <a name="see-also"></a>関連項目
[-refout](refout-compiler-option.md)   
[Visual Basic のコマンド ライン コンパイラ](index.md)  
[コンパイル コマンド ラインのサンプル](sample-compilation-command-lines.md)   
