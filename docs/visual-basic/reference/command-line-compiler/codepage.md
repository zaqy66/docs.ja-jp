---
title: -codepage (Visual Basic)
ms.date: 03/09/2018
helpviewer_keywords:
- -codepage compiler option [Visual Basic]
- codepage compiler option [Visual Basic]
- -codepage compiler option [Visual Basic]
ms.assetid: be36ec33-6800-4505-838c-4124564f5cc9
ms.openlocfilehash: 8aee51df3ba9f92ca662fbbfbd73998e4a3b4538
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43405697"
---
# <a name="-codepage-visual-basic"></a>-codepage (Visual Basic)
コンパイルですべてのソース コード ファイルに使用するコード ページを指定します。  
  
## <a name="syntax"></a>構文  
  
```  
-codepage:id  
```  
  
## <a name="arguments"></a>引数  
  
|用語|定義|  
|---|---|  
|`id`|必須。 コンパイラで指定されたコード ページを使用して`id`ソース ファイルのエンコーディングを解釈します。|  
  
## <a name="remarks"></a>Remarks  
 使用することが特定のエンコーディングで保存されたソース コードをコンパイルする`-codepage`コード ページを使用する必要がありますを指定します。 `-codepage`オプションは、コンパイル時にすべてのソース コード ファイルに適用されます。 詳細については、次を参照してください。 [.NET Framework における文字エンコーディング](https://msdn.microsoft.com/library/bf6d9823-4c2d-48af-b280-919c5af66ae9)します。  
  
 `-codepage`オプションは、シグネチャを持つ現在の ANSI コード ページ、Unicode または utf-8 を使用して、ソース コード ファイルを保存した場合は必要ありません。 Visual Studio に保存既定では、すべてのソース コード ファイルが現在の ANSI コード ページで、ユーザーで別のエンコードを指定しない限り、**エンコード** ダイアログ ボックス。 Visual Studio を使用して、**エンコード**異なるコード ページで保存されたソース コード ファイルを開く ダイアログ ボックス。  
  
> [!NOTE]
>  `-codepage`オプションは、Visual Studio 開発環境内からは使用できません。 コマンドラインからコンパイルする場合にのみ使用可能なです。  
  
## <a name="see-also"></a>関連項目  
 [Visual Basic のコマンド ライン コンパイラ](../../../visual-basic/reference/command-line-compiler/index.md)
