---
title: '方法 : ディレクトリをコピーする'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- directory copying
- I/O [.NET Framework], copying directories
- subdirectory copying
- copying directories
- directories [.NET Framework], copying
ms.assetid: 5a969765-e5f8-4b4e-977e-90e2b0a1fe3c
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6f2c2fbd58b10af80a2a233cbd4211befe2dbd33
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44216055"
---
# <a name="how-to-copy-directories"></a>方法 : ディレクトリをコピーする
この例では、I/O クラスを使用して、別の場所にディレクトリの内容を同期的にコピーする方法について説明します。 ユーザーは、サブディレクトリもコピーするかどうかを指定できます。 サブディレクトリをコピーする場合、この例で使用するメソッドは、コピーするディレクトリがなくなるまで、各サブディレクトリ上で自身を呼び出し、再帰的にコピーを行います。  
  
 ファイルを非同期的にコピーする例については、「 [Asynchronous File I/O](../../../docs/standard/io/asynchronous-file-i-o.md)」を参照してください。  
  
## <a name="example"></a>例  
 [!code-csharp[System.IO.Directory_Copy#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.IO.Directory_Copy/cs/program.cs#1)]
 [!code-vb[System.IO.Directory_Copy#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.IO.Directory_Copy/vb/Program.vb#1)]  
  
## <a name="see-also"></a>関連項目

- <xref:System.IO.FileInfo>  
- <xref:System.IO.DirectoryInfo>  
- <xref:System.IO.FileStream>  
- [ファイルおよびストリーム入出力](../../../docs/standard/io/index.md)  
- [共通 I/O タスク](../../../docs/standard/io/common-i-o-tasks.md)  
- [非同期ファイル I/O](../../../docs/standard/io/asynchronous-file-i-o.md)
