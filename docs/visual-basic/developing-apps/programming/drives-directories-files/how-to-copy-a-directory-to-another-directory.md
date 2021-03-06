---
title: '方法: Visual Basic でディレクトリを別のディレクトリにコピーする'
ms.date: 07/20/2015
helpviewer_keywords:
- I/O [Visual Basic], copying directories
- I/O [Visual Basic], copying folders
- folders [Visual Basic], copying
- directories [Visual Basic], copying
ms.assetid: 2a370bd7-10ba-4219-afc4-4519d031eb6c
ms.openlocfilehash: 25919e0256b967f59bd98d20e75d159e018ac954
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54594747"
---
# <a name="how-to-copy-a-directory-to-another-directory-in-visual-basic"></a>方法: Visual Basic でディレクトリを別のディレクトリにコピーする
ディレクトリを別のディレクトリにコピーするには、<xref:Microsoft.VisualBasic.FileIO.FileSystem.CopyDirectory%2A> メソッドを使用します。 このメソッドでは、ディレクトリ自体とその内容がコピーされます。 コピー先のディレクトリが存在しない場合は作成されます。 コピー先の場所に同じ名前のディレクトリが存在し、`overwrite` が `False` に設定されている場合は、2 つのディレクトリの内容がマージされます。 操作中に、ディレクトリに新しい名前を指定できます。  
  
 ディレクトリ内でファイルをコピーするとき、特定のファイルが原因で例外がスローされることがあります。たとえば、`overwrite` が `False` に設定されていて、マージ中に、既にファイルが存在する場合などです。 こうしてスローされた例外は、単一の例外に統合され、その `Data` プロパティにエントリが保持されます。それらのエントリでは、ファイルまたはディレクトリ パスがキーとなり、固有の例外メッセージがそれに対応した値に格納されます。  
  
### <a name="to-copy-a-directory-to-another-directory"></a>ディレクトリを別のディレクトリにコピーするには  
  
-   `CopyDirectory` メソッドを使用し、コピー元とコピー先のディレクトリ名を指定します。 次の例では、`TestDirectory1` という名前のディレクトリを `TestDirectory2` にコピーし、既存のファイルは上書きします。  
  
     [!code-vb[VbVbcnMyFileSystem#16](../../../../visual-basic/developing-apps/programming/drives-directories-files/codesnippet/VisualBasic/how-to-copy-a-directory-to-another-directory_1.vb)]  
  
     このコード例は、IntelliSense コード スニペットとしても利用できます。 コード スニペット ピッカーでは、コード例は **[ファイル システム - ドライブ、フォルダー、およびファイルの処理]** にあります。 詳細については、「[Code Snippets](/visualstudio/ide/code-snippets)」を参照してください。  
  
## <a name="robust-programming"></a>信頼性の高いプログラミング  
 次の条件を満たす場合は、例外が発生する可能性があります。  
  
-   ディレクトリに指定された新しい名前にコロン (:) またはスラッシュ (\ または /) が含まれている (<xref:System.ArgumentException>)。  
  
-   パスが正しくない。長さが 0 の文字列である、空白だけが含まれている、使用できない文字が含まれている、デバイス パスである (先頭が \\\\.\\)、のいずれかの理由が考えられる (<xref:System.ArgumentException>)。  
  
-   パスが `Nothing` であるため、有効でない (<xref:System.ArgumentNullException>)  
  
-   `destinationDirectoryName` が `Nothing` または空の文字列である (<xref:System.ArgumentNullException>)。  
  
-   ソース ディレクトリが存在しない (<xref:System.IO.DirectoryNotFoundException>)。  
  
-   ソース ディレクトリがルート ディレクトリである (<xref:System.IO.IOException>)。  
  
-   パスを組み合わせると、既存のファイルと同じになる (<xref:System.IO.IOException>)。  
  
-   コピー元のパスとコピー先のパスが同じである (<xref:System.IO.IOException>)。  
  
-   `ShowUI` が `UIOption.AllDialogs` に設定されており、ユーザーが操作をキャンセルした、またはディレクトリ内の 1 つ以上のファイルをコピーできなかった (<xref:System.OperationCanceledException>)。  
  
-   操作が循環している (<xref:System.InvalidOperationException>)。  
  
-   パスにコロン (:) が含まれている (<xref:System.NotSupportedException>)。  
  
-   パスがシステムで定義されている最大長を超えている (<xref:System.IO.PathTooLongException>)。  
  
-   パス内のファイル名またはフォルダー名にコロン (:) が含まれている、または形式が無効である (<xref:System.NotSupportedException>)。  
  
-   ユーザーがパスを参照するのに必要なアクセス許可がない (<xref:System.Security.SecurityException>)  
  
-   コピー先のファイルは存在するが、アクセスできない (<xref:System.UnauthorizedAccessException>)。  
  
## <a name="see-also"></a>関連項目
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.CopyDirectory%2A>
- [方法: 特定のパターンに一致するサブディレクトリを検索する](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-find-subdirectories-with-a-specific-pattern.md)
- [方法: ディレクトリにあるファイルのコレクションを取得する](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-get-the-collection-of-files-in-a-directory.md)
