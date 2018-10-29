---
title: -rootnamespace
ms.date: 03/13/2018
f1_keywords:
- /rootnamespace
- rootnamespace
helpviewer_keywords:
- /rootnamespace compiler option [Visual Basic]
- -rootnamespace compiler option [Visual Basic]
- rootnamespace compiler option [Visual Basic]
ms.assetid: e9245edf-6bef-420d-a7c7-324117752783
ms.openlocfilehash: 2c7fb6c88477899a0cf08a467e8f23d687b90c90
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50201900"
---
# <a name="-rootnamespace"></a><span data-ttu-id="be52e-102">-rootnamespace</span><span class="sxs-lookup"><span data-stu-id="be52e-102">-rootnamespace</span></span>
<span data-ttu-id="be52e-103">すべての型宣言に対して名前空間を指定します。</span><span class="sxs-lookup"><span data-stu-id="be52e-103">Specifies a namespace for all type declarations.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be52e-104">構文</span><span class="sxs-lookup"><span data-stu-id="be52e-104">Syntax</span></span>  
  
```  
-rootnamespace:namespace  
```  
  
## <a name="arguments"></a><span data-ttu-id="be52e-105">引数</span><span class="sxs-lookup"><span data-stu-id="be52e-105">Arguments</span></span>  
  
|<span data-ttu-id="be52e-106">用語</span><span class="sxs-lookup"><span data-stu-id="be52e-106">Term</span></span>|<span data-ttu-id="be52e-107">定義</span><span class="sxs-lookup"><span data-stu-id="be52e-107">Definition</span></span>|  
|---|---|  
|`namespace`|<span data-ttu-id="be52e-108">現在のプロジェクトのすべての型宣言を囲む名前空間の名前。</span><span class="sxs-lookup"><span data-stu-id="be52e-108">The name of the namespace in which to enclose all type declarations for the current project.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="be52e-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="be52e-109">Remarks</span></span>  
 <span data-ttu-id="be52e-110">使用して、Visual Studio 統合開発環境で作成したプロジェクトをコンパイルする Visual Studio の実行可能ファイル (Devenv.exe) を使用する場合`-rootnamespace`の値を指定する、<xref:VSLangProj80.VBProjectProperties3.RootNamespace%2A>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="be52e-110">If you use the Visual Studio executable file (Devenv.exe) to compile a project created in the Visual Studio integrated development environment, use `-rootnamespace` to specify the value of the <xref:VSLangProj80.VBProjectProperties3.RootNamespace%2A> property.</span></span> <span data-ttu-id="be52e-111">参照してください[Devenv コマンド ライン スイッチ](/visualstudio/ide/reference/devenv-command-line-switches)詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="be52e-111">See [Devenv Command Line Switches](/visualstudio/ide/reference/devenv-command-line-switches) for more information.</span></span>  
  
 <span data-ttu-id="be52e-112">共通言語ランタイム MSIL 逆アセンブラーを使用して (`Ildasm.exe`) を出力ファイルの名前空間の名前を表示します。</span><span class="sxs-lookup"><span data-stu-id="be52e-112">Use the common language runtime MSIL Disassembler (`Ildasm.exe`) to view the namespace names in your output file.</span></span>  
  
|<span data-ttu-id="be52e-113">Visual Studio 統合開発環境で-rootnamespace を設定するには</span><span class="sxs-lookup"><span data-stu-id="be52e-113">To set -rootnamespace in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="be52e-114">1.**ソリューション エクスプローラー**でプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="be52e-114">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="be52e-115">**[プロジェクト]** メニューの **[プロパティ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be52e-115">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="be52e-116">2.**[アプリケーション]** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="be52e-116">2.  Click the **Application** tab.</span></span><br /><span data-ttu-id="be52e-117">3.値を変更、**ルート Namespace**ボックス。</span><span class="sxs-lookup"><span data-stu-id="be52e-117">3.  Modify the value in the **Root Namespace** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="be52e-118">例</span><span class="sxs-lookup"><span data-stu-id="be52e-118">Example</span></span>  
 <span data-ttu-id="be52e-119">次のコードのコンパイル`In.vb`と名前空間のすべての型宣言を囲む`mynamespace`します。</span><span class="sxs-lookup"><span data-stu-id="be52e-119">The following code compiles `In.vb` and encloses all type declarations in the namespace `mynamespace`.</span></span>  
  
```console
vbc -rootnamespace:mynamespace in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="be52e-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="be52e-120">See also</span></span>

- [<span data-ttu-id="be52e-121">Visual Basic のコマンド ライン コンパイラ</span><span class="sxs-lookup"><span data-stu-id="be52e-121">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
- [<span data-ttu-id="be52e-122">Ildasm.exe (IL 逆アセンブラー)</span><span class="sxs-lookup"><span data-stu-id="be52e-122">Ildasm.exe (IL Disassembler)</span></span>](../../../framework/tools/ildasm-exe-il-disassembler.md)  
- [<span data-ttu-id="be52e-123">コンパイル コマンド ラインのサンプル</span><span class="sxs-lookup"><span data-stu-id="be52e-123">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
