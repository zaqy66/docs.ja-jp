---
title: '方法 : DataRepeater コントロールにバインドされたデータを表示する (Visual Studio)'
ms.date: 07/20/2015
helpviewer_keywords:
- DataRepeater, data-binding
- DataRepeater, displaying bound controls
ms.assetid: 56a15326-1334-4275-af4e-075cad79e6f7
ms.openlocfilehash: b96fb33a0dcf80a86d1fcb6e219e5f35b1f7351c
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42933407"
---
# <a name="how-to-display-bound-data-in-a-datarepeater-control-visual-studio"></a><span data-ttu-id="dadd2-102">方法 : DataRepeater コントロールにバインドされたデータを表示する (Visual Studio)</span><span class="sxs-lookup"><span data-stu-id="dadd2-102">How to: Display Bound Data in a DataRepeater Control (Visual Studio)</span></span>
<span data-ttu-id="dadd2-103">最も一般的な用途、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールは、データベースまたは他のデータ ソースからバインドされたデータを表示します。</span><span class="sxs-lookup"><span data-stu-id="dadd2-103">The most common use of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control is to display bound data from a database or other data source.</span></span>  
  
 <span data-ttu-id="dadd2-104">バインドされたコントロールのほかに静的ラベルなどの各項目に繰り返されるイメージの他のコントロールを追加したい場合があります、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。</span><span class="sxs-lookup"><span data-stu-id="dadd2-104">In addition to bound controls, you may want to add other controls, such as a static label or an image that is repeated on each item in the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span> <span data-ttu-id="dadd2-105">詳細については、次を参照してください。[方法: DataRepeater コントロールにバインドされていないコントロールを表示](../../../visual-basic/developing-apps/windows-forms/how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio.md)します。</span><span class="sxs-lookup"><span data-stu-id="dadd2-105">For more information, see [How to: Display Unbound Controls in a DataRepeater Control](../../../visual-basic/developing-apps/windows-forms/how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio.md).</span></span>  
  
 <span data-ttu-id="dadd2-106">バインドすることできますもデータ ソースに実行時に設定して、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.VirtualMode%2A>プロパティを`True`とするデータ ソースを割り当て、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DataSource%2A>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="dadd2-106">You can also bind to a data source at run time by setting the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.VirtualMode%2A> property to `True` and assigning a data source to the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DataSource%2A> property.</span></span> <span data-ttu-id="dadd2-107">この場合、データ ソースとのすべての相互作用を管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dadd2-107">In this case, you will need to manage all interaction with the data source.</span></span> <span data-ttu-id="dadd2-108">詳細については、次を参照してください。 [DataRepeater コントロールでの仮想モード](../../../visual-basic/developing-apps/windows-forms/virtual-mode-in-the-datarepeater-control-visual-studio.md)します。</span><span class="sxs-lookup"><span data-stu-id="dadd2-108">For more information, see [Virtual Mode in the DataRepeater Control](../../../visual-basic/developing-apps/windows-forms/virtual-mode-in-the-datarepeater-control-visual-studio.md).</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-data-bound-datarepeater"></a><span data-ttu-id="dadd2-109">データ バインド DataRepeater を作成するには</span><span class="sxs-lookup"><span data-stu-id="dadd2-109">To create a data-bound DataRepeater</span></span>  
  
1.  <span data-ttu-id="dadd2-110">ドラッグ、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールから、 **Visual Basic powerpacks**  タブで、**ツールボックス**フォームまたはコンテナー コントロールにします。</span><span class="sxs-lookup"><span data-stu-id="dadd2-110">Drag a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control from the **Visual Basic PowerPacks** tab in the **Toolbox** to a form or container control.</span></span>  
  
2.  <span data-ttu-id="dadd2-111">サイズにサイズと位置のハンドルをドラッグし、コントロールを配置します。</span><span class="sxs-lookup"><span data-stu-id="dadd2-111">Drag the sizing and position handles to size and position the control.</span></span>  
  
     <span data-ttu-id="dadd2-112">コントロールに 2 つの四角形領域があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="dadd2-112">Note that the control has two rectangular regions.</span></span> <span data-ttu-id="dadd2-113">上部の領域は、*項目テンプレート*; 内の各項目で、テンプレートに追加されたコントロールが繰り返されます、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>実行時にコントロール。</span><span class="sxs-lookup"><span data-stu-id="dadd2-113">The upper region is the *item template*; controls added to the template will be repeated in each item in the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control at run time.</span></span> <span data-ttu-id="dadd2-114">下部の領域は、*ビューポート*項目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="dadd2-114">The lower region is the *viewport*, where the items will be displayed.</span></span>  
  
     <span data-ttu-id="dadd2-115">サイズを変更し、変更することで、コントロールまたは項目テンプレートを配置することもできます、**サイズ**と**位置**プロパティ ウィンドウでプロパティ。</span><span class="sxs-lookup"><span data-stu-id="dadd2-115">You can also size and position the control or the item template by changing the **Size** and **Position** properties in the Properties window.</span></span>  
  
3.  <span data-ttu-id="dadd2-116">**[データ]** メニューの **[データ ソースの表示]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dadd2-116">On the **Data** menu, click **Show Data Sources**.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="dadd2-117">場合、**データソース**ウィンドウが空の場合、データ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="dadd2-117">If the **Data Sources** window is empty, add a data source to it.</span></span> <span data-ttu-id="dadd2-118">詳細については、「[新しいデータ ソースの追加](/visualstudio/data-tools/add-new-data-sources)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dadd2-118">For more information, see [Add new data sources](/visualstudio/data-tools/add-new-data-sources).</span></span>  
  
4.  <span data-ttu-id="dadd2-119">**データソース**ウィンドウで、最上位ノードにバインドするデータを含むテーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="dadd2-119">In the **Data Sources** window, select the top-level node for the table that contains the data that you want to bind.</span></span>  
  
5.  <span data-ttu-id="dadd2-120">変更するテーブルのドロップ タイプ`Details`をクリックして`Details`テーブル ノードのドロップダウン リストでします。</span><span class="sxs-lookup"><span data-stu-id="dadd2-120">Change the drop type of the table to `Details` by clicking `Details` in the drop-down list on the table node.</span></span>  
  
6.  <span data-ttu-id="dadd2-121">テーブル ノードを選択し、項目テンプレート領域にドラッグ、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。</span><span class="sxs-lookup"><span data-stu-id="dadd2-121">Select the table node and drag it onto the item template region of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span>  
  
     <span data-ttu-id="dadd2-122">フィールドごとに表示されるコントロールの種類を指定できます。</span><span class="sxs-lookup"><span data-stu-id="dadd2-122">You can specify which types of controls are displayed for each field.</span></span> <span data-ttu-id="dadd2-123">詳細については、次を参照してください。[設定、データ ソース ウィンドウからドラッグするときに作成されるコントロール](/visualstudio/data-tools/set-the-control-to-be-created-when-dragging-from-the-data-sources-window)します。</span><span class="sxs-lookup"><span data-stu-id="dadd2-123">For more information, see [Set the control to be created when dragging from the Data Sources window](/visualstudio/data-tools/set-the-control-to-be-created-when-dragging-from-the-data-sources-window).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dadd2-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="dadd2-124">See Also</span></span>  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>  
 [<span data-ttu-id="dadd2-125">DataRepeater コントロールの概要</span><span class="sxs-lookup"><span data-stu-id="dadd2-125">Introduction to the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)  
 [<span data-ttu-id="dadd2-126">方法: DataRepeater コントロールに非バインド コントロールを表示する</span><span class="sxs-lookup"><span data-stu-id="dadd2-126">How to: Display Unbound Controls in a DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio.md)  
 [<span data-ttu-id="dadd2-127">方法: 2 つの DataRepeater コントロール (Visual Studio) を使用してマスター/詳細フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="dadd2-127">How to: Create a Master/Detail Form by Using Two DataRepeater Controls (Visual Studio)</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-create-a-master-detail-form-by-using-two-datarepeater-controls.md)  
 [<span data-ttu-id="dadd2-128">方法: DataRepeater コントロールの外観を変更する</span><span class="sxs-lookup"><span data-stu-id="dadd2-128">How to: Change the Appearance of a DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)  
 [<span data-ttu-id="dadd2-129">DataRepeater コントロールのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="dadd2-129">Troubleshooting the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
