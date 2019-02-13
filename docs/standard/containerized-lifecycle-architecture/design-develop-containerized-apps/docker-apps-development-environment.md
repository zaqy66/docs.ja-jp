---
title: Docker アプリの開発環境
description: Docker 開発のライフ サイクルをサポートする最も重要な開発ツールのオプションの確認を取得します。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 1d22b45a8eee9198d337df9f0b8b4b78371fa31a
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219998"
---
# <a name="development-environment-for-docker-apps"></a><span data-ttu-id="06b08-103">Docker アプリの開発環境</span><span class="sxs-lookup"><span data-stu-id="06b08-103">Development environment for Docker apps</span></span>

## <a name="development-tools-choices-ide-or-editor"></a><span data-ttu-id="06b08-104">開発ツールの選択:IDE またはエディター</span><span class="sxs-lookup"><span data-stu-id="06b08-104">Development tools choices: IDE or editor</span></span>

<span data-ttu-id="06b08-105">いたとしてもする場合、完全で強力な IDE または軽量でアジャイルなエディターでは、マイクロソフトは、Docker アプリケーションの開発なったときに対応しています。</span><span class="sxs-lookup"><span data-stu-id="06b08-105">No matter if you prefer a full and powerful IDE or a lightweight and agile editor, Microsoft has you covered when it comes to developing Docker applications.</span></span>

### <a name="visual-studio-code-and-docker-cli-cross-platform-tools-for-mac-linux-and-windows"></a><span data-ttu-id="06b08-106">Visual Studio Code と Docker CLI (Mac、Linux、および Windows 用のクロス プラットフォーム ツール)</span><span class="sxs-lookup"><span data-stu-id="06b08-106">Visual Studio Code and Docker CLI (cross-platform tools for Mac, Linux, and Windows)</span></span>

<span data-ttu-id="06b08-107">軽量でクロスプラット フォーム対応のエディターが任意の開発言語をサポートしている場合は、Visual Studio Code と Docker CLI を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="06b08-107">If you prefer a lightweight, cross-platform editor supporting any development language, you can use Visual Studio Code and Docker CLI.</span></span> <span data-ttu-id="06b08-108">これらの製品では、開発者のワークフローを合理化するための重要なは、簡単かつ堅牢のエクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="06b08-108">These products provide a simple yet robust experience, which is critical for streamlining the developer workflow.</span></span> <span data-ttu-id="06b08-109">"Docker for Mac"または"Docker for Windows"(開発環境) をインストールすると、Docker 開発者は、Windows または Linux (ランタイム環境) の両方のアプリを構築するのに 1 つの Docker CLI を使用できます。</span><span class="sxs-lookup"><span data-stu-id="06b08-109">By installing "Docker for Mac" or "Docker for Windows" (development environment), Docker developers can use a single Docker CLI to build apps for both Windows or Linux (runtime environment).</span></span> <span data-ttu-id="06b08-110">さらに、Visual Studio Code エディターから Docker コマンドを実行するには、Dockerfile とショートカット タスク用の IntelliSense での Docker の拡張機能をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="06b08-110">Plus, Visual Studio Code supports extensions for Docker with IntelliSense for Dockerfiles and shortcut-tasks to run Docker commands from the editor.</span></span>

> [!NOTE]
> <span data-ttu-id="06b08-111">Visual Studio Code をダウンロードするには<https://code.visualstudio.com/download>します。</span><span class="sxs-lookup"><span data-stu-id="06b08-111">To download Visual Studio Code, go to <https://code.visualstudio.com/download>.</span></span>

<span data-ttu-id="06b08-112">Mac および Windows 用 Docker をダウンロードするには<https://www.docker.com/products/docker>します。</span><span class="sxs-lookup"><span data-stu-id="06b08-112">To download Docker for Mac and Windows, go to <https://www.docker.com/products/docker>.</span></span>

### <a name="visual-studio-with-docker-tools"></a><span data-ttu-id="06b08-113">Visual Studio と Docker ツール</span><span class="sxs-lookup"><span data-stu-id="06b08-113">Visual Studio with Docker Tools</span></span>

<span data-ttu-id="06b08-114">Visual Studio 2015 を使用しているときに、「Visual Studio 用 Docker ツールです」アドオン ツールをインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="06b08-114">When you're using Visual Studio 2015 you can install the add-on tools "Docker Tools for Visual Studio."</span></span> <span data-ttu-id="06b08-115">Visual Studio 2017 での Docker ツール組み込まで既にします。</span><span class="sxs-lookup"><span data-stu-id="06b08-115">For Visual Studio 2017, Docker Tools come built in already.</span></span> <span data-ttu-id="06b08-116">どちらの場合も開発、実行、および選択した Docker 環境で直接アプリケーションを検証することができます。</span><span class="sxs-lookup"><span data-stu-id="06b08-116">In both cases you can develop, run, and validate your applications directly in the chosen Docker environment.</span></span> <span data-ttu-id="06b08-117">F5 キーを Docker に直接アプリケーション (1 つのコンテナーまたは複数のコンテナー) は、デバッグとホストまたはを編集して、コンテナーを再構築しなくても、アプリを更新するには、Ctrl + F5 キーを押します。</span><span class="sxs-lookup"><span data-stu-id="06b08-117">F5 your application (single container or multiple containers) directly into a Docker host with debugging, or press Ctrl+F5 to edit and refresh your app without having to rebuild the container.</span></span> <span data-ttu-id="06b08-118">これは、Linux または Windows の Docker コンテナーを作成する Windows 開発者にとって最も簡単でより強力な選択肢です。</span><span class="sxs-lookup"><span data-stu-id="06b08-118">This is the simplest and more powerful choice for Windows developers creating Docker containers for Linux or Windows.</span></span>

> [!NOTE]
> <span data-ttu-id="06b08-119">Visual Studio 用 Docker ツールをダウンロードするには<https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4>します。</span><span class="sxs-lookup"><span data-stu-id="06b08-119">To download Docker Tools for Visual Studio, go to <https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4>.</span></span>

## <a name="language-and-framework-choices"></a><span data-ttu-id="06b08-120">言語とフレームワークの選択</span><span class="sxs-lookup"><span data-stu-id="06b08-120">Language and framework choices</span></span>

<span data-ttu-id="06b08-121">Docker アプリケーションと最新の言語でマイクロソフトのツールを開発することができます。</span><span class="sxs-lookup"><span data-stu-id="06b08-121">You can develop Docker applications and Microsoft tools with most modern languages.</span></span> <span data-ttu-id="06b08-122">次に、最初のリストが、これに限定されません。</span><span class="sxs-lookup"><span data-stu-id="06b08-122">The following is an initial list, but you are not limited to it:</span></span>

-   <span data-ttu-id="06b08-123">.NET Core および ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="06b08-123">.NET Core and ASP.NET Core</span></span>
-   <span data-ttu-id="06b08-124">Node.js</span><span class="sxs-lookup"><span data-stu-id="06b08-124">Node.js</span></span>
-   <span data-ttu-id="06b08-125">Golang</span><span class="sxs-lookup"><span data-stu-id="06b08-125">Golang</span></span>
-   <span data-ttu-id="06b08-126">Java</span><span class="sxs-lookup"><span data-stu-id="06b08-126">Java</span></span>
-   <span data-ttu-id="06b08-127">Ruby</span><span class="sxs-lookup"><span data-stu-id="06b08-127">Ruby</span></span>
-   <span data-ttu-id="06b08-128">Python</span><span class="sxs-lookup"><span data-stu-id="06b08-128">Python</span></span>

<span data-ttu-id="06b08-129">基本的には、Linux または Windows で Docker でサポートされている最新の言語を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="06b08-129">Basically, you can use any modern language supported by Docker in Linux or Windows.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="06b08-130">[前へ](deploy-azure-kubernetes-service.md)
>[次へ](docker-apps-inner-loop-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="06b08-130">[Previous](deploy-azure-kubernetes-service.md)
[Next](docker-apps-inner-loop-workflow.md)</span></span>