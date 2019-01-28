---
title: -codepage (C# コンパイラ オプション)
ms.date: 07/20/2015
f1_keywords:
- /codepage
helpviewer_keywords:
- /codepage compiler option [C#]
- codepage compiler option [C#]
- -codepage compiler option [C#]
ms.assetid: 75942989-b69a-4308-90a0-840c73d2c478
ms.openlocfilehash: 7cbd3ec1b2d134106c6c9429341f5603444dac27
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54693981"
---
# <a name="-codepage-c-compiler-options"></a>-codepage (C# コンパイラ オプション)
このオプションでは、必要とするページが、システムで使用されている現在の既定のコードページでない場合に、コンパイル時に使用するコード ページを指定します。  
  
## <a name="syntax"></a>構文  
  
```console  
-codepage:id  
```  
  
## <a name="arguments"></a>引数  
 `id`  
 コンパイル時にすべてのソース コード ファイルで使うコード ページの ID です。  
  
## <a name="remarks"></a>コメント  
 コンピューターの既定のコード ページを使わずに作成されたソース コード ファイルをコンパイルする場合は、**-codepage** オプションで、使用するコード ページを指定できます。 **-codepage** は、コンパイル時にすべてのソース コード ファイルに適用されます。  
  
 ソース コード ファイルが、コンピューターで有効なコード ページと同じものを使って作成された場合、または UNICODE か UTF-8 で作成された場合、**-codepage** を使う必要はありません。  
  
 使用しているシステムでサポートされているコード ページを確認する方法については、[GetCPInfo](/windows/desktop/api/winnls/nf-winnls-getcpinfo) に関するページをご覧ください。  
  
 このコンパイラ オプションは Visual Studio では使用できず、プログラムで変更することはできません。  
  
## <a name="see-also"></a>関連項目

- [C# コンパイラ オプション](../../../csharp/language-reference/compiler-options/index.md)
- [プロジェクトおよびソリューションのプロパティの管理](/visualstudio/ide/managing-project-and-solution-properties)
