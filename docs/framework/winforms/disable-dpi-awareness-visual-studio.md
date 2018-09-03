---
title: Visual Studio では、DPI の認識を無効にします。
description: HDPI モニターは、Windows フォーム デザイナーと DPI に対応していないプロセスとして Visual Studio を実行する方法の制限事項について説明します。
ms.date: 08/14/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-designers
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 65c997e12aa033b3b08d32c8ab76372e3c52a803
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2018
ms.locfileid: "43467108"
---
# <a name="disable-dpi-awareness-in-visual-studio"></a><span data-ttu-id="016af-103">Visual Studio では、DPI の認識を無効にします。</span><span class="sxs-lookup"><span data-stu-id="016af-103">Disable DPI-awareness in Visual Studio</span></span>

<span data-ttu-id="016af-104">Visual Studio では、表示スケールを自動的に意味インチ (DPI) 対応アプリケーションあたりのドットです。</span><span class="sxs-lookup"><span data-stu-id="016af-104">Visual Studio is a dots per inch (DPI) aware application, which means the display scales automatically.</span></span> <span data-ttu-id="016af-105">アプリケーションでは、DPI 対応ではないことを示す、オペレーティング システムは、ビットマップとしてアプリケーションをスケーリングします。</span><span class="sxs-lookup"><span data-stu-id="016af-105">If an application states that it's not DPI-aware, the operating system scales the application as a bitmap.</span></span> <span data-ttu-id="016af-106">この動作は、DPI の仮想化とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="016af-106">This behavior is also called DPI virtualization.</span></span> <span data-ttu-id="016af-107">アプリケーションは引き続き、100% に拡大縮小、または 96 dpi で実行されていると認識します。</span><span class="sxs-lookup"><span data-stu-id="016af-107">The application still thinks that it's running at 100% scaling, or 96 dpi.</span></span>

## <a name="windows-forms-designer-on-hdpi-monitors"></a><span data-ttu-id="016af-108">HDPI のモニターでの Windows フォーム デザイナー</span><span class="sxs-lookup"><span data-stu-id="016af-108">Windows Forms Designer on HDPI monitors</span></span>

<span data-ttu-id="016af-109">**Windows フォーム デザイナー** Visual Studio ではありませんスケーリングをサポートします。</span><span class="sxs-lookup"><span data-stu-id="016af-109">The **Windows Forms Designer** in Visual Studio doesn't have scaling support.</span></span> <span data-ttu-id="016af-110">表示の問題は、一部のフォームを開いたときにこれにより、 **Windows フォーム デザイナー** high dots per インチ (HDPI) モニターです。</span><span class="sxs-lookup"><span data-stu-id="016af-110">This causes display issues when you open some forms in the **Windows Forms Designer** on high dots per inch (HDPI) monitors.</span></span> <span data-ttu-id="016af-111">例については、コントロールは、次の図のように重複する表示できます。</span><span class="sxs-lookup"><span data-stu-id="016af-111">For examples, controls can appear to overlap as shown in the following image:</span></span>

![HDPI のモニターでの Windows フォーム デザイナー](media/disable-dpi-awareness-visual-studio/win-forms-designer-hdpi.png)

<span data-ttu-id="016af-113">Visual Studio 2017 15.8 でフォームを開くと、以降のバージョンで、 **Windows フォーム デザイナー** HDPI モニターで、Visual Studio は、デザイナーの上部にある黄色のバーの情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="016af-113">In Visual Studio 2017 version 15.8 and later, when you open a form in the **Windows Forms Designer** on an HDPI monitor, Visual Studio displays a yellow informational bar at the top of the designer:</span></span>

![DPI に対応していないモードで再起動する Visual Studio での情報バー](media/disable-dpi-awareness-visual-studio/scaling-gold-bar.png)

<span data-ttu-id="016af-115">メッセージを読み取り**メイン ディスプレイのスケーリングを 200% (192 dpi) に設定します。デザイナー ウィンドウのレンダリングの問題があります。**</span><span class="sxs-lookup"><span data-stu-id="016af-115">The message reads **Scaling on your main display is set to 200% (192 dpi). This might cause rendering problems in the designer window.**</span></span>

<span data-ttu-id="016af-116">場合は、デザイナーを使用していないし、フォームのレイアウトを調整する必要はありません、情報バーを無視し、コード エディターまたはデザイナーの他の種類では、作業を続行できます。</span><span class="sxs-lookup"><span data-stu-id="016af-116">If you aren't working in the designer and don't need to adjust the layout of your form, you can ignore the informational bar and continue working in the code editor or in other types of designers.</span></span> <span data-ttu-id="016af-117">のみ、 **Windows フォーム デザイナー**が影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="016af-117">Only the **Windows Forms Designer** is affected.</span></span> <span data-ttu-id="016af-118">作業する必要がある場合、 **Windows フォーム デザイナー**、次のセクションでは[、問題を解決する](#to-resolve-the-problem)します。</span><span class="sxs-lookup"><span data-stu-id="016af-118">If you do need to work in the **Windows Forms Designer**, the next section helps you [resolve the problem](#to-resolve-the-problem).</span></span>

## <a name="to-resolve-the-problem"></a><span data-ttu-id="016af-119">この問題を解決するのには</span><span class="sxs-lookup"><span data-stu-id="016af-119">To resolve the problem</span></span>

<span data-ttu-id="016af-120">表示に関する問題を解決するのには次の 3 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="016af-120">There are three options to resolve the display problem.</span></span>

### <a name="restart-visual-studio-as-a-dpi-unaware-process"></a><span data-ttu-id="016af-121">DPI に対応していないプロセスとして Visual Studio を再起動します。</span><span class="sxs-lookup"><span data-stu-id="016af-121">Restart Visual Studio as a DPI-unaware process</span></span>

<span data-ttu-id="016af-122">DPI に対応していないプロセスとして Visual Studio を再起動するには、黄色の情報バーのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="016af-122">You can restart Visual Studio as a DPI-unaware process by selecting the option on the yellow informational bar.</span></span> <span data-ttu-id="016af-123">これは、問題を解決することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="016af-123">This is the preferred way of resolving the problem.</span></span>

<span data-ttu-id="016af-124">Visual Studio を DPI に対応していないプロセスとして実行すると、デザイナーのレイアウトの問題を解決するが、フォントがぼやけて表示される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="016af-124">When Visual Studio runs as a DPI-unaware process, the designer layout issues are resolved, but fonts may appear blurry.</span></span> <span data-ttu-id="016af-125">Visual Studio は、ことを示す DPI に対応していないプロセスとして実行した場合に、別の黄色の情報メッセージを表示します**Visual Studio の DPI に対応していないプロセスとして実行します。WPF および XAML デザイナーが正しく表示されない場合があります。**</span><span class="sxs-lookup"><span data-stu-id="016af-125">Visual Studio displays a different yellow informational message when it runs as a DPI-unaware process that says **Visual Studio is running as a DPI-unaware process. WPF and XAML designers might not display correctly.**</span></span> <span data-ttu-id="016af-126">情報バーは、するためのオプションも用意されています。 **DPI 対応のプロセスとして Visual Studio を再起動**します。</span><span class="sxs-lookup"><span data-stu-id="016af-126">The informational bar also provides an option to **Restart Visual Studio as a DPI-aware process**.</span></span>

> [!NOTE]
> - <span data-ttu-id="016af-127">DPI に対応していないプロセスとして再起動するオプションを選択したときに、Visual Studio でツール ウィンドウをドッキング解除が、これらのツール ウィンドウの位置は変更可能性があります。</span><span class="sxs-lookup"><span data-stu-id="016af-127">If you had undocked tool windows in Visual Studio when you selected the option to restart as a DPI-unaware process, the position of those tool windows may change.</span></span>
> - <span data-ttu-id="016af-128">既定の Visual Basic のプロファイルを使用する場合、またはがある場合、**作成時に新しいプロジェクトを保存**でオプションを選択解除**ツール** > **オプション** > **プロジェクトおよびソリューション**DPI に対応していないプロセスとして再起動するとき、Visual Studio がプロジェクトを再び開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="016af-128">If you use the default Visual Basic profile, or if you have the **Save new projects when created** option deselected in **Tools** > **Options** > **Projects and Solutions**, Visual Studio cannot reopen your project when it restarts as a DPI-unaware process.</span></span> <span data-ttu-id="016af-129">ただし、それを選択してプロジェクトを開く**ファイル** > **最近使ったプロジェクトおよびソリューション**します。</span><span class="sxs-lookup"><span data-stu-id="016af-129">However, you can open the project by selecting it under **File** > **Recent Projects and Solutions**.</span></span>

<span data-ttu-id="016af-130">作業が完了したら、DPI 対応のプロセスとして Visual Studio を再起動することが重要、 **Windows フォーム デザイナー**します。</span><span class="sxs-lookup"><span data-stu-id="016af-130">It's important to restart Visual Studio as a DPI-aware process when you're finished working in the **Windows Forms Designer**.</span></span> <span data-ttu-id="016af-131">DPI に対応していないプロセスとして実行されているフォントがぼやけてし、など他のデザイナーでの問題が発生する可能性があります、 **XAML デザイナー**します。</span><span class="sxs-lookup"><span data-stu-id="016af-131">When it's running as a DPI-unaware process, fonts can look blurry and you may see issues in other designers such as the **XAML Designer**.</span></span> <span data-ttu-id="016af-132">DPI に対応していないモードで実行されている Visual Studio を再度開くを起動する場合が DPI 対応もう一度です。</span><span class="sxs-lookup"><span data-stu-id="016af-132">If you close and reopen Visual Studio when it's running in DPI-unaware mode, it becomes DPI-aware again.</span></span> <span data-ttu-id="016af-133">クリックすることも、 **DPI 対応のプロセスとして Visual Studio を再起動**の情報バーのオプション。</span><span class="sxs-lookup"><span data-stu-id="016af-133">You can also click the **Restart Visual Studio as a DPI-aware process** option in the informational bar.</span></span>

### <a name="add-a-registry-entry"></a><span data-ttu-id="016af-134">レジストリ エントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="016af-134">Add a registry entry</span></span>

<span data-ttu-id="016af-135">Visual Studio は、レジストリを変更して DPI 対応としてマークできます。</span><span class="sxs-lookup"><span data-stu-id="016af-135">You can mark Visual Studio as DPI-unaware by modifying the registry.</span></span> <span data-ttu-id="016af-136">開いている**レジストリ エディター**にエントリを追加し、 **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows NT\CurrentVersion\AppCompatFlags\Layers**サブキー。</span><span class="sxs-lookup"><span data-stu-id="016af-136">Open **Registry Editor** and add an entry to the **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows NT\CurrentVersion\AppCompatFlags\Layers** subkey:</span></span>

<span data-ttu-id="016af-137">**エントリ**: % %programfiles (x86) %\Microsoft Visual Studio\2017\your-edition\Common7\IDE\devenv.exe</span><span class="sxs-lookup"><span data-stu-id="016af-137">**Entry**: %ProgramFiles(x86)%\Microsoft Visual Studio\2017\your-edition\Common7\IDE\devenv.exe</span></span>

<span data-ttu-id="016af-138">**型**: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="016af-138">**Type**: REG_SZ</span></span>

<span data-ttu-id="016af-139">**値**: DPIUNAWARE</span><span class="sxs-lookup"><span data-stu-id="016af-139">**Value**: DPIUNAWARE</span></span>

> [!NOTE]
> <span data-ttu-id="016af-140">Visual Studio は、レジストリ エントリを削除するまでに、DPI に対応していないモードでは残ります。</span><span class="sxs-lookup"><span data-stu-id="016af-140">Visual Studio remains in DPI-unaware mode until you remove the registry entry.</span></span>

### <a name="set-your-display-scaling-setting-to-100"></a><span data-ttu-id="016af-141">設定、画面のスケーリングを 100% に設定します。</span><span class="sxs-lookup"><span data-stu-id="016af-141">Set your display scaling setting to 100%</span></span>

<span data-ttu-id="016af-142">100% に設定を Windows 10 にスケールイン ディスプレイを設定する入力**表示設定**タスク バー、クリックして [検索] ボックスに**表示設定を変更**します。</span><span class="sxs-lookup"><span data-stu-id="016af-142">To set your display scaling setting to 100% in Windows 10, type **display settings** in the task bar search box, and then select **Change display settings**.</span></span> <span data-ttu-id="016af-143">**設定**ウィンドウで、設定**テキスト、アプリ、およびその他のアイテムのサイズを変更**に**100%** します。</span><span class="sxs-lookup"><span data-stu-id="016af-143">In the **Settings** window, set **Change the size of text, apps, and other items** to **100%**.</span></span>

<span data-ttu-id="016af-144">100% に拡大縮小、表示を設定できない可能性があります、ため、使用するのには小さすぎてユーザー インターフェイスをことができます。</span><span class="sxs-lookup"><span data-stu-id="016af-144">Setting your display scaling to 100% may be undesirable, because it can make the user interface too small to be usable.</span></span>

## <a name="see-also"></a><span data-ttu-id="016af-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="016af-145">See also</span></span>

- [<span data-ttu-id="016af-146">Windows フォームにおける自動スケーリング</span><span class="sxs-lookup"><span data-stu-id="016af-146">Automatic scaling in Windows Forms</span></span>](automatic-scaling-in-windows-forms.md)