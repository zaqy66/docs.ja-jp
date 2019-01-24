---
title: -keycontainer
ms.date: 03/10/2018
helpviewer_keywords:
- -keycontainer compiler option [Visual Basic]
- keycontainer compiler option [Visual Basic]
- /keycontainer compiler option [Visual Basic]
ms.assetid: 6a9bc861-1752-4db1-9f64-b5252f0482cc
ms.openlocfilehash: 1666c7743f1116f86bc4457af53711cb6f1a6b7b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54579824"
---
# <a name="-keycontainer"></a><span data-ttu-id="0e0dc-102">-keycontainer</span><span class="sxs-lookup"><span data-stu-id="0e0dc-102">-keycontainer</span></span>
<span data-ttu-id="0e0dc-103">アセンブリに厳密な名前を付けるキー ペアのキー コンテナー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-103">Specifies a key container name for a key pair to give an assembly a strong name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0e0dc-104">構文</span><span class="sxs-lookup"><span data-stu-id="0e0dc-104">Syntax</span></span>  
  
```  
-keycontainer:container  
```  
  
## <a name="arguments"></a><span data-ttu-id="0e0dc-105">引数</span><span class="sxs-lookup"><span data-stu-id="0e0dc-105">Arguments</span></span>  
  
|<span data-ttu-id="0e0dc-106">用語</span><span class="sxs-lookup"><span data-stu-id="0e0dc-106">Term</span></span>|<span data-ttu-id="0e0dc-107">定義</span><span class="sxs-lookup"><span data-stu-id="0e0dc-107">Definition</span></span>|  
|---|---|  
|`container`|<span data-ttu-id="0e0dc-108">必須。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-108">Required.</span></span> <span data-ttu-id="0e0dc-109">コンテナー キーを含むファイルです。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-109">Container file that contains the key.</span></span> <span data-ttu-id="0e0dc-110">ファイル名を引用符で囲みます ("")、名前にスペースが含まれている場合。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-110">Enclose the file name in quotation marks ("") if the name contains a space.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0e0dc-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="0e0dc-111">Remarks</span></span>  
 <span data-ttu-id="0e0dc-112">コンパイラは、秘密キーで最終アセンブリに署名して、アセンブリ マニフェストに公開キーを挿入することで、共有可能なコンポーネントを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-112">The compiler creates the sharable component by inserting a public key into the assembly manifest and by signing the final assembly with the private key.</span></span> <span data-ttu-id="0e0dc-113">キー ファイルを生成するには、コマンド ラインで「`sn -k file`」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-113">To generate a key file, type `sn -k file` at the command line.</span></span> <span data-ttu-id="0e0dc-114">`-i`オプションは、コンテナーにキー ペアをインストールします。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-114">The `-i` option installs the key pair into a container.</span></span> <span data-ttu-id="0e0dc-115">詳細については、[Sn.exe (厳密名ツール)] を参照してください。[Sn.exe (厳密名ツール)](../../../framework/tools/sn-exe-strong-name-tool.md))。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-115">For more information, see [Sn.exe (Strong Name Tool)][Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md)).</span></span>  
  
 <span data-ttu-id="0e0dc-116">使用してコンパイルする場合`-target:module`、キー ファイルの名前がモジュールに保持され、使用してアセンブリをコンパイルするときに作成されるアセンブリに組み込まれます[-addmodule](../../../visual-basic/reference/command-line-compiler/addmodule.md)します。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-116">If you compile with `-target:module`, the name of the key file is held in the module and incorporated into the assembly that is created when you compile an assembly with [-addmodule](../../../visual-basic/reference/command-line-compiler/addmodule.md).</span></span>  
  
 <span data-ttu-id="0e0dc-117">このオプションは、任意の Microsoft Intermediate Language (MSIL) モジュールのソース コードで、カスタム属性 (<xref:System.Reflection.AssemblyKeyNameAttribute>) として指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-117">You can also specify this option as a custom attribute (<xref:System.Reflection.AssemblyKeyNameAttribute>) in the source code for any Microsoft intermediate language (MSIL) module.</span></span>  
  
 <span data-ttu-id="0e0dc-118">また、暗号化情報を [-keyfile](../../../visual-basic/reference/command-line-compiler/keyfile.md) でコンパイラに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-118">You can also pass your encryption information to the compiler with [-keyfile](../../../visual-basic/reference/command-line-compiler/keyfile.md).</span></span> <span data-ttu-id="0e0dc-119">部分的に署名されたアセンブリを作成する場合は、[-delaysign](../../../visual-basic/reference/command-line-compiler/delaysign.md) を使います。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-119">Use [-delaysign](../../../visual-basic/reference/command-line-compiler/delaysign.md) if you want a partially signed assembly.</span></span>  
  
 <span data-ttu-id="0e0dc-120">参照してください[の作成と using strong-named Assemblies](../../../framework/app-domains/create-and-use-strong-named-assemblies.md)アセンブリへの署名の詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-120">See [Creating and Using Strong-Named Assemblies](../../../framework/app-domains/create-and-use-strong-named-assemblies.md) for more information on signing an assembly.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0e0dc-121">`-keycontainer`オプションは、Visual Studio 開発環境内からは使用できません。 コマンドラインからコンパイルする場合にのみ使用可能なです。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-121">The `-keycontainer` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0e0dc-122">例</span><span class="sxs-lookup"><span data-stu-id="0e0dc-122">Example</span></span>  
 <span data-ttu-id="0e0dc-123">次のコードは、ソース ファイルをコンパイル`Input.vb`をキー コンテナーを指定します。</span><span class="sxs-lookup"><span data-stu-id="0e0dc-123">The following code compiles source file `Input.vb` and specifies a key container.</span></span>  
  
```  
vbc -keycontainer:key1 input.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="0e0dc-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="0e0dc-124">See also</span></span>
- [<span data-ttu-id="0e0dc-125">アセンブリとグローバル アセンブリ キャッシュ</span><span class="sxs-lookup"><span data-stu-id="0e0dc-125">Assemblies and the Global Assembly Cache</span></span>](../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)
- [<span data-ttu-id="0e0dc-126">Visual Basic のコマンド ライン コンパイラ</span><span class="sxs-lookup"><span data-stu-id="0e0dc-126">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="0e0dc-127">-keyfile</span><span class="sxs-lookup"><span data-stu-id="0e0dc-127">-keyfile</span></span>](../../../visual-basic/reference/command-line-compiler/keyfile.md)
- [<span data-ttu-id="0e0dc-128">コンパイル コマンド ラインのサンプル</span><span class="sxs-lookup"><span data-stu-id="0e0dc-128">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
