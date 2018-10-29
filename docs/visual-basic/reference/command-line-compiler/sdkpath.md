---
title: -sdkpath
ms.date: 07/20/2015
f1_keywords:
- sdkpath
- -sdkpath
helpviewer_keywords:
- -sdkpath compiler option [Visual Basic]
- /sdkpath compiler option [Visual Basic]
- sdkpath compiler option [Visual Basic]
ms.assetid: fec8a3f1-b791-4a37-8af7-344859f8212d
ms.openlocfilehash: bf665082f079901ec45122ce7797090b7519fafe
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50200850"
---
# <a name="-sdkpath"></a><span data-ttu-id="2faa8-102">-sdkpath</span><span class="sxs-lookup"><span data-stu-id="2faa8-102">-sdkpath</span></span>
<span data-ttu-id="2faa8-103">Mscorlib.dll および Microsoft.VisualBasic.dll の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="2faa8-103">Specifies the location of mscorlib.dll and Microsoft.VisualBasic.dll.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2faa8-104">構文</span><span class="sxs-lookup"><span data-stu-id="2faa8-104">Syntax</span></span>  
  
```  
-sdkpath:path  
```  
  
## <a name="arguments"></a><span data-ttu-id="2faa8-105">引数</span><span class="sxs-lookup"><span data-stu-id="2faa8-105">Arguments</span></span>  
 `path`  
 <span data-ttu-id="2faa8-106">Mscorlib.dll および Microsoft.VisualBasic.dll のコンパイルに使用するのバージョンを含むディレクトリ。</span><span class="sxs-lookup"><span data-stu-id="2faa8-106">The directory containing the versions of mscorlib.dll and Microsoft.VisualBasic.dll to use for compilation.</span></span> <span data-ttu-id="2faa8-107">それが読み込まれるまで、このパスは検証されません。</span><span class="sxs-lookup"><span data-stu-id="2faa8-107">This path is not verified until it is loaded.</span></span> <span data-ttu-id="2faa8-108">ディレクトリ名を引用符で囲みます ("")、スペースが含まれている場合。</span><span class="sxs-lookup"><span data-stu-id="2faa8-108">Enclose the directory name in quotation marks (" ") if it contains a space.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2faa8-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="2faa8-109">Remarks</span></span>  
 <span data-ttu-id="2faa8-110">このオプションは、既定以外の場所から mscorlib.dll および Microsoft.VisualBasic.dll のファイルを読み込む Visual Basic コンパイラに指示します。</span><span class="sxs-lookup"><span data-stu-id="2faa8-110">This option tells the Visual Basic compiler to load the mscorlib.dll and Microsoft.VisualBasic.dll files from a non-default location.</span></span> <span data-ttu-id="2faa8-111">`-sdkpath`で使用するオプションが設計されました[-netcf](../../../visual-basic/reference/command-line-compiler/netcf.md)します。</span><span class="sxs-lookup"><span data-stu-id="2faa8-111">The `-sdkpath` option was designed to be used with [-netcf](../../../visual-basic/reference/command-line-compiler/netcf.md).</span></span> <span data-ttu-id="2faa8-112">[!INCLUDE[Compact](~/includes/compact-md.md)]さまざまなバージョンを使用してこれらの型と、デバイスで見つからない言語機能の使用を回避するためにライブラリをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2faa8-112">The [!INCLUDE[Compact](~/includes/compact-md.md)] uses different versions of these support libraries to avoid the use of types and language features not found on the devices.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2faa8-113">`-sdkpath`オプションは、Visual Studio 開発環境内からは使用できません。 コマンドラインからコンパイルする場合にのみ使用可能なです。</span><span class="sxs-lookup"><span data-stu-id="2faa8-113">The `-sdkpath` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span> <span data-ttu-id="2faa8-114">`-sdkpath` Visual Basic プロジェクトのデバイスが読み込まれるときにオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="2faa8-114">The `-sdkpath` option is set when a Visual Basic device project is loaded.</span></span>  
  
 <span data-ttu-id="2faa8-115">使用して、コンパイラが、Visual Basic ランタイム ライブラリを参照しないでコンパイルを指定することができます、`-vbruntime`コンパイラ オプション。</span><span class="sxs-lookup"><span data-stu-id="2faa8-115">You can specify that the compiler should compile without a reference to the Visual Basic Runtime Library by using the `-vbruntime` compiler option.</span></span> <span data-ttu-id="2faa8-116">詳細については、次を参照してください。 [-vbruntime](../../../visual-basic/reference/command-line-compiler/vbruntime.md)します。</span><span class="sxs-lookup"><span data-stu-id="2faa8-116">For more information, see [-vbruntime](../../../visual-basic/reference/command-line-compiler/vbruntime.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="2faa8-117">例</span><span class="sxs-lookup"><span data-stu-id="2faa8-117">Example</span></span>  
 <span data-ttu-id="2faa8-118">次のコードのコンパイル`Myfile.vb`で、[!INCLUDE[Compact](~/includes/compact-md.md)]の既定のインストール ディレクトリにある Mscorlib.dll および Microsoft.VisualBasic.dll のバージョンを使用して、 [!INCLUDE[Compact](~/includes/compact-md.md)] C ドライブにします。</span><span class="sxs-lookup"><span data-stu-id="2faa8-118">The following code compiles `Myfile.vb` with the [!INCLUDE[Compact](~/includes/compact-md.md)], using the versions of Mscorlib.dll and Microsoft.VisualBasic.dll found in the default installation directory of the [!INCLUDE[Compact](~/includes/compact-md.md)] on the C drive.</span></span> <span data-ttu-id="2faa8-119">通常の最新バージョンを使用すると、[!INCLUDE[Compact](~/includes/compact-md.md)]します。</span><span class="sxs-lookup"><span data-stu-id="2faa8-119">Typically, you would use the most recent version of the [!INCLUDE[Compact](~/includes/compact-md.md)].</span></span>  
  
```console
vbc -netcf -sdkpath:"c:\Program Files\Microsoft Visual Studio .NET 2003\CompactFrameworkSDK\v1.0.5000\Windows CE " myfile.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="2faa8-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="2faa8-120">See Also</span></span>  
 [<span data-ttu-id="2faa8-121">Visual Basic のコマンド ライン コンパイラ</span><span class="sxs-lookup"><span data-stu-id="2faa8-121">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="2faa8-122">コンパイル コマンド ラインのサンプル</span><span class="sxs-lookup"><span data-stu-id="2faa8-122">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="2faa8-123">-netcf</span><span class="sxs-lookup"><span data-stu-id="2faa8-123">-netcf</span></span>](../../../visual-basic/reference/command-line-compiler/netcf.md)  
 [<span data-ttu-id="2faa8-124">-vbruntime</span><span class="sxs-lookup"><span data-stu-id="2faa8-124">-vbruntime</span></span>](../../../visual-basic/reference/command-line-compiler/vbruntime.md)
