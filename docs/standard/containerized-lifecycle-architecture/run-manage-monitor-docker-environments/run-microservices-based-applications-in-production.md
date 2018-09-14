---
title: 構成されるマイクロ サービス ベースのアプリケーションを運用環境で実行します。
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 18e6cb1fb5f496b66c89cb8e009a67894b8a76ad
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/13/2018
ms.locfileid: "45515900"
---
# <a name="run-composed-and-microservices-based-applications-in-production-environments"></a><span data-ttu-id="2243a-103">構成されるマイクロ サービス ベースのアプリケーションを運用環境で実行します。</span><span class="sxs-lookup"><span data-stu-id="2243a-103">Run composed and microservices-based applications in production environments</span></span>

<span data-ttu-id="2243a-104">複数のマイクロ サービスで構成されたアプリケーションは展開の複雑さを簡素化し、IT の観点から実行可能なようにするには orchestrator のクラスターをデプロイする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2243a-104">Applications composed by multiple microservices do need to be deployed into orchestrator clusters in order to simplify the complexity of deployment and make it viable from an IT point of view.</span></span> <span data-ttu-id="2243a-105">オーケストレーター クラスタなしは、デプロイおよびスケール アウト、複雑なマイクロ サービス アプリケーションに非常に困難ですがなります。</span><span class="sxs-lookup"><span data-stu-id="2243a-105">Without an orchestrator cluster, it would be very difficult to deploy and scale-out a complex microservices application.</span></span>

## <a name="introduction-to-orchestrators-schedulers-and-container-clusters"></a><span data-ttu-id="2243a-106">クラスターのオーケストレーター、スケジューラ、およびコンテナーの概要</span><span class="sxs-lookup"><span data-stu-id="2243a-106">Introduction to orchestrators, schedulers, and container clusters</span></span>

<span data-ttu-id="2243a-107">この電子書籍の前半で紹介*クラスター*と*スケジューラ*ソフトウェア アーキテクチャと開発についての説明の一部として。</span><span class="sxs-lookup"><span data-stu-id="2243a-107">Earlier in this e-book, we introduced *clusters* and *schedulers* as part of the discussion on software architecture and development.</span></span> <span data-ttu-id="2243a-108">Docker クラスターには、Docker Swarm、Mesosphere Datacenter Operating System (DC/OS) があります。</span><span class="sxs-lookup"><span data-stu-id="2243a-108">Examples of Docker clusters are Docker Swarm and Mesosphere Datacenter Operating System (DC/OS).</span></span> <span data-ttu-id="2243a-109">Microsoft Azure Container Service によって提供されるインフラストラクチャの一部としてこれらの両方を実行できます。</span><span class="sxs-lookup"><span data-stu-id="2243a-109">Both of these can run as a part of the infrastructure provided by Microsoft Azure Container Service.</span></span>

<span data-ttu-id="2243a-110">アプリケーションがスケール アウトされた複数のホスト システムで、各ホスト システムを管理し、基になるプラットフォームの複雑さを抽象化する機能は魅力的なものになります。</span><span class="sxs-lookup"><span data-stu-id="2243a-110">When applications are scaled-out across multiple host systems, the ability to manage each host system and abstract away the complexity of the underlying platform becomes attractive.</span></span> <span data-ttu-id="2243a-111">これがまさにオーケストレーターとスケジューラの提供内容です。</span><span class="sxs-lookup"><span data-stu-id="2243a-111">That is precisely what orchestrators and schedulers provide.</span></span> <span data-ttu-id="2243a-112">ここで見て簡単なを見てみましょう。</span><span class="sxs-lookup"><span data-stu-id="2243a-112">Let's take a brief look at them here:</span></span>

- <span data-ttu-id="2243a-113">**スケジューラ**。</span><span class="sxs-lookup"><span data-stu-id="2243a-113">**Schedulers**.</span></span><span data-ttu-id="2243a-114"> 「スケジュール」は、管理者が、特定のコンテナーを実行する方法を確立するホスト システムにサービス ファイルを読み込む機能を指します。</span><span class="sxs-lookup"><span data-stu-id="2243a-114"> "Scheduling" refers to the ability for an administrator to load a service file onto a host system that establishes how to run a specific container.</span></span> <span data-ttu-id="2243a-115">Docker クラスター内のコンテナーの起動は、スケジュール設定と呼ばれる傾向があります。</span><span class="sxs-lookup"><span data-stu-id="2243a-115">Launching containers in a Docker cluster tends to be known as scheduling.</span></span> <span data-ttu-id="2243a-116">一般的な意味で、サービス定義の読み込みの特定の動作を指しますスケジューリングのスケジューラはサービスに必要なすべての容量を管理するホストの init システムへのフッキング責任を負います。</span><span class="sxs-lookup"><span data-stu-id="2243a-116">Although scheduling refers to the specific act of loading the service definition, in a more general sense, schedulers are responsible for hooking into a host's init system to manage services in whatever capacity needed.</span></span>

   <span data-ttu-id="2243a-117">クラスター スケジューラは、複数の目標: クラスターのリソースを効率的に使用して、ユーザーが指定した配置の制約を使用して、「公平に見て、」エラーに堅牢な中の程度が保留中の状態のままにしない場合に迅速にアプリケーションをスケジュール設定を使用し、常に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2243a-117">A cluster scheduler has multiple goals: using the cluster's resources efficiently, working with user-supplied placement constraints, scheduling applications rapidly to not leave them in a pending state, having a degree of "fairness," being robust to errors, and always be available.</span></span>

- <span data-ttu-id="2243a-118">**オーケストレーション**します。</span><span class="sxs-lookup"><span data-stu-id="2243a-118">**Orchestration**.</span></span><span data-ttu-id="2243a-119"> プラットフォームでは、複雑な複数のコンテナー ワークロードをホストのクラスターに展開されているライフ サイクル管理機能を拡張します。</span><span class="sxs-lookup"><span data-stu-id="2243a-119"> Platforms extend life-cycle management capabilities to complex, multicontainer workloads deployed on a cluster of hosts.</span></span> <span data-ttu-id="2243a-120">ホスト インフラストラクチャを抽象化され、オーケストレーション ツールはユーザーをクラスター全体を 1 つの配置ターゲットとして扱う方法に付与します。</span><span class="sxs-lookup"><span data-stu-id="2243a-120">By abstracting the host infrastructure, orchestration tools give users a way to treat the entire cluster as a single deployment target.</span></span>

   <span data-ttu-id="2243a-121">オーケストレーションのプロセスには、ツールと初期配置またはコンテナーごとの展開からのアプリケーション管理のすべての側面を自動化できるプラットフォームが含まれます。コンテナーをそのホストの正常性やパフォーマンスに応じて異なるホストに移動します。バージョン管理とローリング更新プログラム、および正常性監視のスケーリングとフェールオーバーをサポートする関数その他</span><span class="sxs-lookup"><span data-stu-id="2243a-121">The process of orchestration involves tooling and a platform that can automate all aspects of application management from initial placement or deployment per container; moving containers to different hosts depending on its host's health or performance; versioning and rolling updates and health monitoring functions that support scaling and failover; and many more.</span></span>

   <span data-ttu-id="2243a-122">オーケストレーションは、広義の用語を参照するコンテナーのスケジュール設定、クラスター管理、およびその他のホストのプロビジョニング可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2243a-122">Orchestration is a broad term that refers to container scheduling, cluster management, and possibly the provisioning of additional hosts.</span></span>

<span data-ttu-id="2243a-123">開発し、最初から作成する非常に複雑なオーケストレーターとスケジューラによって提供される機能およびそのため、通常にするオーケストレーション ソリューションの使用がベンダーによって提供されています。</span><span class="sxs-lookup"><span data-stu-id="2243a-123">The capabilities provided by orchestrators and schedulers are very complex to develop and create from scratch, and therefore you usually would want to make use of orchestration solutions offered by vendors.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="2243a-124">[前へ](index.md)
[次へ](manage-production-docker-environments.md)</span><span class="sxs-lookup"><span data-stu-id="2243a-124">[Previous](index.md)
[Next](manage-production-docker-environments.md)</span></span>
