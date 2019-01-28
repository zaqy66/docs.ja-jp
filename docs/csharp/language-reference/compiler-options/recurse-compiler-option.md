---
title: -recurse (C# コンパイラ オプション)
ms.date: 07/20/2015
f1_keywords:
- /recurse
helpviewer_keywords:
- /recurse compiler option [C#]
- recurse compiler option [C#]
- -recurse compiler option [C#]
ms.assetid: 4e8212e5-04e3-45b1-8a42-41bc50e683b0
ms.openlocfilehash: a4a55090cf465d0eac05303392ba7500dd96ee90
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54679371"
---
# <a name="-recurse-c-compiler-options"></a><span data-ttu-id="a01c2-102">-recurse (C# コンパイラ オプション)</span><span class="sxs-lookup"><span data-stu-id="a01c2-102">-recurse (C# Compiler Options)</span></span>
<span data-ttu-id="a01c2-103">-recurse オプションを使用すると、指定のディレクトリ (dir) またはプロジェクト ディレクトリのすべての子ディレクトリ内のソース コード ファイルをコンパイルできます。</span><span class="sxs-lookup"><span data-stu-id="a01c2-103">The -recurse option enables you to compile source code files in all child directories of either the specified directory (dir) or of the project directory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a01c2-104">構文</span><span class="sxs-lookup"><span data-stu-id="a01c2-104">Syntax</span></span>  
  
```console  
-recurse:[dir\]file  
```  
  
## <a name="arguments"></a><span data-ttu-id="a01c2-105">引数</span><span class="sxs-lookup"><span data-stu-id="a01c2-105">Arguments</span></span>  
 <span data-ttu-id="a01c2-106">`dir` (省略可能)</span><span class="sxs-lookup"><span data-stu-id="a01c2-106">`dir` (optional)</span></span>  
 <span data-ttu-id="a01c2-107">検索を開始するディレクトリ。</span><span class="sxs-lookup"><span data-stu-id="a01c2-107">The directory in which you want the search to begin.</span></span> <span data-ttu-id="a01c2-108">指定しない場合は、プロジェクト ディレクトリから検索されます。</span><span class="sxs-lookup"><span data-stu-id="a01c2-108">If this is not specified, the search begins in the project directory.</span></span>  
  
 `file`  
 <span data-ttu-id="a01c2-109">検索するファイル。</span><span class="sxs-lookup"><span data-stu-id="a01c2-109">The file(s) to search for.</span></span> <span data-ttu-id="a01c2-110">ワイルドカード文字を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a01c2-110">Wildcard characters are allowed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a01c2-111">コメント</span><span class="sxs-lookup"><span data-stu-id="a01c2-111">Remarks</span></span>  
 <span data-ttu-id="a01c2-112">**-recurse** オプションを使用すると、指定のディレクトリ (`dir`) またはプロジェクト ディレクトリのすべての子ディレクトリ内のソース コード ファイルをコンパイルできます。</span><span class="sxs-lookup"><span data-stu-id="a01c2-112">The **-recurse** option lets you compile source code files in all child directories of either the specified directory (`dir`) or of the project directory.</span></span>  
  
 <span data-ttu-id="a01c2-113">**-recurse** を使用しなくても、ファイル名にワイルドカードを使用すると、プロジェクト ディレクトリ内で一致するすべてのファイルをコンパイルできます。</span><span class="sxs-lookup"><span data-stu-id="a01c2-113">You can use wildcards in a file name to compile all matching files in the project directory without using **-recurse**.</span></span>  
  
 <span data-ttu-id="a01c2-114">このコンパイラ オプションは Visual Studio では使用できず、プログラムで変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="a01c2-114">This compiler option is unavailable in Visual Studio and cannot be changed programmatically.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a01c2-115">例</span><span class="sxs-lookup"><span data-stu-id="a01c2-115">Example</span></span>  
 <span data-ttu-id="a01c2-116">現在のディレクトリ内のすべての C# ファイルをコンパイルするには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="a01c2-116">Compiles all C# files in the current directory:</span></span>  
  
```console  
csc *.cs  
```  
  
 <span data-ttu-id="a01c2-117">dir1\dir2 ディレクトリおよびそのディレクトリの下の全ディレクトリ内の C# ファイルすべてをコンパイルし、dir2.dll を生成するには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="a01c2-117">Compiles all of the C# files in the dir1\dir2 directory and any directories below it and generates dir2.dll:</span></span>  
  
```console  
csc -target:library -out:dir2.dll -recurse:dir1\dir2\*.cs  
```  
  
## <a name="see-also"></a><span data-ttu-id="a01c2-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="a01c2-118">See also</span></span>

- [<span data-ttu-id="a01c2-119">C# コンパイラ オプション</span><span class="sxs-lookup"><span data-stu-id="a01c2-119">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
- [<span data-ttu-id="a01c2-120">プロジェクトおよびソリューションのプロパティの管理</span><span class="sxs-lookup"><span data-stu-id="a01c2-120">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
