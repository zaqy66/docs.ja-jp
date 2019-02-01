---
title: '方法: 文字列への文字の書き込み'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data streams, writing characters to string
- writing characters to strings
- streams, writing characters to strings
- I/O [.NET Framework], writing characters to strings
ms.assetid: 1222cbeb-0760-44bf-9888-914a2a37174b
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 125c8ba03c4d1006535dd1e10cbd162b32fede4f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54740984"
---
# <a name="how-to-write-characters-to-a-string"></a>方法: 文字列への文字の書き込み
次のコード例では、文字列の配列から同期および非同期的に文字が書き込まれます。  
  
## <a name="example"></a>例  
 次の例では、配列から文字列へ 5 文字が同期的に書き込まれます。  
  
 [!code-csharp[Conceptual.StringBuilder#9](../../../samples/snippets/csharp/VS_Snippets_CLR/Conceptual.StringBuilder/cs/example2.cs#9)]
 [!code-vb[Conceptual.StringBuilder#9](../../../samples/snippets/visualbasic/VS_Snippets_CLR/Conceptual.StringBuilder/vb/example2.vb#9)]  
  
## <a name="example"></a>例  
 次の例では、<xref:System.Windows.Controls.TextBox> コントロールから非同期的にすべての文字を読み取り、配列に格納します。 次に、<xref:System.Windows.Controls.TextBlock> コントロールへの改行が続く個別の行に、各文字または空白文字を非同期的に書き込みます。  
  
 [!code-csharp[Conceptual.StringReader#2](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.stringreader/cs/source2.cs#2)]
 [!code-vb[Conceptual.StringReader#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.stringreader/vb/source2.vb#2)]  
  
## <a name="see-also"></a>関連項目

- <xref:System.IO.StringWriter>
- <xref:System.IO.StringWriter.Write%2A?displayProperty=nameWithType>
- <xref:System.Text.StringBuilder>
- [ファイルおよびストリーム入出力](../../../docs/standard/io/index.md)
- [Asynchronous File I/O](../../../docs/standard/io/asynchronous-file-i-o.md)
- [方法: ディレクトリとファイルを列挙する](../../../docs/standard/io/how-to-enumerate-directories-and-files.md)
- [方法: 新しく作成されたデータ ファイルに対して読み書きする](../../../docs/standard/io/how-to-read-and-write-to-a-newly-created-data-file.md)
- [方法: ログ ファイルを開いて情報を追加する](../../../docs/standard/io/how-to-open-and-append-to-a-log-file.md)
- [方法: ファイルからのテキストの読み取り](../../../docs/standard/io/how-to-read-text-from-a-file.md)
- [方法: テキストのファイルへの書き込み](../../../docs/standard/io/how-to-write-text-to-a-file.md)
- [方法: 文字列からの文字の読み取り](../../../docs/standard/io/how-to-read-characters-from-a-string.md)
