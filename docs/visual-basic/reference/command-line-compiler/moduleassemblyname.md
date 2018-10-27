---
title: -moduleassemblyname
ms.date: 03/13/2018
helpviewer_keywords:
- moduleassemblyname compiler option [Visual Basic]
- /moduleassemblyname compiler option [Visual Basic]
- -moduleassemblyname compiler option [Visual Basic]
ms.assetid: 013a57b6-f425-4dd3-b333-512d72c42f55
ms.openlocfilehash: 92fd068ef0ff892c8b76396edbf1d532a36e338c
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50189512"
---
# <a name="-moduleassemblyname"></a><span data-ttu-id="0338c-102">-moduleassemblyname</span><span class="sxs-lookup"><span data-stu-id="0338c-102">-moduleassemblyname</span></span>
<span data-ttu-id="0338c-103">このモジュールが一部となるアセンブリの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="0338c-103">Specifies the name of the assembly that this module will be a part of.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0338c-104">構文</span><span class="sxs-lookup"><span data-stu-id="0338c-104">Syntax</span></span>  
  
```  
-moduleassemblyname:assembly_name  
```  
  
## <a name="arguments"></a><span data-ttu-id="0338c-105">引数</span><span class="sxs-lookup"><span data-stu-id="0338c-105">Arguments</span></span>  
  
|<span data-ttu-id="0338c-106">用語</span><span class="sxs-lookup"><span data-stu-id="0338c-106">Term</span></span>|<span data-ttu-id="0338c-107">定義</span><span class="sxs-lookup"><span data-stu-id="0338c-107">Definition</span></span>|  
|---|---|  
|`assembly_name`|<span data-ttu-id="0338c-108">このモジュールの一部となるアセンブリの名前。</span><span class="sxs-lookup"><span data-stu-id="0338c-108">The name of the assembly that this module will be a part of.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0338c-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="0338c-109">Remarks</span></span>  
 <span data-ttu-id="0338c-110">コンパイラ プロセス、`-moduleassemblyname`オプション場合にのみ、`-target:module`オプションが指定されました。</span><span class="sxs-lookup"><span data-stu-id="0338c-110">The compiler processes the `-moduleassemblyname` option only if the `-target:module` option has been specified.</span></span> <span data-ttu-id="0338c-111">これにより、コンパイラでモジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="0338c-111">This causes the compiler to create a module.</span></span> <span data-ttu-id="0338c-112">コンパイラによって作成されたモジュールがで指定されたアセンブリに対してのみ有効ですが、`-moduleassemblyname`オプション。</span><span class="sxs-lookup"><span data-stu-id="0338c-112">The module created by the compiler is valid only for the assembly specified with the `-moduleassemblyname` option.</span></span> <span data-ttu-id="0338c-113">別のアセンブリでモジュールを配置する場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0338c-113">If you place the module in a different assembly, run-time errors will occur.</span></span>  
  
 <span data-ttu-id="0338c-114">`-moduleassemblyname`オプションは、次に該当する場合にのみ必要があります。</span><span class="sxs-lookup"><span data-stu-id="0338c-114">The `-moduleassemblyname` option is needed only when the following are true:</span></span>  
  
-   <span data-ttu-id="0338c-115">モジュール内のデータ型へのアクセスを必要な`Friend`参照先アセンブリの型。</span><span class="sxs-lookup"><span data-stu-id="0338c-115">A data type in the module needs access to a `Friend` type in a referenced assembly.</span></span>  
  
-   <span data-ttu-id="0338c-116">参照アセンブリがモジュールをビルドするアセンブリにフレンド アセンブリのアクセスを付与します。</span><span class="sxs-lookup"><span data-stu-id="0338c-116">The referenced assembly has granted friend assembly access to the assembly into which the module will be built.</span></span>  
  
 <span data-ttu-id="0338c-117">モジュールの作成方法の詳細については、次を参照してください。 [/target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md)します。</span><span class="sxs-lookup"><span data-stu-id="0338c-117">For more information about creating a module, see [/target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md).</span></span> <span data-ttu-id="0338c-118">フレンド アセンブリの詳細については、次を参照してください。[フレンド アセンブリ](../../programming-guide/concepts/assemblies-gac/friend-assemblies.md)します。</span><span class="sxs-lookup"><span data-stu-id="0338c-118">For more information about friend assemblies, see [Friend Assemblies](../../programming-guide/concepts/assemblies-gac/friend-assemblies.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0338c-119">`-moduleassemblyname`オプションは、Visual Studio 開発環境内からは使用できません。 コマンド プロンプトからコンパイルするときにのみ、は使用できます。</span><span class="sxs-lookup"><span data-stu-id="0338c-119">The `-moduleassemblyname` option is not available from within the Visual Studio development environment; it is available only when you compile from a command prompt.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0338c-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="0338c-120">See Also</span></span>  
 [<span data-ttu-id="0338c-121">方法: マルチファイル アセンブリをビルドする</span><span class="sxs-lookup"><span data-stu-id="0338c-121">How to: Build a Multifile Assembly</span></span>](../../../framework/app-domains/how-to-build-a-multifile-assembly.md)  
 [<span data-ttu-id="0338c-122">Visual Basic のコマンド ライン コンパイラ</span><span class="sxs-lookup"><span data-stu-id="0338c-122">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="0338c-123">-ターゲット (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0338c-123">-target (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/target.md)  
 [<span data-ttu-id="0338c-124">-main</span><span class="sxs-lookup"><span data-stu-id="0338c-124">-main</span></span>](../../../visual-basic/reference/command-line-compiler/main.md)  
 [<span data-ttu-id="0338c-125">-参照 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0338c-125">-reference (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/reference.md)  
 [<span data-ttu-id="0338c-126">-addmodule</span><span class="sxs-lookup"><span data-stu-id="0338c-126">-addmodule</span></span>](../../../visual-basic/reference/command-line-compiler/addmodule.md)  
 [<span data-ttu-id="0338c-127">アセンブリとグローバル アセンブリ キャッシュ</span><span class="sxs-lookup"><span data-stu-id="0338c-127">Assemblies and the Global Assembly Cache</span></span>](../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)  
 [<span data-ttu-id="0338c-128">コンパイル コマンド ラインのサンプル</span><span class="sxs-lookup"><span data-stu-id="0338c-128">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="0338c-129">フレンド アセンブリ</span><span class="sxs-lookup"><span data-stu-id="0338c-129">Friend Assemblies</span></span>](../../programming-guide/concepts/assemblies-gac/friend-assemblies.md)
