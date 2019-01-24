---
title: バイト配列に読み取るにはファイルが大きすぎます。
ms.date: 07/20/2015
ms.assetid: 686630a6-a439-46c7-8d7b-34613ae4c5d8
ms.openlocfilehash: 90db5214ff26cfacf3a832c904d742c9caf853d6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54728936"
---
# <a name="file-is-too-large-to-read-into-a-byte-array"></a><span data-ttu-id="511c3-102">バイト配列に読み取るにはファイルが大きすぎます。</span><span class="sxs-lookup"><span data-stu-id="511c3-102">File is too large to read into a byte array</span></span>
<span data-ttu-id="511c3-103">バイト配列に読み取るしようとするファイルのサイズが 4 GB を超えています。</span><span class="sxs-lookup"><span data-stu-id="511c3-103">The size of the file you are attempting to read into a byte array exceeds 4 GB.</span></span> <span data-ttu-id="511c3-104">`My.Computer.FileSystem.ReadAllBytes`メソッドは、このサイズを超えるファイルを読み取ることができません。</span><span class="sxs-lookup"><span data-stu-id="511c3-104">The `My.Computer.FileSystem.ReadAllBytes` method cannot read a file that exceeds this size.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="511c3-105">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="511c3-105">To correct this error</span></span>  
  
-   <span data-ttu-id="511c3-106">使用して、<xref:System.IO.StreamReader>ファイルを読み取れません。</span><span class="sxs-lookup"><span data-stu-id="511c3-106">Use a <xref:System.IO.StreamReader> to read the file.</span></span> <span data-ttu-id="511c3-107">詳細については、次を参照してください。 [.NET Framework ファイル I/O の基礎と、ファイル システム (Visual Basic)](../../../visual-basic/developing-apps/programming/drives-directories-files/basics-of-net-framework-file-io-and-the-file-system.md)します。</span><span class="sxs-lookup"><span data-stu-id="511c3-107">For more information, see [Basics of .NET Framework File I/O and the File System (Visual Basic)](../../../visual-basic/developing-apps/programming/drives-directories-files/basics-of-net-framework-file-io-and-the-file-system.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="511c3-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="511c3-108">See also</span></span>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.ReadAllBytes%2A>
- <xref:System.IO.StreamReader>
- [<span data-ttu-id="511c3-109">Visual Basic におけるファイル アクセス</span><span class="sxs-lookup"><span data-stu-id="511c3-109">File Access with Visual Basic</span></span>](../../../visual-basic/developing-apps/programming/drives-directories-files/file-access.md)
- [<span data-ttu-id="511c3-110">方法: StreamReader を使用してファイルからテキストを読み取る</span><span class="sxs-lookup"><span data-stu-id="511c3-110">How to: Read Text from Files with a StreamReader</span></span>](../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-text-from-files-with-a-streamreader.md)
