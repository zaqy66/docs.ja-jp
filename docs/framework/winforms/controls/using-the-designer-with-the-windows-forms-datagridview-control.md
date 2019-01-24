---
title: Windows フォーム DataGridView コントロールでのデザイナーの使用
ms.date: 03/30/2017
helpviewer_keywords:
- tables [Windows Forms]
- DataGridView control [Windows Forms], designer support
- formatting [Windows Forms]
ms.assetid: b66057a6-5983-4864-b4e7-8cbc88a7010c
ms.openlocfilehash: 588db8b2f66bbfd58ea6197a7b5a65bb8ecbfd19
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54644812"
---
# <a name="using-the-designer-with-the-windows-forms-datagridview-control"></a><span data-ttu-id="74a5f-102">Windows フォーム DataGridView コントロールでのデザイナーの使用</span><span class="sxs-lookup"><span data-stu-id="74a5f-102">Using the Designer with the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="74a5f-103">Visual Studio のデザイナー サポートを提供する、`DataGridView`制御コードを記述することがなく多くのセットアップ タスクを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="74a5f-103">Visual Studio provides designer support for the `DataGridView` control that enables you to perform many setup tasks without writing code.</span></span> <span data-ttu-id="74a5f-104">これらのタスクには、データを表示する列の変更、データ ソースにコントロールが使用されるバインディングと、コントロールの基本的な動作と外観を調整することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="74a5f-104">These tasks include binding the control to a data source, modifying the columns used to display data, and adjusting the appearance and basic behavior of the control.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="74a5f-105">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="74a5f-105">In This Section</span></span>  
 [<span data-ttu-id="74a5f-106">方法: 追加して、デザイナーを使用して Windows フォーム DataGridView コントロールで列を削除</span><span class="sxs-lookup"><span data-stu-id="74a5f-106">How to: Add and Remove Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/add-and-remove-columns-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="74a5f-107">使用する方法について説明します、**列の追加**と**列の編集**ダイアログ ボックスで設定して、列のコレクションを変更します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-107">Describes how to use the **Add Columns** and **Edit Columns** dialog boxes to populate and modify the columns collection.</span></span>  
  
 [<span data-ttu-id="74a5f-108">方法: データ デザイナーを使用して Windows フォーム DataGridView コントロールをバインドします。</span><span class="sxs-lookup"><span data-stu-id="74a5f-108">How to: Bind Data to the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/bind-data-to-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="74a5f-109">使用する方法について説明します、**データ ソースの選択**データに接続するコントロールのスマート タグ オプション。</span><span class="sxs-lookup"><span data-stu-id="74a5f-109">Describes how to use the **Choose Data Source** option on the control's smart tag to connect to data.</span></span>  
  
 [<span data-ttu-id="74a5f-110">方法: デザイナーを使用して Windows フォーム DataGridView コントロール内の列の順序を変更します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-110">How to: Change the Order of Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/change-the-order-of-columns-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="74a5f-111">使用する方法について説明します、**列の編集**列を並べ替える ダイアログ ボックス。</span><span class="sxs-lookup"><span data-stu-id="74a5f-111">Describes how to use the **Edit Columns** dialog box to rearrange columns.</span></span>  
  
 [<span data-ttu-id="74a5f-112">方法: デザイナーを使用して Windows フォーム DataGridView 列の型を変更します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-112">How to: Change the Type of a Windows Forms DataGridView Column Using the Designer</span></span>](../../../../docs/framework/winforms/controls/change-the-type-of-a-wf-datagridview-column-using-the-designer.md)  
 <span data-ttu-id="74a5f-113">使用する方法について説明します、**列の編集**ダイアログ ボックスの列の種類を変更します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-113">Describes how to use the **Edit Columns** dialog box to change column types.</span></span>  
  
 [<span data-ttu-id="74a5f-114">方法: デザイナーを使用して Windows フォーム DataGridView コントロール内の列の並べ替えを有効にします。</span><span class="sxs-lookup"><span data-stu-id="74a5f-114">How to: Enable Column Reordering in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/enable-column-reordering-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="74a5f-115">コントロールのスマート タグを使用して、ユーザーが列を再配置を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-115">Describes how to use the control's smart tag to enable users to rearrange columns.</span></span>  
  
 [<span data-ttu-id="74a5f-116">方法: デザイナーを使用して Windows フォーム DataGridView コントロールで列を固定します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-116">How to: Freeze Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/freeze-columns-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="74a5f-117">使用する方法について説明します、**列の編集**を特定の列がスクロールするを防ぐためにダイアログ ボックス。</span><span class="sxs-lookup"><span data-stu-id="74a5f-117">Describes how to use the **Edit Columns** dialog box to prevent specific columns from scrolling.</span></span>  
  
 [<span data-ttu-id="74a5f-118">方法: デザイナーを使用して Windows フォーム DataGridView コントロール内の列を非表示にします。</span><span class="sxs-lookup"><span data-stu-id="74a5f-118">How to: Hide Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/hide-columns-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="74a5f-119">使用する方法について説明します、**列の編集** ダイアログ ボックスの特定の列を非表示にします。</span><span class="sxs-lookup"><span data-stu-id="74a5f-119">Describes how to use the **Edit Columns** dialog box to hide specific columns.</span></span>  
  
 [<span data-ttu-id="74a5f-120">方法: 読み取り専用デザイナーを使用して Windows フォーム DataGridView コントロールで列を作成します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-120">How to: Make Columns Read-Only in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/make-columns-read-only-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="74a5f-121">使用する方法について説明します、**列の編集**ユーザーが編集できないようにする ダイアログ ボックスは、特定の列に値します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-121">Describes how to use the **Edit Columns** dialog box to prevent users from editing values in specific columns.</span></span>  
  
 [<span data-ttu-id="74a5f-122">方法: デザイナーを使用して Windows フォーム DataGridView コントロールで行の追加および削除を防ぐ</span><span class="sxs-lookup"><span data-stu-id="74a5f-122">How to: Prevent Row Addition and Deletion in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/prevent-row-addition-and-deletion-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="74a5f-123">コントロールのスマート タグを使用してユーザーを追加または行の削除を防止する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-123">Describes how to use the control's smart tag to prevent users from adding or deleting rows.</span></span>  
  
 [<span data-ttu-id="74a5f-124">方法: デザイナーを使用して Windows フォーム DataGridView コントロールの交互の行のスタイル設定します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-124">How to: Set Alternating Row Styles for the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/set-alternating-row-styles-for-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="74a5f-125">使用する方法について説明します、 **CellStyle ビルダー**ダイアログ ボックス コントロールで帳簿のような外観を作成します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-125">Describes how to use the **CellStyle Builder** dialog box to create a ledger-like appearance in the control.</span></span>  
  
 [<span data-ttu-id="74a5f-126">方法: デザイナーを使用して Windows フォーム DataGridView コントロールの既定のセル スタイルとデータ形式を設定します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-126">How to: Set Default Cell Styles and Data Formats for the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/default-cell-styles-datagridview.md)  
 <span data-ttu-id="74a5f-127">使用する方法について説明します、 **[CellStyle ビルダー**データ表示と基本的な外観を設定する] ダイアログ ボックスのコントロールの書式設定します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-127">Describes how to use the **CellStyle Builder** dialog box to set up the basic appearance and data-display formats for the control.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="74a5f-128">参照</span><span class="sxs-lookup"><span data-stu-id="74a5f-128">Reference</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <span data-ttu-id="74a5f-129"><xref:System.Windows.Forms.DataGridView> コントロールのリファレンス ドキュメントを提供します。</span><span class="sxs-lookup"><span data-stu-id="74a5f-129">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="74a5f-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="74a5f-130">See also</span></span>
- [<span data-ttu-id="74a5f-131">DataGridView コントロール</span><span class="sxs-lookup"><span data-stu-id="74a5f-131">DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/datagridview-control-windows-forms.md)
