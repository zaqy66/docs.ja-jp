---
title: '方法: Office プログラミングで名前付き引数と省略可能な引数を使用する - C# プログラミング ガイド'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- named and optional arguments [C#], Office programming
- optional arguments [C#], Office programming
- named arguments [C#], Office programming
ms.assetid: 65b8a222-bcd8-454c-845f-84adff5a356f
ms.openlocfilehash: 20228886cabd47b976506509a29f6cfd50137e5f
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243804"
---
# <a name="how-to-use-named-and-optional-arguments-in-office-programming-c-programming-guide"></a><span data-ttu-id="20eb1-102">方法: Office プログラミングで名前付き引数と省略可能な引数を使用する (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="20eb1-102">How to: Use Named and Optional Arguments in Office Programming (C# Programming Guide)</span></span>
<span data-ttu-id="20eb1-103">[!INCLUDE[csharp_dev10_long](~/includes/csharp-dev10-long-md.md)] で導入された名前付き引数と省略可能な引数を使うと、C# プログラミングの便利さ、柔軟性、読みやすさが向上します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-103">Named arguments and optional arguments, introduced in [!INCLUDE[csharp_dev10_long](~/includes/csharp-dev10-long-md.md)], enhance convenience, flexibility, and readability in C# programming.</span></span> <span data-ttu-id="20eb1-104">さらに、Microsoft Office オートメーション API などの COM インターフェイスへのアクセスが大幅に楽になります。</span><span class="sxs-lookup"><span data-stu-id="20eb1-104">In addition, these features greatly facilitate access to COM interfaces such as the Microsoft Office automation APIs.</span></span>  
  
 <span data-ttu-id="20eb1-105">次の例の [ConvertToTable](<xref:Microsoft.Office.Interop.Word.Range.ConvertToTable%2A>) メソッドには、列と行の数、書式設定、罫線、フォント、色など、テーブルの特性を表す 16 個のパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="20eb1-105">In the following example, method [ConvertToTable](<xref:Microsoft.Office.Interop.Word.Range.ConvertToTable%2A>) has sixteen parameters that represent characteristics of a table, such as number of columns and rows, formatting, borders, fonts, and colors.</span></span> <span data-ttu-id="20eb1-106">ほとんどの場合はこれらすべての特性に具体的な値を指定することはないので、16 個のパラメーターはすべて省略可能です。</span><span class="sxs-lookup"><span data-stu-id="20eb1-106">All sixteen parameters are optional, because most of the time you do not want to specify particular values for all of them.</span></span> <span data-ttu-id="20eb1-107">しかし、名前付きの省略可能な引数を使わないと、各パラメーターに値またはプレースホルダー値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20eb1-107">However, without named and optional arguments, a value or a placeholder value has to be provided for each parameter.</span></span> <span data-ttu-id="20eb1-108">名前付きの省略可能な引数を使うと、プロジェクトに必要なパラメーターの値だけを指定できます。</span><span class="sxs-lookup"><span data-stu-id="20eb1-108">With named and optional arguments, you specify values only for the parameters that are required for your project.</span></span>  
  
 <span data-ttu-id="20eb1-109">以下の手順を行うには、Microsoft Office Word がコンピューターにインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="20eb1-109">You must have Microsoft Office Word installed on your computer to complete these procedures.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-new-console-application"></a><span data-ttu-id="20eb1-110">新しいコンソール アプリケーションを作成するには</span><span class="sxs-lookup"><span data-stu-id="20eb1-110">To create a new console application</span></span>  
  
1.  <span data-ttu-id="20eb1-111">Visual Studio を起動します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-111">Start Visual Studio.</span></span>  
  
2.  <span data-ttu-id="20eb1-112">**[ファイル]** メニューの **[新規作成]** をポイントし、 **[プロジェクト]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20eb1-112">On the **File** menu, point to **New**, and then click **Project**.</span></span>  
  
3.  <span data-ttu-id="20eb1-113">**[Templates Categories (テンプレート カテゴリ)]** ウィンドウで、**[Visual C#]** を展開し、**[Windows]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20eb1-113">In the **Templates Categories** pane, expand **Visual C#**, and then click **Windows**.</span></span>  
  
4.  <span data-ttu-id="20eb1-114">**[テンプレート]** ウィンドウの上部で、**[ターゲット フレームワーク]** ボックスに **[.NET Framework 4]** が表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-114">Look in the top of the **Templates** pane to make sure that **.NET Framework 4** appears in the **Target Framework** box.</span></span>  
  
5.  <span data-ttu-id="20eb1-115">**[テンプレート]** ウィンドウで **[コンソール アプリケーション]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20eb1-115">In the **Templates** pane, click **Console Application**.</span></span>  
  
6.  <span data-ttu-id="20eb1-116">**[名前]** フィールドに、プロジェクトの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-116">Type a name for your project in the **Name** field.</span></span>  
  
7.  <span data-ttu-id="20eb1-117">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20eb1-117">Click **OK**.</span></span>  
  
     <span data-ttu-id="20eb1-118">**ソリューション エクスプローラー**に新しいプロジェクトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="20eb1-118">The new project appears in **Solution Explorer**.</span></span>  
  
### <a name="to-add-a-reference"></a><span data-ttu-id="20eb1-119">参照を追加するには</span><span class="sxs-lookup"><span data-stu-id="20eb1-119">To add a reference</span></span>  
  
1.  <span data-ttu-id="20eb1-120">**ソリューション エクスプローラー**で、プロジェクトの名前を右クリックし、**[参照の追加]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20eb1-120">In **Solution Explorer**, right-click your project's name and then click **Add Reference**.</span></span> <span data-ttu-id="20eb1-121">**[参照の追加]** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="20eb1-121">The **Add Reference** dialog box appears.</span></span>  
  
2.  <span data-ttu-id="20eb1-122">**[.NET]** ページの **[コンポーネント名]** の一覧で、**Microsoft.Office.Interop.Word** を選びます。</span><span class="sxs-lookup"><span data-stu-id="20eb1-122">On the **.NET** page, select **Microsoft.Office.Interop.Word** in the **Component Name** list.</span></span>  
  
3.  <span data-ttu-id="20eb1-123">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20eb1-123">Click **OK**.</span></span>  
  
### <a name="to-add-necessary-using-directives"></a><span data-ttu-id="20eb1-124">ディレクティブを使用して必要なものを追加するには</span><span class="sxs-lookup"><span data-stu-id="20eb1-124">To add necessary using directives</span></span>  
  
1.  <span data-ttu-id="20eb1-125">**ソリューション エクスプローラー**で、**Program.cs** ファイルを右クリックし、**[コードの表示]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20eb1-125">In **Solution Explorer**, right-click the **Program.cs** file and then click **View Code**.</span></span>  
  
2.  <span data-ttu-id="20eb1-126">次の `using` ディレクティブをコード ファイルの先頭に追加します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-126">Add the following `using` directives to the top of the code file.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#4](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_1.cs)]  
  
### <a name="to-display-text-in-a-word-document"></a><span data-ttu-id="20eb1-127">Word 文書にテキストを表示するには</span><span class="sxs-lookup"><span data-stu-id="20eb1-127">To display text in a Word document</span></span>  
  
1.  <span data-ttu-id="20eb1-128">Program.cs の `Program` クラスに、Word アプリケーションと Word 文書を作成する次のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-128">In the `Program` class in Program.cs, add the following method to create a Word application and a Word document.</span></span> <span data-ttu-id="20eb1-129">[Add](<xref:Microsoft.Office.Interop.Word.Documents.Add%2A>) メソッドには、4 つの省略可能なパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="20eb1-129">The [Add](<xref:Microsoft.Office.Interop.Word.Documents.Add%2A>) method has four optional parameters.</span></span> <span data-ttu-id="20eb1-130">この例では、それらの既定値を使います。</span><span class="sxs-lookup"><span data-stu-id="20eb1-130">This example uses their default values.</span></span> <span data-ttu-id="20eb1-131">そのため、呼び出しステートメントに引数は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="20eb1-131">Therefore, no arguments are necessary in the calling statement.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#6](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_2.cs)]  
  
2.  <span data-ttu-id="20eb1-132">文書内でテキストを表示する場所と表示するテキストを定義する次のコードを、メソッドの最後に追加します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-132">Add the following code at the end of the method to define where to display text in the document, and what text to display.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#7](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_3.cs)]  
  
### <a name="to-run-the-application"></a><span data-ttu-id="20eb1-133">アプリケーションを実行するには</span><span class="sxs-lookup"><span data-stu-id="20eb1-133">To run the application</span></span>  
  
1.  <span data-ttu-id="20eb1-134">次のステートメントを Main に追加します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-134">Add the following statement to Main.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#8](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_4.cs)]  
  
2.  <span data-ttu-id="20eb1-135">Ctrl キーを押しながら F5 キーを押してプロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-135">Press CTRL+F5 to run the project.</span></span> <span data-ttu-id="20eb1-136">指定したテキストを含む Word 文書が表示されます。</span><span class="sxs-lookup"><span data-stu-id="20eb1-136">A Word document appears that contains the specified text.</span></span>  
  
### <a name="to-change-the-text-to-a-table"></a><span data-ttu-id="20eb1-137">テキストをテーブルに変更するには</span><span class="sxs-lookup"><span data-stu-id="20eb1-137">To change the text to a table</span></span>  
  
1.  <span data-ttu-id="20eb1-138">`ConvertToTable` メソッドを使って、テーブル内のテキストを囲みます。</span><span class="sxs-lookup"><span data-stu-id="20eb1-138">Use the `ConvertToTable` method to enclose the text in a table.</span></span> <span data-ttu-id="20eb1-139">このメソッドには、16 個の省略可能なパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="20eb1-139">The method has sixteen optional parameters.</span></span> <span data-ttu-id="20eb1-140">次の例に示すように、IntelliSense では省略可能なパラメーターは角かっこで囲まれています。</span><span class="sxs-lookup"><span data-stu-id="20eb1-140">IntelliSense encloses optional parameters in brackets, as shown in the following illustration.</span></span>  
  
     <span data-ttu-id="20eb1-141">![ConvertToTable メソッドのパラメーターのリスト。](../../../csharp/programming-guide/classes-and-structs/media/convert_tableparameters.png "Convert_TableParameters")</span><span class="sxs-lookup"><span data-stu-id="20eb1-141">![List of parameters for ConvertToTable method.](../../../csharp/programming-guide/classes-and-structs/media/convert_tableparameters.png "Convert_TableParameters")</span></span>  
<span data-ttu-id="20eb1-142">ConvertToTable のパラメーター</span><span class="sxs-lookup"><span data-stu-id="20eb1-142">ConvertToTable parameters</span></span>  
  
     <span data-ttu-id="20eb1-143">名前付きの省略可能な引数を使うと、変更するパラメーターの値だけを指定できます。</span><span class="sxs-lookup"><span data-stu-id="20eb1-143">Named and optional arguments enable you to specify values for only the parameters that you want to change.</span></span> <span data-ttu-id="20eb1-144">簡単なテーブルを作成するには、`DisplayInWord` メソッドの最後に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-144">Add the following code to the end of method `DisplayInWord` to create a simple table.</span></span> <span data-ttu-id="20eb1-145">この引数は、`range` 内のテキスト文字列のコンマがテーブルのセルを区切ることを指定します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-145">The argument specifies that the commas in the text string in `range` separate the cells of the table.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#9](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_5.cs)]  
  
     <span data-ttu-id="20eb1-146">以前のバージョンの C# で `ConvertToTable` を呼び出すには、次のコードで示すように、パラメーターごとに参照引数が必要です。</span><span class="sxs-lookup"><span data-stu-id="20eb1-146">In earlier versions of C#, the call to `ConvertToTable` requires a reference argument for each parameter, as shown in the following code.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#14](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_6.cs)]  
  
2.  <span data-ttu-id="20eb1-147">Ctrl キーを押しながら F5 キーを押してプロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-147">Press CTRL+F5 to run the project.</span></span>  
  
### <a name="to-experiment-with-other-parameters"></a><span data-ttu-id="20eb1-148">他のパラメーターを調べるには</span><span class="sxs-lookup"><span data-stu-id="20eb1-148">To experiment with other parameters</span></span>  
  
1.  <span data-ttu-id="20eb1-149">テーブルを 1 列 3 行に変更するには、`DisplayInWord` の最後の行を次のステートメントに置き換えてから、Ctrl + F5 キーを押します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-149">To change the table so that it has one column and three rows, replace the last line in `DisplayInWord` with the following statement and then type CTRL+F5.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#10](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_7.cs)]  
  
2.  <span data-ttu-id="20eb1-150">テーブルに対して定義済みの書式を指定するには、`DisplayInWord` の最後の行を次のステートメントに置き換えてから、Ctrl + F5 キーを押します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-150">To specify a predefined format for the table, replace the last line in `DisplayInWord` with the following statement and then type CTRL+F5.</span></span> <span data-ttu-id="20eb1-151">書式には、[WdTableFormat](<xref:Microsoft.Office.Interop.Word.WdTableFormat>) 定数のどれでも指定できます。</span><span class="sxs-lookup"><span data-stu-id="20eb1-151">The format can be any of the [WdTableFormat](<xref:Microsoft.Office.Interop.Word.WdTableFormat>) constants.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#11](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_8.cs)]  
  
## <a name="example"></a><span data-ttu-id="20eb1-152">例</span><span class="sxs-lookup"><span data-stu-id="20eb1-152">Example</span></span>  
 <span data-ttu-id="20eb1-153">ここまでの例をすべて含んだコードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="20eb1-153">The following code includes the full example.</span></span>  
  
 [!code-csharp[csProgGuideNamedAndOptional#12](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_9.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="20eb1-154">参照</span><span class="sxs-lookup"><span data-stu-id="20eb1-154">See Also</span></span>

- [<span data-ttu-id="20eb1-155">名前付き引数と省略可能な引数</span><span class="sxs-lookup"><span data-stu-id="20eb1-155">Named and Optional Arguments</span></span>](../../../csharp/programming-guide/classes-and-structs/named-and-optional-arguments.md)
