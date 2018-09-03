---
title: '方法 : コントロールを Windows フォームのスナップ線とグリッドを使用して配置する'
ms.date: 03/30/2017
f1_keywords:
- GridSize
helpviewer_keywords:
- snap to grid [Windows Forms], Windows Forms Designer
- Windows Forms, grid options in designer
- controls [Windows Forms], aligning
ms.assetid: bb54bce5-880f-4a36-af68-8cf92058dc1c
ms.openlocfilehash: bbe6ae2adfe364e41f6627e6b067aa8e18e6e079
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43488082"
---
# <a name="how-to-arrange-controls-with-snaplines-and-the-grid-in-windows-forms"></a><span data-ttu-id="813d5-102">方法 : コントロールを Windows フォームのスナップ線とグリッドを使用して配置する</span><span class="sxs-lookup"><span data-stu-id="813d5-102">How to: Arrange Controls with Snaplines and the Grid in Windows Forms</span></span>
<span data-ttu-id="813d5-103">Visual Studio のレイアウト機能を使用すると、フォーム上のコントロールの配置場所を正確に指定できます。</span><span class="sxs-lookup"><span data-stu-id="813d5-103">Using the layout features of Visual Studio, you can precisely direct where controls are placed on a form.</span></span> <span data-ttu-id="813d5-104">コントロールをフォームに追加またはフォーム上の移動を行と、Windows フォーム デザイナーのグリッドの列に自動的に配置またはスナップ線の機能を使用してコントロールを配置することができます。</span><span class="sxs-lookup"><span data-stu-id="813d5-104">Controls added to a form or moved on a form can be automatically aligned to the rows and columns of the Windows Forms Designer's grid, or you can align controls by using the snaplines feature.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="813d5-105">実際に画面に表示されるダイアログ ボックスとメニュー コマンドは、アクティブな設定またはエディションによっては、ヘルプの説明と異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="813d5-105">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="813d5-106">設定を変更するには、 **[ツール]** メニューの **[設定のインポートとエクスポート]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="813d5-106">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="813d5-107">詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="813d5-107">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-snap-all-controls-to-the-grid"></a><span data-ttu-id="813d5-108">すべてのコントロールをグリッドにスナップするには</span><span class="sxs-lookup"><span data-stu-id="813d5-108">To snap all controls to the grid</span></span>  
  
-   <span data-ttu-id="813d5-109">選択、 **SnapToGrid** Windows フォーム デザイナーでレイアウト モード**オプション** ダイアログ ボックス。</span><span class="sxs-lookup"><span data-stu-id="813d5-109">Select the **SnapToGrid** layout mode in the Windows Forms Designer **Options** dialog box.</span></span>  
  
     <span data-ttu-id="813d5-110">詳細については、次を参照してください。 [全般、Windows フォーム デザイナー、オプション ダイアログ ボックス](https://msdn.microsoft.com/library/8dd170af-72f0-4212-b04b-034ceee92834)です。</span><span class="sxs-lookup"><span data-stu-id="813d5-110">For more information, see [General, Windows Forms Designer, Options Dialog Box](https://msdn.microsoft.com/library/8dd170af-72f0-4212-b04b-034ceee92834).</span></span> <span data-ttu-id="813d5-111">すべてのコントロールでは、グリッド上の点に沿った自体今すぐ揃えます。</span><span class="sxs-lookup"><span data-stu-id="813d5-111">All controls now align themselves along the points on the grid.</span></span>  
  
     <span data-ttu-id="813d5-112">グリッドの個々 のコントロールをスナップするには、それらの場所にロックできます。</span><span class="sxs-lookup"><span data-stu-id="813d5-112">You can snap individual controls to the grid by locking them in place.</span></span> <span data-ttu-id="813d5-113">ただしがロックされているときに移動したりできないサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="813d5-113">However, while they are locked, they cannot be moved or resized.</span></span> <span data-ttu-id="813d5-114">コントロールのロックの詳細については、次を参照してください。[方法: Windows フォーム コントロールのロック](../../../../docs/framework/winforms/controls/how-to-lock-controls-to-windows-forms.md)します。</span><span class="sxs-lookup"><span data-stu-id="813d5-114">For more information about locking controls, see [How to: Lock Controls to Windows Forms](../../../../docs/framework/winforms/controls/how-to-lock-controls-to-windows-forms.md).</span></span>  
  
### <a name="to-align-controls-using-snaplines"></a><span data-ttu-id="813d5-115">スナップ線を使用してコントロールを配置するには</span><span class="sxs-lookup"><span data-stu-id="813d5-115">To align controls using snaplines</span></span>  
  
-   <span data-ttu-id="813d5-116">選択、**スナップ**Windows フォーム デザイナーでレイアウト モード**オプション** ダイアログ ボックス。</span><span class="sxs-lookup"><span data-stu-id="813d5-116">Select the **SnapLines** layout mode in the Windows Forms Designer **Options** dialog box.</span></span>  
  
     <span data-ttu-id="813d5-117">詳細については、次を参照してください。[チュートリアル: Arranging Controls on Windows フォームを使用してスナップ](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)します。</span><span class="sxs-lookup"><span data-stu-id="813d5-117">For more information, see [Walkthrough: Arranging Controls on Windows Forms Using Snaplines](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md).</span></span> <span data-ttu-id="813d5-118">スナップ線を使用して、フォーム上のコントロールを揃えたり整列したりすることができますようになりました。</span><span class="sxs-lookup"><span data-stu-id="813d5-118">You can now use snaplines to align and arrange controls on your form.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="813d5-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="813d5-119">See Also</span></span>  
 [<span data-ttu-id="813d5-120">一般に、Windows フォーム デザイナー オプション ダイアログ ボックス</span><span class="sxs-lookup"><span data-stu-id="813d5-120">General, Windows Forms Designer, Options Dialog Box</span></span>](https://msdn.microsoft.com/library/8dd170af-72f0-4212-b04b-034ceee92834)  
 [<span data-ttu-id="813d5-121">チュートリアル: スナップ線を使用した Windows フォーム上のコントロールの配置</span><span class="sxs-lookup"><span data-stu-id="813d5-121">Walkthrough: Arranging Controls on Windows Forms Using Snaplines</span></span>](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)  
 [<span data-ttu-id="813d5-122">Windows フォーム コントロール</span><span class="sxs-lookup"><span data-stu-id="813d5-122">Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/index.md)  
 [<span data-ttu-id="813d5-123">方法: Windows フォームにコントロールを追加する</span><span class="sxs-lookup"><span data-stu-id="813d5-123">How to: Add Controls to Windows Forms</span></span>](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)  
 [<span data-ttu-id="813d5-124">Windows フォームでのコントロールの配置</span><span class="sxs-lookup"><span data-stu-id="813d5-124">Arranging Controls on Windows Forms</span></span>](../../../../docs/framework/winforms/controls/arranging-controls-on-windows-forms.md)  
 [<span data-ttu-id="813d5-125">各 Windows フォーム コントロールのラベル設定とショートカットの作成</span><span class="sxs-lookup"><span data-stu-id="813d5-125">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](../../../../docs/framework/winforms/controls/labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)  
 [<span data-ttu-id="813d5-126">Windows フォームで使用するコントロール</span><span class="sxs-lookup"><span data-stu-id="813d5-126">Controls to Use on Windows Forms</span></span>](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)  
 [<span data-ttu-id="813d5-127">Windows フォーム コントロールの機能別一覧</span><span class="sxs-lookup"><span data-stu-id="813d5-127">Windows Forms Controls by Function</span></span>](../../../../docs/framework/winforms/controls/windows-forms-controls-by-function.md)
