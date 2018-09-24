---
title: '##pragma checksum (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '#pragma checksum'
helpviewer_keywords:
- '#pragma checksum [C#]'
ms.assetid: 3673e4ca-6098-4ec1-890f-8fceb2a794a2
ms.openlocfilehash: 28a9ccfb9d36e648304a177294904ab1b7f18892
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2018
ms.locfileid: "47027176"
---
# <a name="pragma-checksum-c-reference"></a><span data-ttu-id="b7d55-102">#pragma checksum (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="b7d55-102">#pragma checksum (C# Reference)</span></span>
<span data-ttu-id="b7d55-103">[!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] ページのデバッグに使用するソース ファイルのチェックサムを生成します。</span><span class="sxs-lookup"><span data-stu-id="b7d55-103">Generates checksums for source files to aid with debugging [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] pages.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7d55-104">構文</span><span class="sxs-lookup"><span data-stu-id="b7d55-104">Syntax</span></span>  
  
```csharp
#pragma checksum "filename" "{guid}" "checksum bytes"  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b7d55-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b7d55-105">Parameters</span></span>  
 `"filename"`  
 <span data-ttu-id="b7d55-106">変更または更新を監視する必要があるファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="b7d55-106">The name of the file that requires monitoring for changes or updates.</span></span>  
  
 `"{guid}"`  
 <span data-ttu-id="b7d55-107">ハッシュ アルゴリズムのグローバル一意識別子 (GUID)。</span><span class="sxs-lookup"><span data-stu-id="b7d55-107">The Globally Unique Identifier (GUID) for the hash algorithm.</span></span>  
  
 `"checksum_bytes"`  
 <span data-ttu-id="b7d55-108">チェックサムのバイト数を表す 16 進数の文字列。</span><span class="sxs-lookup"><span data-stu-id="b7d55-108">The string of hexadecimal digits representing the bytes of the checksum.</span></span> <span data-ttu-id="b7d55-109">偶数の 16 進数である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7d55-109">Must be an even number of hexadecimal digits.</span></span> <span data-ttu-id="b7d55-110">奇数の数値を指定すると、コンパイル時に警告が出力され、ディレクティブが無視されます。</span><span class="sxs-lookup"><span data-stu-id="b7d55-110">An odd number of digits results in a compile-time warning, and the directive are ignored.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b7d55-111">コメント</span><span class="sxs-lookup"><span data-stu-id="b7d55-111">Remarks</span></span>  
 <span data-ttu-id="b7d55-112">Visual Studio デバッガーは、常に正しいソースを検出するために、チェックサムを使用します。</span><span class="sxs-lookup"><span data-stu-id="b7d55-112">The Visual Studio debugger uses a checksum to make sure  that it always finds the right source.</span></span> <span data-ttu-id="b7d55-113">コンパイラはソース ファイルのチェックサムを計算し、プログラム データベース (PDB) ファイルに結果を出力します。</span><span class="sxs-lookup"><span data-stu-id="b7d55-113">The compiler computes the checksum for a source file, and then emits the output to the program database (PDB) file.</span></span> <span data-ttu-id="b7d55-114">デバッガーは、その PDB ファイルを使用して、ソース ファイルについて計算したチェックサムと比較します。</span><span class="sxs-lookup"><span data-stu-id="b7d55-114">The debugger then uses the PDB to compare against the checksum that it computes for the source file.</span></span>  
  
 <span data-ttu-id="b7d55-115">このソリューションは [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] プロジェクトには使用できません。それは計算されたチェックサムは、.aspx ファイルではなく、生成されたソース ファイルを対象としているためです。</span><span class="sxs-lookup"><span data-stu-id="b7d55-115">This solution does not work for [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] projects, because the computed checksum is for the generated source file, rather than the .aspx file.</span></span> <span data-ttu-id="b7d55-116">この問題に対応するため、`#pragma checksum` によって [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] ページのチェックサムがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b7d55-116">To address this problem, `#pragma checksum` provides checksum support for [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] pages.</span></span>  
  
 <span data-ttu-id="b7d55-117">Visual C# で [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] プロジェクトを作成すると、生成されるソース ファイルにソースの生成元である .aspx ファイルのチェックサムが含められます。</span><span class="sxs-lookup"><span data-stu-id="b7d55-117">When you create an [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] project in Visual C#, the generated source file contains a checksum for the .aspx file, from which the source is generated.</span></span> <span data-ttu-id="b7d55-118">コンパイラは、この情報を PDB ファイルに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="b7d55-118">The compiler then writes this information into the PDB file.</span></span>  
  
 <span data-ttu-id="b7d55-119">ファイルに `#pragma checksum` ディレクティブが見つからない場合、コンパイラはチェックサムを計算し、PDB ファイルにその値を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="b7d55-119">If the compiler encounters no `#pragma checksum` directive in the file, it computes the checksum and writes the value to the PDB file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b7d55-120">例</span><span class="sxs-lookup"><span data-stu-id="b7d55-120">Example</span></span>  
  
```csharp
class TestClass  
{  
    static int Main()  
    {  
        #pragma checksum "file.cs" "{406EA660-64CF-4C82-B6F0-42D48172A799}" "ab007f1d23d9" // New checksum  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="b7d55-121">参照</span><span class="sxs-lookup"><span data-stu-id="b7d55-121">See Also</span></span>

- [<span data-ttu-id="b7d55-122">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="b7d55-122">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="b7d55-123">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="b7d55-123">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="b7d55-124">C# プリプロセッサ ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="b7d55-124">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
