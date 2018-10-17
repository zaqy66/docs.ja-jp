---
title: SourceLink および .NET ライブラリ
description: SourceLink を使用して .NET ライブラリのデバッグを改善するための推奨されるベスト プラクティスです。
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: fa4af47eaa5dd1510640c2bf0ebb2187b56efae0
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2018
ms.locfileid: "49370315"
---
# <a name="sourcelink"></a><span data-ttu-id="4c6ec-103">SourceLink</span><span class="sxs-lookup"><span data-stu-id="4c6ec-103">SourceLink</span></span>

<span data-ttu-id="4c6ec-104">SourceLink は、開発者が NuGet から .NET アセンブリのソース コードのデバッグを有効にするテクノロジです。</span><span class="sxs-lookup"><span data-stu-id="4c6ec-104">SourceLink is a technology that enables source code debugging of .NET assemblies from NuGet by developers.</span></span> <span data-ttu-id="4c6ec-105">SourceLink は NuGet パッケージを作成するときに実行し、アセンブリとパッケージ内のソース コントロールのメタデータを埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="4c6ec-105">SourceLink executes when creating the NuGet package and embeds source control metadata inside assemblies and the package.</span></span> <span data-ttu-id="4c6ec-106">パッケージをダウンロードし、Visual Studio で有効になっている SourceLink がある開発者は、そのソース コードにステップ インできます。</span><span class="sxs-lookup"><span data-stu-id="4c6ec-106">Developers who download the package and have SourceLink enabled in Visual Studio can step into its source code.</span></span> <span data-ttu-id="4c6ec-107">SourceLink では、優れたデバッグ エクスペリエンスを作成するソース コントロールのメタデータを提供します。</span><span class="sxs-lookup"><span data-stu-id="4c6ec-107">SourceLink provides source control metadata to create a great debugging experience.</span></span>

## <a name="sourcelink-demo"></a><span data-ttu-id="4c6ec-108">SourceLink デモ</span><span class="sxs-lookup"><span data-stu-id="4c6ec-108">SourceLink demo</span></span>

> [!VIDEO https://www.youtube.com/embed/gyRGhCQPkB4?start=61]

## <a name="using-sourcelink"></a><span data-ttu-id="4c6ec-109">SourceLink を使用します。</span><span class="sxs-lookup"><span data-stu-id="4c6ec-109">Using SourceLink</span></span>

<span data-ttu-id="4c6ec-110">SourceLink を使用するための手順で確認できます、 [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) GitHub リポジトリ。</span><span class="sxs-lookup"><span data-stu-id="4c6ec-110">Instructions for using SourceLink can be found on the [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) GitHub repository.</span></span>

<span data-ttu-id="4c6ec-111">使用することができます[NuGet パッケージ エクスプ ローラー](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) SourceLink メタデータがパッケージに正常に埋め込まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4c6ec-111">You can use [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) to confirm that the SourceLink metadata has been successfully embedded in the package.</span></span> <span data-ttu-id="4c6ec-112">チェック、`Repository`メタデータがコメントの識別子を持つ存在し、各ターゲットの .dll で .pdb ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="4c6ec-112">Check the `Repository` metadata is present with a comment identifier and that .pdb files are located with each target's .dll.</span></span>

<span data-ttu-id="4c6ec-113">![NuGet パッケージ エクスプ ローラーで SourceLink](./media/sourcelink/nuget-package-explorer-sourcelink.png "NuGet パッケージ エクスプ ローラーで SourceLink")</span><span class="sxs-lookup"><span data-stu-id="4c6ec-113">![SourceLink in NuGet Package Explorer](./media/sourcelink/nuget-package-explorer-sourcelink.png "SourceLink in NuGet Package Explorer")</span></span>

<span data-ttu-id="4c6ec-114">**✔️ をご検討ください**SourceLink を使用して、アセンブリと NuGet パッケージをソース コントロールのメタデータを追加します。</span><span class="sxs-lookup"><span data-stu-id="4c6ec-114">**✔️ CONSIDER** using SourceLink to add source control metadata to your assemblies and NuGet package.</span></span>

<span data-ttu-id="4c6ec-115">**✔️ をご検討ください**NuGet パッケージに PDB ファイルを含めます。</span><span class="sxs-lookup"><span data-stu-id="4c6ec-115">**✔️ CONSIDER** including PDB files in the NuGet package.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="4c6ec-116">[前へ](./dependencies.md)
[次へ](./publish-nuget-package.md)</span><span class="sxs-lookup"><span data-stu-id="4c6ec-116">[Previous](./dependencies.md)
[Next](./publish-nuget-package.md)</span></span>
