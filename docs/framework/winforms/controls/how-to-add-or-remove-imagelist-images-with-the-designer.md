---
title: '方法 : デザイナーを使って ImageList イメージを追加または削除する'
ms.date: 03/30/2017
helpviewer_keywords:
- ImageList component [Windows Forms], adding images
- ImageList component [Windows Forms], removing images
- images [Windows Forms], adding to ImageList component
ms.assetid: 5699b244-e37c-4d20-bc35-7441e55c1e3a
ms.openlocfilehash: cc85306c68baa4b4a0fe3418c511672d34790ae7
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43864001"
---
# <a name="how-to-add-or-remove-imagelist-images-with-the-designer"></a><span data-ttu-id="9c928-102">方法 : デザイナーを使って ImageList イメージを追加または削除する</span><span class="sxs-lookup"><span data-stu-id="9c928-102">How to: Add or Remove ImageList Images with the Designer</span></span>
<span data-ttu-id="9c928-103">イメージを追加することができます、<xref:System.Windows.Forms.ImageList>コンポーネントのいくつかの方法です。</span><span class="sxs-lookup"><span data-stu-id="9c928-103">You can add images to an <xref:System.Windows.Forms.ImageList> component several different ways.</span></span> <span data-ttu-id="9c928-104">関連付けられているスマート タグを使用してイメージを非常に簡単に追加することができます、 <xref:System.Windows.Forms.ImageList>、やの他のいくつかのプロパティを設定する場合、 <xref:System.Windows.Forms.ImageList>、[プロパティ] ウィンドウを使用したイメージを追加する方が便利見つけることがあります。</span><span class="sxs-lookup"><span data-stu-id="9c928-104">You can add images very quickly by using the smart tag associated with the <xref:System.Windows.Forms.ImageList>, or if you are setting several other properties on the <xref:System.Windows.Forms.ImageList>, you may find it more convenient to add images with the Properties window.</span></span> <span data-ttu-id="9c928-105">コードを使用してイメージを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="9c928-105">You can also add images by using code.</span></span> <span data-ttu-id="9c928-106">コードを使用したイメージを追加する方法の詳細については、次を参照してください。[方法: Windows フォームの ImageList コンポーネントにイメージを追加または](../../../../docs/framework/winforms/controls/how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md)します。</span><span class="sxs-lookup"><span data-stu-id="9c928-106">For more information about how to add images with code, see [How to: Add or Remove Images with the Windows Forms ImageList Component](../../../../docs/framework/winforms/controls/how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).</span></span> <span data-ttu-id="9c928-107">値を設定する通常、<xref:System.Windows.Forms.ImageList>コンポーネントにイメージの前に、コントロールに関連付けられているが、これは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="9c928-107">Typically you populate the <xref:System.Windows.Forms.ImageList> component with images before it is associated with a control, but this is not required.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9c928-108">実際に画面に表示されるダイアログ ボックスとメニュー コマンドは、アクティブな設定またはエディションによっては、ヘルプの説明と異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9c928-108">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="9c928-109">設定を変更するには、 **[ツール]** メニューの **[設定のインポートとエクスポート]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9c928-109">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="9c928-110">詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c928-110">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-add-or-remove-images-by-using-the-properties-window"></a><span data-ttu-id="9c928-111">追加またはプロパティ ウィンドウを使用してイメージを削除するには</span><span class="sxs-lookup"><span data-stu-id="9c928-111">To add or remove images by using the Properties window</span></span>  
  
1.  <span data-ttu-id="9c928-112">選択、<xref:System.Windows.Forms.ImageList>コンポーネントをフォームに追加します。</span><span class="sxs-lookup"><span data-stu-id="9c928-112">Select the <xref:System.Windows.Forms.ImageList> component, or add one to the form.</span></span>  
  
2.  <span data-ttu-id="9c928-113">[プロパティ] ウィンドウで、省略記号ボタンをクリックします。 (![VisualStudioEllipsesButton スクリーン ショット](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) 横に、<xref:System.Windows.Forms.ImageList.Images%2A>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="9c928-113">In the Properties window, click the ellipsis button (![VisualStudioEllipsesButton screenshot](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) next to the <xref:System.Windows.Forms.ImageList.Images%2A> property.</span></span>  
  
3.  <span data-ttu-id="9c928-114">**イメージ コレクション エディター**、 をクリックして**追加**または**削除**を追加または一覧からイメージを削除します。</span><span class="sxs-lookup"><span data-stu-id="9c928-114">In the **Image Collection Editor**, click **Add** or **Remove** to add or remove images from the list.</span></span>  
  
### <a name="to-add-or-remove-images-using-the-smart-tag"></a><span data-ttu-id="9c928-115">スマート タグを使用してイメージを追加または削除</span><span class="sxs-lookup"><span data-stu-id="9c928-115">To add or remove images using the smart tag</span></span>  
  
1.  <span data-ttu-id="9c928-116">選択、<xref:System.Windows.Forms.ImageList>コンポーネントをフォームに追加します。</span><span class="sxs-lookup"><span data-stu-id="9c928-116">Select the <xref:System.Windows.Forms.ImageList> component, or add one to the form.</span></span>  
  
2.  <span data-ttu-id="9c928-117">スマート タグ グリフをクリックします (![スマート タグ グリフ](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph"))</span><span class="sxs-lookup"><span data-stu-id="9c928-117">Click the smart tag glyph (![Smart Tag Glyph](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph"))</span></span>  
  
3.  <span data-ttu-id="9c928-118">**ImageList タスク**ダイアログ ボックスで、**イメージの選択**します。</span><span class="sxs-lookup"><span data-stu-id="9c928-118">In the **ImageList Tasks** dialog box, select **Choose Images**.</span></span>  
  
4.  <span data-ttu-id="9c928-119">**イメージ コレクション エディター**クリックして**追加**または**削除**を追加または一覧からイメージを削除します。</span><span class="sxs-lookup"><span data-stu-id="9c928-119">In the **Images Collection Editor** click **Add** or **Remove** to add or remove images from the list.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c928-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c928-120">See Also</span></span>  
 [<span data-ttu-id="9c928-121">イメージ、ビットマップ、メタファイル</span><span class="sxs-lookup"><span data-stu-id="9c928-121">Images, Bitmaps, and Metafiles</span></span>](../../../../docs/framework/winforms/advanced/images-bitmaps-and-metafiles.md)  
 [<span data-ttu-id="9c928-122">チュートリアル: Windows フォーム コントロールのスマート タグを使用した共通タスクの実行</span><span class="sxs-lookup"><span data-stu-id="9c928-122">Walkthrough: Performing Common Tasks Using Smart Tags on Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/performing-common-tasks-using-smart-tags-on-wf-controls.md)  
 [<span data-ttu-id="9c928-123">ImageList コンポーネント</span><span class="sxs-lookup"><span data-stu-id="9c928-123">ImageList Component</span></span>](../../../../docs/framework/winforms/controls/imagelist-component-windows-forms.md)
