---
title: '方法: 追加と削除 (Visual Studio) DataRepeater の項目を無効にします。'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, disabling delete
- DataRepeater, disabling add
ms.assetid: 298d8f60-ddfe-4361-ab66-cf76d0df5220
ms.openlocfilehash: 3a304132d0514da4c19811be2536c9516e2838f0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54618543"
---
# <a name="how-to-disable-adding-and-deleting-datarepeater-items-visual-studio"></a><span data-ttu-id="c6f8d-102">方法: 追加と削除 (Visual Studio) DataRepeater の項目を無効にします。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-102">How to: Disable Adding and Deleting DataRepeater Items (Visual Studio)</span></span>
<span data-ttu-id="c6f8d-103">既定では、ユーザーは追加し、項目の削除、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-103">By default, users can add and delete items in a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span> <span data-ttu-id="c6f8d-104">ユーザーは、CTRL キーを押しながら N キーを押して、新しい項目を追加するときに、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A>フォーカスを持っているか、クリックして、 **AddNewItem**のボタンでは、<xref:System.Windows.Forms.BindingNavigator>コントロール。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-104">Users can add a new item by pressing CTRL+N when a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A> has focus or by clicking the **AddNewItem** button on the <xref:System.Windows.Forms.BindingNavigator> control.</span></span> <span data-ttu-id="c6f8d-105">ユーザーがキーを押して、項目を削除できるときに削除、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A>フォーカスを持っているか、クリックして、 **DeleteItem**のボタンでは、<xref:System.Windows.Forms.BindingNavigator>コントロール。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-105">Users can delete an item by pressing DELETE when a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A> has focus or by clicking the **DeleteItem** button on the <xref:System.Windows.Forms.BindingNavigator> control.</span></span>  
  
 <span data-ttu-id="c6f8d-106">追加と削除のデザイン時または実行時に無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-106">You can disable adding and/or deleting at design time or at run time.</span></span>  
  
### <a name="to-disable-adding-and-deleting-at-design-time"></a><span data-ttu-id="c6f8d-107">デザイン時に追加と削除を無効にするには</span><span class="sxs-lookup"><span data-stu-id="c6f8d-107">To disable adding and deleting at design time</span></span>  
  
1.  <span data-ttu-id="c6f8d-108">Windows フォーム デザイナーで、選択、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-108">In the Windows Forms Designer, select the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="c6f8d-109">コントロールの下のセクションを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-109">You must select the lower section of the control.</span></span> <span data-ttu-id="c6f8d-110">項目テンプレートのセクションを選択すると、異なるプロパティのセットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-110">If you select the item template section, a different set of properties will be displayed.</span></span>  
  
2.  <span data-ttu-id="c6f8d-111">[プロパティ] ウィンドウで次のように設定します。、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToAddItems%2A>プロパティを**False**します。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-111">In the Properties window, set the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToAddItems%2A> property to **False**.</span></span>  
  
3.  <span data-ttu-id="c6f8d-112">設定、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToDeleteItems%2A>プロパティを**False**します。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-112">Set the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToDeleteItems%2A> property to **False**.</span></span>  
  
4.  <span data-ttu-id="c6f8d-113">Windows フォーム デザイナーで、選択、<xref:System.Windows.Forms.BindingNavigator>コントロールをクリックして、 **AddNewItem**ボタン (これで、プラス記号のボタン)。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-113">In the Windows Forms Designer, select the <xref:System.Windows.Forms.BindingNavigator> control, and then click the **AddNewItem** button (the button with a plus sign on it).</span></span>  
  
5.  <span data-ttu-id="c6f8d-114">[プロパティ] ウィンドウで次のように設定します。、<xref:System.Windows.Forms.ToolBarButton.Enabled%2A>プロパティを**False**します。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-114">In the Properties window, set the <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> property to **False**.</span></span>  
  
6.  <span data-ttu-id="c6f8d-115">Windows フォーム デザイナーで、選択、<xref:System.Windows.Forms.BindingNavigator>コントロールをクリックして、 **DeleteItem**ボタン (に赤い x 印のボタン)。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-115">In the Windows Forms Designer, select the <xref:System.Windows.Forms.BindingNavigator> control, and then click the **DeleteItem** button (the button with a red X on it).</span></span>  
  
7.  <span data-ttu-id="c6f8d-116">[プロパティ] ウィンドウで次のように設定します。、<xref:System.Windows.Forms.ToolBarButton.Enabled%2A>プロパティを**False**します。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-116">In the Properties window, set the <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> property to **False**.</span></span>  
  
8.  <span data-ttu-id="c6f8d-117">コンポーネント トレイの選択、<xref:System.Windows.Forms.BindingSource>先、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>がバインドされています。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-117">In the Component Tray, select the <xref:System.Windows.Forms.BindingSource> to which the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> is bound.</span></span>  
  
9. <span data-ttu-id="c6f8d-118">[プロパティ] ウィンドウで次のように設定します。、<xref:System.Windows.Forms.BindingSource.AllowNew%2A>プロパティを**False**します。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-118">In the Properties window, set the <xref:System.Windows.Forms.BindingSource.AllowNew%2A> property to **False**.</span></span>  
  
10. <span data-ttu-id="c6f8d-119">Windows フォーム デザイナーで、ダブルクリック、 **DeleteItem**コード エディターを開くボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-119">In the Windows Forms Designer, double-click the **DeleteItem** button to open the Code Editor.</span></span>  
  
11. <span data-ttu-id="c6f8d-120">イベントのドロップダウン リストで選択、`BindingNavigatorDeleteItem_EnabledChanged`イベント。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-120">In the Events drop-down list, select the `BindingNavigatorDeleteItem_EnabledChanged` event.</span></span>  
  
12. <span data-ttu-id="c6f8d-121">`BindingNavigatorDeleteItem_EnabledChanged` イベント ハンドラーに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-121">Add the following code to the `BindingNavigatorDeleteItem_EnabledChanged` event handler:</span></span>  
  
     [!code-csharp[VbPowerPacksDataRepeaterDisableAddDelete#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksDataRepeaterDisableAddDelete#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_1.vb)]  
  
    > [!NOTE]
    >  <span data-ttu-id="c6f8d-122">この手順が必要なのは、現在のレコードが変更されるたびに <xref:System.Windows.Forms.BindingSource> によって **DeleteItem** ボタンが有効になるためです。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-122">This step is necessary because the <xref:System.Windows.Forms.BindingSource> will enable the **DeleteItem** button every time that the current record changes.</span></span>  
  
### <a name="to-disable-adding-and-deleting-at-run-time"></a><span data-ttu-id="c6f8d-123">実行時に追加と削除を無効にするには</span><span class="sxs-lookup"><span data-stu-id="c6f8d-123">To disable adding and deleting at run time</span></span>  
  
1.  <span data-ttu-id="c6f8d-124">Windows フォーム デザイナーで、フォームをダブルクリックしてコード エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-124">In the Windows Forms Designer, double-click the form to open the Code Editor.</span></span>  
  
2.  <span data-ttu-id="c6f8d-125">`Form_Load` イベントに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-125">Add the following code to the `Form_Load` event:</span></span>  
  
     [!code-csharp[VbPowerPacksDataRepeaterDisableAddDelete#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_2.cs)]
     [!code-vb[VbPowerPacksDataRepeaterDisableAddDelete#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_2.vb)]  
  
3.  <span data-ttu-id="c6f8d-126">`BindingNavigatorDeleteItem_EnabledChanged` イベント ハンドラーに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-126">Add the following code to the `BindingNavigatorDeleteItem_EnabledChanged` event handler:</span></span>  
  
     [!code-csharp[VbPowerPacksDataRepeaterDisableAddDelete#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksDataRepeaterDisableAddDelete#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_1.vb)]  
  
    > [!NOTE]
    >  <span data-ttu-id="c6f8d-127">この手順が必要なのは、現在のレコードが変更されるたびに <xref:System.Windows.Forms.BindingSource> によって **DeleteItem** ボタンが有効になるためです。</span><span class="sxs-lookup"><span data-stu-id="c6f8d-127">This step is necessary because the <xref:System.Windows.Forms.BindingSource> will enable the **DeleteItem** button every time that the current record changes.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6f8d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="c6f8d-128">See also</span></span>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- [<span data-ttu-id="c6f8d-129">DataRepeater コントロールの概要</span><span class="sxs-lookup"><span data-stu-id="c6f8d-129">Introduction to the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [<span data-ttu-id="c6f8d-130">DataRepeater コントロールのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="c6f8d-130">Troubleshooting the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
