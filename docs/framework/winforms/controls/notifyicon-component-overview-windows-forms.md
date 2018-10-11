---
title: NotifyIcon コンポーネントの概要 (Windows フォーム)
ms.date: 03/30/2017
f1_keywords:
- NotifyIcon
helpviewer_keywords:
- NotifyIcon component [Windows Forms], about NotifyIcon component
- system tray icons [Windows Forms], about system tray icons
- system tray icons [Windows Forms], using in Windows Forms
ms.assetid: 5b9189fa-d4ae-41a6-9b97-eb1f44bb1a69
ms.openlocfilehash: 5d77099eeb1ef33f3b9e65bd99d4e22e38c3ec38
ms.sourcegitcommit: 2eb5ca4956231c1a0efd34b6a9cab6153a5438af
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/11/2018
ms.locfileid: "49087207"
---
# <a name="notifyicon-component-overview-windows-forms"></a><span data-ttu-id="70682-102">NotifyIcon コンポーネントの概要 (Windows フォーム)</span><span class="sxs-lookup"><span data-stu-id="70682-102">NotifyIcon Component Overview (Windows Forms)</span></span>

<span data-ttu-id="70682-103">Windows フォームの <xref:System.Windows.Forms.NotifyIcon> コンポーネントは、通常、バックグラウンドで動作し、ユーザー インターフェイスに長時間表示されないプロセスのアイコンを表示する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="70682-103">The Windows Forms <xref:System.Windows.Forms.NotifyIcon> component is typically used to display icons for processes that run in the background and do not show a user interface much of the time.</span></span> <span data-ttu-id="70682-104">たとえば、タスク バーの状態通知領域のアイコンをクリックしてアクセス可能なウイルス対策プログラムなどです。</span><span class="sxs-lookup"><span data-stu-id="70682-104">An example would be a virus protection program that can be accessed by clicking an icon in the status notification area of the taskbar.</span></span>

## <a name="key-properties-of-notifyicons"></a><span data-ttu-id="70682-105">NotifyIcons のキー プロパティ</span><span class="sxs-lookup"><span data-stu-id="70682-105">Key Properties of NotifyIcons</span></span>

<span data-ttu-id="70682-106">各 <xref:System.Windows.Forms.NotifyIcon> コンポーネントは、ステータス領域に 1 つのアイコンを表示します。</span><span class="sxs-lookup"><span data-stu-id="70682-106">Each <xref:System.Windows.Forms.NotifyIcon> component displays a single icon in the status area.</span></span> <span data-ttu-id="70682-107">3 つのバック グラウンド プロセスがあり、それぞれのアイコンを表示する必要がある場合は、3 つの <xref:System.Windows.Forms.NotifyIcon> コンポーネントをフォームに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70682-107">If you have three background processes and wish to display an icon for each, you must add three <xref:System.Windows.Forms.NotifyIcon> components to the form.</span></span> <span data-ttu-id="70682-108"><xref:System.Windows.Forms.NotifyIcon> コンポーネントのキー プロパティは、<xref:System.Windows.Forms.NotifyIcon.Icon%2A> および <xref:System.Windows.Forms.NotifyIcon.Visible%2A> です。</span><span class="sxs-lookup"><span data-stu-id="70682-108">The key properties of the <xref:System.Windows.Forms.NotifyIcon> component are <xref:System.Windows.Forms.NotifyIcon.Icon%2A> and <xref:System.Windows.Forms.NotifyIcon.Visible%2A>.</span></span> <span data-ttu-id="70682-109"><xref:System.Windows.Forms.NotifyIcon.Icon%2A> プロパティは、ステータス領域に表示されるアイコンを設定します。</span><span class="sxs-lookup"><span data-stu-id="70682-109">The <xref:System.Windows.Forms.NotifyIcon.Icon%2A> property sets the icon that appears in the status area.</span></span> <span data-ttu-id="70682-110">アイコンを表示するために、<xref:System.Windows.Forms.NotifyIcon.Visible%2A> プロパティを `true` に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70682-110">In order for the icon to appear, the <xref:System.Windows.Forms.NotifyIcon.Visible%2A> property must be set to `true`.</span></span>

## <a name="notifyicons-options"></a><span data-ttu-id="70682-111">NotifyIcons オプション</span><span class="sxs-lookup"><span data-stu-id="70682-111">NotifyIcons Options</span></span>

<span data-ttu-id="70682-112">バルーン ヒント、ショートカット メニュー、およびツールヒントを <xref:System.Windows.Forms.NotifyIcon> に関連付けて、ユーザーを支援できます。</span><span class="sxs-lookup"><span data-stu-id="70682-112">You can associate balloon tips, shortcut menus, and ToolTips with a <xref:System.Windows.Forms.NotifyIcon> to assist the user.</span></span>

<span data-ttu-id="70682-113"><xref:System.Windows.Forms.NotifyIcon.ShowBalloonTip%2A> メソッドを呼び出して、バルーンヒントを表示する期間を指定することで、<xref:System.Windows.Forms.NotifyIcon> のバルーン ヒントを表示できます。</span><span class="sxs-lookup"><span data-stu-id="70682-113">You can display balloon tips for a <xref:System.Windows.Forms.NotifyIcon> by calling the <xref:System.Windows.Forms.NotifyIcon.ShowBalloonTip%2A> method specifying the time span you wish the balloon tip to display.</span></span> <span data-ttu-id="70682-114">テキスト、アイコン、およびとバルーン ヒントのタイトルを、それぞれ <xref:System.Windows.Forms.NotifyIcon.BalloonTipText%2A>、<xref:System.Windows.Forms.NotifyIcon.BalloonTipIcon%2A>、および <xref:System.Windows.Forms.NotifyIcon.BalloonTipTitle%2A> を使用して指定できます。</span><span class="sxs-lookup"><span data-stu-id="70682-114">You can also specify the text, icon and title of the balloon tip with the <xref:System.Windows.Forms.NotifyIcon.BalloonTipText%2A>, <xref:System.Windows.Forms.NotifyIcon.BalloonTipIcon%2A> and <xref:System.Windows.Forms.NotifyIcon.BalloonTipTitle%2A>, respectively.</span></span> <span data-ttu-id="70682-115"><xref:System.Windows.Forms.NotifyIcon> コンポーネントには、ツールヒントとショートカット メニューも関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="70682-115"><xref:System.Windows.Forms.NotifyIcon> components can also have associated ToolTips and shortcut menus.</span></span> <span data-ttu-id="70682-116">詳細については、次を参照してください。 [ToolTip コンポーネントの概要](../../../../docs/framework/winforms/controls/tooltip-component-overview-windows-forms.md)と[ContextMenu コンポーネントの概要](../../../../docs/framework/winforms/controls/contextmenu-component-overview-windows-forms.md)します。</span><span class="sxs-lookup"><span data-stu-id="70682-116">For more information, see [ToolTip Component Overview](../../../../docs/framework/winforms/controls/tooltip-component-overview-windows-forms.md) and [ContextMenu Component Overview](../../../../docs/framework/winforms/controls/contextmenu-component-overview-windows-forms.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="70682-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="70682-117">See Also</span></span>

- <xref:System.Windows.Forms.NotifyIcon>
- [<span data-ttu-id="70682-118">NotifyIcon コンポーネント</span><span class="sxs-lookup"><span data-stu-id="70682-118">NotifyIcon Component</span></span>](../../../../docs/framework/winforms/controls/notifyicon-component-windows-forms.md)