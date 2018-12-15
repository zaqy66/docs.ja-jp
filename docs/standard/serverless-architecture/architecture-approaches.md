---
title: サーバーレス アプリのアーキテクチャ アプローチ
description: アーキテクチャの概要については、サーバーレスに N 層アーキテクチャからのクラウド ベースのエンタープライズ アプリケーションを構築するために近くなります。
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: 04ad383586f974bb2dccc4623a9a254f5668dab4
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53126746"
---
# <a name="architecture-approaches"></a><span data-ttu-id="d1f0b-103">アーキテクチャのアプローチ</span><span class="sxs-lookup"><span data-stu-id="d1f0b-103">Architecture approaches</span></span>

<span data-ttu-id="d1f0b-104">エンタープライズ アプリの設計に既存のアプローチを理解するのに役立ちますはサーバーレスが果たす役割を明確にすることにします。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-104">Understanding existing approaches to architecting enterprise apps helps clarify the role played by serverless.</span></span> <span data-ttu-id="d1f0b-105">多くの方法や、ソフトウェア開発の数十年にわたって進化してパターンが存在し、独自の長所と短所があるすべて。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-105">There are many approaches and patterns that evolved over decades of software development, and all have their own pros and cons.</span></span> <span data-ttu-id="d1f0b-106">多くの場合、究極のソリューションは 1 つのアプローチを決定する必要がありますされませんが、いくつかのアプローチを統合することがあります。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-106">In many cases, the ultimate solution may not involve deciding on a single approach but may integrate several approaches.</span></span> <span data-ttu-id="d1f0b-107">移行シナリオには、多くの場合、1 つのアーキテクチャ アプローチからハイブリッド アプローチを通じて別に移行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-107">Migration scenarios often involve shifting from one architecture approach to another through a hybrid approach.</span></span>

<span data-ttu-id="d1f0b-108">この章では、エンタープライズ アプリケーションの両方の論理および物理アーキテクチャ パターンの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-108">This chapter provides an overview of both logical and physical architecture patterns for enterprise applications.</span></span>

## <a name="architecture-patterns"></a><span data-ttu-id="d1f0b-109">アーキテクチャーパターン</span><span class="sxs-lookup"><span data-stu-id="d1f0b-109">Architecture patterns</span></span>

<span data-ttu-id="d1f0b-110">最新のビジネスアプリケーションは、さまざまなアーキテクチャーパターンに従っています。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-110">Modern business applications follow a variety of architecture patterns.</span></span> <span data-ttu-id="d1f0b-111">このセクションでは、一般的なパターンの調査を表します。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-111">This section represents a survey of common patterns.</span></span> <span data-ttu-id="d1f0b-112">ここで示したパターンでは、必ずしもすべてのベストプラクティスはありませんが、さまざまな方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-112">The patterns listed here aren't necessarily all best practices, but illustrate different approaches.</span></span>

<span data-ttu-id="d1f0b-113">詳細については、次を参照してください。 [Azure アプリケーション アーキテクチャ ガイド](https://docs.microsoft.com/azure/architecture/guide/)します。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-113">For more information, see [Azure application architecture guide](https://docs.microsoft.com/azure/architecture/guide/).</span></span>

## <a name="monoliths"></a><span data-ttu-id="d1f0b-114">モノリス</span><span class="sxs-lookup"><span data-stu-id="d1f0b-114">Monoliths</span></span>

<span data-ttu-id="d1f0b-115">多くのビジネスアプリケーションは、モノリスパターンに従っています。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-115">Many business applications follow a monolith pattern.</span></span> <span data-ttu-id="d1f0b-116">レガシーアプリケーションは、モノリスに実装されていることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-116">Legacy applications are often implemented as monoliths.</span></span> <span data-ttu-id="d1f0b-117">モノリスパターンでは、アプリケーションが1つのデプロイに含まれていることが問題です。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-117">In the monolith pattern, all application concerns are contained in a single deployment.</span></span> <span data-ttu-id="d1f0b-118">データベースの呼び出しからユーザーインターフェースまですべてが、同じコードベースに含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-118">Everything from user interface to database calls is included in the same codebase.</span></span>

![モノリシック アーキテクチャ](./media/monolith-architecture.png)

<span data-ttu-id="d1f0b-120">モノリスのアプローチにもいくつかの利点はあります。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-120">There are several advantages to the monolith approach.</span></span> <span data-ttu-id="d1f0b-121">1つのコードベースをプルして作業を開始するのは簡単です。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-121">It's often easy to pull down a single code base and start working.</span></span> <span data-ttu-id="d1f0b-122">構築時間は短縮され、テスト環境の作成は新しいコピーを提供するのと同じくらいシンプルです。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-122">Ramp up time may be less, and creating test environments is as simple as providing a new copy.</span></span> <span data-ttu-id="d1f0b-123">モノリスは、複数のコンポーネントまたはアプリケーションを含むように設計されています。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-123">The monolith may be designed to include multiple components and applications.</span></span>

<span data-ttu-id="d1f0b-124">残念なことに、モノリスパターンはスケールで破綻する傾向があります。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-124">Unfortunately, the monolith pattern tends to break down at scale.</span></span> <span data-ttu-id="d1f0b-125">モノリスのアプローチの主な欠点は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-125">Major disadvantages of the monolith approach include:</span></span>

* <span data-ttu-id="d1f0b-126">同じコードベースで並列して作業するのは困難</span><span class="sxs-lookup"><span data-stu-id="d1f0b-126">Difficult to work in parallel in the same code base.</span></span>
* <span data-ttu-id="d1f0b-127">どんな些細な変更でも、アプリケーション全体を新しいバージョンにデプロイする必要がある</span><span class="sxs-lookup"><span data-stu-id="d1f0b-127">Any change, no matter how trivial, requires deploying a new version of the entire application.</span></span>
* <span data-ttu-id="d1f0b-128">リファクタリングは、潜在的にアプリケーション全体に影響を及ぼす</span><span class="sxs-lookup"><span data-stu-id="d1f0b-128">Refactoring potentially impacts the entire application.</span></span>
* <span data-ttu-id="d1f0b-129">多くの場合、スケールする唯一のソリューションは、リソースが集約されたモノリスのコピーを複数作ることです。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-129">Often the only solution to scale is to create multiple, resource-intensive copies of the monolith.</span></span>
* <span data-ttu-id="d1f0b-130">システムの拡張や他システムとの結合といったインテグレーションは難しい可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-130">As systems expand or other systems are acquired, integration can be difficult.</span></span>
* <span data-ttu-id="d1f0b-131">テストは、モノリス全体の構成をする必要があるため難しい可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-131">It may be difficult to test due to the need to configure the entire monolith.</span></span>
* <span data-ttu-id="d1f0b-132">コードの再利用は困難であり、多くの場合、他のアプリは元のコードのコピーを持つことになります。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-132">Code reuse is challenging and often other apps end up having their own copies of code.</span></span>

<span data-ttu-id="d1f0b-133">多くの企業は、モノリスのアプリケーションを移行する機会としてクラウドに注目し、同時により有用なパターンにリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-133">Many businesses look to the cloud as an opportunity to migrate monolith applications and at the same time refactor them to more usable patterns.</span></span> <span data-ttu-id="d1f0b-134">個々のアプリケーションやコンポーネントを切り離して、個別に保守、デプロイ、およびスケーリングできるようにするのが一般的です。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-134">It's common to break out the individual applications and components to allow them to be maintained, deployed, and scaled separately.</span></span>

## <a name="n-layer-applications"></a><span data-ttu-id="d1f0b-135">N 層アプリケーション</span><span class="sxs-lookup"><span data-stu-id="d1f0b-135">N-Layer applications</span></span>

<span data-ttu-id="d1f0b-136">N 層アプリケーションの特定のレイヤーにアプリケーション ロジックをパーティション。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-136">N-layer application partition application logic into specific layers.</span></span> <span data-ttu-id="d1f0b-137">最も一般的なレイヤーは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-137">The most common layers include:</span></span>

* <span data-ttu-id="d1f0b-138">[ユーザー インターフェイス]</span><span class="sxs-lookup"><span data-stu-id="d1f0b-138">User interface</span></span>
* <span data-ttu-id="d1f0b-139">ビジネス ロジック</span><span class="sxs-lookup"><span data-stu-id="d1f0b-139">Business logic</span></span>
* <span data-ttu-id="d1f0b-140">データ アクセス</span><span class="sxs-lookup"><span data-stu-id="d1f0b-140">Data access</span></span>

<span data-ttu-id="d1f0b-141">他のレイヤーには、ミドルウェア、バッチ処理、および API を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-141">Other layers may include middleware, batch processing, and API.</span></span> <span data-ttu-id="d1f0b-142">レイヤーは論理的に注意して重要です。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-142">It's important to note the layers are logical.</span></span> <span data-ttu-id="d1f0b-143">分離で開発する、ですが、すべて展開することが、同じターゲット プラットフォーム。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-143">Although they're developed in isolation, they may all be deployed to the same target platform.</span></span>

![N 層アーキテクチャ](./media/n-layer-architecture.png)

<span data-ttu-id="d1f0b-145">N 層のアプローチをいくつかの利点があるなど。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-145">There are several advantages to the N-Layer approach, including:</span></span>

* <span data-ttu-id="d1f0b-146">リファクタリングは、レイヤーに分離されます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-146">Refactoring is isolated to a layer.</span></span>
* <span data-ttu-id="d1f0b-147">チームできます個別にビルド、テスト、展開、および別のレイヤーを維持します。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-147">Teams can independently build, test, deploy, and maintain separate layers.</span></span>
* <span data-ttu-id="d1f0b-148">レイヤーをスワップ アウト、たとえば、データ層は UI レイヤーに変更することがなく複数のデータベースをアクセス可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-148">Layers can be swapped out, for example the data layer may access multiple databases without requiring changes to the UI layer.</span></span>

<span data-ttu-id="d1f0b-149">サーバーレスは、1 つまたは複数のレイヤーを実装するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-149">Serverless may be used to implement one or more layers.</span></span>

## <a name="microservices"></a><span data-ttu-id="d1f0b-150">マイクロサービス</span><span class="sxs-lookup"><span data-stu-id="d1f0b-150">Microservices</span></span>

<span data-ttu-id="d1f0b-151">**[マイクロ サービス](https://docs.microsoft.com/azure/architecture/guide/architecture-styles/microservices)** アーキテクチャが含まれる共通の特徴を含みます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-151">**[Microservices](https://docs.microsoft.com/azure/architecture/guide/architecture-styles/microservices)** architectures contain common characteristics that include:</span></span>

* <span data-ttu-id="d1f0b-152">アプリケーションは、いくつかの小さなサービスで構成されます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-152">Applications are composed of several small services.</span></span>
* <span data-ttu-id="d1f0b-153">各サービスは、独自のプロセスで実行されます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-153">Each service runs in its own process.</span></span>
* <span data-ttu-id="d1f0b-154">サービスは、ビジネス ドメインの周囲に配置されます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-154">Services are aligned around business domains.</span></span>
* <span data-ttu-id="d1f0b-155">サービスは、通常、トランスポートとして HTTP を使用して軽量の Api 経由で通信します。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-155">Services communicate over lightweight APIs, typically using HTTP as the transport.</span></span>
* <span data-ttu-id="d1f0b-156">サービスのデプロイし、は個別にアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-156">Services can be deployed and upgraded independently.</span></span>
* <span data-ttu-id="d1f0b-157">サービスが 1 つのデータ ストアに依存します。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-157">Services aren't dependent on a single data store.</span></span>
* <span data-ttu-id="d1f0b-158">システムはエラーを考慮して設計されていて、アプリには、特定のサービスが失敗する場合でも引き続きを実行できます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-158">The system is designed with failure in mind, and the app may still run even when certain services fail.</span></span>

<span data-ttu-id="d1f0b-159">マイクロ サービスは、他のアーキテクチャのアプローチを相互に排他的にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-159">Microservices don't have to be mutually exclusive to other architecture approaches.</span></span> <span data-ttu-id="d1f0b-160">たとえば、N 層アーキテクチャでは、中間層のマイクロ サービスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-160">For example, an N-Tier architecture may use microservices for the middle tier.</span></span> <span data-ttu-id="d1f0b-161">さまざまなコンテナーに IIS ホスト上の仮想ディレクトリからの方法でマイクロ サービスを実装することもできます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-161">It's also possible to implement microservices in a variety of ways, from virtual directories on IIS hosts to containers.</span></span> <span data-ttu-id="d1f0b-162">マイクロ サービスの特性となってサーバーレスの実装に特に適しています。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-162">The characteristics of microservices make them especially ideal for serverless implementations.</span></span>

![マイクロサービス アーキテクチャ](./media/microservices-architecture.png)

<span data-ttu-id="d1f0b-164">マイクロ サービス アーキテクチャの利点は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-164">The pros of microservices architectures include:</span></span>

* <span data-ttu-id="d1f0b-165">リファクタリングは、1 つのサービスに分離では多くの場合です。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-165">Refactoring is often isolated to a single service.</span></span>
* <span data-ttu-id="d1f0b-166">サービスは、それぞれ個別にアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-166">Services can be upgraded independently of each other.</span></span>
* <span data-ttu-id="d1f0b-167">回復性と弾力性は、個々 のサービスのニーズに合わせて調整できます。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-167">Resiliency and elasticity can be tuned to the demands of individual services.</span></span>
* <span data-ttu-id="d1f0b-168">開発がさまざまなチームおよびプラットフォーム間で並列に発生します。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-168">Development can happen in parallel across disparate teams and platforms.</span></span>
* <span data-ttu-id="d1f0b-169">分離サービスの包括的なテストを記述しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-169">It's easier to write comprehensive tests for isolated services.</span></span>

<span data-ttu-id="d1f0b-170">マイクロ サービスなど、独自の課題が付属します。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-170">Microservices come with their own challenges, including:</span></span>

* <span data-ttu-id="d1f0b-171">どのようなサービスを利用し、これらを呼び出す方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-171">Determining what services are available and how to call them.</span></span>
* <span data-ttu-id="d1f0b-172">サービスのライフ サイクルを管理します。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-172">Managing the lifecycle of services.</span></span>
* <span data-ttu-id="d1f0b-173">サービスをまとめる方法でアプリケーション全体について理解します。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-173">Understanding how services fit together in the overall application.</span></span>
* <span data-ttu-id="d1f0b-174">完全なシステムは、異なるサービス間で行われた呼び出しのテスト。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-174">Full system testing of calls made across disparate services.</span></span>

<span data-ttu-id="d1f0b-175">最終的には、すべての後で説明するサーバーレスのメリットを利用することを含め、これらの課題に対応するソリューションがあります。</span><span class="sxs-lookup"><span data-stu-id="d1f0b-175">Ultimately there are solutions to address all of these challenges, including tapping into the benefits of serverless that are discussed later.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="d1f0b-176">[前へ](index.md)
>[次へ](architecture-deployment-approaches.md)</span><span class="sxs-lookup"><span data-stu-id="d1f0b-176">[Previous](index.md)
[Next](architecture-deployment-approaches.md)</span></span>