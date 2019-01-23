---
title: '方法: ローカリゼーションに対応する Windows フォーム レイアウトをデザインします。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms]
- application design [Windows Forms], localization
- Windows Forms, localization
- localization [Windows Forms], Windows Forms layout
ms.assetid: d13eff2d-701c-4b6e-8838-3885cbfb7223
ms.openlocfilehash: 15f290f7d076eede7a8092d7295df810e4e51bf3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54563523"
---
# <a name="how-to-design-a-windows-forms-layout-that-responds-well-to-localization"></a><span data-ttu-id="389f2-102">方法: ローカリゼーションに対応する Windows フォーム レイアウトをデザインします。</span><span class="sxs-lookup"><span data-stu-id="389f2-102">How to: Design a Windows Forms Layout that Responds Well to Localization</span></span>
<span data-ttu-id="389f2-103">ローカライズが可能なフォームを作成すると、各国市場向けの開発期間が大幅に短縮されます。</span><span class="sxs-lookup"><span data-stu-id="389f2-103">Creating forms that are ready to be localized greatly speeds development for international markets.</span></span> <span data-ttu-id="389f2-104"><xref:System.Windows.Forms.TableLayoutPanel> コントロールを使用すると、<xref:System.Windows.Forms.Control.Text%2A> プロパティ値の変更によってコントロールのサイズが変更された際に、これに適切に応答するレイアウトを実装できます</span><span class="sxs-lookup"><span data-stu-id="389f2-104">You can use the <xref:System.Windows.Forms.TableLayoutPanel> control to implement layouts that respond gracefully as controls resize due to changes in their <xref:System.Windows.Forms.Control.Text%2A> property values.</span></span>  
  
## <a name="example"></a><span data-ttu-id="389f2-105">例</span><span class="sxs-lookup"><span data-stu-id="389f2-105">Example</span></span>  
 <span data-ttu-id="389f2-106">このフォームでは、表示される文字列値を他の言語に翻訳するときに、均等に調整されるレイアウトを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="389f2-106">This form demonstrates how to create a layout that proportionally adjusts when you translate displayed string values into other languages.</span></span> <span data-ttu-id="389f2-107">この翻訳プロセスのことを "*ローカリゼーション*" といいます。</span><span class="sxs-lookup"><span data-stu-id="389f2-107">This process of translation is called *localization*.</span></span> <span data-ttu-id="389f2-108">詳細については、「[ローカリゼーション](../../../../docs/standard/globalization-localization/localization.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="389f2-108">For more information, see [Localization](../../../../docs/standard/globalization-localization/localization.md).</span></span>  
  
 <span data-ttu-id="389f2-109">Visual Studio では、このタスクに対する広範なサポートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="389f2-109">There is extensive support for this task in Visual Studio.</span></span>  <span data-ttu-id="389f2-110">参照してください[チュートリアル。ローカライズの縦横比が調整されるレイアウトの作成](https://msdn.microsoft.com/library/7k9fa71y\(v=vs.110\))です。</span><span class="sxs-lookup"><span data-stu-id="389f2-110">See also [Walkthrough: Creating a Layout That Adjusts Proportion for Localization](https://msdn.microsoft.com/library/7k9fa71y\(v=vs.110\)).</span></span>  
  
 [!code-csharp[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/CS/localizableform.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/VB/localizableform.vb#1)]  
  
1.  [<span data-ttu-id="389f2-111">方法: 配置して、コントロールを TableLayoutPanel コントロールで伸縮</span><span class="sxs-lookup"><span data-stu-id="389f2-111">How to: Align and Stretch a Control in a TableLayoutPanel Control</span></span>](how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control.md)  
  
2.  <span data-ttu-id="389f2-112">[チュートリアル: FlowLayoutPanel を使用して Windows フォーム コントロールの配置](https://msdn.microsoft.com/library/z9w7ek2f\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="389f2-112">[Walkthrough: Arranging Controls on Windows Forms Using a FlowLayoutPanel](https://msdn.microsoft.com/library/z9w7ek2f\(v=vs.110\))</span></span>  
  
3.  [<span data-ttu-id="389f2-113">方法: TableLayoutPanel コントロールの行と列にまたがる</span><span class="sxs-lookup"><span data-stu-id="389f2-113">How to: Span Rows and Columns in a TableLayoutPanel Control</span></span>](how-to-span-rows-and-columns-in-a-tablelayoutpanel-control.md)  
  
4.  [<span data-ttu-id="389f2-114">方法: TableLayoutPanel コントロールの列と行を編集します。</span><span class="sxs-lookup"><span data-stu-id="389f2-114">How to: Edit Columns and Rows in a TableLayoutPanel Control</span></span>](how-to-edit-columns-and-rows-in-a-tablelayoutpanel-control.md)  
  
5.  <span data-ttu-id="389f2-115">[チュートリアル: スマートを使用して一般的なタスクを実行する Windows フォーム コントロールをタグ](https://msdn.microsoft.com/library/xhz359sc\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="389f2-115">[Walkthrough: Performing Common Tasks Using Smart Tags on Windows Forms Controls](https://msdn.microsoft.com/library/xhz359sc\(v=vs.110\))</span></span>  
  
6.  <span data-ttu-id="389f2-116">[チュートリアル: TableLayoutPanel を使用して Windows フォーム コントロールの配置](https://msdn.microsoft.com/library/w4yc3e8c\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="389f2-116">[Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel](https://msdn.microsoft.com/library/w4yc3e8c\(v=vs.110\))</span></span>  
  
7.  <span data-ttu-id="389f2-117">[チュートリアル: Windows フォーム コントロール Padding、Margin、および AutoSize プロパティをレイアウト](https://msdn.microsoft.com/library/3z3f9e8b\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="389f2-117">[Walkthrough: Laying Out Windows Forms Controls with Padding, Margins, and the AutoSize Property](https://msdn.microsoft.com/library/3z3f9e8b\(v=vs.110\))</span></span>  
  
8.  <span data-ttu-id="389f2-118">[方法: AutoSize と TableLayoutPanel コントロールを使用して Windows フォームのローカリゼーションをサポートします。](https://msdn.microsoft.com/library/1zkt8b33\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="389f2-118">[How to: Support Localization on Windows Forms Using AutoSize and the TableLayoutPanel Control](https://msdn.microsoft.com/library/1zkt8b33\(v=vs.110\))</span></span>  
  
9. <span data-ttu-id="389f2-119">[チュートリアル: データ エントリのサイズ変更可能な Windows フォームを作成します。](https://msdn.microsoft.com/library/991eahec\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="389f2-119">[Walkthrough: Creating a Resizable Windows Form for Data Entry](https://msdn.microsoft.com/library/991eahec\(v=vs.110\))</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="389f2-120">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="389f2-120">Compiling the Code</span></span>  
 <span data-ttu-id="389f2-121">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="389f2-121">This example requires:</span></span>  
  
-   <span data-ttu-id="389f2-122">System、System.Data、System.Drawing、および System.Windows.Forms の各アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="389f2-122">References to the System, System.Data, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="389f2-123">コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。</span><span class="sxs-lookup"><span data-stu-id="389f2-123">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="389f2-124">新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="389f2-124">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="389f2-125">参照してください[方法。Visual Studio を使用して、完全な Windows フォームのコードの例をコンパイルして](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))します。</span><span class="sxs-lookup"><span data-stu-id="389f2-125">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="389f2-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="389f2-126">See also</span></span>
- <xref:System.Windows.Forms.TableLayoutPanel>
- <xref:System.Windows.Forms.FlowLayoutPanel>
- [<span data-ttu-id="389f2-127">ローカリゼーション</span><span class="sxs-lookup"><span data-stu-id="389f2-127">Localization</span></span>](../../../../docs/standard/globalization-localization/localization.md)
