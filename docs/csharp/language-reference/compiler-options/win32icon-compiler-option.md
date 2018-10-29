---
title: -win32icon (C# コンパイラ オプション)
ms.date: 07/20/2015
f1_keywords:
- /win32icon
helpviewer_keywords:
- win32icon compiler option [C#]
- /win32icon compiler option [C#]
- -win32icon compiler option [C#]
ms.assetid: 756d9b6d-ab07-41b7-ba58-5bd88f711138
ms.openlocfilehash: 5014b1da714f8e29f869d4641da93796a607aa4d
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48027794"
---
# <a name="-win32icon-c-compiler-options"></a><span data-ttu-id="2ec75-102">-win32icon (C# コンパイラ オプション)</span><span class="sxs-lookup"><span data-stu-id="2ec75-102">-win32icon (C# Compiler Options)</span></span>
<span data-ttu-id="2ec75-103">**-win32icon** オプションは、エクスプローラーで出力ファイルを適切に表示する .ico ファイルを出力ファイルに挿入します。</span><span class="sxs-lookup"><span data-stu-id="2ec75-103">The **-win32icon** option inserts an .ico file in the output file, which gives the output file the desired appearance in the File Explorer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2ec75-104">構文</span><span class="sxs-lookup"><span data-stu-id="2ec75-104">Syntax</span></span>  
  
```console  
-win32icon:filename  
```  
  
## <a name="arguments"></a><span data-ttu-id="2ec75-105">引数</span><span class="sxs-lookup"><span data-stu-id="2ec75-105">Arguments</span></span>  
 `filename`  
 <span data-ttu-id="2ec75-106">出力ファイルに追加する .ico ファイル。</span><span class="sxs-lookup"><span data-stu-id="2ec75-106">The .ico file that you want to add to your output file.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2ec75-107">コメント</span><span class="sxs-lookup"><span data-stu-id="2ec75-107">Remarks</span></span>  
 <span data-ttu-id="2ec75-108">.ico ファイルは[リソース コンパイラ](/windows/desktop/menurc/resource-compiler)で作成できます。</span><span class="sxs-lookup"><span data-stu-id="2ec75-108">An .ico file can be created with the [Resource Compiler](/windows/desktop/menurc/resource-compiler).</span></span> <span data-ttu-id="2ec75-109">リソース コンパイラは、Visual C++ プログラムをコンパイルするときに呼び出されます。 .ico ファイルは .rc ファイルから作成されます。</span><span class="sxs-lookup"><span data-stu-id="2ec75-109">The Resource Compiler is invoked when you compile a Visual C++ program; an .ico file is created from the .rc file.</span></span>  
  
 <span data-ttu-id="2ec75-110">.NET Framework リソース ファイルの [-linkresource](../../../csharp/language-reference/compiler-options/linkresource-compiler-option.md) (参照) または [-resource](../../../csharp/language-reference/compiler-options/resource-compiler-option.md) (アタッチ) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2ec75-110">See [-linkresource](../../../csharp/language-reference/compiler-options/linkresource-compiler-option.md) (to reference) or [-resource](../../../csharp/language-reference/compiler-options/resource-compiler-option.md) (to attach) a .NET Framework resource file.</span></span> <span data-ttu-id="2ec75-111">.res ファイルのインポートについては、[-win32res](../../../csharp/language-reference/compiler-options/win32res-compiler-option.md) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2ec75-111">See [-win32res](../../../csharp/language-reference/compiler-options/win32res-compiler-option.md) to import a .res file.</span></span>  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a><span data-ttu-id="2ec75-112">Visual Studio 開発環境でこのコンパイラ オプションを設定するには</span><span class="sxs-lookup"><span data-stu-id="2ec75-112">To set this compiler option in the Visual Studio development environment</span></span>  
  
1.  <span data-ttu-id="2ec75-113">プロジェクトの **[プロパティ]** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="2ec75-113">Open the project's **Properties** pages.</span></span>  
  
2.  <span data-ttu-id="2ec75-114">**[アプリケーション]** プロパティ ページをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ec75-114">Click the **Application** property page.</span></span>  
  
3.  <span data-ttu-id="2ec75-115">**[アプリケーション アイコン]** プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="2ec75-115">Modify the **Application icon** property.</span></span>  
  
 <span data-ttu-id="2ec75-116">このコンパイラ オプションをプログラムで設定する方法については、「 <xref:VSLangProj80.ProjectProperties3.ApplicationIcon%2A>」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2ec75-116">For information on how to set this compiler option programmatically, see <xref:VSLangProj80.ProjectProperties3.ApplicationIcon%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2ec75-117">例</span><span class="sxs-lookup"><span data-stu-id="2ec75-117">Example</span></span>  
 <span data-ttu-id="2ec75-118">`in.cs` をコンパイルし、.ico ファイル `rf.ico` をアタッチし、`in.exe` を作成します。</span><span class="sxs-lookup"><span data-stu-id="2ec75-118">Compile `in.cs` and attach an .ico file `rf.ico` to produce `in.exe`:</span></span>  
  
```console  
csc -win32icon:rf.ico in.cs  
```  
  
## <a name="see-also"></a><span data-ttu-id="2ec75-119">参照</span><span class="sxs-lookup"><span data-stu-id="2ec75-119">See Also</span></span>  

- [<span data-ttu-id="2ec75-120">C# コンパイラ オプション</span><span class="sxs-lookup"><span data-stu-id="2ec75-120">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)  
- [<span data-ttu-id="2ec75-121">プロジェクトおよびソリューションのプロパティの管理</span><span class="sxs-lookup"><span data-stu-id="2ec75-121">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
