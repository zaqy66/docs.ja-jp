---
title: 'チュートリアル: WPF での Windows フォーム コントロールのホスト'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hosting Windows Forms control in WPF [WPF]
ms.assetid: 9cb88415-39b0-4c46-80c4-ff325b674286
ms.openlocfilehash: fcf2b4bd552a8c718ebd4d3f5c06ad7af8efd2a2
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/18/2018
ms.locfileid: "46001130"
---
# <a name="walkthrough-hosting-a-windows-forms-control-in-wpf"></a><span data-ttu-id="48cc6-102">チュートリアル: WPF での Windows フォーム コントロールのホスト</span><span class="sxs-lookup"><span data-stu-id="48cc6-102">Walkthrough: Hosting a Windows Forms Control in WPF</span></span>
[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]<span data-ttu-id="48cc6-103"> 豊富な機能セットには、多くのコントロールを提供します。</span><span class="sxs-lookup"><span data-stu-id="48cc6-103"> provides many controls with a rich feature set.</span></span> <span data-ttu-id="48cc6-104">ただしを使用する可能性がありますも[!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]のコントロールに対して、[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]ページ。</span><span class="sxs-lookup"><span data-stu-id="48cc6-104">However, you may sometimes want to use [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls on your [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] pages.</span></span> <span data-ttu-id="48cc6-105">たとえば、既存のかなりの投資を必要に応じて[!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]コントロール、またはする必要があります、[!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]独自の機能を提供するコントロール。</span><span class="sxs-lookup"><span data-stu-id="48cc6-105">For example, you may have a substantial investment in existing [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls, or you may have a [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] control that provides unique functionality.</span></span>  
  
 <span data-ttu-id="48cc6-106">このチュートリアルは、ホストする方法を示します、 [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] <xref:System.Windows.Forms.MaskedTextBox?displayProperty=nameWithType>の control 権限、[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]コードを使用してページ。</span><span class="sxs-lookup"><span data-stu-id="48cc6-106">This walkthrough shows you how to host a [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]<xref:System.Windows.Forms.MaskedTextBox?displayProperty=nameWithType> control on a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] page by using code.</span></span>  
  
 <span data-ttu-id="48cc6-107">このチュートリアルで示すタスクの完全なコード一覧については、次を参照してください。 [WPF のサンプルでの Windows フォーム コントロールをホストしている](https://go.microsoft.com/fwlink/?LinkID=160057)します。</span><span class="sxs-lookup"><span data-stu-id="48cc6-107">For a complete code listing of the tasks shown in this walkthrough, see [Hosting a Windows Forms Control in WPF Sample](https://go.microsoft.com/fwlink/?LinkID=160057).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="48cc6-108">必須コンポーネント</span><span class="sxs-lookup"><span data-stu-id="48cc6-108">Prerequisites</span></span>  
 <span data-ttu-id="48cc6-109">このチュートリアルを実行するには、次のコンポーネントが必要です。</span><span class="sxs-lookup"><span data-stu-id="48cc6-109">You need the following components to complete this walkthrough:</span></span>  
  
-   [!INCLUDE[vs_dev10_long](../../../../includes/vs-dev10-long-md.md)]<span data-ttu-id="48cc6-110">。</span><span class="sxs-lookup"><span data-stu-id="48cc6-110">.</span></span>  
  
## <a name="hosting-the-windows-forms-control"></a><span data-ttu-id="48cc6-111">Windows フォームのコントロールのホスト</span><span class="sxs-lookup"><span data-stu-id="48cc6-111">Hosting the Windows Forms Control</span></span>  
  
#### <a name="to-host-the-maskedtextbox-control"></a><span data-ttu-id="48cc6-112">MaskedTextBox コントロールをホストするには</span><span class="sxs-lookup"><span data-stu-id="48cc6-112">To host the MaskedTextBox control</span></span>  
  
1.  <span data-ttu-id="48cc6-113">という名前の WPF アプリケーション プロジェクトを作成する`HostingWfInWpf`します。</span><span class="sxs-lookup"><span data-stu-id="48cc6-113">Create a WPF Application project named `HostingWfInWpf`.</span></span>  
  
2.  <span data-ttu-id="48cc6-114">次のアセンブリへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="48cc6-114">Add references to the following assemblies.</span></span>  
  
    -   <span data-ttu-id="48cc6-115">WindowsFormsIntegration</span><span class="sxs-lookup"><span data-stu-id="48cc6-115">WindowsFormsIntegration</span></span>  
  
    -   <span data-ttu-id="48cc6-116">System.Windows.Forms</span><span class="sxs-lookup"><span data-stu-id="48cc6-116">System.Windows.Forms</span></span>  
  
3.  <span data-ttu-id="48cc6-117">MainWindow.xaml を開き、[!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)]します。</span><span class="sxs-lookup"><span data-stu-id="48cc6-117">Open MainWindow.xaml in the [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].</span></span>  
  
4.  <span data-ttu-id="48cc6-118">名前、<xref:System.Windows.Controls.Grid>要素`grid1`します。</span><span class="sxs-lookup"><span data-stu-id="48cc6-118">Name the <xref:System.Windows.Controls.Grid> element `grid1`.</span></span>  
  
     [!code-xaml[HostingWfInWPF#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HostingWfInWPF/CSharp/HostingWfInWPF/Window1.xaml#1)]  
  
5.  <span data-ttu-id="48cc6-119">デザイン ビューまたは XAML ビューで、選択、<xref:System.Windows.Window>要素。</span><span class="sxs-lookup"><span data-stu-id="48cc6-119">In Design view or XAML view, select the <xref:System.Windows.Window> element.</span></span>  
  
6.  <span data-ttu-id="48cc6-120">[プロパティ] ウィンドウ、**イベント**タブ。</span><span class="sxs-lookup"><span data-stu-id="48cc6-120">In the Properties window, click the **Events** tab.</span></span>  
  
7.  <span data-ttu-id="48cc6-121">ダブルクリックして、<xref:System.Windows.FrameworkElement.Loaded>イベント。</span><span class="sxs-lookup"><span data-stu-id="48cc6-121">Double-click the <xref:System.Windows.FrameworkElement.Loaded> event.</span></span>  
  
8.  <span data-ttu-id="48cc6-122">処理するために次のコードを挿入、<xref:System.Windows.FrameworkElement.Loaded>イベント。</span><span class="sxs-lookup"><span data-stu-id="48cc6-122">Insert the following code to handle the <xref:System.Windows.FrameworkElement.Loaded> event.</span></span>  
  
     [!code-csharp[HostingWfInWPF#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HostingWfInWPF/CSharp/HostingWfInWPF/Window1.xaml.cs#10)]
     [!code-vb[HostingWfInWPF#10](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HostingWfInWPF/VisualBasic/HostingWfInWpf/Window1.xaml.vb#10)]  
  
9. <span data-ttu-id="48cc6-123">次のコードを追加、ファイルの上部にある`Imports`または`using`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="48cc6-123">At the top of the file, add the following `Imports` or `using` statement.</span></span>  
  
     [!code-csharp[HostingWfInWPF#11](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HostingWfInWPF/CSharp/HostingWfInWPF/Window1.xaml.cs#11)]
     [!code-vb[HostingWfInWPF#11](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HostingWfInWPF/VisualBasic/HostingWfInWpf/Window1.xaml.vb#11)]  
  
10. <span data-ttu-id="48cc6-124">F5 キーを押してアプリケーションをビルドし、実行します。</span><span class="sxs-lookup"><span data-stu-id="48cc6-124">Press F5 to build and run the application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48cc6-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="48cc6-125">See Also</span></span>  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 [<span data-ttu-id="48cc6-126">Visual Studio で XAML をデザインする</span><span class="sxs-lookup"><span data-stu-id="48cc6-126">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)  
 [<span data-ttu-id="48cc6-127">チュートリアル: WPF での XAML を使用した Windows フォーム コントロールのホスト</span><span class="sxs-lookup"><span data-stu-id="48cc6-127">Walkthrough: Hosting a Windows Forms Control in WPF by Using XAML</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-control-in-wpf-by-using-xaml.md)  
 [<span data-ttu-id="48cc6-128">チュートリアル: WPF での Windows フォーム複合コントロールのホスト</span><span class="sxs-lookup"><span data-stu-id="48cc6-128">Walkthrough: Hosting a Windows Forms Composite Control in WPF</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-composite-control-in-wpf.md)  
 [<span data-ttu-id="48cc6-129">チュートリアル: Windows フォームでの WPF 複合コントロールのホスト</span><span class="sxs-lookup"><span data-stu-id="48cc6-129">Walkthrough: Hosting a WPF Composite Control in Windows Forms</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)  
 [<span data-ttu-id="48cc6-130">Windows フォーム コントロールおよび同等の WPF コントロール</span><span class="sxs-lookup"><span data-stu-id="48cc6-130">Windows Forms Controls and Equivalent WPF Controls</span></span>](../../../../docs/framework/wpf/advanced/windows-forms-controls-and-equivalent-wpf-controls.md)  
 [<span data-ttu-id="48cc6-131">WPF のサンプル Windows フォーム コントロールのホスト</span><span class="sxs-lookup"><span data-stu-id="48cc6-131">Hosting a Windows Forms Control in WPF Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160057)
