---
title: '方法 : BindingSource を使用して Windows フォーム コントロール内にデータ ソースの更新を反映させる'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- data binding [Windows Forms], updating
- BindingSource component [Windows Forms], updating data binding
- examples [Windows Forms], BindingSource component
- data sources [Windows Forms], updating
- BindingSource component [Windows Forms], examples
ms.assetid: bd8bd9b2-af8a-4f11-a3d5-54eecbe2400b
ms.openlocfilehash: 95e17675011b7e4d628b980fc0cbf15a50ce3932
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44061274"
---
# <a name="how-to-reflect-data-source-updates-in-a-windows-forms-control-with-the-bindingsource"></a><span data-ttu-id="7dbe5-102">方法 : BindingSource を使用して Windows フォーム コントロール内にデータ ソースの更新を反映させる</span><span class="sxs-lookup"><span data-stu-id="7dbe5-102">How to: Reflect Data Source Updates in a Windows Forms Control with the BindingSource</span></span>
<span data-ttu-id="7dbe5-103">データ バインド コントロールを使用する場合、データ ソースがリスト変更イベントを発生させないことがあります。そのようなケースで、データ ソース内の変更に応答する必要が生じることがあります。</span><span class="sxs-lookup"><span data-stu-id="7dbe5-103">When you use data-bound controls, you sometimes have to respond to changes in the data source when the data source does not raise list-changed events.</span></span> <span data-ttu-id="7dbe5-104"><xref:System.Windows.Forms.BindingSource> コンポーネントを使用してデータ ソースを Windows フォーム コントロールにバインドすれば、データ ソースが変更されたことを <xref:System.Windows.Forms.BindingSource.ResetBindings%2A> メソッドを呼び出すことによってコントロールに通知できます。</span><span class="sxs-lookup"><span data-stu-id="7dbe5-104">When you use the <xref:System.Windows.Forms.BindingSource> component to bind your data source to a Windows Forms control, you can notify the control that your data source has changed by calling the <xref:System.Windows.Forms.BindingSource.ResetBindings%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7dbe5-105">例</span><span class="sxs-lookup"><span data-stu-id="7dbe5-105">Example</span></span>  
 <span data-ttu-id="7dbe5-106">次のコード例では、バインドされたコントロールにデータ ソース内の更新について <xref:System.Windows.Forms.BindingSource.ResetBindings%2A> メソッドを使用して通知する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7dbe5-106">The following code example demonstrates using the <xref:System.Windows.Forms.BindingSource.ResetBindings%2A> method to notify a bound control about an update in the data source.</span></span>  
  
 [!code-cpp[System.Windows.Forms.DataConnector.ResetBindings#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.ResetBindings/CPP/form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.DataConnector.ResetBindings#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.ResetBindings/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataConnector.ResetBindings#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.ResetBindings/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="7dbe5-107">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="7dbe5-107">Compiling the Code</span></span>  
 <span data-ttu-id="7dbe5-108">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7dbe5-108">This example requires:</span></span>  
  
-   <span data-ttu-id="7dbe5-109">System、System.Drawing、および System.Windows.Forms の各アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="7dbe5-109">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="7dbe5-110">コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。</span><span class="sxs-lookup"><span data-stu-id="7dbe5-110">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="7dbe5-111">新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="7dbe5-111">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="7dbe5-112">「[方法: 完成した Windows フォーム コードの例を Visual Studio を使ってコンパイルして実行する](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))」も参照してください。</span><span class="sxs-lookup"><span data-stu-id="7dbe5-112">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7dbe5-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="7dbe5-113">See Also</span></span>  
 <xref:System.Windows.Forms.BindingNavigator>  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.BindingSource>  
 [<span data-ttu-id="7dbe5-114">BindingSource コンポーネント</span><span class="sxs-lookup"><span data-stu-id="7dbe5-114">BindingSource Component</span></span>](../../../../docs/framework/winforms/controls/bindingsource-component.md)  
 [<span data-ttu-id="7dbe5-115">方法: Windows フォーム コントロールを型にバインドする</span><span class="sxs-lookup"><span data-stu-id="7dbe5-115">How to: Bind a Windows Forms Control to a Type</span></span>](../../../../docs/framework/winforms/controls/how-to-bind-a-windows-forms-control-to-a-type.md)
