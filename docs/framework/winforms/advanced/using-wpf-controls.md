---
title: WPF コントロールの使用
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms Designer [Windows Forms], interoperability with WPF
- interoperability [WPF]
ms.assetid: 03c85dce-26ad-44cd-bc1d-8e0cb56de096
ms.openlocfilehash: be925bdceea3dd01c568d85fe025d6e037066454
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47459660"
---
# <a name="using-wpf-controls"></a><span data-ttu-id="bf844-102">WPF コントロールの使用</span><span class="sxs-lookup"><span data-stu-id="bf844-102">Using WPF Controls</span></span>
<span data-ttu-id="bf844-103">Windows フォーム ベースのアプリケーションでは、Windows Presentation Foundation (WPF) コントロールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="bf844-103">You can use Windows Presentation Foundation (WPF) controls in your Windows Forms-based applications.</span></span> <span data-ttu-id="bf844-104">これらは、2 つの異なるビュー テクノロジが円滑に相互運用します。</span><span class="sxs-lookup"><span data-stu-id="bf844-104">Although these are two different view technologies, they interoperate smoothly.</span></span>  
  
 <span data-ttu-id="bf844-105">Windows フォーム デザイナーでは、Windows Presentation Foundation コントロールをホストするためのビジュアル デ ザイン環境を提供します。</span><span class="sxs-lookup"><span data-stu-id="bf844-105">The Windows Forms Designer provides a visual design environment for hosting Windows Presentation Foundation controls.</span></span> <span data-ttu-id="bf844-106">WPF コントロールがという特殊な Windows フォーム コントロールによってホストされている<xref:System.Windows.Forms.Integration.ElementHost>します。</span><span class="sxs-lookup"><span data-stu-id="bf844-106">A WPF control is hosted by a special Windows Forms control that is named <xref:System.Windows.Forms.Integration.ElementHost>.</span></span> <span data-ttu-id="bf844-107">このコントロールは、フォームのレイアウトに参加して、キーボードとマウスのメッセージを受信する WPF コントロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="bf844-107">This control enables the WPF control to participate in the form's layout and to receive keyboard and mouse messages.</span></span> <span data-ttu-id="bf844-108">デザイン時に配置することができます、<xref:System.Windows.Forms.Integration.ElementHost>任意の Windows フォーム コントロールと同様に制御します。</span><span class="sxs-lookup"><span data-stu-id="bf844-108">At design time, you can arrange the <xref:System.Windows.Forms.Integration.ElementHost> control just as you would any Windows Forms control.</span></span>  
  
 <span data-ttu-id="bf844-109">Windows フォーム コントロールは WPF ベースのアプリケーションで使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="bf844-109">You can also use Windows Forms controls in your WPF-based applications.</span></span> <span data-ttu-id="bf844-110">詳細については、次を参照してください。 [Visual Studio で XAML をデザイン](/visualstudio/designers/designing-xaml-in-visual-studio)します。</span><span class="sxs-lookup"><span data-stu-id="bf844-110">For more information, see [Design XAML in Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="bf844-111">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="bf844-111">In This Section</span></span>  
 [<span data-ttu-id="bf844-112">方法: デザイン時に ElementHost コントロールをコピーして貼り付ける</span><span class="sxs-lookup"><span data-stu-id="bf844-112">How to: Copy and Paste an ElementHost Control at Design Time</span></span>](../../../../docs/framework/winforms/advanced/how-to-copy-and-paste-an-elementhost-control-at-design-time.md)  
 <span data-ttu-id="bf844-113">Windows フォーム上の Windows Presentation Foundation コントロールをコピーする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bf844-113">Shows how to copy a Windows Presentation Foundation control on a Windows Form.</span></span>  
  
 [<span data-ttu-id="bf844-114">チュートリアル: デザイン時の Windows フォームでの WPF コンテンツの配置</span><span class="sxs-lookup"><span data-stu-id="bf844-114">Walkthrough: Arranging WPF Content on Windows Forms at Design Time</span></span>](../../../../docs/framework/winforms/advanced/walkthrough-arranging-wpf-content-on-windows-forms-at-design-time.md)  
 <span data-ttu-id="bf844-115">固定やスナップ線をなど、Windows フォームのレイアウト機能を使用して、Windows Presentation Foundation コントロールを配置する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bf844-115">Shows how to use the Windows Forms layout features, such as anchoring and snaplines, to arrange Windows Presentation Foundation controls.</span></span>
  
 [<span data-ttu-id="bf844-116">チュートリアル: デザイン時の Windows フォームでの新しい WPF コンテンツの作成</span><span class="sxs-lookup"><span data-stu-id="bf844-116">Walkthrough: Creating New WPF Content on Windows Forms at Design Time</span></span>](../../../../docs/framework/winforms/advanced/walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md)  
 <span data-ttu-id="bf844-117">Windows フォーム ベースのアプリケーションで使用するための Windows Presentation Foundation コントロールを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bf844-117">Shows how to create a Windows Presentation Foundation control for use in your Windows Forms-based applications.</span></span>
  
 [<span data-ttu-id="bf844-118">チュートリアル: デザイン時の Windows フォームでの WPF コンテンツの割り当て</span><span class="sxs-lookup"><span data-stu-id="bf844-118">Walkthrough: Assigning WPF Content on Windows Forms at Design Time</span></span>](../../../../docs/framework/winforms/advanced/walkthrough-assigning-wpf-content-on-windows-forms-at-design-time.md)  
 <span data-ttu-id="bf844-119">フォームに表示する Windows Presentation Foundation コントロールの種類を選択する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bf844-119">Shows how to select the Windows Presentation Foundation control types you want to display on your form.</span></span>  
  
 [<span data-ttu-id="bf844-120">チュートリアル: WPF コンテンツへのスタイルの適用</span><span class="sxs-lookup"><span data-stu-id="bf844-120">Walkthrough: Styling WPF Content</span></span>](../../../../docs/framework/winforms/advanced/walkthrough-styling-wpf-content.md)  
 <span data-ttu-id="bf844-121">Windows フォーム デザイナー間のワークフローを示しています、 [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)] Windows Presentation Foundation コントロールにスタイルを適用するためです。</span><span class="sxs-lookup"><span data-stu-id="bf844-121">Shows the workflow between the Windows Forms Designer and the [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)] for applying styles to Windows Presentation Foundation controls.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="bf844-122">参照</span><span class="sxs-lookup"><span data-stu-id="bf844-122">Reference</span></span>  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 <span data-ttu-id="bf844-123">Windows フォーム ベースのアプリケーションでホストの Windows Presentation Foundation コントロールに使用できるクラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bf844-123">Describes a class which you can use to host Windows Presentation Foundation controls in your Windows Forms-based applications.</span></span>  
  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 <span data-ttu-id="bf844-124">Windows フォーム コントロールをホストする Windows Presentation Foundation ベースのアプリケーションで使用できるクラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bf844-124">Describes a class which you can use to host Windows Forms controls in your Windows Presentation Foundation-based application.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="bf844-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf844-125">Related Sections</span></span>  
 [<span data-ttu-id="bf844-126">移行と相互運用性</span><span class="sxs-lookup"><span data-stu-id="bf844-126">Migration and Interoperability</span></span>](../../../../docs/framework/wpf/advanced/migration-and-interoperability.md)  
 <span data-ttu-id="bf844-127">Windows Presentation Foundation と Windows フォーム テクノロジ間の相互運用をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bf844-127">Describes interoperation between the Windows Presentation Foundation and Windows Forms technologies.</span></span>  
  
 [<span data-ttu-id="bf844-128">Visual Studio で XAML をデザインする</span><span class="sxs-lookup"><span data-stu-id="bf844-128">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)  
 <span data-ttu-id="bf844-129">Visual Studio での Windows Presentation Foundation コントロールをデザインする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bf844-129">Describes how to design Windows Presentation Foundation controls in Visual Studio.</span></span>
