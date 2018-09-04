---
title: '方法 : スプラッシュ スクリーンを WPF アプリケーションに追加する'
ms.date: 08/18/2018
helpviewer_keywords:
- WPF [WPF], splash screen
- startup window [WPF]
- SplashScreen class [WPF]
- splash screen [WPF]
ms.assetid: d70a25c4-5fb9-4c27-b01d-b1b8ef39b3fd
ms.openlocfilehash: 46efa041736870c5c0f08baa321ef0dc53cacc0d
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43502755"
---
# <a name="how-to-add-a-splash-screen-to-a-wpf-application"></a><span data-ttu-id="1fab9-102">方法 : スプラッシュ スクリーンを WPF アプリケーションに追加する</span><span class="sxs-lookup"><span data-stu-id="1fab9-102">How to: Add a Splash Screen to a WPF Application</span></span>

<span data-ttu-id="1fab9-103">このトピックでは、スタートアップ ウィンドウを追加する方法または*スプラッシュ スクリーン*、Windows Presentation Foundation (WPF) アプリケーションにします。</span><span class="sxs-lookup"><span data-stu-id="1fab9-103">This topic shows how to add a startup window, or *splash screen*, to a Windows Presentation Foundation (WPF) application.</span></span>

## <a name="to-add-an-existing-image-as-a-splash-screen"></a><span data-ttu-id="1fab9-104">スプラッシュ スクリーンとして既存のイメージを追加するには</span><span class="sxs-lookup"><span data-stu-id="1fab9-104">To add an existing image as a splash screen</span></span>

1.  <span data-ttu-id="1fab9-105">スプラッシュ スクリーンを使用するイメージを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="1fab9-105">Create or find an image that you want to use for the splash screen.</span></span> <span data-ttu-id="1fab9-106">Windows Imaging Component (WIC) ではサポートされている任意のイメージ形式を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="1fab9-106">You can use any image format that is supported by the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="1fab9-107">たとえば、BMP、GIF、JPEG、PNG、または TIFF の形式を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="1fab9-107">For example, you can use the BMP, GIF, JPEG, PNG, or TIFF format.</span></span>

2.  <span data-ttu-id="1fab9-108">WPF アプリケーション プロジェクトにイメージ ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="1fab9-108">Add the image file to the WPF Application project.</span></span>

3.  <span data-ttu-id="1fab9-109">**ソリューション エクスプ ローラー**イメージを選択します。</span><span class="sxs-lookup"><span data-stu-id="1fab9-109">In **Solution Explorer**, select the image.</span></span>

4.  <span data-ttu-id="1fab9-110">[プロパティ] ウィンドウで、ドロップダウン矢印をクリックします。、**ビルド アクション**プロパティ。</span><span class="sxs-lookup"><span data-stu-id="1fab9-110">In the Properties window, click the drop-down arrow for the **Build Action** property.</span></span>

5.  <span data-ttu-id="1fab9-111">選択**SplashScreen**ドロップダウン リストから。</span><span class="sxs-lookup"><span data-stu-id="1fab9-111">Select **SplashScreen** from the drop-down list.</span></span>

6.  <span data-ttu-id="1fab9-112">**F5** キーを押してアプリケーションをビルドし、実行します。</span><span class="sxs-lookup"><span data-stu-id="1fab9-112">Press **F5** to build and run the application.</span></span>

     <span data-ttu-id="1fab9-113">スプラッシュ スクリーンのイメージは、画面の中央に表示され、メイン アプリケーション ウィンドウが表示されたらをフェードアウトします。</span><span class="sxs-lookup"><span data-stu-id="1fab9-113">The splash screen image appears in the center of the screen, and then fades when the main application window appears.</span></span>

## <a name="to-exclude-the-splash-screen-from-build"></a><span data-ttu-id="1fab9-114">スプラッシュ スクリーンをビルドから除外するには</span><span class="sxs-lookup"><span data-stu-id="1fab9-114">To exclude the splash screen from build</span></span>

1.  <span data-ttu-id="1fab9-115">**ソリューション エクスプ ローラー**、スプラッシュ スクリーン イメージを選択します。</span><span class="sxs-lookup"><span data-stu-id="1fab9-115">In **Solution Explorer**, select the splash screen image.</span></span>

2.  <span data-ttu-id="1fab9-116">**プロパティ**ウィンドウで、設定、**ビルド アクション**に**None**します。</span><span class="sxs-lookup"><span data-stu-id="1fab9-116">In the **Properties** window, set the **Build Action** to **None**.</span></span>

## <a name="to-remove-the-splash-screen-from-an-application"></a><span data-ttu-id="1fab9-117">スプラッシュ スクリーンをアプリケーションから削除するには</span><span class="sxs-lookup"><span data-stu-id="1fab9-117">To remove the splash screen from an application</span></span>

<span data-ttu-id="1fab9-118">**ソリューション エクスプ ローラー**、スプラッシュ スクリーン イメージを削除します。</span><span class="sxs-lookup"><span data-stu-id="1fab9-118">In **Solution Explorer**, delete the splash screen image.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fab9-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="1fab9-119">See Also</span></span>

- <xref:System.Windows.SplashScreen>
- <span data-ttu-id="1fab9-120">[方法: 既存の項目をプロジェクトに追加します。](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1fab9-120">[How to: Add Existing Items to a Project](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100))</span></span>
