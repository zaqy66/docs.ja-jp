---
title: -warnaserror (C# コンパイラ オプション)
ms.date: 07/20/2015
f1_keywords:
- /warnaserror
helpviewer_keywords:
- /warnaserror compiler option [C#]
- -warnaserror compiler option [C#]
- warnaserror compiler option [C#]
ms.assetid: 04680ec3-08d6-4e2e-a274-38310e10e33c
ms.openlocfilehash: a29b0a6095453e3d2747cad9d9f71b463d8f6b1f
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43406196"
---
# <a name="-warnaserror-c-compiler-options"></a><span data-ttu-id="7b2fb-102">-warnaserror (C# コンパイラ オプション)</span><span class="sxs-lookup"><span data-stu-id="7b2fb-102">-warnaserror (C# Compiler Options)</span></span>
<span data-ttu-id="7b2fb-103">**-warnaserror+** オプションは、すべての警告をエラーとして扱います</span><span class="sxs-lookup"><span data-stu-id="7b2fb-103">The **-warnaserror+** option treats all warnings as errors</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b2fb-104">構文</span><span class="sxs-lookup"><span data-stu-id="7b2fb-104">Syntax</span></span>  
  
```console  
-warnaserror[+ | -][:warning-list]  
```  
  
## <a name="remarks"></a><span data-ttu-id="7b2fb-105">コメント</span><span class="sxs-lookup"><span data-stu-id="7b2fb-105">Remarks</span></span>  
 <span data-ttu-id="7b2fb-106">通常は警告として報告されるすべてのメッセージが、代わりにエラーとして報告され、ビルド プロセスが停止します (出力ファイルはビルドされません)。</span><span class="sxs-lookup"><span data-stu-id="7b2fb-106">Any messages that would ordinarily be reported as warnings are instead reported as errors, and the build process is halted (no output files are built).</span></span>  
  
 <span data-ttu-id="7b2fb-107">既定では、**-warnaserror-** が有効になっているため、警告により出力ファイルの生成が妨げられることはありません。</span><span class="sxs-lookup"><span data-stu-id="7b2fb-107">By default, **-warnaserror-** is in effect, which causes warnings to not prevent the generation of an output file.</span></span> <span data-ttu-id="7b2fb-108">**-warnaserror** は **-warnaserror+** と同じで、警告がエラーとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="7b2fb-108">**-warnaserror**, which is the same as **-warnaserror+**, causes warnings to be treated as errors.</span></span>  
  
 <span data-ttu-id="7b2fb-109">必要に応じて、いくつかの特定の警告のみをエラーとして扱う場合は、エラーとして扱う警告番号のコンマ区切りのリストを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7b2fb-109">Optionally, if you want only a few specific warnings to be treated as errors, you may specify a comma-separated list of warning numbers to treat as errors.</span></span>  
  
 <span data-ttu-id="7b2fb-110">コンパイラで表示する警告のレベルを指定するには、[-warn](../../../csharp/language-reference/compiler-options/warn-compiler-option.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="7b2fb-110">Use [-warn](../../../csharp/language-reference/compiler-options/warn-compiler-option.md) to specify the level of warnings that you want the compiler to display.</span></span> <span data-ttu-id="7b2fb-111">特定の警告を無効にするには、[-nowarn](../../../csharp/language-reference/compiler-options/nowarn-compiler-option.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="7b2fb-111">Use [-nowarn](../../../csharp/language-reference/compiler-options/nowarn-compiler-option.md) to disable certain warnings.</span></span>  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a><span data-ttu-id="7b2fb-112">Visual Studio 開発環境でこのコンパイラ オプションを設定するには</span><span class="sxs-lookup"><span data-stu-id="7b2fb-112">To set this compiler option in the Visual Studio development environment</span></span>  
  
1.  <span data-ttu-id="7b2fb-113">プロジェクトの **[プロパティ]** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="7b2fb-113">Open the project's **Properties** page.</span></span>  
  
2.  <span data-ttu-id="7b2fb-114">**[ビルド]** プロパティ ページをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b2fb-114">Click the **Build** property page.</span></span>  
  
3.  <span data-ttu-id="7b2fb-115">**警告をエラーとして扱う**プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="7b2fb-115">Modify the **Treat Warnings As Errors** property.</span></span>  
  
 <span data-ttu-id="7b2fb-116">このコンパイラ オプションをプログラムによって設定するには、「<xref:VSLangProj80.CSharpProjectConfigurationProperties3.TreatWarningsAsErrors>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b2fb-116">To set this compiler option programmatically, see <xref:VSLangProj80.CSharpProjectConfigurationProperties3.TreatWarningsAsErrors>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7b2fb-117">例</span><span class="sxs-lookup"><span data-stu-id="7b2fb-117">Example</span></span>  
 <span data-ttu-id="7b2fb-118">`in.cs` をコンパイルして、コンパイラで警告を表示させないようにします。</span><span class="sxs-lookup"><span data-stu-id="7b2fb-118">Compile `in.cs` and have the compiler display no warnings:</span></span>  
  
```console  
csc -warnaserror in.cs  
csc -warnaserror:642,649,652 in.cs  
```  
  
## <a name="see-also"></a><span data-ttu-id="7b2fb-119">参照</span><span class="sxs-lookup"><span data-stu-id="7b2fb-119">See Also</span></span>  

- [<span data-ttu-id="7b2fb-120">C# コンパイラ オプション</span><span class="sxs-lookup"><span data-stu-id="7b2fb-120">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)  
- [<span data-ttu-id="7b2fb-121">プロジェクトおよびソリューションのプロパティの管理</span><span class="sxs-lookup"><span data-stu-id="7b2fb-121">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
