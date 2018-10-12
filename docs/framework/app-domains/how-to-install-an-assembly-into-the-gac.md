---
title: アセンブリを GAC にインストールする
ms.date: 09/20/2018
helpviewer_keywords:
- assemblies [.NET Framework], global assembly cache
- Gacutil.exe
- strong-named assemblies, global assembly cache
- global assembly cache, installing assemblies
- Global Assembly Cache tool
- windows installer, global assembly cache
ms.assetid: a7e6f091-d02c-49ba-b736-7295cb0eb743
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d365ac77fe6cd7fc4fca36705729ec12b06d6830
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2018
ms.locfileid: "46584582"
---
# <a name="how-to-install-an-assembly-into-the-global-assembly-cache"></a><span data-ttu-id="27835-102">方法: アセンブリをグローバル アセンブリ キャッシュにインストールする</span><span class="sxs-lookup"><span data-stu-id="27835-102">How to: Install an assembly into the global assembly cache</span></span>

<span data-ttu-id="27835-103">厳密な名前付きのアセンブリをグローバル アセンブリ キャッシュ (GAC) にインストールには、次の 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="27835-103">There are two ways to install a strong-named assembly into the global assembly cache (GAC).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27835-104">GAC にインストールできるのは、厳密な名前付きのアセンブリだけです。</span><span class="sxs-lookup"><span data-stu-id="27835-104">Only strong-named assemblies can be installed into the GAC.</span></span> <span data-ttu-id="27835-105">厳密な名前付きのアセンブリを作成する方法については、「[方法: 厳密な名前でアセンブリに署名する](how-to-sign-an-assembly-with-a-strong-name.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="27835-105">For information about how to create a strong-named assembly, see [How to: Sign an Assembly with a Strong Name](how-to-sign-an-assembly-with-a-strong-name.md).</span></span>

## <a name="windows-installer"></a><span data-ttu-id="27835-106">Windows インストーラー</span><span class="sxs-lookup"><span data-stu-id="27835-106">Windows Installer</span></span>

<span data-ttu-id="27835-107">アセンブリをグローバル アセンブリ キャッシュに追加するための推奨する方法は、[Windows インストーラー](/windows/desktop/Msi/installation-of-assemblies-to-the-global-assembly-cache)(Windows インストール エンジン) です。</span><span class="sxs-lookup"><span data-stu-id="27835-107">[Windows Installer](/windows/desktop/Msi/installation-of-assemblies-to-the-global-assembly-cache), the Windows installation engine, is the recommended way to add assemblies to the global assembly cache.</span></span> <span data-ttu-id="27835-108">Windows インストーラーを使用すると、グローバル アセンブリ キャッシュ内のアセンブリの参照カウントが示されるなどの利点があります。</span><span class="sxs-lookup"><span data-stu-id="27835-108">Windows Installer provides reference counting of assemblies in the global assembly cache and other benefits.</span></span> <span data-ttu-id="27835-109">[ Visual Studio 2017 用 WiX Toolset 拡張機能](https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension)を使用して、Windows インストーラーのインストーラー パッケージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="27835-109">You can use the [WiX Toolset extension for Visual Studio 2017](https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension) to create an installer package for Windows Installer.</span></span>

## <a name="global-assembly-cache-tool"></a><span data-ttu-id="27835-110">グローバル アセンブリ キャッシュ ツール</span><span class="sxs-lookup"><span data-stu-id="27835-110">Global assembly cache tool</span></span>

<span data-ttu-id="27835-111">グローバル アセンブリ キャッシュ ツール [(gacutil.exe)](../tools/gacutil-exe-gac-tool.md) を使用して、厳密な名前付きアセンブリをグローバル アセンブリ キャッシュに追加したり、グローバル アセンブリ キャッシュの内容を表示したりできます。</span><span class="sxs-lookup"><span data-stu-id="27835-111">You can use the [Global assembly cache tool (gacutil.exe)](../tools/gacutil-exe-gac-tool.md) to add strong-named assemblies to the global assembly cache and to view the contents of the global assembly cache.</span></span>

   > [!NOTE]
   > <span data-ttu-id="27835-112">Gacutil.exe は開発専用です。製品アセンブリをグローバル アセンブリ キャッシュにインストールするためには使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="27835-112">Gacutil.exe is only for development purposes and should not be used to install production assemblies into the global assembly cache.</span></span>

<span data-ttu-id="27835-113">gacutil の構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="27835-113">The syntax for gacutil is as follows:</span></span>

```shell
gacutil -i <assembly name>
```

<span data-ttu-id="27835-114">このコマンドで、*assembly name* はグローバル アセンブリ キャッシュにインストールされるアセンブリの名前です。</span><span class="sxs-lookup"><span data-stu-id="27835-114">In this command, *assembly name* is the name of the assembly to install in the global assembly cache.</span></span>

<span data-ttu-id="27835-115">ファイル名 `hello.dll` のアセンブリをグローバル アセンブリ キャッシュにインストールする例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="27835-115">The following example installs an assembly with the file name `hello.dll` into the global assembly cache.</span></span>

```shell
gacutil -i hello.dll
```

> [!NOTE]
> <span data-ttu-id="27835-116">以前のバージョンの .NET Framework では、Windows のシェル拡張機能である Shfusion.dll により、**エクスプローラー**でアセンブリをドラッグしてインストールすることができました。</span><span class="sxs-lookup"><span data-stu-id="27835-116">In earlier versions of the .NET Framework, the Shfusion.dll Windows shell extension enabled you to install assemblies by dragging them in **File Explorer**.</span></span> <span data-ttu-id="27835-117">.NET Framework 4 以降、Shfusion.dll は廃止されましたが、互換性のために残されています。</span><span class="sxs-lookup"><span data-stu-id="27835-117">Beginning with the .NET Framework 4, Shfusion.dll is obsolete.</span></span>

## <a name="see-also"></a><span data-ttu-id="27835-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="27835-118">See also</span></span>

- [<span data-ttu-id="27835-119">アセンブリとグローバル アセンブリ キャッシュの使用</span><span class="sxs-lookup"><span data-stu-id="27835-119">Working with Assemblies and the Global Assembly Cache</span></span>](working-with-assemblies-and-the-gac.md)
- [<span data-ttu-id="27835-120">方法: グローバル アセンブリ キャッシュからアセンブリを削除する</span><span class="sxs-lookup"><span data-stu-id="27835-120">How to: Remove an Assembly from the Global Assembly Cache</span></span>](how-to-remove-an-assembly-from-the-gac.md)
- [<span data-ttu-id="27835-121">Gacutil.exe (グローバル アセンブリ キャッシュ ツール)</span><span class="sxs-lookup"><span data-stu-id="27835-121">Gacutil.exe (Global Assembly Cache Tool)</span></span>](../tools/gacutil-exe-gac-tool.md)
- [<span data-ttu-id="27835-122">方法: 厳密な名前でアセンブリに署名する</span><span class="sxs-lookup"><span data-stu-id="27835-122">How to: Sign an Assembly with a Strong Name</span></span>](how-to-sign-an-assembly-with-a-strong-name.md)