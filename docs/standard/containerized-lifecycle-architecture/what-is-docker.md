---
title: Docker について
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/21/2017
ms.openlocfilehash: 056fb613c078cc407380060dc11890406ac8cffd
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50197679"
---
# <a name="what-is-docker"></a><span data-ttu-id="349a4-103">Docker について</span><span class="sxs-lookup"><span data-stu-id="349a4-103">What is Docker?</span></span>

<span data-ttu-id="349a4-104">[Docker](https://www.docker.com/)は、[オープン ソース プロジェクト](https://github.com/docker/docker)クラウドまたはオンプレミスで実行できる移植可能な自己完結型コンテナーとしてのアプリケーションのデプロイを自動化するため (を参照してください図 1-2)。</span><span class="sxs-lookup"><span data-stu-id="349a4-104">[Docker](https://www.docker.com/) is an [open-source project](https://github.com/docker/docker) for automating the deployment of applications as portable, self-sufficient containers that can run in the cloud or on-premises (see Figure 1-2).</span></span> <span data-ttu-id="349a4-105">Docker はまた、[会社](https://www.docker.com/)を促進およびこのテクノロジは、クラウド、Linux、および Windows のベンダーなどの Microsoft と共同で作業を開発します。</span><span class="sxs-lookup"><span data-stu-id="349a4-105">Docker is also a [company](https://www.docker.com/) that promotes and develops this technology, working in collaboration with cloud, Linux, and Windows vendors, including Microsoft.</span></span>

![](./media/image2.png)

<span data-ttu-id="349a4-106">図 1-2: Docker は、ハイブリッド クラウドのすべてのレイヤーでコンテナーをデプロイします</span><span class="sxs-lookup"><span data-stu-id="349a4-106">Figure 1-2: Docker deploys containers at all layers of the hybrid cloud</span></span>

<span data-ttu-id="349a4-107">Docker イメージ コンテナーは、Linux と Windows 上でネイティブに実行できます。</span><span class="sxs-lookup"><span data-stu-id="349a4-107">Docker image containers can run natively on Linux and Windows.</span></span> <span data-ttu-id="349a4-108">ただし、Windows イメージを Windows ホストでのみ実行でき、Linux イメージは、Linux ホスト、つまり、ホスト サーバーまたは VM でのみ実行できます。</span><span class="sxs-lookup"><span data-stu-id="349a4-108">However, Windows images can run only on Windows hosts and Linux images can run only on Linux hosts, meaning a host server or a VM.</span></span>

<span data-ttu-id="349a4-109">開発者は、Windows、Linux、または macOS 上の開発環境を使用できます。</span><span class="sxs-lookup"><span data-stu-id="349a4-109">Developers can use development environments on Windows, Linux, or macOS.</span></span> <span data-ttu-id="349a4-110">開発用コンピューターでは、開発者は、どの Docker イメージの配置、アプリとその依存関係を含む Docker ホストを実行します。</span><span class="sxs-lookup"><span data-stu-id="349a4-110">On the development computer, the developer runs a Docker host to which Docker images are deployed, including the app and its dependencies.</span></span> <span data-ttu-id="349a4-111">Linux または Mac 上で開発する場合は、Linux ベースの Docker ホストを使用し、Linux コンテナー専用のイメージを作成できます</span><span class="sxs-lookup"><span data-stu-id="349a4-111">Developers who work on Linux or on the Mac use a Docker host that is Linux based, and they can create images only for Linux containers.</span></span> <span data-ttu-id="349a4-112">(Mac で作業する開発者はコードを編集したり、Docker コマンド ライン インターフェイスを実行\[CLI\]から macOS では、この記事の執筆時点、コンテナーが macOS 上で直接実行しないでください)。Windows 上で開発する場合は、Linux または Windows コンテナーのいずれかのイメージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="349a4-112">(Developers working on the Mac can edit code or run the Docker command-line interface \[CLI\] from macOS, but, as of this writing, containers do not run directly on macOS.) Developers who work on Windows can create images for either Linux or Windows Containers.</span></span>

<span data-ttu-id="349a4-113">開発環境でコンテナーをホストし、開発ツールを追加するために、Docker は Windows 用または macOS 用の [Docker Community Edition (CE)](https://www.docker.com/community-edition) をリリースしています。</span><span class="sxs-lookup"><span data-stu-id="349a4-113">To host containers in development environments and provide additional developer tools, Docker ships [Docker Community Edition (CE)](https://www.docker.com/community-edition) for Windows or for macOS.</span></span> <span data-ttu-id="349a4-114">これらの製品で、コンテナーをホストするために必要な VM (Docker ホスト) がインストールされます。</span><span class="sxs-lookup"><span data-stu-id="349a4-114">These products install the necessary VM (the Docker host) to host the containers.</span></span> <span data-ttu-id="349a4-115">Docker は [Docker Enterprise Edition (EE) ](https://www.docker.com/enterprise-edition) もリリースしています。エンタープライズ開発向けに設計されており、大規模なビジネスクリティカル アプリケーションをビルドし、リリースし、運用環境で実行する IT チームに使用されています。</span><span class="sxs-lookup"><span data-stu-id="349a4-115">Docker also makes available [Docker Enterprise Edition (EE)](https://www.docker.com/enterprise-edition), which is designed for enterprise development and is used by IT teams who build, ship, and run large business-critical applications in production.</span></span>

<span data-ttu-id="349a4-116">[Windows コンテナー](/virtualization/windowscontainers/about/)を実行するには、次の 2 つの種類のランタイムがあります。</span><span class="sxs-lookup"><span data-stu-id="349a4-116">To run [Windows Containers](/virtualization/windowscontainers/about/), there are two types of runtimes:</span></span>

-   <span data-ttu-id="349a4-117">**Windows Server コンテナー** このランタイムには、プロセスと名前空間の分離テクノロジによる分離性をアプリケーションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="349a4-117">**Windows Server Container** This runtime provides application isolation through process and namespace isolation technology.</span></span> <span data-ttu-id="349a4-118">Windows Server コンテナーは、コンテナー ホストおよびホストで実行されているすべてのコンテナーとカーネルを共有します。</span><span class="sxs-lookup"><span data-stu-id="349a4-118">A Windows Server Container shares a kernel with the container host and with all containers running on the host.</span></span>

-   <span data-ttu-id="349a4-119">**HYPER-V コンテナー** 大幅に最適化された VM で各コンテナーを実行して、Windows Server コンテナーによって提供される分離でこれを展開します。</span><span class="sxs-lookup"><span data-stu-id="349a4-119">**Hyper-V Container** This expands on the isolation provided by Windows Server Containers by running each container in a highly optimized VM.</span></span> <span data-ttu-id="349a4-120">この構成では、コンテナー ホストのカーネルは、Hyper-V コンテナーと共有されず、分離性を提供します。</span><span class="sxs-lookup"><span data-stu-id="349a4-120">In this configuration, the kernel of the container host is not shared with the Hyper-V Containers, providing better isolation.</span></span>

<span data-ttu-id="349a4-121">これらのコンテナー イメージは、同じ方法で作成され、同じ機能します。</span><span class="sxs-lookup"><span data-stu-id="349a4-121">The images for these containers are created in the same way and function the same.</span></span> <span data-ttu-id="349a4-122">違いは、イメージからコンテナーを作成する方法、HYPER-V コンテナーを実行するには、追加のパラメーターが必要です。</span><span class="sxs-lookup"><span data-stu-id="349a4-122">The difference is in how the container is created from the image—running a Hyper-V Container requires an extra parameter.</span></span> <span data-ttu-id="349a4-123">詳細については、「[Hyper-V コンテナー](/virtualization/windowscontainers/about/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="349a4-123">For details, see [Hyper-V Containers](/virtualization/windowscontainers/about/).</span></span>

## <a name="comparing-docker-containers-with-vms"></a><span data-ttu-id="349a4-124">Vm での Docker コンテナーの比較</span><span class="sxs-lookup"><span data-stu-id="349a4-124">Comparing Docker containers with VMs</span></span>

<span data-ttu-id="349a4-125">図 1-3 は、Vm と Docker の比較を示しています。 コンテナー。</span><span class="sxs-lookup"><span data-stu-id="349a4-125">Figure 1-3 shows a comparison between VMs and Docker containers.</span></span>

<span data-ttu-id="349a4-126">コンテナーは、はるかに少ないリソースを必要とするため (たとえば、する必要はありません完全な OS)、簡単にデプロイされ、高速に起動します。</span><span class="sxs-lookup"><span data-stu-id="349a4-126">Because containers require far fewer resources (for example, they do not need a full OS), they are easy to deploy and they start fast.</span></span> <span data-ttu-id="349a4-127">これにより、密度の高い、コストを減らす、同じハードウェア単位に、その他のサービスを実行できることを意味することが可能にします。</span><span class="sxs-lookup"><span data-stu-id="349a4-127">This makes it possible for you to have higher density, meaning that you can run more services on the same hardware unit, thereby reducing costs.</span></span>

<span data-ttu-id="349a4-128">同じカーネルで実行されていることの副作用として、Vm よりも緩やかな分離を実現します。</span><span class="sxs-lookup"><span data-stu-id="349a4-128">As a side effect of running on the same kernel, you achieve less isolation than VMs.</span></span>

<span data-ttu-id="349a4-129">イメージの主な目的は、異なる展開間で同じ環境 (依存関係) にすることです。</span><span class="sxs-lookup"><span data-stu-id="349a4-129">The main goal of an image is that it makes the environment (dependencies) the same across different deployments.</span></span> <span data-ttu-id="349a4-130">自分のコンピューターでデバッグし、同じ環境が保証されている別のコンピューターに展開できます。</span><span class="sxs-lookup"><span data-stu-id="349a4-130">This means that you can debug it on your machine and then deploy it to another machine with the same environment guaranteed.</span></span>

<span data-ttu-id="349a4-131">コンテナー イメージは、アプリやサービスをパッケージ化し、信頼性が高く、再現可能な方法でデプロイする方法です。</span><span class="sxs-lookup"><span data-stu-id="349a4-131">A container image is a way to package an app or service and deploy it in a reliable and reproducible manner.</span></span> <span data-ttu-id="349a4-132">この点で、Docker はテクノロジだけではありませんも、哲学やプロセス。</span><span class="sxs-lookup"><span data-stu-id="349a4-132">In this respect, Docker is not only a technology, it's also a philosophy and a process.</span></span>

<span data-ttu-id="349a4-133">Docker を使用する場合と開発者を聞くことがない、「機能は私のコンピューターでは、なぜ実稼働環境ででしょうか。」</span><span class="sxs-lookup"><span data-stu-id="349a4-133">When using Docker, you will not hear developers say, "It works on my machine, why not in production?"</span></span> <span data-ttu-id="349a4-134">いることができます簡単に言えば「には、Docker で実行される」ためのサポートされている Docker 環境でパッケージ化された Docker アプリケーションを実行することができます、展開のすべての宛先 (開発、QA、ステージング、運用など。) にするためのものが、方法は、実行されます。</span><span class="sxs-lookup"><span data-stu-id="349a4-134">They can simply say, "It runs on Docker," because the packaged Docker application can be run on any supported Docker environment, and it will run the way it was intended to on all deployment destinations (Dev, QA, staging, production, etc.).</span></span>

![](./media/image3.png)

<span data-ttu-id="349a4-135">図 1-3: 従来の Vm を Docker コンテナーの比較</span><span class="sxs-lookup"><span data-stu-id="349a4-135">Figure 1-3: Comparison of traditional VMs to Docker containers</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="349a4-136">[前へ](index.md)
[次へ](docker-terminology.md)</span><span class="sxs-lookup"><span data-stu-id="349a4-136">[Previous](index.md)
[Next](docker-terminology.md)</span></span>
