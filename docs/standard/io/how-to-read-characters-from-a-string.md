---
title: '方法 : 文字列から文字を読み取る'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- reading characters from strings
- data streams, reading characters from string
- I/O [.NET Framework], reading characters from strings
- reading data, strings
- streams, reading characters from string
ms.assetid: 27ea5e52-6db8-42d8-980a-50bcfc7fd270
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 13a57f8ea7db91e5357ecfb20c4e907f2706f78d
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2018
ms.locfileid: "45592920"
---
# <a name="how-to-read-characters-from-a-string"></a>方法 : 文字列から文字を読み取る
次のコード例は、文字列から同期で文字を読み取る方法と非同期で文字を読み取る方法を示しています。  
  
## <a name="example"></a>例  
 この例では、文字列から同期的に 13 文字を読み取り、配列に格納し、これらの文字を表示します。 次に、文字列の残りの文字を読み取り、6 番目の要素で始まる配列に格納し、配列の内容を表示します。  
  
 [!code-cpp[Conceptual.StringReader#1](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.stringreader/cpp/source.cpp#1)]
 [!code-csharp[Conceptual.StringReader#1](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.stringreader/cs/source.cs#1)]
 [!code-vb[Conceptual.StringReader#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.stringreader/vb/source.vb#1)]  
  
## <a name="example"></a>例  
 次の例では、<xref:System.Windows.Controls.TextBox> コントロールから非同期的にすべての文字を読み取り、配列に格納します。 次に、<xref:System.Windows.Controls.TextBlock> コントロールへの改行が続く個別の行に、各文字または空白文字を非同期的に書き込みます。  
  
 [!code-csharp[Conceptual.StringReader#2](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.stringreader/cs/source2.cs#2)]
 [!code-vb[Conceptual.StringReader#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.stringreader/vb/source2.vb#2)]  
  
## <a name="see-also"></a>関連項目

- <xref:System.IO.StringReader>  
- <xref:System.IO.StringReader.Read%2A?displayProperty=nameWithType>  
- [非同期ファイル I/O](../../../docs/standard/io/asynchronous-file-i-o.md)  
- [NIB: 方法: ディレクトリ一覧を作成する](https://msdn.microsoft.com/library/4d2772b1-b991-4532-a8a6-6ef733277e69)  
- [方法: 新しく作成されたデータ ファイルに対して読み書きする](../../../docs/standard/io/how-to-read-and-write-to-a-newly-created-data-file.md)  
- [方法: ログ ファイルを開いて情報を追加する](../../../docs/standard/io/how-to-open-and-append-to-a-log-file.md)  
- [方法: ファイルからテキストを読み取る](../../../docs/standard/io/how-to-read-text-from-a-file.md)  
- [方法: ファイルにテキストを書き込む](../../../docs/standard/io/how-to-write-text-to-a-file.md)  
- [方法: 文字列に文字を書き込む](../../../docs/standard/io/how-to-write-characters-to-a-string.md)  
- [ファイルおよびストリーム入出力](../../../docs/standard/io/index.md)
