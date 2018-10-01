---
title: ローカリゼーション
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- culture, localization
- application development [.NET Framework], localization
- globalization [.NET Framework], localization
- code blocks
- international applications [.NET Framework], localization
- global applications, localization
- world-ready applications, localization
- user interface blocks
- localization [.NET Framework], about localization
- localizing resources
ms.assetid: 49d520d7-92d7-44ee-bb24-8b615db1d41b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ee7de15130644e63b17a6d067c5cce9088d199a0
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2018
ms.locfileid: "47236463"
---
# <a name="localization"></a>ローカリゼーション
ローカリゼーションはアプリケーションのリソースを翻訳するプロセスであり、そのアプリケーションで対応するカルチャ別のバージョンが作られます。 [ローカライズ化の確認](../../../docs/standard/globalization-localization/localizability-review.md)手順で世界展開するアプリケーションがローカライズ可能であることを確認してから、ローカリゼーション手順に進んでください。  
  
 ローカライズ可能なアプリケーションは、概念的に 2 つのブロックに分けられます。すべてのユーザー インターフェイス要素を含むブロックと実行可能なコードを含むブロックです。 ユーザー インターフェイス ブロックには、ローカライズ可能なユーザー インターフェイス要素のみが含まれます。ニュートラル カルチャの場合、文字列、エラー メッセージ、ダイアログ ボックス、メニュー、埋め込みオブジェクト リソースなどです。 コード ブロックには、すべての対応カルチャで使用されるアプリケーション コードのみが含まれます。 共通言語ランタイムは、アプリケーションの実行可能コードをそのリソースから分離させるサテライト アセンブリ リソース モデルに対応しています。 このモデルの実装方法については、「[デスクトップ アプリケーションのリソース](../../../docs/framework/resources/index.md)」を参照してください。  
  
 アプリケーションのローカライズ バージョンごとに、ターゲット カルチャの言語に翻訳されたユーザー インターフェイス ブロックを含む新しいサテライト アセンブリを追加します。 すべてのカルチャのコード ブロックを同じにしてください。 ユーザー インターフェイス ブロックのローカライズされたバージョンとコード ブロックを組み合わせることで、アプリケーションのローカライズ バージョンが作られます。  
  
 [!INCLUDE[winsdklong](../../../includes/winsdklong-md.md)] には Windows フォーム リソース エディター (Winres.exe) があります。このエディターでは、ターゲット カルチャに合わせて Windows フォームを簡単にローカライズできます。 このツールの使用方法については、「[Winres.exe (Windows フォーム リソース エディター)](../../../docs/framework/tools/winres-exe-windows-forms-resource-editor.md)」を参照してください。  
  
## <a name="see-also"></a>関連項目

- [グローバライズとローカライズ](../../../docs/standard/globalization-localization/index.md)  
- [ローカライズ化の確認](../../../docs/standard/globalization-localization/localizability-review.md)  
- [グローバリゼーション](../../../docs/standard/globalization-localization/globalization.md)  
- [デスクトップ アプリケーションのリソース](../../../docs/framework/resources/index.md)
