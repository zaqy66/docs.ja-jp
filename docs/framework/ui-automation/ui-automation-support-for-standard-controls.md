---
title: UI オートメーションによる標準コントロールのサポート
ms.date: 03/30/2017
helpviewer_keywords:
- controls, UI Automation support for
- UI Automation, support for standard controls
ms.assetid: 3770ea8a-2655-4add-9c59-fe0610ad5084
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: cbfb640a068a2c1178d321480ee3a112db07b6ac
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2018
ms.locfileid: "43463893"
---
# <a name="ui-automation-support-for-standard-controls"></a><span data-ttu-id="f1057-102">UI オートメーションによる標準コントロールのサポート</span><span class="sxs-lookup"><span data-stu-id="f1057-102">UI Automation Support for Standard Controls</span></span>
> [!NOTE]
>  <span data-ttu-id="f1057-103">このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="f1057-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="f1057-104">に関する最新情報については[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]を参照してください[Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746)します。</span><span class="sxs-lookup"><span data-stu-id="f1057-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="f1057-105">このトピックでは、 [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] 、 [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)]、および [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)]フレームワーク向けに開発されたアプリケーションの標準コントロールに対する [!INCLUDE[TLA#tla_winforms](../../../includes/tlasharptla-winforms-md.md)] サポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f1057-105">This topic contains information about [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] support for standard controls in applications developed for the [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)], [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)], and [!INCLUDE[TLA#tla_winforms](../../../includes/tlasharptla-winforms-md.md)] frameworks.</span></span>  
  
<a name="Windows_Presentation_Foundation_Controls"></a>   
## <a name="windows-presentation-foundation-controls"></a><span data-ttu-id="f1057-106">Windows Presentation Foundation コントロール</span><span class="sxs-lookup"><span data-stu-id="f1057-106">Windows Presentation Foundation Controls</span></span>  
 <span data-ttu-id="f1057-107">ユーザー操作に関する情報やサポートを提供するすべての [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)] コントロール要素は、 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]を全面的にネイティブ サポートしています。</span><span class="sxs-lookup"><span data-stu-id="f1057-107">All [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)] control elements that provide information or support for user interaction have full native support for [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span></span> <span data-ttu-id="f1057-108">パネルなどのその他の要素は、 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]からは認識できません。</span><span class="sxs-lookup"><span data-stu-id="f1057-108">Other elements, such as panels, are not visible to [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span></span>  
  
<a name="Win32_Controls"></a>   
## <a name="win32-controls"></a><span data-ttu-id="f1057-109">Win32 コントロール</span><span class="sxs-lookup"><span data-stu-id="f1057-109">Win32 Controls</span></span>  
 <span data-ttu-id="f1057-110">ほとんどの [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] コントロールは、UIAutomationClientsideProviders.dll のクライアント側プロバイダーによって [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] に公開されています。</span><span class="sxs-lookup"><span data-stu-id="f1057-110">Most [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] controls are exposed to [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] through client-side providers in UIAutomationClientsideProviders.dll.</span></span> <span data-ttu-id="f1057-111">このアセンブリは、UI オートメーション クライアント アプリケーションで使用するために、自動的に登録されます。</span><span class="sxs-lookup"><span data-stu-id="f1057-111">This assembly is automatically registered for use with UI Automation client applications.</span></span>  
  
 <span data-ttu-id="f1057-112">完全なサポートは、ComCtrl32.dll のバージョン 6 ( [!INCLUDE[TLA#tla_winxp](../../../includes/tlasharptla-winxp-md.md)] 以降で使用可能) のコントロールに対してのみ提供されています。</span><span class="sxs-lookup"><span data-stu-id="f1057-112">Full support is provided only for controls from version 6 of ComCtrl32.dll (available with [!INCLUDE[TLA#tla_winxp](../../../includes/tlasharptla-winxp-md.md)] and later).</span></span>  
  
 <span data-ttu-id="f1057-113">次のコントロールがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f1057-113">The following controls are supported.</span></span>  
  
|<span data-ttu-id="f1057-114">クラス名</span><span class="sxs-lookup"><span data-stu-id="f1057-114">Class name</span></span>|<span data-ttu-id="f1057-115">コントロール型</span><span class="sxs-lookup"><span data-stu-id="f1057-115">Control Type</span></span>|  
|----------------|------------------|  
|<span data-ttu-id="f1057-116">ボタン</span><span class="sxs-lookup"><span data-stu-id="f1057-116">Button</span></span>|<span data-ttu-id="f1057-117">ボタン</span><span class="sxs-lookup"><span data-stu-id="f1057-117">Button</span></span>|  
|<span data-ttu-id="f1057-118">ボタン</span><span class="sxs-lookup"><span data-stu-id="f1057-118">Button</span></span>|<span data-ttu-id="f1057-119">RadioButton</span><span class="sxs-lookup"><span data-stu-id="f1057-119">RadioButton</span></span>|  
|<span data-ttu-id="f1057-120">ボタン</span><span class="sxs-lookup"><span data-stu-id="f1057-120">Button</span></span>|<span data-ttu-id="f1057-121">グループ化</span><span class="sxs-lookup"><span data-stu-id="f1057-121">Group</span></span>|  
|<span data-ttu-id="f1057-122">ボタン</span><span class="sxs-lookup"><span data-stu-id="f1057-122">Button</span></span>|<span data-ttu-id="f1057-123">CheckBox</span><span class="sxs-lookup"><span data-stu-id="f1057-123">CheckBox</span></span>|  
|<span data-ttu-id="f1057-124">ボタン</span><span class="sxs-lookup"><span data-stu-id="f1057-124">Button</span></span>|<span data-ttu-id="f1057-125">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="f1057-125">Hyperlink</span></span>|  
|<span data-ttu-id="f1057-126">ボタン</span><span class="sxs-lookup"><span data-stu-id="f1057-126">Button</span></span>|<span data-ttu-id="f1057-127">SplitButton</span><span class="sxs-lookup"><span data-stu-id="f1057-127">SplitButton</span></span>|  
|<span data-ttu-id="f1057-128">ボタン</span><span class="sxs-lookup"><span data-stu-id="f1057-128">Button</span></span>|<span data-ttu-id="f1057-129">CheckBox</span><span class="sxs-lookup"><span data-stu-id="f1057-129">CheckBox</span></span>|  
|<span data-ttu-id="f1057-130">ComboBoxEx32</span><span class="sxs-lookup"><span data-stu-id="f1057-130">ComboBoxEx32</span></span>|<span data-ttu-id="f1057-131">ComboBox</span><span class="sxs-lookup"><span data-stu-id="f1057-131">ComboBox</span></span>|  
|<span data-ttu-id="f1057-132">ComboBox</span><span class="sxs-lookup"><span data-stu-id="f1057-132">ComboBox</span></span>|<span data-ttu-id="f1057-133">ComboBox</span><span class="sxs-lookup"><span data-stu-id="f1057-133">ComboBox</span></span>|  
|<span data-ttu-id="f1057-134">編集</span><span class="sxs-lookup"><span data-stu-id="f1057-134">Edit</span></span>|<span data-ttu-id="f1057-135">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="f1057-135">Document</span></span>|  
|<span data-ttu-id="f1057-136">編集</span><span class="sxs-lookup"><span data-stu-id="f1057-136">Edit</span></span>|<span data-ttu-id="f1057-137">編集</span><span class="sxs-lookup"><span data-stu-id="f1057-137">Edit</span></span>|  
|<span data-ttu-id="f1057-138">SysLink</span><span class="sxs-lookup"><span data-stu-id="f1057-138">SysLink</span></span>|<span data-ttu-id="f1057-139">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="f1057-139">Hyperlink</span></span>|  
|<span data-ttu-id="f1057-140">スタティック</span><span class="sxs-lookup"><span data-stu-id="f1057-140">Static</span></span>|<span data-ttu-id="f1057-141">テキスト</span><span class="sxs-lookup"><span data-stu-id="f1057-141">Text</span></span>|  
|<span data-ttu-id="f1057-142">スタティック</span><span class="sxs-lookup"><span data-stu-id="f1057-142">Static</span></span>|<span data-ttu-id="f1057-143">イメージ</span><span class="sxs-lookup"><span data-stu-id="f1057-143">Image</span></span>|  
|<span data-ttu-id="f1057-144">SysIPAddress32</span><span class="sxs-lookup"><span data-stu-id="f1057-144">SysIPAddress32</span></span>|<span data-ttu-id="f1057-145">カスタム</span><span class="sxs-lookup"><span data-stu-id="f1057-145">Custom</span></span>|  
|<span data-ttu-id="f1057-146">SysHeader32</span><span class="sxs-lookup"><span data-stu-id="f1057-146">SysHeader32</span></span>|<span data-ttu-id="f1057-147">Header/HeaderItem</span><span class="sxs-lookup"><span data-stu-id="f1057-147">Header/HeaderItem</span></span>|  
|<span data-ttu-id="f1057-148">SysListView32</span><span class="sxs-lookup"><span data-stu-id="f1057-148">SysListView32</span></span>|<span data-ttu-id="f1057-149">DataGrid</span><span class="sxs-lookup"><span data-stu-id="f1057-149">DataGrid</span></span>|  
|<span data-ttu-id="f1057-150">SysListView32</span><span class="sxs-lookup"><span data-stu-id="f1057-150">SysListView32</span></span>|<span data-ttu-id="f1057-151">リスト</span><span class="sxs-lookup"><span data-stu-id="f1057-151">List</span></span>|  
|<span data-ttu-id="f1057-152">ListBox</span><span class="sxs-lookup"><span data-stu-id="f1057-152">ListBox</span></span>|<span data-ttu-id="f1057-153">リスト</span><span class="sxs-lookup"><span data-stu-id="f1057-153">List</span></span>|  
|<span data-ttu-id="f1057-154">ListBox</span><span class="sxs-lookup"><span data-stu-id="f1057-154">ListBox</span></span>|<span data-ttu-id="f1057-155">ListItem</span><span class="sxs-lookup"><span data-stu-id="f1057-155">ListItem</span></span>|  
|<span data-ttu-id="f1057-156">#32768</span><span class="sxs-lookup"><span data-stu-id="f1057-156">#32768</span></span>|<span data-ttu-id="f1057-157">メニュー</span><span class="sxs-lookup"><span data-stu-id="f1057-157">Menu</span></span>|  
|<span data-ttu-id="f1057-158">#32768</span><span class="sxs-lookup"><span data-stu-id="f1057-158">#32768</span></span>|<span data-ttu-id="f1057-159">MenuItem</span><span class="sxs-lookup"><span data-stu-id="f1057-159">MenuItem</span></span>|  
|<span data-ttu-id="f1057-160">msctls_progress32</span><span class="sxs-lookup"><span data-stu-id="f1057-160">msctls_progress32</span></span>|<span data-ttu-id="f1057-161">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="f1057-161">ProgressBar</span></span>|  
|<span data-ttu-id="f1057-162">RichEdit</span><span class="sxs-lookup"><span data-stu-id="f1057-162">RichEdit</span></span>|<span data-ttu-id="f1057-163">ドキュメント。</span><span class="sxs-lookup"><span data-stu-id="f1057-163">Document.</span></span> <span data-ttu-id="f1057-164">注を参照。</span><span class="sxs-lookup"><span data-stu-id="f1057-164">See note.</span></span>|  
|<span data-ttu-id="f1057-165">RichEdit20A</span><span class="sxs-lookup"><span data-stu-id="f1057-165">RichEdit20A</span></span>|<span data-ttu-id="f1057-166">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="f1057-166">Document</span></span>|  
|<span data-ttu-id="f1057-167">RichEdit20W</span><span class="sxs-lookup"><span data-stu-id="f1057-167">RichEdit20W</span></span>|<span data-ttu-id="f1057-168">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="f1057-168">Document</span></span>|  
|<span data-ttu-id="f1057-169">RichEdit50W</span><span class="sxs-lookup"><span data-stu-id="f1057-169">RichEdit50W</span></span>|<span data-ttu-id="f1057-170">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="f1057-170">Document</span></span>|  
|<span data-ttu-id="f1057-171">ScrollBar</span><span class="sxs-lookup"><span data-stu-id="f1057-171">ScrollBar</span></span>|<span data-ttu-id="f1057-172">スライダー</span><span class="sxs-lookup"><span data-stu-id="f1057-172">Slider</span></span>|  
|<span data-ttu-id="f1057-173">msctls_trackbar32</span><span class="sxs-lookup"><span data-stu-id="f1057-173">msctls_trackbar32</span></span>|<span data-ttu-id="f1057-174">スライダー</span><span class="sxs-lookup"><span data-stu-id="f1057-174">Slider</span></span>|  
|<span data-ttu-id="f1057-175">msctls_updown32</span><span class="sxs-lookup"><span data-stu-id="f1057-175">msctls_updown32</span></span>|<span data-ttu-id="f1057-176">Spinner</span><span class="sxs-lookup"><span data-stu-id="f1057-176">Spinner</span></span>|  
|<span data-ttu-id="f1057-177">msctls_statusbar32</span><span class="sxs-lookup"><span data-stu-id="f1057-177">msctls_statusbar32</span></span>|<span data-ttu-id="f1057-178">StatusBar</span><span class="sxs-lookup"><span data-stu-id="f1057-178">StatusBar</span></span>|  
|<span data-ttu-id="f1057-179">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="f1057-179">SysTabControl32</span></span>|<span data-ttu-id="f1057-180">タブ</span><span class="sxs-lookup"><span data-stu-id="f1057-180">Tab</span></span>|  
|<span data-ttu-id="f1057-181">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="f1057-181">SysTabControl32</span></span>|<span data-ttu-id="f1057-182">TabItem</span><span class="sxs-lookup"><span data-stu-id="f1057-182">TabItem</span></span>|  
|<span data-ttu-id="f1057-183">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="f1057-183">ToolbarWindow32</span></span>|<span data-ttu-id="f1057-184">ToolBar</span><span class="sxs-lookup"><span data-stu-id="f1057-184">ToolBar</span></span>|  
|<span data-ttu-id="f1057-185">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="f1057-185">ToolbarWindow32</span></span>|<span data-ttu-id="f1057-186">MenuItem</span><span class="sxs-lookup"><span data-stu-id="f1057-186">MenuItem</span></span>|  
|<span data-ttu-id="f1057-187">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="f1057-187">ToolbarWindow32</span></span>|<span data-ttu-id="f1057-188">ボタン</span><span class="sxs-lookup"><span data-stu-id="f1057-188">Button</span></span>|  
|<span data-ttu-id="f1057-189">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="f1057-189">ToolbarWindow32</span></span>|<span data-ttu-id="f1057-190">CheckBox</span><span class="sxs-lookup"><span data-stu-id="f1057-190">CheckBox</span></span>|  
|<span data-ttu-id="f1057-191">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="f1057-191">ToolbarWindow32</span></span>|<span data-ttu-id="f1057-192">RadioButton</span><span class="sxs-lookup"><span data-stu-id="f1057-192">RadioButton</span></span>|  
|<span data-ttu-id="f1057-193">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="f1057-193">ToolbarWindow32</span></span>|<span data-ttu-id="f1057-194">区切り記号</span><span class="sxs-lookup"><span data-stu-id="f1057-194">Separator</span></span>|  
|<span data-ttu-id="f1057-195">tooltips_class32</span><span class="sxs-lookup"><span data-stu-id="f1057-195">tooltips_class32</span></span>|<span data-ttu-id="f1057-196">ヒント</span><span class="sxs-lookup"><span data-stu-id="f1057-196">ToolTip</span></span>|  
|<span data-ttu-id="f1057-197">#32774</span><span class="sxs-lookup"><span data-stu-id="f1057-197">#32774</span></span>|<span data-ttu-id="f1057-198">ヒント</span><span class="sxs-lookup"><span data-stu-id="f1057-198">ToolTip</span></span>|  
|<span data-ttu-id="f1057-199">ReBarWindow32</span><span class="sxs-lookup"><span data-stu-id="f1057-199">ReBarWindow32</span></span>|<span data-ttu-id="f1057-200">ツール バー</span><span class="sxs-lookup"><span data-stu-id="f1057-200">Toolbar</span></span>|  
|<span data-ttu-id="f1057-201">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="f1057-201">SysTreeView32</span></span>|<span data-ttu-id="f1057-202">ツリー</span><span class="sxs-lookup"><span data-stu-id="f1057-202">Tree</span></span>|  
|<span data-ttu-id="f1057-203">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="f1057-203">SysTreeView32</span></span>|<span data-ttu-id="f1057-204">TreeItem</span><span class="sxs-lookup"><span data-stu-id="f1057-204">TreeItem</span></span>|  
  
 <span data-ttu-id="f1057-205">**注** RichEdit コントロールは、 [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)] に付属するバージョン (RichEd20.dll バージョン 3.1 以降、および MsftEdit.dll バージョン 4.1 以降) に対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f1057-205">**Note** The RichEdit control is supported only for versions shipped with [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)] (in RichEd20.dll version 3.1 and later, and MsftEdit.dll version 4.1 and later).</span></span>  
  
 <span data-ttu-id="f1057-206">次のコントロールはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f1057-206">The following controls are not supported.</span></span>  
  
|<span data-ttu-id="f1057-207">クラス名</span><span class="sxs-lookup"><span data-stu-id="f1057-207">Class name</span></span>|<span data-ttu-id="f1057-208">コントロール型</span><span class="sxs-lookup"><span data-stu-id="f1057-208">Control type</span></span>|  
|----------------|------------------|  
|<span data-ttu-id="f1057-209">SysAnimate32</span><span class="sxs-lookup"><span data-stu-id="f1057-209">SysAnimate32</span></span>|<span data-ttu-id="f1057-210">イメージ</span><span class="sxs-lookup"><span data-stu-id="f1057-210">Image</span></span>|  
|<span data-ttu-id="f1057-211">SysPager</span><span class="sxs-lookup"><span data-stu-id="f1057-211">SysPager</span></span>|<span data-ttu-id="f1057-212">Spinner</span><span class="sxs-lookup"><span data-stu-id="f1057-212">Spinner</span></span>|  
|<span data-ttu-id="f1057-213">SysDateTimePick32</span><span class="sxs-lookup"><span data-stu-id="f1057-213">SysDateTimePick32</span></span>|<span data-ttu-id="f1057-214">カスタム</span><span class="sxs-lookup"><span data-stu-id="f1057-214">Custom</span></span>|  
|<span data-ttu-id="f1057-215">SysMonthCal32</span><span class="sxs-lookup"><span data-stu-id="f1057-215">SysMonthCal32</span></span>|<span data-ttu-id="f1057-216">予定表</span><span class="sxs-lookup"><span data-stu-id="f1057-216">Calendar</span></span>|  
|<span data-ttu-id="f1057-217">MS_WINNOTE</span><span class="sxs-lookup"><span data-stu-id="f1057-217">MS_WINNOTE</span></span>|<span data-ttu-id="f1057-218">ヒント</span><span class="sxs-lookup"><span data-stu-id="f1057-218">Tooltip</span></span>|  
|<span data-ttu-id="f1057-219">VBBubble</span><span class="sxs-lookup"><span data-stu-id="f1057-219">VBBubble</span></span>|<span data-ttu-id="f1057-220">ヒント</span><span class="sxs-lookup"><span data-stu-id="f1057-220">Tooltip</span></span>|  
|<span data-ttu-id="f1057-221">ScrollBar (スタンドアロン コントロールとして使用される場合)</span><span class="sxs-lookup"><span data-stu-id="f1057-221">ScrollBar (when used as a standalone control)</span></span>|<span data-ttu-id="f1057-222">スライダー</span><span class="sxs-lookup"><span data-stu-id="f1057-222">Slider</span></span>|  
|<span data-ttu-id="f1057-223">SuperGrid</span><span class="sxs-lookup"><span data-stu-id="f1057-223">SuperGrid</span></span>|<span data-ttu-id="f1057-224">カスタム</span><span class="sxs-lookup"><span data-stu-id="f1057-224">Custom</span></span>|  
  
<a name="Windows_Forms_Controls"></a>   
## <a name="windows-forms-controls"></a><span data-ttu-id="f1057-225">Windows フォーム コントロール</span><span class="sxs-lookup"><span data-stu-id="f1057-225">Windows Forms Controls</span></span>  
 <span data-ttu-id="f1057-226">Windows フォーム コントロールに公開[!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]UIAutomationClientsideProviders.dll のクライアント側プロバイダーを経由します。</span><span class="sxs-lookup"><span data-stu-id="f1057-226">Windows Forms controls are exposed to [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] through client-side providers in UIAutomationClientsideProviders.dll.</span></span> <span data-ttu-id="f1057-227">このアセンブリは、UI オートメーション クライアント アプリケーションで使用するために、自動的に登録されます。</span><span class="sxs-lookup"><span data-stu-id="f1057-227">This assembly is automatically registered for use with UI Automation client applications.</span></span>  
  
 <span data-ttu-id="f1057-228">通常、Windows フォーム コントロール用のマネージ ラッパー[!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)]で一般的なコントロールがサポートされる[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]します。</span><span class="sxs-lookup"><span data-stu-id="f1057-228">Typically, Windows Forms controls that are managed wrappers for [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] common controls are supported by [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span></span> <span data-ttu-id="f1057-229">次のコントロールがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f1057-229">The following controls are supported.</span></span>  
  
|<span data-ttu-id="f1057-230">クラス名</span><span class="sxs-lookup"><span data-stu-id="f1057-230">Class Name</span></span>|  
|----------------|  
|<span data-ttu-id="f1057-231">ボタン</span><span class="sxs-lookup"><span data-stu-id="f1057-231">Button</span></span>|  
|<span data-ttu-id="f1057-232">CheckBox</span><span class="sxs-lookup"><span data-stu-id="f1057-232">CheckBox</span></span>|  
|<span data-ttu-id="f1057-233">CheckedListBox</span><span class="sxs-lookup"><span data-stu-id="f1057-233">CheckedListBox</span></span>|  
|<span data-ttu-id="f1057-234">ColorDialog</span><span class="sxs-lookup"><span data-stu-id="f1057-234">ColorDialog</span></span>|  
|<span data-ttu-id="f1057-235">ComboBox</span><span class="sxs-lookup"><span data-stu-id="f1057-235">ComboBox</span></span>|  
|<span data-ttu-id="f1057-236">FolderBrowser</span><span class="sxs-lookup"><span data-stu-id="f1057-236">FolderBrowser</span></span>|  
|<span data-ttu-id="f1057-237">FontDialog</span><span class="sxs-lookup"><span data-stu-id="f1057-237">FontDialog</span></span>|  
|<span data-ttu-id="f1057-238">GroupBox</span><span class="sxs-lookup"><span data-stu-id="f1057-238">GroupBox</span></span>|  
|<span data-ttu-id="f1057-239">HscrollBar</span><span class="sxs-lookup"><span data-stu-id="f1057-239">HscrollBar</span></span>|  
|<span data-ttu-id="f1057-240">ImageList</span><span class="sxs-lookup"><span data-stu-id="f1057-240">ImageList</span></span>|  
|<span data-ttu-id="f1057-241">group1</span><span class="sxs-lookup"><span data-stu-id="f1057-241">Label</span></span>|  
|<span data-ttu-id="f1057-242">ListBox</span><span class="sxs-lookup"><span data-stu-id="f1057-242">ListBox</span></span>|  
|<span data-ttu-id="f1057-243">ListView</span><span class="sxs-lookup"><span data-stu-id="f1057-243">ListView</span></span>|  
|<span data-ttu-id="f1057-244">MainMenu/ContextMenu</span><span class="sxs-lookup"><span data-stu-id="f1057-244">MainMenu/ContextMenu</span></span>|  
|<span data-ttu-id="f1057-245">MonthCalendar</span><span class="sxs-lookup"><span data-stu-id="f1057-245">MonthCalendar</span></span>|  
|<span data-ttu-id="f1057-246">NotifyIcon</span><span class="sxs-lookup"><span data-stu-id="f1057-246">NotifyIcon</span></span>|  
|<span data-ttu-id="f1057-247">OpenFileDialog</span><span class="sxs-lookup"><span data-stu-id="f1057-247">OpenFileDialog</span></span>|  
|<span data-ttu-id="f1057-248">PageSetupDialog</span><span class="sxs-lookup"><span data-stu-id="f1057-248">PageSetupDialog</span></span>|  
|<span data-ttu-id="f1057-249">PrintDialog</span><span class="sxs-lookup"><span data-stu-id="f1057-249">PrintDialog</span></span>|  
|<span data-ttu-id="f1057-250">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="f1057-250">ProgressBar</span></span>|  
|<span data-ttu-id="f1057-251">RadioButton</span><span class="sxs-lookup"><span data-stu-id="f1057-251">RadioButton</span></span>|  
|<span data-ttu-id="f1057-252">RichTextBox</span><span class="sxs-lookup"><span data-stu-id="f1057-252">RichTextBox</span></span>|  
|<span data-ttu-id="f1057-253">SaveFileDialog</span><span class="sxs-lookup"><span data-stu-id="f1057-253">SaveFileDialog</span></span>|  
|<span data-ttu-id="f1057-254">ScrollableControl</span><span class="sxs-lookup"><span data-stu-id="f1057-254">ScrollableControl</span></span>|  
|<span data-ttu-id="f1057-255">SoundPlayer</span><span class="sxs-lookup"><span data-stu-id="f1057-255">SoundPlayer</span></span>|  
|<span data-ttu-id="f1057-256">StatusBar</span><span class="sxs-lookup"><span data-stu-id="f1057-256">StatusBar</span></span>|  
|<span data-ttu-id="f1057-257">TabControl/TabPage</span><span class="sxs-lookup"><span data-stu-id="f1057-257">TabControl/TabPage</span></span>|  
|<span data-ttu-id="f1057-258">TextBox</span><span class="sxs-lookup"><span data-stu-id="f1057-258">TextBox</span></span>|  
|<span data-ttu-id="f1057-259">タイマー</span><span class="sxs-lookup"><span data-stu-id="f1057-259">Timer</span></span>|  
|<span data-ttu-id="f1057-260">ToolBar</span><span class="sxs-lookup"><span data-stu-id="f1057-260">Toolbar</span></span>|  
|<span data-ttu-id="f1057-261">ヒント</span><span class="sxs-lookup"><span data-stu-id="f1057-261">ToolTip</span></span>|  
|<span data-ttu-id="f1057-262">TrackBar</span><span class="sxs-lookup"><span data-stu-id="f1057-262">TrackBar</span></span>|  
|<span data-ttu-id="f1057-263">TreeView</span><span class="sxs-lookup"><span data-stu-id="f1057-263">TreeView</span></span>|  
|<span data-ttu-id="f1057-264">VscrollBar</span><span class="sxs-lookup"><span data-stu-id="f1057-264">VscrollBar</span></span>|  
|<span data-ttu-id="f1057-265">Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="f1057-265">WebBrowser</span></span>|  
  
 <span data-ttu-id="f1057-266">次に示すコントロールは、 [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] のサポートによってのみ、 [!INCLUDE[TLA#tla_aa](../../../includes/tlasharptla-aa-md.md)]に公開されています。</span><span class="sxs-lookup"><span data-stu-id="f1057-266">The following controls are exposed to [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] only through their support for [!INCLUDE[TLA#tla_aa](../../../includes/tlasharptla-aa-md.md)].</span></span> <span data-ttu-id="f1057-267">一部の機能が使用できないことがあります。</span><span class="sxs-lookup"><span data-stu-id="f1057-267">Some functionality may not be available.</span></span>  
  
|<span data-ttu-id="f1057-268">コントロール名</span><span class="sxs-lookup"><span data-stu-id="f1057-268">Control Name</span></span>|  
|------------------|  
|<span data-ttu-id="f1057-269">BindingSource</span><span class="sxs-lookup"><span data-stu-id="f1057-269">BindingSource</span></span>|  
|<span data-ttu-id="f1057-270">DataGrid</span><span class="sxs-lookup"><span data-stu-id="f1057-270">DataGrid</span></span>|  
|<span data-ttu-id="f1057-271">DataGridView</span><span class="sxs-lookup"><span data-stu-id="f1057-271">DataGridView</span></span>|  
|<span data-ttu-id="f1057-272">DataNavigator</span><span class="sxs-lookup"><span data-stu-id="f1057-272">DataNavigator</span></span>|  
|<span data-ttu-id="f1057-273">DomainUpDown</span><span class="sxs-lookup"><span data-stu-id="f1057-273">DomainUpDown</span></span>|  
|<span data-ttu-id="f1057-274">ErrorProvider</span><span class="sxs-lookup"><span data-stu-id="f1057-274">ErrorProvider</span></span>|  
|<span data-ttu-id="f1057-275">FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="f1057-275">FlowLayoutPanel</span></span>|  
|<span data-ttu-id="f1057-276">フォーム</span><span class="sxs-lookup"><span data-stu-id="f1057-276">Form</span></span>|  
|<span data-ttu-id="f1057-277">LinkLabel</span><span class="sxs-lookup"><span data-stu-id="f1057-277">LinkLabel</span></span>|  
|<span data-ttu-id="f1057-278">HelpProvider</span><span class="sxs-lookup"><span data-stu-id="f1057-278">HelpProvider</span></span>|  
|<span data-ttu-id="f1057-279">MaskedTextBox</span><span class="sxs-lookup"><span data-stu-id="f1057-279">MaskedTextBox</span></span>|  
|<span data-ttu-id="f1057-280">MenuStrip/ContextMenuStrip</span><span class="sxs-lookup"><span data-stu-id="f1057-280">MenuStrip/ContextMenuStrip</span></span>|  
|<span data-ttu-id="f1057-281">NumericUpDown</span><span class="sxs-lookup"><span data-stu-id="f1057-281">NumericUpDown</span></span>|  
|<span data-ttu-id="f1057-282">パネル</span><span class="sxs-lookup"><span data-stu-id="f1057-282">Panel</span></span>|  
|<span data-ttu-id="f1057-283">PictureBox</span><span class="sxs-lookup"><span data-stu-id="f1057-283">PictureBox</span></span>|  
|<span data-ttu-id="f1057-284">PrintDocument</span><span class="sxs-lookup"><span data-stu-id="f1057-284">PrintDocument</span></span>|  
|<span data-ttu-id="f1057-285">PrintPreview-Control</span><span class="sxs-lookup"><span data-stu-id="f1057-285">PrintPreview-Control</span></span>|  
|<span data-ttu-id="f1057-286">PrintPreview-Dialog</span><span class="sxs-lookup"><span data-stu-id="f1057-286">PrintPreview-Dialog</span></span>|  
|<span data-ttu-id="f1057-287">PropertyGrid</span><span class="sxs-lookup"><span data-stu-id="f1057-287">PropertyGrid</span></span>|  
|<span data-ttu-id="f1057-288">UserControl</span><span class="sxs-lookup"><span data-stu-id="f1057-288">UserControl</span></span>|  
|<span data-ttu-id="f1057-289">ToolStrip</span><span class="sxs-lookup"><span data-stu-id="f1057-289">ToolStrip</span></span>|  
|<span data-ttu-id="f1057-290">TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="f1057-290">TableLayoutPanel</span></span>|  
|<span data-ttu-id="f1057-291">SplitContainer/SplitterPanel</span><span class="sxs-lookup"><span data-stu-id="f1057-291">SplitContainer/SplitterPanel</span></span>|  
|<span data-ttu-id="f1057-292">スプリッター</span><span class="sxs-lookup"><span data-stu-id="f1057-292">Splitter</span></span>|  
|<span data-ttu-id="f1057-293">RaftingContainer</span><span class="sxs-lookup"><span data-stu-id="f1057-293">RaftingContainer</span></span>|  
|<span data-ttu-id="f1057-294">StatusStrip</span><span class="sxs-lookup"><span data-stu-id="f1057-294">StatusStrip</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f1057-295">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1057-295">See Also</span></span>  
 [<span data-ttu-id="f1057-296">UI オートメーション コントロール型</span><span class="sxs-lookup"><span data-stu-id="f1057-296">UI Automation Control Types</span></span>](../../../docs/framework/ui-automation/ui-automation-control-types.md)
