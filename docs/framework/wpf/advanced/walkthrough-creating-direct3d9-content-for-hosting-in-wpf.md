---
title: チュートリアル:WPF でホストするための Direct3D9 コンテンツの作成
ms.date: 03/30/2017
dev_langs:
- cpp
helpviewer_keywords:
- WPF [WPF], creating Direct3D9 content
- Direct3D9 [WPF interoperability], creating Direct3D9 content
ms.assetid: 286e98bc-1eaa-4b5e-923d-3490a9cca5fc
ms.openlocfilehash: 192036836dfb010274944006feea44e5d81ff4e3
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53168753"
---
# <a name="walkthrough-creating-direct3d9-content-for-hosting-in-wpf"></a><span data-ttu-id="aa6a7-102">チュートリアル:WPF でホストするための Direct3D9 コンテンツの作成</span><span class="sxs-lookup"><span data-stu-id="aa6a7-102">Walkthrough: Creating Direct3D9 Content for Hosting in WPF</span></span>
<span data-ttu-id="aa6a7-103">このチュートリアルでは、Windows Presentation Foundation (WPF) アプリケーションでホストするための適切な Direct3D9 コンテンツを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-103">This walkthrough shows how to create Direct3D9 content that is suitable for hosting in a Windows Presentation Foundation (WPF) application.</span></span> <span data-ttu-id="aa6a7-104">WPF アプリケーションでの Direct3D9 コンテンツのホストの詳細については、次を参照してください。 [WPF と Direct3D9 の相互運用性](../../../../docs/framework/wpf/advanced/wpf-and-direct3d9-interoperation.md)します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-104">For more information on hosting Direct3D9 content in WPF applications, see [WPF and Direct3D9 Interoperation](../../../../docs/framework/wpf/advanced/wpf-and-direct3d9-interoperation.md).</span></span>

 <span data-ttu-id="aa6a7-105">このチュートリアルでは次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-105">In this walkthrough, you perform the following tasks:</span></span>

-   <span data-ttu-id="aa6a7-106">Direct3D9 プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-106">Create a Direct3D9 project.</span></span>

-   <span data-ttu-id="aa6a7-107">WPF アプリケーションでホストするための Direct3D9 プロジェクトを構成します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-107">Configure the Direct3D9 project for hosting in a WPF application.</span></span>

 <span data-ttu-id="aa6a7-108">完了したら、WPF アプリケーションで使用するための Direct3D9 コンテンツを含む DLL 必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-108">When you are finished, you will have a DLL that contains Direct3D9 content for use in a WPF application.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="aa6a7-109">必須コンポーネント</span><span class="sxs-lookup"><span data-stu-id="aa6a7-109">Prerequisites</span></span>
 <span data-ttu-id="aa6a7-110">このチュートリアルを実行するには、次のコンポーネントが必要です。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-110">You need the following components to complete this walkthrough:</span></span>

-   <span data-ttu-id="aa6a7-111">Visual Studio 2010。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-111">Visual Studio 2010.</span></span>

-   <span data-ttu-id="aa6a7-112">DirectX 9 以降の SDK です。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-112">DirectX SDK 9 or later.</span></span>

## <a name="creating-the-direct3d9-project"></a><span data-ttu-id="aa6a7-113">Direct3D9 プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-113">Creating the Direct3D9 Project</span></span>
 <span data-ttu-id="aa6a7-114">最初の手順では、作成および Direct3D9 プロジェクトを構成します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-114">The first step is to create and configure the Direct3D9 project.</span></span>

#### <a name="to-create-the-direct3d9-project"></a><span data-ttu-id="aa6a7-115">Direct3D9 プロジェクトを作成するには</span><span class="sxs-lookup"><span data-stu-id="aa6a7-115">To create the Direct3D9 project</span></span>

1.  <span data-ttu-id="aa6a7-116">C++ という名前で新しい Win32 プロジェクトを作成`D3DContent`です。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-116">Create a new Win32 Project in C++ named `D3DContent`.</span></span>

     <span data-ttu-id="aa6a7-117">Win32 アプリケーション ウィザードが開き、ようこそ画面が表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-117">The Win32 Application Wizard opens and displays the Welcome screen.</span></span>

2.  <span data-ttu-id="aa6a7-118">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-118">Click **Next**.</span></span>

     <span data-ttu-id="aa6a7-119">[アプリケーション設定] 画面が表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-119">The Application Settings screen appears.</span></span>

3.  <span data-ttu-id="aa6a7-120">**アプリケーションの種類:** セクションで、 **DLL**オプション。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-120">In the **Application type:** section, select the **DLL** option.</span></span>

4.  <span data-ttu-id="aa6a7-121">**[完了]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-121">Click **Finish**.</span></span>

     <span data-ttu-id="aa6a7-122">D3DContent プロジェクトが生成されます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-122">The D3DContent project is generated.</span></span>

5.  <span data-ttu-id="aa6a7-123">ソリューション エクスプ ローラーでは、D3DContent プロジェクトを右クリックして**プロパティ**します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-123">In Solution Explorer, right-click the D3DContent project and select **Properties**.</span></span>

     <span data-ttu-id="aa6a7-124">**D3DContent プロパティ ページ** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-124">The **D3DContent Property Pages** dialog box opens.</span></span>

6.  <span data-ttu-id="aa6a7-125">選択、 **C/C++** ノード。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-125">Select the **C/C++** node.</span></span>

7.  <span data-ttu-id="aa6a7-126">**追加のインクルード ディレクトリ**フィールドに、DirectX の場所は、フォルダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-126">In the **Additional Include Directories** field, specify the location of the DirectX include folder.</span></span> <span data-ttu-id="aa6a7-127">このフォルダーの既定の場所は %ProgramFiles%\Microsoft DirectX SDK (*バージョン*) \Include します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-127">The default location for this folder is %ProgramFiles%\Microsoft DirectX SDK (*version*)\Include.</span></span>

8.  <span data-ttu-id="aa6a7-128">ダブルクリックして、**リンカー**ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-128">Double-click the **Linker** node to expand it.</span></span>

9. <span data-ttu-id="aa6a7-129">**追加のライブラリ ディレクトリ**フィールドに、DirectX のライブラリ フォルダーの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-129">In the **Additional Library Directories** field, specify the location of the DirectX libraries folder.</span></span> <span data-ttu-id="aa6a7-130">このフォルダーの既定の場所は %ProgramFiles%\Microsoft DirectX SDK (*バージョン*) \Lib\x86 します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-130">The default location for this folder is %ProgramFiles%\Microsoft DirectX SDK (*version*)\Lib\x86.</span></span>

10. <span data-ttu-id="aa6a7-131">選択、**入力**ノード。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-131">Select the **Input** node.</span></span>

11. <span data-ttu-id="aa6a7-132">**追加の依存関係**フィールドに、追加、`d3d9.lib`と`d3dx9.lib`ファイル。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-132">In the **Additional Dependencies** field, add the `d3d9.lib` and `d3dx9.lib` files.</span></span>

12. <span data-ttu-id="aa6a7-133">ソリューション エクスプ ローラーの追加という名前の新しいモジュール定義ファイル (.def)`D3DContent.def`をプロジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-133">In Solution Explorer, add a new module definition file (.def) named `D3DContent.def` to the project.</span></span>

## <a name="creating-the-direct3d9-content"></a><span data-ttu-id="aa6a7-134">Direct3D9 コンテンツを作成します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-134">Creating the Direct3D9 Content</span></span>
 <span data-ttu-id="aa6a7-135">最適なパフォーマンスを得るには、Direct3D9 コンテンツは特定の設定を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-135">To get the best performance, your Direct3D9 content must use particular settings.</span></span> <span data-ttu-id="aa6a7-136">次のコードでは、最適なパフォーマンス特性を持つ Direct3D9 サーフェスを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-136">The following code shows how to create a Direct3D9 surface that has the best performance characteristics.</span></span> <span data-ttu-id="aa6a7-137">詳細については、次を参照してください。 [Direct3D9 および WPF の相互運用性のパフォーマンスに関する考慮事項](../../../../docs/framework/wpf/advanced/performance-considerations-for-direct3d9-and-wpf-interoperability.md)します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-137">For more information, see [Performance Considerations for Direct3D9 and WPF Interoperability](../../../../docs/framework/wpf/advanced/performance-considerations-for-direct3d9-and-wpf-interoperability.md).</span></span>

#### <a name="to-create-the-direct3d9-content"></a><span data-ttu-id="aa6a7-138">Direct3D9 コンテンツを作成するには</span><span class="sxs-lookup"><span data-stu-id="aa6a7-138">To create the Direct3D9 content</span></span>

1.  <span data-ttu-id="aa6a7-139">ソリューション エクスプ ローラーを使用して、次の名前のプロジェクトに 3 つの C++ クラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-139">Using Solution Explorer, add three C++ classes to the project named the following.</span></span>

     <span data-ttu-id="aa6a7-140">`CRenderer` (で仮想デストラクター)</span><span class="sxs-lookup"><span data-stu-id="aa6a7-140">`CRenderer` (with virtual destructor)</span></span>

     `CRendererManager`

     `CTriangleRenderer`

2.  <span data-ttu-id="aa6a7-141">Renderer.h をコード エディターで開くし、自動的に生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-141">Open Renderer.h in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#RendererH](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderer.h#rendererh)]

3.  <span data-ttu-id="aa6a7-142">Renderer.cpp をコード エディターで開くし、自動的に生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-142">Open Renderer.cpp in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#RendererCPP](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderer.cpp#renderercpp)]

4.  <span data-ttu-id="aa6a7-143">RendererManager.h をコード エディターで開くし、自動的に生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-143">Open RendererManager.h in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#RendererManagerH](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderermanager.h#renderermanagerh)]

5.  <span data-ttu-id="aa6a7-144">RendererManager.cpp をコード エディターで開くし、自動的に生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-144">Open RendererManager.cpp in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#RendererManagerCPP](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderermanager.cpp#renderermanagercpp)]

6.  <span data-ttu-id="aa6a7-145">TriangleRenderer.h をコード エディターで開くし、自動的に生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-145">Open TriangleRenderer.h in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#TriangleRendererH](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/trianglerenderer.h#trianglerendererh)]

7.  <span data-ttu-id="aa6a7-146">TriangleRenderer.cpp をコード エディターで開くし、自動的に生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-146">Open TriangleRenderer.cpp in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#TriangleRendererCPP](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/trianglerenderer.cpp#trianglerenderercpp)]

8.  <span data-ttu-id="aa6a7-147">Stdafx.h をコード エディターで開くし、自動的に生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-147">Open stdafx.h in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#StdafxH](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/stdafx.h#stdafxh)]

9. <span data-ttu-id="aa6a7-148">Dllmain.cpp をコード エディターで開くし、自動的に生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-148">Open dllmain.cpp in the Code Editor and replace the automatically generated code with the following code.</span></span>

     [!code-cpp[System.Windows.Interop.D3DImage#DllMain](../../../../samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/dllmain.cpp#dllmain)]

10. <span data-ttu-id="aa6a7-149">D3DContent.def をコード エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-149">Open D3DContent.def in the code editor.</span></span>

11. <span data-ttu-id="aa6a7-150">自動的に生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-150">Replace the automatically generated code with the following code.</span></span>

    ```
    LIBRARY "D3DContent"

    EXPORTS

    SetSize
    SetAlpha
    SetNumDesiredSamples
    SetAdapter

    GetBackBufferNoRef
    Render
    Destroy
    ```

12. <span data-ttu-id="aa6a7-151">プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-151">Build the project.</span></span>

## <a name="next-steps"></a><span data-ttu-id="aa6a7-152">次の手順</span><span class="sxs-lookup"><span data-stu-id="aa6a7-152">Next Steps</span></span>

-   <span data-ttu-id="aa6a7-153">WPF アプリケーションでの Direct3D9 コンテンツをホストします。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-153">Host the Direct3D9 content in a WPF application.</span></span> <span data-ttu-id="aa6a7-154">詳細については、次を参照してください。[チュートリアル。WPF での Direct3D9 コンテンツをホストしている](../../../../docs/framework/wpf/advanced/walkthrough-hosting-direct3d9-content-in-wpf.md)します。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-154">For more information, see [Walkthrough: Hosting Direct3D9 Content in WPF](../../../../docs/framework/wpf/advanced/walkthrough-hosting-direct3d9-content-in-wpf.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="aa6a7-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa6a7-155">See Also</span></span>

- <xref:System.Windows.Interop.D3DImage>
- [<span data-ttu-id="aa6a7-156">Direct3D9 および WPF の相互運用性のパフォーマンスに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="aa6a7-156">Performance Considerations for Direct3D9 and WPF Interoperability</span></span>](../../../../docs/framework/wpf/advanced/performance-considerations-for-direct3d9-and-wpf-interoperability.md)
- [<span data-ttu-id="aa6a7-157">チュートリアル:WPF での Direct3D9 コンテンツをホストしています。</span><span class="sxs-lookup"><span data-stu-id="aa6a7-157">Walkthrough: Hosting Direct3D9 Content in WPF</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-direct3d9-content-in-wpf.md)
