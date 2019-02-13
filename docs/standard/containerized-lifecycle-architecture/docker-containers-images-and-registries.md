---
title: Docker コンテナー、イメージ、レジストリ
description: レジストリにアプリケーションを展開する Docker の方法で全体的な再生される重要な役割について説明します。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 7a2e20e09561a5cc91aa29059fb8d19a14205bb5
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56221200"
---
# <a name="docker-containers-images-and-registries"></a><span data-ttu-id="3d492-103">Docker コンテナー、イメージ、レジストリ</span><span class="sxs-lookup"><span data-stu-id="3d492-103">Docker containers, images, and registries</span></span>

<span data-ttu-id="3d492-104">Docker を使用する場合、およびその依存関係コンテナー イメージにアプリまたはサービス、およびパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="3d492-104">When using Docker, you create an app or service and package it and its dependencies into a container image.</span></span> <span data-ttu-id="3d492-105">イメージとは、アプリケーションまたはサービスと、その構成と依存関係の静的な表現です。</span><span class="sxs-lookup"><span data-stu-id="3d492-105">An image is a static representation of the app or service and its configuration and dependencies.</span></span>

<span data-ttu-id="3d492-106">アプリケーションまたはサービスを実行するために、アプリケーションのイメージはインスタンス化され、コンテナーが作成されます。このコンテナーが Docker ホスト上で実行されます。</span><span class="sxs-lookup"><span data-stu-id="3d492-106">To run the app or service, the app's image is instantiated to create a container, which will be running on the Docker host.</span></span> <span data-ttu-id="3d492-107">コンテナーは、最初に開発環境または PC でテストされます。</span><span class="sxs-lookup"><span data-stu-id="3d492-107">Containers are initially tested in a development environment or PC.</span></span>

<span data-ttu-id="3d492-108">イメージのライブラリとして機能する、レジストリにイメージを格納します。</span><span class="sxs-lookup"><span data-stu-id="3d492-108">You store images in a registry, which acts as a library of images.</span></span> <span data-ttu-id="3d492-109">運用環境のオーケストレーターに展開する場合は、レジストリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d492-109">You need a registry when deploying to production orchestrators.</span></span> <span data-ttu-id="3d492-110">Docker は [Docker Hub](https://hub.docker.com/) 経由で公開レジストリを保守します。他のベンダーは、さまざまなイメージのコレクション用にレジストリを用意しています。</span><span class="sxs-lookup"><span data-stu-id="3d492-110">Docker maintains a public registry via [Docker Hub](https://hub.docker.com/); other vendors provide registries for different collections of images.</span></span> <span data-ttu-id="3d492-111">また、企業は自社の Docker イメージ用に非公開のレジストリをオンプレミスに持つことができます。</span><span class="sxs-lookup"><span data-stu-id="3d492-111">Alternatively, enterprises can have a private registry on-premises for their own Docker images.</span></span>

<span data-ttu-id="3d492-112">図 1-4 は、他のコンポーネントにイメージと Docker でレジストリを関連付ける方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3d492-112">Figure 1-4 shows how images and registries in Docker relate to other components.</span></span> <span data-ttu-id="3d492-113">また、ベンダーから提供される複数のレジストリも示しています。</span><span class="sxs-lookup"><span data-stu-id="3d492-113">It also shows the multiple registry offerings from vendors.</span></span>

![](./media/image4.png)

<span data-ttu-id="3d492-114">図 1-4:Docker の用語と概念の分類</span><span class="sxs-lookup"><span data-stu-id="3d492-114">Figure 1-4: Taxonomy of Docker terms and concepts</span></span>

<span data-ttu-id="3d492-115">レジストリにイメージを配置する、フレームワーク レベルの依存関係のすべてを含む、静的で不変アプリケーション ビットを格納できます。</span><span class="sxs-lookup"><span data-stu-id="3d492-115">By putting images in a registry, you can store static and immutable application bits, including all of their dependencies, at a framework level.</span></span> <span data-ttu-id="3d492-116">バージョンことができますと複数の環境でイメージを展開し、したがって一貫した展開ユニットを提供します。</span><span class="sxs-lookup"><span data-stu-id="3d492-116">You then can version and deploy images in multiple environments and thus provide a consistent deployment unit.</span></span>

<span data-ttu-id="3d492-117">プライベート イメージ レジストリは、オンプレミスでホストされているか、クラウドでは、次の状況をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3d492-117">Private image registries, either hosted on-premises or in the cloud, are recommended for the following situations:</span></span>

-   <span data-ttu-id="3d492-118">機密保持のためにイメージを一般公開して共有することができない場合。</span><span class="sxs-lookup"><span data-stu-id="3d492-118">Your images must not be shared publicly due to confidentiality.</span></span>

-   <span data-ttu-id="3d492-119">イメージと選択した展開環境間のネットワーク待機時間を最小限に抑えたい場合。</span><span class="sxs-lookup"><span data-stu-id="3d492-119">You want to have minimum network latency between your images and your chosen deployment environment.</span></span> <span data-ttu-id="3d492-120">など、実稼働環境が Azure の場合は、おそらくするネットワーク待機時間が最小限になるように、Azure Container Registry にイメージを保存します。</span><span class="sxs-lookup"><span data-stu-id="3d492-120">For example, if your production environment is Azure, you probably want to store your images in Azure Container Registry so that network latency will be minimal.</span></span> <span data-ttu-id="3d492-121">同様に、実稼働環境がオンプレミスの場合は、同じローカル ネットワーク内でオンプレミスの Docker Trusted Registry を使用できるようにする方法があります。</span><span class="sxs-lookup"><span data-stu-id="3d492-121">In a similar way, if your production environment is on-premises, you might want to have an on-premises Docker Trusted Registry available within the same local network.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="3d492-122">[前へ](docker-terminology.md)
>[次へ](road-to-modern-applications-based-on-containers.md)</span><span class="sxs-lookup"><span data-stu-id="3d492-122">[Previous](docker-terminology.md)
[Next](road-to-modern-applications-based-on-containers.md)</span></span>
