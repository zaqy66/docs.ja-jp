---
title: .NET Core の Docker イメージのビルド
description: Docker イメージと .NET Core について
author: jralexander
ms.author: johalex
ms.date: 11/06/2017
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: e48a263334ebb93a5d281032336aeb4073d8467c
ms.sourcegitcommit: e8dc507cfdaad504fc9d4c83d28d24569dcef91c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/03/2018
ms.locfileid: "34827340"
---
# <a name="building-docker-images-for-net-core-applications"></a><span data-ttu-id="624b8-103">.NET Core アプリケーションの Docker イメージのビルド</span><span class="sxs-lookup"><span data-stu-id="624b8-103">Building Docker Images for .NET Core Applications</span></span>

 <span data-ttu-id="624b8-104">このチュートリアルでは、Docker で .NET Core を使用する方法を紹介します。</span><span class="sxs-lookup"><span data-stu-id="624b8-104">In this tutorial, We focus on how to use .NET Core on Docker.</span></span> <span data-ttu-id="624b8-105">最初に、Microsoft が提供し、保守管理しているさまざま Docker イメージと使用例について考察します。</span><span class="sxs-lookup"><span data-stu-id="624b8-105">First, we explore the different Docker images offered and maintained by Microsoft, and use cases.</span></span> <span data-ttu-id="624b8-106">次に、ASP.NET Core アプリをビルドし、Docker で動作させる方法について学習します。</span><span class="sxs-lookup"><span data-stu-id="624b8-106">We then learn how to build and dockerize an ASP.NET Core app.</span></span>

<span data-ttu-id="624b8-107">このチュートリアルを通して、以下のことを学びます。</span><span class="sxs-lookup"><span data-stu-id="624b8-107">During the course of this tutorial, you learn:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="624b8-108">Microsoft .NET Core Docker イメージについて学習する</span><span class="sxs-lookup"><span data-stu-id="624b8-108">Learn about Microsoft .NET Core Docker images</span></span> 
> * <span data-ttu-id="624b8-109">Docker で動作させる ASP.NET Core サンプル アプリを取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-109">Get an ASP.NET Core sample app to Dockerize</span></span>
> * <span data-ttu-id="624b8-110">ASP.NET サンプル アプリをローカルで実行する</span><span class="sxs-lookup"><span data-stu-id="624b8-110">Run the ASP.NET sample app locally</span></span>
> * <span data-ttu-id="624b8-111">サンプルをビルドし、Docker for Linux コンテナーで実行する</span><span class="sxs-lookup"><span data-stu-id="624b8-111">Build and run the sample with Docker for Linux containers</span></span>
> * <span data-ttu-id="624b8-112">サンプルをビルドし、Docker for Windows コンテナーで実行する</span><span class="sxs-lookup"><span data-stu-id="624b8-112">Build and run the sample with Docker for Windows containers</span></span>

## <a name="docker-image-optimizations"></a><span data-ttu-id="624b8-113">Docker イメージの最適化</span><span class="sxs-lookup"><span data-stu-id="624b8-113">Docker Image Optimizations</span></span>

<span data-ttu-id="624b8-114">開発者向けの Docker イメージをビルドするにあたり、次の主な 3 つのシナリオに重点を置きました。</span><span class="sxs-lookup"><span data-stu-id="624b8-114">When building Docker images for developers, we focused on three main scenarios:</span></span>

* <span data-ttu-id="624b8-115">.NET Core アプリの開発に使用されるイメージ</span><span class="sxs-lookup"><span data-stu-id="624b8-115">Images used to develop .NET Core apps</span></span>
* <span data-ttu-id="624b8-116">.NET Core アプリのビルドに使用されるイメージ</span><span class="sxs-lookup"><span data-stu-id="624b8-116">Images used to build .NET Core apps</span></span>
* <span data-ttu-id="624b8-117">.NET Core アプリの実行に使用されるイメージ</span><span class="sxs-lookup"><span data-stu-id="624b8-117">Images used to run .NET Core apps</span></span>

<span data-ttu-id="624b8-118">3 つのイメージである理由は、</span><span class="sxs-lookup"><span data-stu-id="624b8-118">Why three images?</span></span>
<span data-ttu-id="624b8-119">コンテナー化されたアプリケーションを開発、ビルドおよび実行する場合、優先順位がそれぞれ異なるためです。</span><span class="sxs-lookup"><span data-stu-id="624b8-119">When developing, building, and running containerized applications, we have different priorities.</span></span>

* <span data-ttu-id="624b8-120">**開発:** 変更をどれだけ速く繰り返せるかと変更のデバッグ機能が優先されます。</span><span class="sxs-lookup"><span data-stu-id="624b8-120">**Development:**  The priority focuses on quickly iterate changes, and the ability to debug the changes.</span></span> <span data-ttu-id="624b8-121">イメージのサイズはそれほど重要ではなく、むしろ、コードを変更し、それをすばやく確認できるかが重要になります。</span><span class="sxs-lookup"><span data-stu-id="624b8-121">The size of the image isn't as important, rather can you make changes to your code and see them quickly?</span></span>

* <span data-ttu-id="624b8-122">**ビルド:** このイメージには、コンパイラやバイナリを最適化するその他の依存関係など、アプリのコンパイルに必要なすべてが含まれます。</span><span class="sxs-lookup"><span data-stu-id="624b8-122">**Build:** This image contains everything needed to compile your app, which includes the compiler and any other dependencies to optimize the binaries.</span></span>  <span data-ttu-id="624b8-123">ビルド イメージを使用し、実稼働イメージに置くアセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="624b8-123">You use the build image to create the assets you place into a production image.</span></span> <span data-ttu-id="624b8-124">ビルド イメージは継続的インテグレーション、またはビルド環境で使用されます。</span><span class="sxs-lookup"><span data-stu-id="624b8-124">The build image would be used for continuous integration, or in a build environment.</span></span> <span data-ttu-id="624b8-125">この手法では、ビルド エージェントがビルド イメージ インスタンスで (必要なすべての依存関係と共に) アプリケーションをコンパイルし、ビルドできます。</span><span class="sxs-lookup"><span data-stu-id="624b8-125">This approach allows a build agent to compile and build the application (with all the required dependencies) in a build image instance.</span></span> <span data-ttu-id="624b8-126">この Docker イメージの実行方法を理解する必要があるのはビルド エージェントのみです。</span><span class="sxs-lookup"><span data-stu-id="624b8-126">Your build agent only needs to know how to run this Docker image.</span></span>

* <span data-ttu-id="624b8-127">**実稼働:** イメージをどれだけ速く配置し、開始できるか。</span><span class="sxs-lookup"><span data-stu-id="624b8-127">**Production:** How fast you can deploy and start your image?</span></span> <span data-ttu-id="624b8-128">このイメージは小さく、Docker レジストリから Docker ホストまでのネットワーク パフォーマンスが最適化されます。</span><span class="sxs-lookup"><span data-stu-id="624b8-128">This image is small so network performance from your Docker Registry to your Docker hosts is optimized.</span></span> <span data-ttu-id="624b8-129">コンテンツは実行できる状態であるため、Docker の実行から結果の処理までを最速で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="624b8-129">The contents are ready to run enabling the fastest time from Docker run to processing results.</span></span> <span data-ttu-id="624b8-130">動的コード コンパイルは Docker モデルで必要ありません。</span><span class="sxs-lookup"><span data-stu-id="624b8-130">Dynamic code compilation isn't needed in the Docker model.</span></span> <span data-ttu-id="624b8-131">このイメージに配置するコンテンツは、アプリケーションの実行に必要なバイナリとコンテンツに制限されます。</span><span class="sxs-lookup"><span data-stu-id="624b8-131">The content you place in this image would be limited to the binaries and content needed to run the application.</span></span>

    <span data-ttu-id="624b8-132">たとえば、`dotnet publish` 出力には次が含まれています。</span><span class="sxs-lookup"><span data-stu-id="624b8-132">For example, the `dotnet publish` output contains:</span></span>

    * <span data-ttu-id="624b8-133">コンパイルされたバイナリ</span><span class="sxs-lookup"><span data-stu-id="624b8-133">the compiled binaries</span></span>
    * <span data-ttu-id="624b8-134">.js ファイルと .css ファイル</span><span class="sxs-lookup"><span data-stu-id="624b8-134">.js and .css files</span></span>


<span data-ttu-id="624b8-135">実稼働イメージに `dotnet publish` コマンド出力を含める理由は、そのサイズを最小限に抑えることにあります。</span><span class="sxs-lookup"><span data-stu-id="624b8-135">The reason to include the `dotnet publish` command output in your production image is to keep its size to a minimum.</span></span>

<span data-ttu-id="624b8-136">一部の .NET Core イメージは異なるタグの間で層を共有します。そのため、最新のタグをダウンロードするプロセスが比較的軽くなります。</span><span class="sxs-lookup"><span data-stu-id="624b8-136">Some .NET Core images share layers between different tags so downloading the latest tag is a relatively lightweight process.</span></span> <span data-ttu-id="624b8-137">コンピューターに以前のバージョンがインストールされている場合、このアーキテクチャで必要なディスク領域が減ります。</span><span class="sxs-lookup"><span data-stu-id="624b8-137">If you already have an older version on your machine, this architecture decreases the needed disk space.</span></span>

<span data-ttu-id="624b8-138">複数のアプリケーションが同じコンピューターで共通のイメージを使用するとき、共通のイメージ間でメモリが共有されます。</span><span class="sxs-lookup"><span data-stu-id="624b8-138">When multiple applications use common images on the same machine, memory is shared between the common images.</span></span> <span data-ttu-id="624b8-139">共有するイメージは同じものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="624b8-139">The images must be the same to be shared.</span></span>

## <a name="docker-image-variations"></a><span data-ttu-id="624b8-140">Docker イメージのバリエーション</span><span class="sxs-lookup"><span data-stu-id="624b8-140">Docker image variations</span></span>

<span data-ttu-id="624b8-141">上記の目標を達成するために、[`microsoft/dotnet`](https://hub.docker.com/r/microsoft/dotnet/) にはイメージ バリアントが用意されています。</span><span class="sxs-lookup"><span data-stu-id="624b8-141">To achieve the goals above, we provide image variants under [`microsoft/dotnet`](https://hub.docker.com/r/microsoft/dotnet/).</span></span>

* <span data-ttu-id="624b8-142">`microsoft/dotnet:<version>-sdk`(`microsoft/dotnet:2.1-sdk`) このイメージには、.NET Core とコマンド ライン ツール (CLI) を含む .NET Core SDK が含まれています。</span><span class="sxs-lookup"><span data-stu-id="624b8-142">`microsoft/dotnet:<version>-sdk`(`microsoft/dotnet:2.1-sdk`) This image contains the .NET Core SDK, which includes the .NET Core and Command Line Tools (CLI).</span></span> <span data-ttu-id="624b8-143">このイメージは **開発シナリオ** にマップされます。</span><span class="sxs-lookup"><span data-stu-id="624b8-143">This image maps to the **development scenario**.</span></span> <span data-ttu-id="624b8-144">このイメージは、ローカル開発、デバッグおよび単体テストに使用します。</span><span class="sxs-lookup"><span data-stu-id="624b8-144">You use this image for local development, debugging, and unit testing.</span></span> <span data-ttu-id="624b8-145">このイメージは、**ビルド** シナリオでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="624b8-145">This image can also be used for your **build** scenarios.</span></span> <span data-ttu-id="624b8-146">`microsoft/dotnet:sdk` を使用すると、常に最新版が取得されます。</span><span class="sxs-lookup"><span data-stu-id="624b8-146">Using `microsoft/dotnet:sdk` always gives you the latest version.</span></span>

> [!TIP]
> <span data-ttu-id="624b8-147">要件が確定していない場合、`microsoft/dotnet:<version>-sdk` イメージの使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="624b8-147">If you are unsure about your needs, you want to use the `microsoft/dotnet:<version>-sdk` image.</span></span> <span data-ttu-id="624b8-148">これは "事実上標準の" イメージであり、使い捨てのコンテナーとして使用されます (ソース コードをマウントし、コンテナーを起動してアプリを開始します)。また、基礎イメージとして使用し、これに基づいて他のイメージをビルドします。</span><span class="sxs-lookup"><span data-stu-id="624b8-148">As the "de facto" image, it's designed to be used as a throw away container (mount your source code and start the container to start your app), and as the base image to build other images from.</span></span>

* <span data-ttu-id="624b8-149">`microsoft/dotnet:<version>-runtime`: このイメージには .NET Core が含まれ (ランタイムとライブラリ)、**実稼働**で .NET Core アプリを実行するために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="624b8-149">`microsoft/dotnet:<version>-runtime`: This image contains the .NET Core (runtime and libraries) and is optimized for running .NET Core apps in **production**.</span></span>

## <a name="alternative-images"></a><span data-ttu-id="624b8-150">その他のイメージ</span><span class="sxs-lookup"><span data-stu-id="624b8-150">Alternative images</span></span>

<span data-ttu-id="624b8-151">開発、ビルドおよび実稼働の最適化されたシナリオに加え、次の追加イメージが提供されます。</span><span class="sxs-lookup"><span data-stu-id="624b8-151">In addition to the optimized scenarios of development, build and production, we provide additional images:</span></span>

* <span data-ttu-id="624b8-152">`microsoft/dotnet:<version>-runtime-deps`: **runtime-deps** イメージには、オペレーティング システムと .NET Core で必要とされるすべてのネイティブ依存関係が含まれます。</span><span class="sxs-lookup"><span data-stu-id="624b8-152">`microsoft/dotnet:<version>-runtime-deps`: The **runtime-deps** image contains the operating system with all of the native dependencies needed by .NET Core.</span></span> <span data-ttu-id="624b8-153">このイメージは[自己完結型アプリケーション](../deploying/index.md)用です。</span><span class="sxs-lookup"><span data-stu-id="624b8-153">This image is for [self-contained applications](../deploying/index.md).</span></span>

<span data-ttu-id="624b8-154">各バリアントの最新バージョン:</span><span class="sxs-lookup"><span data-stu-id="624b8-154">Latest versions of each variant:</span></span>

* <span data-ttu-id="624b8-155">`microsoft/dotnet` または `microsoft/dotnet:latest` (SDK イメージのエイリアス)</span><span class="sxs-lookup"><span data-stu-id="624b8-155">`microsoft/dotnet` or `microsoft/dotnet:latest` (alias for the SDK image)</span></span>
* `microsoft/dotnet:sdk`
* `microsoft/dotnet:runtime`
* `microsoft/dotnet:runtime-deps`

## <a name="samples-to-explore"></a><span data-ttu-id="624b8-156">お試しいただきたいサンプル</span><span class="sxs-lookup"><span data-stu-id="624b8-156">Samples to explore</span></span>

* <span data-ttu-id="624b8-157">[この ASP.NET Core の Docker サンプル](https://github.com/dotnet/dotnet-docker/tree/master/samples/aspnetapp)は、運用向けの ASP.NET Core アプリの Docker イメージを構築するためのベスト プラクティス パターンを示します。</span><span class="sxs-lookup"><span data-stu-id="624b8-157">[This ASP.NET Core Docker sample](https://github.com/dotnet/dotnet-docker/tree/master/samples/aspnetapp) demonstrates a best practice pattern for building Docker images for ASP.NET Core apps for production.</span></span> <span data-ttu-id="624b8-158">このサンプルは Linux コンテナーと Windows コンテナーのどちらでも動作します。</span><span class="sxs-lookup"><span data-stu-id="624b8-158">The sample works with both Linux and Windows containers.</span></span>

* <span data-ttu-id="624b8-159">この .NET Core の Docker サンプルでは、[運用環境用の .NET Core アプリの Docker イメージをビルドする](https://github.com/dotnet/dotnet-docker/tree/master/samples/dotnetapp)方法に関するベスト プラクティス パターンを示します。</span><span class="sxs-lookup"><span data-stu-id="624b8-159">This .NET Core Docker sample demonstrates a best practice pattern for [building Docker images for .NET Core apps for production.](https://github.com/dotnet/dotnet-docker/tree/master/samples/dotnetapp)</span></span>

## <a name="forward-the-request-scheme-and-original-ip-address"></a><span data-ttu-id="624b8-160">要求スキームと元の IP アドレスを転送する</span><span class="sxs-lookup"><span data-stu-id="624b8-160">Forward the request scheme and original IP address</span></span>

<span data-ttu-id="624b8-161">プロキシ サーバー、ロード バランサー、および他のネットワーク アプライアンスにより、要求に関する情報が、コンテナー化されたアプリに到達する前にわからなくなることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="624b8-161">Proxy servers, load balancers, and other network appliances often obscure information about a request before it reaches the containerized app:</span></span>

* <span data-ttu-id="624b8-162">HTTPS 要求が HTTP によってプロキシされると、元のスキーム (HTTPS) は失われ、ヘッダーで転送される必要があります。</span><span class="sxs-lookup"><span data-stu-id="624b8-162">When HTTPS requests are proxied over HTTP, the original scheme (HTTPS) is lost and must be forwarded in a header.</span></span>
* <span data-ttu-id="624b8-163">アプリは、インターネット上または社内ネットワーク上の本来の送信元ではなく、プロキシから要求を受信するため、元のクライアントの IP アドレスもヘッダーで転送される必要があります。</span><span class="sxs-lookup"><span data-stu-id="624b8-163">Because an app receives a request from the proxy and not its true source on the Internet or corporate network, the original client IP address must also be forwarded in a header.</span></span>

<span data-ttu-id="624b8-164">この情報は、リダイレクト、認証、リンクの生成、ポリシーの評価、クライアントの位置情報など、要求の処理で重要になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="624b8-164">This information may be important in request processing, for example in redirects, authentication, link generation, policy evaluation, and client geolocation.</span></span>

<span data-ttu-id="624b8-165">スキームと元の IP アドレスをコンテナー化された ASP.NET Core アプリに転送するには、Forwarded Headers Middleware を使用します。</span><span class="sxs-lookup"><span data-stu-id="624b8-165">To forward the scheme and original IP address to a containerized ASP.NET Core app, use Forwarded Headers Middleware.</span></span> <span data-ttu-id="624b8-166">詳細については、「[プロキシ サーバーとロード バランサーを使用するために ASP.NET Core を構成する](/aspnet/core/host-and-deploy/proxy-load-balancer)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="624b8-166">For more information, see [Configure ASP.NET Core to work with proxy servers and load balancers](/aspnet/core/host-and-deploy/proxy-load-balancer).</span></span>

## <a name="your-first-aspnet-core-docker-app"></a><span data-ttu-id="624b8-167">初めての ASP.NET Core Docker アプリ</span><span class="sxs-lookup"><span data-stu-id="624b8-167">Your first ASP.NET Core Docker app</span></span>

<span data-ttu-id="624b8-168">このチュートリアルでは、Docker で動作させるアプリに ASP.NET Core Docker サンプル アプリケーションを使用しましょう。</span><span class="sxs-lookup"><span data-stu-id="624b8-168">For this tutorial, lets use an ASP.NET Core Docker sample application for the app we want to dockerize.</span></span> <span data-ttu-id="624b8-169">この ASP.NET Core Docker サンプル アプリケーションでは、運用環境向け ASP.NET Core アプリの Docker イメージをビルドする場合のベスト プラクティス パターンを確認できます。</span><span class="sxs-lookup"><span data-stu-id="624b8-169">This ASP.NET Core Docker sample application demonstrates a best practice pattern for building Docker images for ASP.NET Core apps for production.</span></span> <span data-ttu-id="624b8-170">このサンプルは Linux コンテナーと Windows コンテナーのどちらでも動作します。</span><span class="sxs-lookup"><span data-stu-id="624b8-170">The sample works with both Linux and Windows containers.</span></span>

<span data-ttu-id="624b8-171">このサンプル Dockerfile は、ASP.NET Core Runtime Docker ベース イメージに基づき、ASP.NET Core アプリケーション Docker イメージを作成します。</span><span class="sxs-lookup"><span data-stu-id="624b8-171">The sample Dockerfile creates an ASP.NET Core application Docker image based off of the ASP.NET Core Runtime Docker base image.</span></span>

<span data-ttu-id="624b8-172">[Docker のマルチステージ ビルド機能](https://docs.docker.com/engine/userguide/eng-image/multistage-build/)を利用し、次のことを行います。</span><span class="sxs-lookup"><span data-stu-id="624b8-172">It uses the [Docker multi-stage build feature](https://docs.docker.com/engine/userguide/eng-image/multistage-build/) to:</span></span>

* <span data-ttu-id="624b8-173">**より大きな** ASP.NET Core Build Docker ベース イメージに基づき、コンテナーでサンプルをビルドする</span><span class="sxs-lookup"><span data-stu-id="624b8-173">build the sample in a container based on the **larger** ASP.NET Core Build Docker base image</span></span> 
* <span data-ttu-id="624b8-174">**より小さい** ASP.NET Core Docker Runtime ベース イメージに基づき、最終的なビルド結果を Docker イメージにコピーする</span><span class="sxs-lookup"><span data-stu-id="624b8-174">copies the final build result into a Docker image based on the **smaller** ASP.NET Core Docker Runtime base image</span></span>

> [!NOTE]
> <span data-ttu-id="624b8-175">このビルド イメージには、アプリケーションのビルドに必要なツールが含まれています。ランタイム イメージにはそれが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="624b8-175">The build image contains required tools to build applications while the runtime image does not.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="624b8-176">必須コンポーネント</span><span class="sxs-lookup"><span data-stu-id="624b8-176">Prerequisites</span></span>

<span data-ttu-id="624b8-177">ビルドし、実行するには、次のアイテムをインストールします。</span><span class="sxs-lookup"><span data-stu-id="624b8-177">To build and run, install the following items:</span></span>

#### <a name="net-core-21-sdk"></a><span data-ttu-id="624b8-178">.NET Core 2.1 SDK</span><span class="sxs-lookup"><span data-stu-id="624b8-178">.NET Core 2.1 SDK</span></span>

* <span data-ttu-id="624b8-179">[.NET Core SDK 2.1](https://www.microsoft.com/net/core) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="624b8-179">Install [.NET Core SDK 2.1](https://www.microsoft.com/net/core).</span></span>

* <span data-ttu-id="624b8-180">コード エディターをまだインストールしていなければ、お気に入りのエディターをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="624b8-180">Install your favorite code editor, if you haven't already.</span></span>

> [!TIP]
> <span data-ttu-id="624b8-181">コード エディターをインストールする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="624b8-181">Need to install a code editor?</span></span> <span data-ttu-id="624b8-182">[Visual Studio](https://visualstudio.com/downloads) をお試しください。</span><span class="sxs-lookup"><span data-stu-id="624b8-182">Try [Visual Studio](https://visualstudio.com/downloads)!</span></span>

#### <a name="installing-docker-client"></a><span data-ttu-id="624b8-183">Docker クライアントをインストールする</span><span class="sxs-lookup"><span data-stu-id="624b8-183">Installing Docker Client</span></span>

<span data-ttu-id="624b8-184">[Docker 18.03](https://docs.docker.com/release-notes/docker-ce/) 以降の Docker クライアントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="624b8-184">Install [Docker 18.03](https://docs.docker.com/release-notes/docker-ce/) or later of the Docker client.</span></span>

<span data-ttu-id="624b8-185">Docker クライアントがインストール可能な OS:</span><span class="sxs-lookup"><span data-stu-id="624b8-185">The Docker client can be installed in:</span></span>

* <span data-ttu-id="624b8-186">Linux ディストリビューション</span><span class="sxs-lookup"><span data-stu-id="624b8-186">Linux distributions</span></span>

   * [<span data-ttu-id="624b8-187">CentOS</span><span class="sxs-lookup"><span data-stu-id="624b8-187">CentOS</span></span>](https://www.docker.com/docker-centos-distribution)

   * [<span data-ttu-id="624b8-188">Debian</span><span class="sxs-lookup"><span data-stu-id="624b8-188">Debian</span></span>](https://www.docker.com/docker-debian)

   * [<span data-ttu-id="624b8-189">Fedora</span><span class="sxs-lookup"><span data-stu-id="624b8-189">Fedora</span></span>](https://www.docker.com/docker-fedora)

   * [<span data-ttu-id="624b8-190">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="624b8-190">Ubuntu</span></span>](https://www.docker.com/docker-ubuntu)

* [<span data-ttu-id="624b8-191">macOS</span><span class="sxs-lookup"><span data-stu-id="624b8-191">macOS</span></span>](https://docs.docker.com/docker-for-mac/)

* <span data-ttu-id="624b8-192">[Windows](https://docs.docker.com/docker-for-windows/)</span><span class="sxs-lookup"><span data-stu-id="624b8-192">[Windows](https://docs.docker.com/docker-for-windows/).</span></span>

#### <a name="installing-git-for-sample-repository"></a><span data-ttu-id="624b8-193">サンプル リポジトリとして Git をインストールする</span><span class="sxs-lookup"><span data-stu-id="624b8-193">Installing Git for sample repository</span></span>

* <span data-ttu-id="624b8-194">リポジトリを複製する場合、[git](https://git-scm.com/download) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="624b8-194">Install [git](https://git-scm.com/download) if you wish to clone the repository.</span></span>

### <a name="getting-the-sample-application"></a><span data-ttu-id="624b8-195">サンプル アプリケーションを入手する</span><span class="sxs-lookup"><span data-stu-id="624b8-195">Getting the sample application</span></span>

<span data-ttu-id="624b8-196">サンプルを用意する最も簡単な方法は、git で[.NET Core Docker リポジトリ](https://github.com/dotnet/dotnet-docker)を複製することです。次の指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="624b8-196">The easiest way to get the sample is by cloning the [.NET Core Docker repository](https://github.com/dotnet/dotnet-docker) with git, using the following instructions:</span></span> 

```console
git clone https://github.com/dotnet/dotnet-docker
```

<span data-ttu-id="624b8-197">.NET Core Docker リポジトリから zip ファイルとしてリポジトリ (小さい) をダウンロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="624b8-197">You can also download the repository (it is small) as a zip from the .NET Core Docker repository.</span></span>

### <a name="run-the-aspnet-app-locally"></a><span data-ttu-id="624b8-198">ASP.NET アプリをローカルで実行する</span><span class="sxs-lookup"><span data-stu-id="624b8-198">Run the ASP.NET app locally</span></span>

<span data-ttu-id="624b8-199">参照ポイントとして、アプリケーションをコンテナー化する前に、まず、アプリケーションをローカルで実行します。</span><span class="sxs-lookup"><span data-stu-id="624b8-199">For a reference point, before we containerize the application, first run the application locally.</span></span>

<span data-ttu-id="624b8-200">.NET Core 2.1 SDK を利用してアプリケーションをビルドし、ローカルで実行できます。次のコマンドを利用します (この指示では、リポジトリのルートを想定しています)。</span><span class="sxs-lookup"><span data-stu-id="624b8-200">You can build and run the application locally with the .NET Core 2.1 SDK using the following commands (The instructions assume the root of the repository):</span></span>

```console
cd dotnet-docker
cd samples
cd aspnetapp // solution scope where the dockerfile is located
cd aspnetapp // project scope

dotnet run
```

<span data-ttu-id="624b8-201">アプリケーションが起動したら、お使いの Web ブラウザーで **http://localhost:5000** にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="624b8-201">After the application starts, visit **http://localhost:5000** in your web browser.</span></span>

### <a name="build-and-run-the-sample-with-docker-for-linux-containers"></a><span data-ttu-id="624b8-202">サンプルをビルドし、Docker for Linux コンテナーで実行する</span><span class="sxs-lookup"><span data-stu-id="624b8-202">Build and run the sample with Docker for Linux containers</span></span>

<span data-ttu-id="624b8-203">Linux コンテナーを利用し、Docker でサンプルをビルドし、実行できます。次のコマンドを利用します (この指示では、リポジトリのルートを想定しています)。</span><span class="sxs-lookup"><span data-stu-id="624b8-203">You can build and run the sample in Docker using Linux containers using the following commands (The instructions assume the root of the repository):</span></span>

```console
cd dotnet-docker
cd samples
cd aspnetapp // solution scope where the dockerfile is located

docker build -t aspnetapp .
docker run -it --rm -p 5000:80 --name aspnetcore_sample aspnetapp
```

> [!NOTE]
> <span data-ttu-id="624b8-204">`docker run` '-p' 引数は、コンピューターのポート 5000 をコンテナーのポート 80 にマッピングします (ポート マッピングの形式は `host:container` です)。</span><span class="sxs-lookup"><span data-stu-id="624b8-204">The `docker run` '-p' argument maps port 5000 on your local machine to port 80 in the container (the port mapping form is `host:container`).</span></span> <span data-ttu-id="624b8-205">詳細については、コマンドライン パラメーターの [docker run](https://docs.docker.com/engine/reference/commandline/exec/) 参照をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="624b8-205">For more information, see the [docker run](https://docs.docker.com/engine/reference/commandline/exec/) reference on command-line parameters.</span></span>

<span data-ttu-id="624b8-206">アプリケーションが起動したら、お使いの Web ブラウザーで **http://localhost:5000** にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="624b8-206">After the application starts, visit **http://localhost:5000** in your web browser.</span></span>

### <a name="build-and-run-the-sample-with-docker-for-windows-containers"></a><span data-ttu-id="624b8-207">サンプルをビルドし、Docker for Windows コンテナーで実行する</span><span class="sxs-lookup"><span data-stu-id="624b8-207">Build and run the sample with Docker for Windows containers</span></span>

<span data-ttu-id="624b8-208">Window コンテナーを利用し、Docker でサンプルをビルドし、実行できます。次のコマンドを利用します (この指示では、リポジトリのルートを想定しています)。</span><span class="sxs-lookup"><span data-stu-id="624b8-208">You can build and run the sample in Docker using Windows containers using the following commands (The instructions assume the root of the repository):</span></span>

```console
cd dotnet-docker
cd samples
cd aspnetapp // solution scope where the dockerfile is located

docker build -t aspnetapp .
docker run -it --rm --name aspnetcore_sample aspnetapp
```

> [!IMPORTANT]
> <span data-ttu-id="624b8-209">Windows コンテナーの利用時、お使いのブラウザーで (http://localhost) ではなく) **コンテナー IP アドレス**に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="624b8-209">You must navigate to the **container IP address** (as opposed to http://localhost) in your browser directly when using Windows containers.</span></span> <span data-ttu-id="624b8-210">次の手順でコンテナーの IP アドレスを取得できます。</span><span class="sxs-lookup"><span data-stu-id="624b8-210">You can get the IP address of your container with the following steps:</span></span>

* <span data-ttu-id="624b8-211">別のコマンド プロンプトを開きます。</span><span class="sxs-lookup"><span data-stu-id="624b8-211">Open up another command prompt.</span></span>
* <span data-ttu-id="624b8-212">`docker ps` を実行し、実行中のコンテナーを確認します。</span><span class="sxs-lookup"><span data-stu-id="624b8-212">Run `docker ps` to see your running containers.</span></span> <span data-ttu-id="624b8-213">"aspnetcore_sample" コンテナーを確認できるはずです。</span><span class="sxs-lookup"><span data-stu-id="624b8-213">The "aspnetcore_sample" container should be there.</span></span>
* <span data-ttu-id="624b8-214">`docker exec aspnetcore_sample ipconfig` を実行します。</span><span class="sxs-lookup"><span data-stu-id="624b8-214">Run `docker exec aspnetcore_sample ipconfig`.</span></span>
* <span data-ttu-id="624b8-215">コンテナー IP アドレスをコピーし、ブラウザーに貼り付けます (たとえば、172.29.245.43)。</span><span class="sxs-lookup"><span data-stu-id="624b8-215">Copy the container IP address and paste into your browser (for example, 172.29.245.43).</span></span>

> [!NOTE]
> <span data-ttu-id="624b8-216">Docker exec は、名前やハッシュでコンテナーを識別できます。</span><span class="sxs-lookup"><span data-stu-id="624b8-216">Docker exec supports identifying containers with name or hash.</span></span> <span data-ttu-id="624b8-217">今回のサンプルでは名前 (aspnetcore_sample) が使用されています。</span><span class="sxs-lookup"><span data-stu-id="624b8-217">The name (aspnetcore_sample) is used in our example.</span></span>

<span data-ttu-id="624b8-218">次の例では、実行中の Windows コンテナーの IP アドレスを取得する方法を確認できます。</span><span class="sxs-lookup"><span data-stu-id="624b8-218">See the following example of how to get the IP address of a running Windows container.</span></span>

```console
docker exec aspnetcore_sample ipconfig

Windows IP Configuration

Ethernet adapter Ethernet:

   Connection-specific DNS Suffix  . : contoso.com
   Link-local IPv6 Address . . . . . : fe80::1967:6598:124:cfa3%4
   IPv4 Address. . . . . . . . . . . : 172.29.245.43
   Subnet Mask . . . . . . . . . . . : 255.255.240.0
   Default Gateway . . . . . . . . . : 172.29.240.1
```

> [!NOTE]
> <span data-ttu-id="624b8-219">Docker exec は、実行中のコンテナーで新しいコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="624b8-219">Docker exec runs a new command in a running container.</span></span> <span data-ttu-id="624b8-220">詳細については、コマンドライン パラメーターの [docker exec 参照](https://docs.docker.com/engine/reference/commandline/exec/)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="624b8-220">For more information, see the [docker exec reference](https://docs.docker.com/engine/reference/commandline/exec/) on command-line parameters.</span></span>

<span data-ttu-id="624b8-221">[dotnet publish](../tools/dotnet-publish.md) コマンドを利用し、運用環境にローカル展開できるアプリケーションを生成できます。</span><span class="sxs-lookup"><span data-stu-id="624b8-221">You can produce an application that is ready to deploy to production locally using the [dotnet publish](../tools/dotnet-publish.md) command.</span></span>

```console
dotnet publish -c Release -o published
```

> [!NOTE]
> <span data-ttu-id="624b8-222">-c リリース引数はリリース モードでアプリケーションをビルドします (既定はデバッグ モードです)。</span><span class="sxs-lookup"><span data-stu-id="624b8-222">The -c Release argument builds the application in release mode (the default is debug mode).</span></span> <span data-ttu-id="624b8-223">詳細については、コマンドライン パラメーターの [dotnet run 参照](../tools/dotnet-run.md)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="624b8-223">For more information, see the [dotnet run reference](../tools/dotnet-run.md) on command-line parameters.</span></span>

<span data-ttu-id="624b8-224">次のコマンドを利用し、**Windows** でアプリケーションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="624b8-224">You can run the application on **Windows** using the following command.</span></span>

```console
dotnet published\aspnetapp.dll
```

<span data-ttu-id="624b8-225">次のコマンドを利用し、**Linux** または **macOS** でアプリケーションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="624b8-225">You can run the application on **Linux** or **macOS** using the following command.</span></span>

```bash
dotnet published/aspnetapp.dll
```

### <a name="docker-images-used-in-this-sample"></a><span data-ttu-id="624b8-226">このサンプルで使用されている Docker イメージ</span><span class="sxs-lookup"><span data-stu-id="624b8-226">Docker Images used in this sample</span></span>

<span data-ttu-id="624b8-227">次の Docker イメージはこのサンプルの dockerfile で使用されています。</span><span class="sxs-lookup"><span data-stu-id="624b8-227">The following Docker images are used in this sample's dockerfile.</span></span>

* `microsoft/dotnet:2.1-sdk`
* `microsoft/dotnet:2.1-aspnetcore-runtime`

<span data-ttu-id="624b8-228">おめでとうございます! </span><span class="sxs-lookup"><span data-stu-id="624b8-228">Congratulations!</span></span> <span data-ttu-id="624b8-229">今回の成果:</span><span class="sxs-lookup"><span data-stu-id="624b8-229">you have just:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="624b8-230">Microsoft .NET Core Docker イメージについて学習しました</span><span class="sxs-lookup"><span data-stu-id="624b8-230">Learned about Microsoft .NET Core Docker images</span></span>
> * <span data-ttu-id="624b8-231">Docker で動作させる ASP.NET Core サンプル アプリを取得しました</span><span class="sxs-lookup"><span data-stu-id="624b8-231">Got an ASP.NET Core sample app to Dockerize</span></span>
> * <span data-ttu-id="624b8-232">ASP.NET サンプル アプリをローカルで実行しました</span><span class="sxs-lookup"><span data-stu-id="624b8-232">Ran the ASP.NET sample app locally</span></span>
> * <span data-ttu-id="624b8-233">サンプルをビルドし、Docker for Linux コンテナーで実行しました</span><span class="sxs-lookup"><span data-stu-id="624b8-233">Built and ran the sample with Docker for Linux containers</span></span>
> * <span data-ttu-id="624b8-234">サンプルをビルドし、Docker for Windows コンテナーで実行しました</span><span class="sxs-lookup"><span data-stu-id="624b8-234">Built and ran the sample with Docker for Windows containers</span></span>

<span data-ttu-id="624b8-235">**次の手順**</span><span class="sxs-lookup"><span data-stu-id="624b8-235">**Next Steps**</span></span>

<span data-ttu-id="624b8-236">次の手順としては以下のものを用意しています。</span><span class="sxs-lookup"><span data-stu-id="624b8-236">Here are some next steps you can take:</span></span>

* [<span data-ttu-id="624b8-237">Visual Studio Docker ツールの使用</span><span class="sxs-lookup"><span data-stu-id="624b8-237">Working with Visual Studio Docker Tools</span></span>](https://docs.microsoft.com/aspnet/core/publishing/visual-studio-tools-for-docker)
* [<span data-ttu-id="624b8-238">Azure Container Registry から Azure Container Instances に Docker イメージを配置する</span><span class="sxs-lookup"><span data-stu-id="624b8-238">Deploying Docker Images from the Azure Container Registry to Azure Container Instances</span></span>](https://blogs.msdn.microsoft.com/stevelasker/2017/07/28/deploying-docker-images-from-the-azure-container-registry-to-azure-container-instances/)
* [<span data-ttu-id="624b8-239">Visual Studio Code でのデバッグ</span><span class="sxs-lookup"><span data-stu-id="624b8-239">Debugging with Visual Studio Code</span></span>](https://code.visualstudio.com/docs/nodejs/debugging-recipes#_nodejs-typescript-docker-container) 
* [<span data-ttu-id="624b8-240">クラウドにおける Visual Studio for Mac、コンテナー、サーバーレス コードの入門</span><span class="sxs-lookup"><span data-stu-id="624b8-240">Getting hands on with Visual Studio for Mac, containers, and serverless code in the cloud</span></span>](https://blogs.msdn.microsoft.com/visualstudio/2017/08/31/hands-on-with-visual-studio-for-mac-containers-serverless-code-in-the-cloud/#comments)
* [<span data-ttu-id="624b8-241">Docker と Visual Studio for Mac の入門ラボ</span><span class="sxs-lookup"><span data-stu-id="624b8-241">Getting Started with Docker and Visual Studio for Mac Lab</span></span>](https://github.com/Microsoft/vs4mac-labs/tree/master/Docker/Getting-Started)

> [!NOTE]
> <span data-ttu-id="624b8-242">Azure サブスクリプションをお持ちでない場合は、[今すぐサインアップ](https://azure.microsoft.com/free/?b=16.48)して 30 日間の無料アカウントと 200 ドル分の Azure クレジットを取得し、お好きな Azure サービスの組み合わせを試しましょう。</span><span class="sxs-lookup"><span data-stu-id="624b8-242">If you do not have an Azure subscription, [sign up today](https://azure.microsoft.com/free/?b=16.48) for a free 30-day account and get $200 in Azure Credits to try out any combination of Azure services.</span></span>
