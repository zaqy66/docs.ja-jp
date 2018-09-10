---
title: '方法: ディレクトリとファイルを列挙する'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- I/O [.NET Framework], enumerating directories and files
ms.assetid: 86b69a08-3bfa-4e5f-b4e1-3b7cb8478215
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3de83395df9e8c89a92e85b96ddd15e9f0be6ad5
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2018
ms.locfileid: "44207695"
---
# <a name="how-to-enumerate-directories-and-files"></a><span data-ttu-id="57ab8-102">方法: ディレクトリとファイルを列挙する</span><span class="sxs-lookup"><span data-stu-id="57ab8-102">How to: Enumerate Directories and Files</span></span>
<span data-ttu-id="57ab8-103">名前の文字列の列挙可能なコレクションを返すメソッドを使用して、ディレクトリとファイルを列挙することができます。</span><span class="sxs-lookup"><span data-stu-id="57ab8-103">You can enumerate directories and files by using methods that return an enumerable collection of strings of their names.</span></span> <span data-ttu-id="57ab8-104"><xref:System.IO.DirectoryInfo>、<xref:System.IO.FileInfo>、または <xref:System.IO.FileSystemInfo> オブジェクトの列挙可能なコレクションを返すメソッドを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="57ab8-104">You can also use methods that return an enumerable collection of <xref:System.IO.DirectoryInfo>, <xref:System.IO.FileInfo>, or <xref:System.IO.FileSystemInfo> objects.</span></span> <span data-ttu-id="57ab8-105">列挙可能なコレクションでは、ディレクトリとファイルの大きなコレクションを操作する際に配列よりも優れたパフォーマンスが得られます。</span><span class="sxs-lookup"><span data-stu-id="57ab8-105">Enumerable collections provide better performance than arrays when you work with large collections of directories and files.</span></span>  
  
 <span data-ttu-id="57ab8-106">これらのメソッドから取得される列挙可能なコレクションを使用して、<xref:System.Collections.Generic.List%601> クラスなどのコレクション クラスのコンストラクターに対して <xref:System.Collections.Generic.IEnumerable%601> パラメーターを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="57ab8-106">You can also use enumerable collections obtained from these methods to supply the <xref:System.Collections.Generic.IEnumerable%601> parameter for constructors of collection classes such as the <xref:System.Collections.Generic.List%601> class.</span></span>  
  
 <span data-ttu-id="57ab8-107">ディレクトリまたはファイルの名前のみを取得する場合は、<xref:System.IO.Directory> クラスの列挙メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="57ab8-107">If you want to obtain only the names of directories or files, use the enumeration methods of the <xref:System.IO.Directory> class.</span></span> <span data-ttu-id="57ab8-108">ディレクトリまたはファイルの他のプロパティを取得する場合は、<xref:System.IO.DirectoryInfo> および <xref:System.IO.FileSystemInfo> クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="57ab8-108">If you want to obtain other properties of directories or files, use the <xref:System.IO.DirectoryInfo> and <xref:System.IO.FileSystemInfo> classes.</span></span>  
  
 <span data-ttu-id="57ab8-109">次の表では、列挙コレクションを返すメソッドのガイドを提供します。</span><span class="sxs-lookup"><span data-stu-id="57ab8-109">The following table provides a guide to the methods that return enumerable collections.</span></span>  
  
|<span data-ttu-id="57ab8-110">列挙対象</span><span class="sxs-lookup"><span data-stu-id="57ab8-110">To enumerate</span></span>|<span data-ttu-id="57ab8-111">返される列挙可能なコレクション</span><span class="sxs-lookup"><span data-stu-id="57ab8-111">Enumerable collection to return</span></span>|<span data-ttu-id="57ab8-112">使用するメソッド</span><span class="sxs-lookup"><span data-stu-id="57ab8-112">Method to use</span></span>|  
|------------------|-------------------------------------|-------------------|  
|<span data-ttu-id="57ab8-113">ディレクトリ</span><span class="sxs-lookup"><span data-stu-id="57ab8-113">Directories</span></span>|<span data-ttu-id="57ab8-114">ディレクトリ名</span><span class="sxs-lookup"><span data-stu-id="57ab8-114">Directory names</span></span>|<xref:System.IO.Directory.EnumerateDirectories%2A?displayProperty=nameWithType>|  
||<span data-ttu-id="57ab8-115">ディレクトリ情報 (<xref:System.IO.DirectoryInfo>)</span><span class="sxs-lookup"><span data-stu-id="57ab8-115">Directory information (<xref:System.IO.DirectoryInfo>)</span></span>|<xref:System.IO.DirectoryInfo.EnumerateDirectories%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="57ab8-116">ファイル</span><span class="sxs-lookup"><span data-stu-id="57ab8-116">Files</span></span>|<span data-ttu-id="57ab8-117">ファイル名</span><span class="sxs-lookup"><span data-stu-id="57ab8-117">File names</span></span>|<xref:System.IO.Directory.EnumerateFiles%2A?displayProperty=nameWithType>|  
||<span data-ttu-id="57ab8-118">ファイル情報 (<xref:System.IO.FileInfo>)</span><span class="sxs-lookup"><span data-stu-id="57ab8-118">File information (<xref:System.IO.FileInfo>)</span></span>|<xref:System.IO.DirectoryInfo.EnumerateFiles%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="57ab8-119">ファイル システム情報</span><span class="sxs-lookup"><span data-stu-id="57ab8-119">File system information</span></span>|<span data-ttu-id="57ab8-120">ファイル システム エントリ</span><span class="sxs-lookup"><span data-stu-id="57ab8-120">File system entries</span></span>|<xref:System.IO.Directory.EnumerateFileSystemEntries%2A?displayProperty=nameWithType>|  
||<span data-ttu-id="57ab8-121">ファイル システム情報 (<xref:System.IO.FileSystemInfo>)</span><span class="sxs-lookup"><span data-stu-id="57ab8-121">File system information (<xref:System.IO.FileSystemInfo>)</span></span>|<xref:System.IO.DirectoryInfo.EnumerateFileSystemInfos%2A?displayProperty=nameWithType>|  
  
 <span data-ttu-id="57ab8-122"><xref:System.IO.SearchOption> 列挙で提供される <xref:System.IO.SearchOption.AllDirectories> 検索オプションを使用して、親ディレクトリのサブディレクトリ内のすべてのファイルをすぐに列挙することはできますが、未承認アクセスの例外 (<xref:System.UnauthorizedAccessException>) によって、列挙が不完全になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="57ab8-122">Although you can immediately enumerate all the files in the subdirectories of a parent directory by using the <xref:System.IO.SearchOption.AllDirectories> search option provided by the <xref:System.IO.SearchOption> enumeration, unauthorized access exceptions (<xref:System.UnauthorizedAccessException>) may cause the enumeration to be incomplete.</span></span> <span data-ttu-id="57ab8-123">このような例外が考えられる場合は、その例外をキャッチして作業を続行します。その場合、最初にディレクトリを列挙してからファイルを列挙します。</span><span class="sxs-lookup"><span data-stu-id="57ab8-123">If these exceptions are possible, you can catch them and continue by first enumerating directories and then enumerating files.</span></span>  
  
### <a name="to-enumerate-directory-names"></a><span data-ttu-id="57ab8-124">ディレクトリ名を列挙するには</span><span class="sxs-lookup"><span data-stu-id="57ab8-124">To enumerate directory names</span></span>  
  
-   <span data-ttu-id="57ab8-125"><xref:System.IO.Directory.EnumerateDirectories%28System.String%29?displayProperty=nameWithType> メソッドを使用して、指定されたパスの最上位レベルのディレクトリ名のリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="57ab8-125">Use the <xref:System.IO.Directory.EnumerateDirectories%28System.String%29?displayProperty=nameWithType> method to obtain a list of the top-level directory names in a specified path.</span></span>  
  
     [!code-csharp[System.IO.EnumDirs1#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.enumdirs1/cs/program.cs#1)]
     [!code-vb[System.IO.EnumDirs1#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.enumdirs1/vb/program.vb#1)]  
  
### <a name="to-enumerate-file-names-in-a-directory-and-subdirectories"></a><span data-ttu-id="57ab8-126">ディレクトリとサブディレクトリ内のファイル名を列挙するには</span><span class="sxs-lookup"><span data-stu-id="57ab8-126">To enumerate file names in a directory and subdirectories</span></span>  
  
-   <span data-ttu-id="57ab8-127"><xref:System.IO.Directory.EnumerateFiles%28System.String%2CSystem.String%2CSystem.IO.SearchOption%29?displayProperty=nameWithType> メソッドを使用して、ディレクトリと (必要に応じて) そのサブディレクトリを検索し、指定された検索パターンに一致するファイル名のリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="57ab8-127">Use the <xref:System.IO.Directory.EnumerateFiles%28System.String%2CSystem.String%2CSystem.IO.SearchOption%29?displayProperty=nameWithType> method to search a directory and (optionally) its subdirectories, and to obtain a list of file names that match a specified search pattern.</span></span>  
  
     [!code-csharp[System.IO.Directory.EnumerateFiles#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.directory.enumeratefiles/cs/program.cs#1)]
     [!code-vb[System.IO.Directory.EnumerateFiles#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.directory.enumeratefiles/vb/program.vb#1)]  
  
### <a name="to-enumerate-a-collection-of-directoryinfo-objects"></a><span data-ttu-id="57ab8-128">DirectoryInfo オブジェクトのコレクションを列挙するには</span><span class="sxs-lookup"><span data-stu-id="57ab8-128">To enumerate a collection of DirectoryInfo objects</span></span>  
  
-   <span data-ttu-id="57ab8-129"><xref:System.IO.DirectoryInfo.EnumerateDirectories%2A?displayProperty=nameWithType> メソッドを使用して、最上位レベルのディレクトリのコレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="57ab8-129">Use the <xref:System.IO.DirectoryInfo.EnumerateDirectories%2A?displayProperty=nameWithType> method to obtain a collection of top-level directories.</span></span>  
  
     [!code-csharp[System.IO.DirectoryInfo.EnumDirs#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.directoryinfo.enumdirs/cs/program.cs#1)]
     [!code-vb[System.IO.DirectoryInfo.EnumDirs#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.directoryinfo.enumdirs/vb/module1.vb#1)]  
  
### <a name="to-enumerate-a-collection-of-fileinfo-objects-in-all-directories"></a><span data-ttu-id="57ab8-130">すべてのディレクトリ内の FileInfo オブジェクトのコレクションを列挙するには</span><span class="sxs-lookup"><span data-stu-id="57ab8-130">To enumerate a collection of FileInfo objects in all directories</span></span>  
  
-   <span data-ttu-id="57ab8-131"><xref:System.IO.DirectoryInfo.EnumerateFiles%2A?displayProperty=nameWithType> メソッドを使用して、すべてのディレクトリ内の指定された検索パターンに一致するファイルのコレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="57ab8-131">Use the <xref:System.IO.DirectoryInfo.EnumerateFiles%2A?displayProperty=nameWithType> method to obtain a collection of files that match a specified search pattern in all directories.</span></span> <span data-ttu-id="57ab8-132">この例では、まず、最上位レベルのディレクトリを列挙して考えられる未承認アクセス例外をキャッチしてから、ファイルを列挙します。</span><span class="sxs-lookup"><span data-stu-id="57ab8-132">This example first enumerates the top-level directories to catch possible unauthorized access exceptions, and then enumerates the files.</span></span>  
  
     [!code-csharp[System.IO.DirectoryInfo.EnumerateDirectories#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.io.directoryinfo.enumeratedirectories/cs/program.cs#1)]
     [!code-vb[System.IO.DirectoryInfo.EnumerateDirectories#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.directoryinfo.enumeratedirectories/vb/program.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="57ab8-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="57ab8-133">See also</span></span>

- [<span data-ttu-id="57ab8-134">ファイルおよびストリーム入出力</span><span class="sxs-lookup"><span data-stu-id="57ab8-134">File and Stream I/O</span></span>](../../../docs/standard/io/index.md)
