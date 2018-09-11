---
title: '方法 : Windows フォーム コントロールでユーザー入力イベントを処理する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms controls, user input
- user input [Windows Forms], Windows Forms controls
ms.assetid: 3de74dcf-fae3-42d0-92b5-bc04a61a6888
ms.openlocfilehash: 3b15edfec25282d5a0b79ef48cabd2a27c694055
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44367302"
---
# <a name="how-to-handle-user-input-events-in-windows-forms-controls"></a><span data-ttu-id="ab99f-102">方法 : Windows フォーム コントロールでユーザー入力イベントを処理する</span><span class="sxs-lookup"><span data-stu-id="ab99f-102">How to: Handle User Input Events in Windows Forms Controls</span></span>
<span data-ttu-id="ab99f-103">この例では、Windows フォーム コントロールで発生する可能性がある、ほとんどのキーボード、マウス、フォーカス、および検証イベントを処理する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ab99f-103">This example demonstrates how to handle most keyboard, mouse, focus, and validation events that can occur in a Windows Forms control.</span></span> <span data-ttu-id="ab99f-104">`TextBoxInput` という名前のテキスト ボックスは、フォーカスがあるときにイベントを受け取り、各イベントに関する情報は、イベントが発生する順序で、`TextBoxOutput` という名前のテキスト ボックスに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="ab99f-104">The text box named `TextBoxInput` receives the events when it has focus, and information about each event is written in the text box named `TextBoxOutput` in the order in which the events are raised.</span></span> <span data-ttu-id="ab99f-105">アプリケーションには、レポートするイベントをフィルター処理するために使用できるチェック ボックスのセットも含まれています。</span><span class="sxs-lookup"><span data-stu-id="ab99f-105">The application also includes a set of check boxes that can be used to filter which events to report.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ab99f-106">例</span><span class="sxs-lookup"><span data-stu-id="ab99f-106">Example</span></span>  
 [!code-cpp[System.Windows.Forms.UserInputWalkthrough#0](../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.UserInputWalkthrough/cpp/form1.cpp#0)]
 [!code-csharp[System.Windows.Forms.UserInputWalkthrough#0](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.UserInputWalkthrough/CS/form1.cs#0)]
 [!code-vb[System.Windows.Forms.UserInputWalkthrough#0](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.UserInputWalkthrough/VB/form1.vb#0)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="ab99f-107">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="ab99f-107">Compiling the Code</span></span>  
 <span data-ttu-id="ab99f-108">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ab99f-108">This example requires:</span></span>  
  
-   <span data-ttu-id="ab99f-109">System、System.Drawing、および System.Windows.Forms の各アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="ab99f-109">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="ab99f-110">コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。</span><span class="sxs-lookup"><span data-stu-id="ab99f-110">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="ab99f-111">新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="ab99f-111">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="ab99f-112">「[方法: 完成した Windows フォーム コードの例を Visual Studio を使ってコンパイルして実行する](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))」も参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab99f-112">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab99f-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab99f-113">See Also</span></span>  
 [<span data-ttu-id="ab99f-114">Windows フォームでのユーザー入力</span><span class="sxs-lookup"><span data-stu-id="ab99f-114">User Input in Windows Forms</span></span>](../../../docs/framework/winforms/user-input-in-windows-forms.md)
