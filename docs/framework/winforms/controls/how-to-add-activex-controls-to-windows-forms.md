---
title: '方法 : Windows フォームに ActiveX コントロールを追加する'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, ActiveX controls
- forms [Windows Forms], adding ActiveX controls
- ActiveX controls [Windows Forms], adding
ms.assetid: 54a61e5b-555e-4887-b41e-6244fed271eb
ms.openlocfilehash: 7d6514c679187e9ec193f6dda8336c8bd56fac81
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2018
ms.locfileid: "47396943"
---
# <a name="how-to-add-activex-controls-to-windows-forms"></a><span data-ttu-id="1fa6a-102">方法 : Windows フォームに ActiveX コントロールを追加する</span><span class="sxs-lookup"><span data-stu-id="1fa6a-102">How to: Add ActiveX Controls to Windows Forms</span></span>
<span data-ttu-id="1fa6a-103">Windows フォーム コントロールをホストするには、Windows フォーム デザイナーが最適化され、中には、Windows フォームで ActiveX コントロールも記述できます。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-103">While the Windows Forms Designer is optimized to host Windows Forms controls, you can also put ActiveX controls on Windows Forms.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="1fa6a-104">ActiveX コントロールを追加することがある場合に、Windows フォームのパフォーマンスの制限があります。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-104">There are performance limitations for Windows Forms when ActiveX controls are added to them.</span></span>  
  
 <span data-ttu-id="1fa6a-105">ActiveX コントロールをフォームに追加する前に、ツールボックスに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-105">Before you add ActiveX controls to your form, you must add them to the Toolbox.</span></span> <span data-ttu-id="1fa6a-106">詳細については、次を参照してください。 [COM コンポーネント、ツールボックスのカスタマイズ ダイアログ ボックス](https://msdn.microsoft.com/library/171333f3-f207-4e02-bbdc-17862556212c)します。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-106">For more information, see [COM Components, Customize Toolbox Dialog Box](https://msdn.microsoft.com/library/171333f3-f207-4e02-bbdc-17862556212c).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1fa6a-107">実際に画面に表示されるダイアログ ボックスとメニュー コマンドは、アクティブな設定またはエディションによっては、ヘルプの説明と異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-107">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="1fa6a-108">設定を変更するには、 **[ツール]** メニューの **[設定のインポートとエクスポート]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-108">To change your settings, click **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="1fa6a-109">詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-109">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-add-an-activex-control-to-your-windows-form"></a><span data-ttu-id="1fa6a-110">Windows フォームに ActiveX コントロールを追加するには</span><span class="sxs-lookup"><span data-stu-id="1fa6a-110">To add an ActiveX control to your Windows Form</span></span>  
  
-   <span data-ttu-id="1fa6a-111">ツールボックスにコントロールをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-111">Double-click the control on the Toolbox.</span></span>  
  
     <span data-ttu-id="1fa6a-112">Visual Studio では、プロジェクトのコントロールにすべての参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-112">Visual Studio adds all references to the control in your project.</span></span> <span data-ttu-id="1fa6a-113">Windows フォームで ActiveX コントロールを使用する場合に留意すべき点の詳細については、次を参照してください。 [Windows フォームで ActiveX コントロールをホストしている場合の考慮事項](../../../../docs/framework/winforms/controls/considerations-when-hosting-an-activex-control-on-a-windows-form.md)します。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-113">For more information about things to keep in mind when using ActiveX controls on Windows Forms, see [Considerations When Hosting an ActiveX Control on a Windows Form](../../../../docs/framework/winforms/controls/considerations-when-hosting-an-activex-control-on-a-windows-form.md).</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="1fa6a-114">Windows フォーム ActiveX コントロール インポーター (AxImp.exe) は、ActiveX のダイナミック リンク ライブラリのインポート時に予想よりも、別の種類のイベント引数を作成します。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-114">The Windows Forms ActiveX Control Importer (AxImp.exe) creates event arguments of a different type than expected upon importation of ActiveX dynamic link libraries.</span></span> <span data-ttu-id="1fa6a-115">AxImp.exe によって作成された引数は、次のような: `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEvent e)`、`Invoke(object sender, DWebBrowserEvents2_ProgressChangeEventArgs e)`が必要です。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-115">The arguments created by AxImp.exe are similar to the following: `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEvent e)`, when `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEventArgs e)` is expected.</span></span> <span data-ttu-id="1fa6a-116">この不規則性から正常に機能して、コードが回避しないことに注意します。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-116">Be aware that this irregularity does not prevent code from functioning normally.</span></span> <span data-ttu-id="1fa6a-117">詳細については、次を参照してください。 [Windows フォーム ActiveX コントロール インポーター (Aximp.exe)](../../../../docs/framework/tools/aximp-exe-windows-forms-activex-control-importer.md)します。</span><span class="sxs-lookup"><span data-stu-id="1fa6a-117">For details, see [Windows Forms ActiveX Control Importer (Aximp.exe)](../../../../docs/framework/tools/aximp-exe-windows-forms-activex-control-importer.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1fa6a-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="1fa6a-118">See Also</span></span>  
 [<span data-ttu-id="1fa6a-119">Windows フォーム コントロール</span><span class="sxs-lookup"><span data-stu-id="1fa6a-119">Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/index.md)  
 [<span data-ttu-id="1fa6a-120">各言語およびライブラリにおける、コントロールとプログラミング可能オブジェクトの比較</span><span class="sxs-lookup"><span data-stu-id="1fa6a-120">Controls and Programmable Objects Compared in Various Languages and Libraries</span></span>](https://msdn.microsoft.com/library/021f2a1b-8247-4348-a5ad-e1d9ab23004b)  
 [<span data-ttu-id="1fa6a-121">方法: Windows フォームにコントロールを追加する</span><span class="sxs-lookup"><span data-stu-id="1fa6a-121">How to: Add Controls to Windows Forms</span></span>](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)  
 [<span data-ttu-id="1fa6a-122">Windows フォームでのコントロールの配置</span><span class="sxs-lookup"><span data-stu-id="1fa6a-122">Arranging Controls on Windows Forms</span></span>](../../../../docs/framework/winforms/controls/arranging-controls-on-windows-forms.md)  
 [<span data-ttu-id="1fa6a-123">各 Windows フォーム コントロールのラベル設定とショートカットの作成</span><span class="sxs-lookup"><span data-stu-id="1fa6a-123">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](../../../../docs/framework/winforms/controls/labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)  
 [<span data-ttu-id="1fa6a-124">Windows フォームで使用するコントロール</span><span class="sxs-lookup"><span data-stu-id="1fa6a-124">Controls to Use on Windows Forms</span></span>](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)  
 [<span data-ttu-id="1fa6a-125">Windows フォーム コントロールの機能別一覧</span><span class="sxs-lookup"><span data-stu-id="1fa6a-125">Windows Forms Controls by Function</span></span>](../../../../docs/framework/winforms/controls/windows-forms-controls-by-function.md)
