---
title: SourceLink と .NET ライブラリ
description: SourceLink を使用して .NET ライブラリのデバッグ機能を改善するためのベスト プラクティス推奨事項。
author: jamesnk
ms.author: mairaw
ms.date: 01/15/2019
ms.openlocfilehash: be97f868e2fcfc6c45e4bbac45b033f8914f4d99
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333539"
---
# <a name="sourcelink"></a><span data-ttu-id="d2f30-103">SourceLink</span><span class="sxs-lookup"><span data-stu-id="d2f30-103">SourceLink</span></span>

<span data-ttu-id="d2f30-104">SourceLink は NuGet からの .NET アセンブリのソース コードを開発者がデバッグすることを可能にするテクノロジです。</span><span class="sxs-lookup"><span data-stu-id="d2f30-104">SourceLink is a technology that enables source code debugging of .NET assemblies from NuGet by developers.</span></span> <span data-ttu-id="d2f30-105">SourceLink は NuGet パッケージの作成時に実行され、ソース コントロール メタデータをアセンブリとパッケージの内部に埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="d2f30-105">SourceLink executes when creating the NuGet package and embeds source control metadata inside assemblies and the package.</span></span> <span data-ttu-id="d2f30-106">パッケージをダウンロードし、Visual Studio で SourceLink を有効にした開発者は、そのソース コードにステップ インできます。</span><span class="sxs-lookup"><span data-stu-id="d2f30-106">Developers who download the package and have SourceLink enabled in Visual Studio can step into its source code.</span></span> <span data-ttu-id="d2f30-107">SourceLink からは、効率的なデバッグを可能にするソース コントロール メタデータが提供されます。</span><span class="sxs-lookup"><span data-stu-id="d2f30-107">SourceLink provides source control metadata to create a great debugging experience.</span></span>

## <a name="sourcelink-demo"></a><span data-ttu-id="d2f30-108">SourceLink デモ</span><span class="sxs-lookup"><span data-stu-id="d2f30-108">SourceLink demo</span></span>

> [!VIDEO https://www.youtube.com/embed/gyRGhCQPkB4?start=61]

## <a name="using-sourcelink"></a><span data-ttu-id="d2f30-109">SourceLink の使用</span><span class="sxs-lookup"><span data-stu-id="d2f30-109">Using SourceLink</span></span>

<span data-ttu-id="d2f30-110">SourceLink の使用方法は、[dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) GitHub リポジトリにあります。</span><span class="sxs-lookup"><span data-stu-id="d2f30-110">Instructions for using SourceLink can be found on the [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) GitHub repository.</span></span>

<span data-ttu-id="d2f30-111">[NuGet パッケージ エクスプローラー](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer)を使用すれば、SourceLink メタデータがパッケージに正常に埋め込まれたことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="d2f30-111">You can use [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) to confirm that the SourceLink metadata has been successfully embedded in the package.</span></span> <span data-ttu-id="d2f30-112">`Repository` メタデータがコメント ID と共に存在すること、各ターゲットの .dll と共に .pdb ファイルが見つかることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d2f30-112">Check the `Repository` metadata is present with a comment identifier and that .pdb files are located with each target's .dll.</span></span>

<span data-ttu-id="d2f30-113">![NuGet パッケージ エクスプローラーの SourceLink](./media/sourcelink/nuget-package-explorer-sourcelink.png "NuGet パッケージ エクスプローラーの SourceLink")</span><span class="sxs-lookup"><span data-stu-id="d2f30-113">![SourceLink in NuGet Package Explorer](./media/sourcelink/nuget-package-explorer-sourcelink.png "SourceLink in NuGet Package Explorer")</span></span>

<span data-ttu-id="d2f30-114">**✔️ 検討** SourceLink を使用して、お使いのアセンブリと NuGet パッケージにソース管理のメタデータを追加する。</span><span class="sxs-lookup"><span data-stu-id="d2f30-114">**✔️ CONSIDER** using SourceLink to add source control metadata to your assemblies and NuGet packages.</span></span>

> [!TIP]
> <span data-ttu-id="d2f30-115">デバッガー属性を型に追加することで開発者のデバッグ機能をさらに強化できます。</span><span class="sxs-lookup"><span data-stu-id="d2f30-115">You can further enhance a developer's debugging experience by adding debugger attributes to your types.</span></span>
> * <span data-ttu-id="d2f30-116"><xref:System.Diagnostics.DebuggerDisplayAttribute> では、デバッガーの変数ウィンドウでクラスやフィールドを表示する方法をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="d2f30-116"><xref:System.Diagnostics.DebuggerDisplayAttribute> can customize how a class or field is displayed in the debugger variable windows.</span></span>
> * <span data-ttu-id="d2f30-117"><xref:System.Diagnostics.DebuggerStepThroughAttribute> では、デバッガーに対してコードのステップ インではなくステップ実行が指示されます。</span><span class="sxs-lookup"><span data-stu-id="d2f30-117"><xref:System.Diagnostics.DebuggerStepThroughAttribute> instructs the debugger to step through the code instead of stepping into the code.</span></span>
> * <span data-ttu-id="d2f30-118"><xref:System.Diagnostics.DebuggerBrowsableAttribute> では、デバッガー変数ウィンドウにメンバーを表示するかどうかが制御されます。</span><span class="sxs-lookup"><span data-stu-id="d2f30-118"><xref:System.Diagnostics.DebuggerBrowsableAttribute> controls whether a member is displayed in the debugger variable windows.</span></span>

<span data-ttu-id="d2f30-119">**✔️ 検討** シンボル ファイルを発行する (`*.pdb`)。</span><span class="sxs-lookup"><span data-stu-id="d2f30-119">**✔️ CONSIDER** publishing symbol files (`*.pdb`).</span></span>

> <span data-ttu-id="d2f30-120">シンボル ファイルとシンボル パッケージの詳細については、「[シンボル パッケージ](./nuget.md#symbol-packages)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2f30-120">For more information about symbol files and symbol packages, see [Symbol packages](./nuget.md#symbol-packages).</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="d2f30-121">[前へ](dependencies.md)
>[次へ](publish-nuget-package.md)</span><span class="sxs-lookup"><span data-stu-id="d2f30-121">[Previous](dependencies.md)
[Next](publish-nuget-package.md)</span></span>
