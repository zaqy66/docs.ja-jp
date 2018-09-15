---
title: -ドキュメント
ms.date: 03/10/2018
helpviewer_keywords:
- doc compiler option [Visual Basic]
- -doc compiler option [Visual Basic]
- /doc compiler option [Visual Basic]
ms.assetid: 5fc32ec9-a149-4648-994c-a8d0cccd0a65
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4c77d063d64354bf4693ce82509f36be9d2e5b0c
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/15/2018
ms.locfileid: "45638945"
---
# <a name="-doc"></a><span data-ttu-id="86c05-102">-ドキュメント</span><span class="sxs-lookup"><span data-stu-id="86c05-102">-doc</span></span>
<span data-ttu-id="86c05-103">ドキュメント コメントを XML ファイルに出力します。</span><span class="sxs-lookup"><span data-stu-id="86c05-103">Processes documentation comments to an XML file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86c05-104">構文</span><span class="sxs-lookup"><span data-stu-id="86c05-104">Syntax</span></span>  
  
```  
-doc[+ | -]  
' -or-  
-doc:file  
```  
  
## <a name="arguments"></a><span data-ttu-id="86c05-105">引数</span><span class="sxs-lookup"><span data-stu-id="86c05-105">Arguments</span></span>  
  
|<span data-ttu-id="86c05-106">用語</span><span class="sxs-lookup"><span data-stu-id="86c05-106">Term</span></span>|<span data-ttu-id="86c05-107">定義</span><span class="sxs-lookup"><span data-stu-id="86c05-107">Definition</span></span>|  
|---|---|  
|<span data-ttu-id="86c05-108">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="86c05-108">`+` &#124; `-`</span></span>|<span data-ttu-id="86c05-109">任意。</span><span class="sxs-lookup"><span data-stu-id="86c05-109">Optional.</span></span> <span data-ttu-id="86c05-110">指定する +、または単`-doc`、コンパイラが、ドキュメント情報を生成し、XML ファイル内に配置します。</span><span class="sxs-lookup"><span data-stu-id="86c05-110">Specifying +, or just `-doc`, causes the compiler to generate documentation information and place it in an XML file.</span></span> <span data-ttu-id="86c05-111">指定する`-`指定しない場合のと同じ`-doc`、なり、ドキュメントの情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="86c05-111">Specifying `-` is the equivalent of not specifying `-doc`, causing no documentation information to be created.</span></span>|  
|`file`|<span data-ttu-id="86c05-112">`-doc:` を使用する場合に、必ず指定します。</span><span class="sxs-lookup"><span data-stu-id="86c05-112">Required if `-doc:` is used.</span></span> <span data-ttu-id="86c05-113">コンパイルのソース コード ファイルからのコメントが設定されている出力 XML ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="86c05-113">Specifies the output XML file, which is populated with the comments from the source-code files of the compilation.</span></span> <span data-ttu-id="86c05-114">ファイル名にスペースが含まれている場合は、引用符で名を囲む ("")。</span><span class="sxs-lookup"><span data-stu-id="86c05-114">If the file name contains a space, surround the name with quotation marks (" ").</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="86c05-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="86c05-115">Remarks</span></span>  
 <span data-ttu-id="86c05-116">`-doc`オプションでは、コンパイラは、ドキュメント コメントを含む XML ファイルを生成するかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="86c05-116">The `-doc` option controls whether the compiler generates an XML file containing the documentation comments.</span></span> <span data-ttu-id="86c05-117">使用する場合、 `-doc:file` 、構文、`file`パラメーターを XML ファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="86c05-117">If you use the `-doc:file` syntax, the `file` parameter specifies the name of the XML file.</span></span> <span data-ttu-id="86c05-118">使用する場合`-doc`または`-doc+`コンパイラは、実行可能ファイルまたはコンパイラを作成しているライブラリから XML ファイルの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="86c05-118">If you use `-doc` or `-doc+`, the compiler takes the XML file name from the executable file or library that the compiler is creating.</span></span> <span data-ttu-id="86c05-119">使用する場合`-doc-`を指定しないか、`-doc`オプション、コンパイラは、XML ファイルを作成しません。</span><span class="sxs-lookup"><span data-stu-id="86c05-119">If you use `-doc-` or do not specify the `-doc` option, the compiler does not create an XML file.</span></span>  
  
 <span data-ttu-id="86c05-120">ソース コード ファイル、ドキュメントのコメントは以下の定義の前にことができます。</span><span class="sxs-lookup"><span data-stu-id="86c05-120">In source-code files, documentation comments can precede the following definitions:</span></span>  
  
-   <span data-ttu-id="86c05-121">ユーザー定義型の場合など、[クラス](../../../visual-basic/language-reference/statements/class-statement.md)または[インターフェイス](../../../visual-basic/language-reference/statements/interface-statement.md)</span><span class="sxs-lookup"><span data-stu-id="86c05-121">User-defined types, such as a [class](../../../visual-basic/language-reference/statements/class-statement.md) or [interface](../../../visual-basic/language-reference/statements/interface-statement.md)</span></span>  
  
-   <span data-ttu-id="86c05-122">など、フィールド メンバー[イベント](../../../visual-basic/language-reference/statements/event-statement.md)、[プロパティ](../../../visual-basic/language-reference/statements/property-statement.md)、[関数](../../../visual-basic/language-reference/statements/function-statement.md)、または[サブルーチン](../../../visual-basic/language-reference/statements/sub-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="86c05-122">Members, such as a field, [event](../../../visual-basic/language-reference/statements/event-statement.md), [property](../../../visual-basic/language-reference/statements/property-statement.md), [function](../../../visual-basic/language-reference/statements/function-statement.md), or [subroutine](../../../visual-basic/language-reference/statements/sub-statement.md).</span></span>  
  
 <span data-ttu-id="86c05-123">Visual Studio で生成された XML ファイルを使用する[IntelliSense](/visualstudio/ide/using-intellisense)機能をサポートするアセンブリと同じである XML ファイルのファイル名を使用します。</span><span class="sxs-lookup"><span data-stu-id="86c05-123">To use the generated XML file with the Visual Studio [IntelliSense](/visualstudio/ide/using-intellisense) feature, let the file name of the XML file be the same as the assembly you want to support.</span></span> <span data-ttu-id="86c05-124">.Xml ファイルにも見つかるアセンブリは、Visual Studio プロジェクトで参照されるとき、に、アセンブリと同じディレクトリに XML ファイルが確認します。</span><span class="sxs-lookup"><span data-stu-id="86c05-124">Make sure the XML file is in the same directory as the assembly so that when the assembly is referenced in the Visual Studio project, the .xml file is found as well.</span></span> <span data-ttu-id="86c05-125">XML ドキュメント ファイルは、コード プロジェクト内、またはプロジェクトによって参照されているプロジェクト内で動作する IntelliSense の必要はありません。</span><span class="sxs-lookup"><span data-stu-id="86c05-125">XML documentation files are not required for IntelliSense to work for code within a project or within projects referenced by a project.</span></span>  
  
 <span data-ttu-id="86c05-126">コンパイルしない限り`/target:module`、XML ファイルには、タグが含まれています。`<assembly></assembly>`します。</span><span class="sxs-lookup"><span data-stu-id="86c05-126">Unless you compile with `/target:module`, the XML file contains the tags `<assembly></assembly>`.</span></span> <span data-ttu-id="86c05-127">これらのタグは、コンパイルの出力ファイルのアセンブリ マニフェストを含むファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="86c05-127">These tags specify the name of the file containing the assembly manifest for the output file of the compilation.</span></span>  
  
 <span data-ttu-id="86c05-128">参照してください[XML コメント タグ](../../../visual-basic/language-reference/xmldoc/index.md)コードのコメントからドキュメントを生成する方法について。</span><span class="sxs-lookup"><span data-stu-id="86c05-128">See [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/index.md) for ways to generate documentation from comments in your code.</span></span>  
  
|<span data-ttu-id="86c05-129">設定されているドキュメントは、Visual studio 統合開発環境</span><span class="sxs-lookup"><span data-stu-id="86c05-129">To set -doc in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="86c05-130">1.**ソリューション エクスプローラー**でプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="86c05-130">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="86c05-131">**[プロジェクト]** メニューの **[プロパティ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86c05-131">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="86c05-132">2.**[コンパイル]** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="86c05-132">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="86c05-133">3.値を設定、**生成 XML ドキュメント ファイル**ボックス。</span><span class="sxs-lookup"><span data-stu-id="86c05-133">3.  Set the value in the **Generate XML documentation file** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="86c05-134">例</span><span class="sxs-lookup"><span data-stu-id="86c05-134">Example</span></span>  
 <span data-ttu-id="86c05-135">参照してください[xml コードの文書化](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md)サンプルについては、します。</span><span class="sxs-lookup"><span data-stu-id="86c05-135">See [Documenting Your Code with XML](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md) for a sample.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86c05-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="86c05-136">See Also</span></span>  
 [<span data-ttu-id="86c05-137">Visual Basic のコマンド ライン コンパイラ</span><span class="sxs-lookup"><span data-stu-id="86c05-137">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="86c05-138">XML の使用によるコードのドキュメントの作成</span><span class="sxs-lookup"><span data-stu-id="86c05-138">Documenting Your Code with XML</span></span>](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md)
