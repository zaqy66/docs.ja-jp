---
title: Windows フォーム コントロールおよび同等の WPF コントロール
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms [WPF], interoperability with
- Windows Forms [WPF], WPF interoperation
- interoperability [WPF], Windows Forms
ms.assetid: 8a157e6b-8054-46db-a5cf-a78966acc7a1
ms.openlocfilehash: 0daa399e2d000a228773ee20f157af7439f7acbb
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43396668"
---
# <a name="windows-forms-controls-and-equivalent-wpf-controls"></a><span data-ttu-id="64a8f-102">Windows フォーム コントロールおよび同等の WPF コントロール</span><span class="sxs-lookup"><span data-stu-id="64a8f-102">Windows Forms Controls and Equivalent WPF Controls</span></span>
<span data-ttu-id="64a8f-103">多く[!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]コントロールと同等のある[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]、コントロールではなく一部[!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]コントロールに相当するあるありません[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]します。</span><span class="sxs-lookup"><span data-stu-id="64a8f-103">Many [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls have equivalent [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] controls, but some [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls have no equivalents in [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)].</span></span> <span data-ttu-id="64a8f-104">このトピックでは、2 つのテクノロジによって提供されるコントロールの型を比較します。</span><span class="sxs-lookup"><span data-stu-id="64a8f-104">This topic compares control types provided by the two technologies.</span></span>  
  
 <span data-ttu-id="64a8f-105">ホストの相互運用性を常に使用することができます[!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]に相当するを持たないコントロール、 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]-ベースのアプリケーション。</span><span class="sxs-lookup"><span data-stu-id="64a8f-105">You can always use interoperation to host [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls that do not have equivalents in your [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]-based applications.</span></span>  
  
 <span data-ttu-id="64a8f-106">次の表では[!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]コントロールとコンポーネントがあると同等[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]機能を制御します。</span><span class="sxs-lookup"><span data-stu-id="64a8f-106">The following table shows which [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls and components have equivalent [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] control functionality.</span></span>  
  
|<span data-ttu-id="64a8f-107">Windows フォーム コントロール</span><span class="sxs-lookup"><span data-stu-id="64a8f-107">Windows Forms control</span></span>|<span data-ttu-id="64a8f-108">同等の WPF コントロール</span><span class="sxs-lookup"><span data-stu-id="64a8f-108">WPF equivalent control</span></span>|<span data-ttu-id="64a8f-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="64a8f-109">Remarks</span></span>|  
|---------------------------|----------------------------|-------------|  
|<xref:System.Windows.Forms.BindingNavigator>|<span data-ttu-id="64a8f-110">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-110">No equivalent control.</span></span>||  
|<xref:System.Windows.Forms.BindingSource>|<xref:System.Windows.Data.CollectionViewSource>||  
|<xref:System.Windows.Forms.Button>|<xref:System.Windows.Controls.Button>||  
|<xref:System.Windows.Forms.CheckBox>|<xref:System.Windows.Controls.CheckBox>||  
|<xref:System.Windows.Forms.CheckedListBox>|<span data-ttu-id="64a8f-111"><xref:System.Windows.Controls.ListBox> で合成します。</span><span class="sxs-lookup"><span data-stu-id="64a8f-111"><xref:System.Windows.Controls.ListBox> with composition.</span></span>||  
|<xref:System.Windows.Forms.ColorDialog>|<span data-ttu-id="64a8f-112">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-112">No equivalent control.</span></span>||  
|<xref:System.Windows.Forms.ComboBox>|<xref:System.Windows.Controls.ComboBox>|<span data-ttu-id="64a8f-113"><xref:System.Windows.Controls.ComboBox> オート コンプリートをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="64a8f-113"><xref:System.Windows.Controls.ComboBox> does not support auto-complete.</span></span>|  
|<xref:System.Windows.Forms.ContextMenuStrip>|<xref:System.Windows.Controls.ContextMenu>||  
|<xref:System.Windows.Forms.DataGridView>|<xref:System.Windows.Controls.DataGrid>||  
|<xref:System.Windows.Forms.DateTimePicker>|<xref:System.Windows.Controls.DatePicker>||  
|<xref:System.Windows.Forms.DomainUpDown>|<span data-ttu-id="64a8f-114"><xref:System.Windows.Controls.TextBox> 2 つと<xref:System.Windows.Controls.Primitives.RepeatButton>コントロール。</span><span class="sxs-lookup"><span data-stu-id="64a8f-114"><xref:System.Windows.Controls.TextBox> and two <xref:System.Windows.Controls.Primitives.RepeatButton> controls.</span></span>||  
|<xref:System.Windows.Forms.ErrorProvider>|<span data-ttu-id="64a8f-115">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-115">No equivalent control.</span></span>||  
|<xref:System.Windows.Forms.FlowLayoutPanel>|<span data-ttu-id="64a8f-116"><xref:System.Windows.Controls.WrapPanel> または <xref:System.Windows.Controls.StackPanel></span><span class="sxs-lookup"><span data-stu-id="64a8f-116"><xref:System.Windows.Controls.WrapPanel> or <xref:System.Windows.Controls.StackPanel></span></span>||  
|<xref:System.Windows.Forms.FolderBrowserDialog>|<span data-ttu-id="64a8f-117">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-117">No equivalent control.</span></span>||  
|<xref:System.Windows.Forms.FontDialog>|<span data-ttu-id="64a8f-118">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-118">No equivalent control.</span></span>||  
|<xref:System.Windows.Forms.Form>|<xref:System.Windows.Window>|<span data-ttu-id="64a8f-119"><xref:System.Windows.Window> 子ウィンドウをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="64a8f-119"><xref:System.Windows.Window> does not support child windows.</span></span>|  
|<xref:System.Windows.Forms.GroupBox>|<xref:System.Windows.Controls.GroupBox>||  
|<xref:System.Windows.Forms.HelpProvider>|<span data-ttu-id="64a8f-120">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-120">No equivalent control.</span></span>|<span data-ttu-id="64a8f-121">F1 ヘルプはありません。</span><span class="sxs-lookup"><span data-stu-id="64a8f-121">No F1 Help.</span></span> <span data-ttu-id="64a8f-122">"What is この"ヘルプがツールヒントに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="64a8f-122">"What's This" Help is replaced by ToolTips.</span></span>|  
|<xref:System.Windows.Forms.HScrollBar>|<xref:System.Windows.Controls.Primitives.ScrollBar>|<span data-ttu-id="64a8f-123">スクロールは、コンテナー コントロールに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="64a8f-123">Scrolling is built into container controls.</span></span>|  
|<xref:System.Windows.Forms.ImageList>|<span data-ttu-id="64a8f-124">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-124">No equivalent control.</span></span>||  
|<xref:System.Windows.Forms.Label>|<xref:System.Windows.Controls.Label>||  
|<xref:System.Windows.Forms.LinkLabel>|<span data-ttu-id="64a8f-125">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-125">No equivalent control.</span></span>|<span data-ttu-id="64a8f-126">使用することができます、<xref:System.Windows.Documents.Hyperlink>フロー コンテンツ内でハイパーリンクをホストするクラス。</span><span class="sxs-lookup"><span data-stu-id="64a8f-126">You can use the <xref:System.Windows.Documents.Hyperlink> class to host hyperlinks within flow content.</span></span>|  
|<xref:System.Windows.Forms.ListBox>|<xref:System.Windows.Controls.ListBox>||  
|<xref:System.Windows.Forms.ListView>|<xref:System.Windows.Controls.ListView>|<span data-ttu-id="64a8f-127"><xref:System.Windows.Controls.ListView>コントロールは読み取り専用の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="64a8f-127">The <xref:System.Windows.Controls.ListView> control provides a read-only details view.</span></span>|  
|<xref:System.Windows.Forms.MaskedTextBox>|<span data-ttu-id="64a8f-128">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-128">No equivalent control.</span></span>||  
|<xref:System.Windows.Forms.MenuStrip>|<xref:System.Windows.Controls.Menu>|<span data-ttu-id="64a8f-129"><xref:System.Windows.Controls.Menu> コントロールのスタイル設定できるおおよその動作と外観の<xref:System.Windows.Forms.ToolStripProfessionalRenderer?displayProperty=nameWithType>クラス。</span><span class="sxs-lookup"><span data-stu-id="64a8f-129"><xref:System.Windows.Controls.Menu> control styling can approximate the behavior and appearance of the <xref:System.Windows.Forms.ToolStripProfessionalRenderer?displayProperty=nameWithType> class.</span></span>|  
|<xref:System.Windows.Forms.MonthCalendar>|<xref:System.Windows.Controls.Calendar>||  
|<xref:System.Windows.Forms.NotifyIcon>|<span data-ttu-id="64a8f-130">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-130">No equivalent control.</span></span>||  
|<xref:System.Windows.Forms.NumericUpDown>|<span data-ttu-id="64a8f-131"><xref:System.Windows.Controls.TextBox> 2 つと<xref:System.Windows.Controls.Primitives.RepeatButton>コントロール。</span><span class="sxs-lookup"><span data-stu-id="64a8f-131"><xref:System.Windows.Controls.TextBox> and two <xref:System.Windows.Controls.Primitives.RepeatButton> controls.</span></span>||  
|<xref:System.Windows.Forms.OpenFileDialog>|<xref:Microsoft.Win32.OpenFileDialog>|<span data-ttu-id="64a8f-132"><xref:Microsoft.Win32.OpenFileDialog>クラスは、[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]ラッパー、[!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)]コントロール。</span><span class="sxs-lookup"><span data-stu-id="64a8f-132">The <xref:Microsoft.Win32.OpenFileDialog> class is a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] wrapper around the [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] control.</span></span>|  
|<xref:System.Windows.Forms.PageSetupDialog>|<span data-ttu-id="64a8f-133">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-133">No equivalent control.</span></span>||  
|<xref:System.Windows.Forms.Panel>|<xref:System.Windows.Controls.Canvas>||  
|<xref:System.Windows.Forms.PictureBox>|<xref:System.Windows.Controls.Image>||  
|<xref:System.Windows.Forms.PrintDialog>|<xref:System.Windows.Controls.PrintDialog>||  
|<xref:System.Drawing.Printing.PrintDocument>|<span data-ttu-id="64a8f-134">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-134">No equivalent control.</span></span>||  
|<xref:System.Windows.Forms.PrintPreviewControl>|<xref:System.Windows.Controls.DocumentViewer>||  
|<xref:System.Windows.Forms.PrintPreviewDialog>|<span data-ttu-id="64a8f-135">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-135">No equivalent control.</span></span>||  
|<xref:System.Windows.Forms.ProgressBar>|<xref:System.Windows.Controls.ProgressBar>||  
|<xref:System.Windows.Forms.PropertyGrid>|<span data-ttu-id="64a8f-136">同じコントロールなし。</span><span class="sxs-lookup"><span data-stu-id="64a8f-136">No equivalent control.</span></span>||  
|<xref:System.Windows.Forms.RadioButton>|<xref:System.Windows.Controls.RadioButton>||  
|<xref:System.Windows.Forms.RichTextBox>|<xref:System.Windows.Controls.RichTextBox>||  
|<xref:System.Windows.Forms.SaveFileDialog>|<xref:Microsoft.Win32.SaveFileDialog>|<span data-ttu-id="64a8f-137"><xref:Microsoft.Win32.SaveFileDialog>クラスは、[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]ラッパー、[!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)]コントロール。</span><span class="sxs-lookup"><span data-stu-id="64a8f-137">The <xref:Microsoft.Win32.SaveFileDialog> class is a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] wrapper around the [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] control.</span></span>|  
|<xref:System.Windows.Forms.ScrollableControl>|<xref:System.Windows.Controls.ScrollViewer>||  
|<xref:System.Media.SoundPlayer>|<xref:System.Windows.Media.MediaPlayer>||  
|<xref:System.Windows.Forms.SplitContainer>|<xref:System.Windows.Controls.GridSplitter>||  
|<xref:System.Windows.Forms.StatusStrip>|<xref:System.Windows.Controls.Primitives.StatusBar>||  
|<xref:System.Windows.Forms.TabControl>|<xref:System.Windows.Controls.TabControl>||  
|<xref:System.Windows.Forms.TableLayoutPanel>|<xref:System.Windows.Controls.Grid>||  
|<xref:System.Windows.Forms.TextBox>|<xref:System.Windows.Controls.TextBox>||  
|<xref:System.Windows.Forms.Timer>|<xref:System.Windows.Threading.DispatcherTimer>||  
|<xref:System.Windows.Forms.ToolStrip>|<xref:System.Windows.Controls.ToolBar>||  
|<xref:System.Windows.Forms.ToolStripContainer>|<span data-ttu-id="64a8f-138"><xref:System.Windows.Controls.ToolBar> で合成します。</span><span class="sxs-lookup"><span data-stu-id="64a8f-138"><xref:System.Windows.Controls.ToolBar> with composition.</span></span>||  
|<xref:System.Windows.Forms.ToolStripDropDown>|<span data-ttu-id="64a8f-139"><xref:System.Windows.Controls.ToolBar> で合成します。</span><span class="sxs-lookup"><span data-stu-id="64a8f-139"><xref:System.Windows.Controls.ToolBar> with composition.</span></span>||  
|<xref:System.Windows.Forms.ToolStripDropDownMenu>|<span data-ttu-id="64a8f-140"><xref:System.Windows.Controls.ToolBar> で合成します。</span><span class="sxs-lookup"><span data-stu-id="64a8f-140"><xref:System.Windows.Controls.ToolBar> with composition.</span></span>||  
|<xref:System.Windows.Forms.ToolStripPanel>|<span data-ttu-id="64a8f-141"><xref:System.Windows.Controls.ToolBar> で合成します。</span><span class="sxs-lookup"><span data-stu-id="64a8f-141"><xref:System.Windows.Controls.ToolBar> with composition.</span></span>||  
|<xref:System.Windows.Forms.ToolTip>|<xref:System.Windows.Controls.ToolTip>||  
|<xref:System.Windows.Forms.TrackBar>|<xref:System.Windows.Controls.Slider>||  
|<xref:System.Windows.Forms.TreeView>|<xref:System.Windows.Controls.TreeView>||  
|<xref:System.Windows.Forms.UserControl>|<xref:System.Windows.Controls.UserControl>||  
|<xref:System.Windows.Forms.VScrollBar>|<xref:System.Windows.Controls.Primitives.ScrollBar>|<span data-ttu-id="64a8f-142">スクロールは、コンテナー コントロールに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="64a8f-142">Scrolling is built into container controls.</span></span>|  
|<xref:System.Windows.Forms.WebBrowser>|<span data-ttu-id="64a8f-143"><xref:System.Windows.Controls.Frame>, <xref:System.Windows.Controls.WebBrowser?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="64a8f-143"><xref:System.Windows.Controls.Frame>, <xref:System.Windows.Controls.WebBrowser?displayProperty=nameWithType></span></span>|<span data-ttu-id="64a8f-144"><xref:System.Windows.Controls.Frame>コントロールは HTML ページをホストできます。</span><span class="sxs-lookup"><span data-stu-id="64a8f-144">The <xref:System.Windows.Controls.Frame> control can host HTML pages.</span></span><br /><br /> <span data-ttu-id="64a8f-145">以降では、 [!INCLUDE[net_v35SP1_short](../../../../includes/net-v35sp1-short-md.md)]、<xref:System.Windows.Controls.WebBrowser?displayProperty=nameWithType>コントロールは、HTML ページともバックアップをホストできる、<xref:System.Windows.Controls.Frame>コントロール。</span><span class="sxs-lookup"><span data-stu-id="64a8f-145">Starting in the [!INCLUDE[net_v35SP1_short](../../../../includes/net-v35sp1-short-md.md)], the <xref:System.Windows.Controls.WebBrowser?displayProperty=nameWithType> control can host HTML pages and also backs the <xref:System.Windows.Controls.Frame> control.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="64a8f-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="64a8f-146">See Also</span></span>  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 [<span data-ttu-id="64a8f-147">Windows の WPF デザイナーの開発者をフォームします。</span><span class="sxs-lookup"><span data-stu-id="64a8f-147">WPF Designer for Windows Forms Developers</span></span>](https://msdn.microsoft.com/library/47ad0909-e89b-4996-b4ac-874d929f94ca)  
 [<span data-ttu-id="64a8f-148">チュートリアル: WPF での Windows フォーム コントロールのホスト</span><span class="sxs-lookup"><span data-stu-id="64a8f-148">Walkthrough: Hosting a Windows Forms Control in WPF</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-control-in-wpf.md)  
 [<span data-ttu-id="64a8f-149">チュートリアル: Windows フォームでの WPF 複合コントロールのホスト</span><span class="sxs-lookup"><span data-stu-id="64a8f-149">Walkthrough: Hosting a WPF Composite Control in Windows Forms</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)  
 [<span data-ttu-id="64a8f-150">移行と相互運用性</span><span class="sxs-lookup"><span data-stu-id="64a8f-150">Migration and Interoperability</span></span>](../../../../docs/framework/wpf/advanced/migration-and-interoperability.md)
