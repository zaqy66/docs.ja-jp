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
# <a name="architecture-approaches"></a><span data-ttu-id="b6ae2-103">アーキテクチャのアプローチ</span><span class="sxs-lookup"><span data-stu-id="b6ae2-103">Architecture approaches</span></span>

<span data-ttu-id="b6ae2-104">エンタープライズ アプリの設計に既存のアプローチを理解するのに役立ちますはサーバーレスが果たす役割を明確にすることにします。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-104">Understanding existing approaches to architecting enterprise apps helps clarify the role played by serverless.</span></span> <span data-ttu-id="b6ae2-105">多くの方法や、ソフトウェア開発の数十年にわたって進化してパターンが存在し、独自の長所と短所があるすべて。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-105">There are many approaches and patterns that evolved over decades of software development, and all have their own pros and cons.</span></span> <span data-ttu-id="b6ae2-106">多くの場合、究極のソリューションは 1 つのアプローチを決定する必要がありますされませんが、いくつかのアプローチを統合することがあります。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-106">In many cases, the ultimate solution may not involve deciding on a single approach but may integrate several approaches.</span></span> <span data-ttu-id="b6ae2-107">移行シナリオには、多くの場合、1 つのアーキテクチャ アプローチからハイブリッド アプローチを通じて別に移行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-107">Migration scenarios often involve shifting from one architecture approach to another through a hybrid approach.</span></span>

<span data-ttu-id="b6ae2-108">この章では、エンタープライズ アプリケーションの両方の論理および物理アーキテクチャ パターンの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-108">This chapter provides an overview of both logical and physical architecture patterns for enterprise applications.</span></span>

## <a name="architecture-patterns"></a><span data-ttu-id="b6ae2-109">アーキテクチャ パターン</span><span class="sxs-lookup"><span data-stu-id="b6ae2-109">Architecture patterns</span></span>

<span data-ttu-id="b6ae2-110">最新のビジネス アプリケーションでは、さまざまなアーキテクチャ パターンに従います。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-110">Modern business applications follow a variety of architecture patterns.</span></span> <span data-ttu-id="b6ae2-111">このセクションでは、一般的なパターンの調査を表します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-111">This section represents a survey of common patterns.</span></span> <span data-ttu-id="b6ae2-112">ここで示したパターンでは、必ずしもすべてのベスト プラクティスはありませんが、さまざまな方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-112">The patterns listed here aren't necessarily all best practices, but illustrate different approaches.</span></span>

<span data-ttu-id="b6ae2-113">詳細については、次を参照してください。 [Azure アプリケーション アーキテクチャ ガイド](https://docs.microsoft.com/azure/architecture/guide/)します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-113">For more information, see [Azure application architecture guide](https://docs.microsoft.com/azure/architecture/guide/).</span></span>

## <a name="monoliths"></a><span data-ttu-id="b6ae2-114">モノリス</span><span class="sxs-lookup"><span data-stu-id="b6ae2-114">Monoliths</span></span>

<span data-ttu-id="b6ae2-115">多くのビジネス アプリケーションでは、モノリス パターンに従います。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-115">Many business applications follow a monolith pattern.</span></span> <span data-ttu-id="b6ae2-116">多くの場合、レガシ アプリケーションは、モノリスとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-116">Legacy applications are often implemented as monoliths.</span></span> <span data-ttu-id="b6ae2-117">モノリシック パターンでは、すべてのアプリケーションの問題は、1 つの配置に格納されます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-117">In the monolith pattern, all application concerns are contained in a single deployment.</span></span> <span data-ttu-id="b6ae2-118">同じコードベースにはデータベース呼び出しをユーザー インターフェイスからすべてのものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-118">Everything from user interface to database calls is included in the same codebase.</span></span>

![モノリシック アーキテクチャ](./media/monolith-architecture.png)

<span data-ttu-id="b6ae2-120">モノリシック アプローチをいくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-120">There are several advantages to the monolith approach.</span></span> <span data-ttu-id="b6ae2-121">1 つのコード ベースをプルし、作業開始することがよくあります。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-121">It's often easy to pull down a single code base and start working.</span></span> <span data-ttu-id="b6ae2-122">ランプ アップ時間は、小さい可能性があり、新しいコピーを提供するだけでは、テスト環境を作成します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-122">Ramp up time may be less, and creating test environments is as simple as providing a new copy.</span></span> <span data-ttu-id="b6ae2-123">複数のコンポーネントとアプリケーションを含む、モノリスを設計することがあります。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-123">The monolith may be designed to include multiple components and applications.</span></span>

<span data-ttu-id="b6ae2-124">残念ながら、モノリシック パターンは、大規模に分類する傾向があります。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-124">Unfortunately, the monolith pattern tends to break down at scale.</span></span> <span data-ttu-id="b6ae2-125">モノリシック アプローチの大きな欠点は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-125">Major disadvantages of the monolith approach include:</span></span>

* <span data-ttu-id="b6ae2-126">同じコード ベースで並列処理が難しくなっています。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-126">Difficult to work in parallel in the same code base.</span></span>
* <span data-ttu-id="b6ae2-127">どのように簡単に関係なく、任意の変更は、アプリケーション全体の新しいバージョンを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-127">Any change, no matter how trivial, requires deploying a new version of the entire application.</span></span>
* <span data-ttu-id="b6ae2-128">リファクタリングの可能性がある、アプリケーション全体に影響します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-128">Refactoring potentially impacts the entire application.</span></span>
* <span data-ttu-id="b6ae2-129">スケールする唯一のソリューションは複数作成する、多くの場合、モノリスのコピーをリソースを消費します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-129">Often the only solution to scale is to create multiple, resource-intensive copies of the monolith.</span></span>
* <span data-ttu-id="b6ae2-130">システムを展開するか、またはその他のシステムは、取得、統合が難しいことができます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-130">As systems expand or other systems are acquired, integration can be difficult.</span></span>
* <span data-ttu-id="b6ae2-131">全体のモノリスを構成する必要性のためのテストが難しいことがあります。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-131">It may be difficult to test due to the need to configure the entire monolith.</span></span>
* <span data-ttu-id="b6ae2-132">コードの再利用が困難と多くの場合、その他のアプリが最終的にコードの独自のコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-132">Code reuse is challenging and often other apps end up having their own copies of code.</span></span>

<span data-ttu-id="b6ae2-133">多くの企業は、クラウドにモノリシック アプリケーションを移行し、同時に利用可能なパターンの詳細にそれらをリファクターするチャンスとなります。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-133">Many businesses look to the cloud as an opportunity to migrate monolith applications and at the same time refactor them to more usable patterns.</span></span> <span data-ttu-id="b6ae2-134">管理、展開、およびを個別にスケーリングするためには、個々 のアプリケーションとコンポーネントを一般的です。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-134">It's common to break out the individual applications and components to allow them to be maintained, deployed, and scaled separately.</span></span>

## <a name="n-layer-applications"></a><span data-ttu-id="b6ae2-135">N 層アプリケーション</span><span class="sxs-lookup"><span data-stu-id="b6ae2-135">N-Layer applications</span></span>

<span data-ttu-id="b6ae2-136">N 層アプリケーションの特定のレイヤーにアプリケーション ロジックをパーティション。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-136">N-layer application partition application logic into specific layers.</span></span> <span data-ttu-id="b6ae2-137">最も一般的なレイヤーは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-137">The most common layers include:</span></span>

* <span data-ttu-id="b6ae2-138">[ユーザー インターフェイス]</span><span class="sxs-lookup"><span data-stu-id="b6ae2-138">User interface</span></span>
* <span data-ttu-id="b6ae2-139">ビジネス ロジック</span><span class="sxs-lookup"><span data-stu-id="b6ae2-139">Business logic</span></span>
* <span data-ttu-id="b6ae2-140">データ アクセス</span><span class="sxs-lookup"><span data-stu-id="b6ae2-140">Data access</span></span>

<span data-ttu-id="b6ae2-141">他のレイヤーには、ミドルウェア、バッチ処理、および API を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-141">Other layers may include middleware, batch processing, and API.</span></span> <span data-ttu-id="b6ae2-142">レイヤーは論理的に注意して重要です。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-142">It's important to note the layers are logical.</span></span> <span data-ttu-id="b6ae2-143">分離で開発する、ですが、すべて展開することが、同じターゲット プラットフォーム。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-143">Although they're developed in isolation, they may all be deployed to the same target platform.</span></span>

![N 層アーキテクチャ](./media/n-layer-architecture.png)

<span data-ttu-id="b6ae2-145">N 層のアプローチをいくつかの利点があるなど。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-145">There are several advantages to the N-Layer approach, including:</span></span>

* <span data-ttu-id="b6ae2-146">リファクタリングは、レイヤーに分離されます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-146">Refactoring is isolated to a layer.</span></span>
* <span data-ttu-id="b6ae2-147">チームできます個別にビルド、テスト、展開、および別のレイヤーを維持します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-147">Teams can independently build, test, deploy, and maintain separate layers.</span></span>
* <span data-ttu-id="b6ae2-148">レイヤーをスワップ アウト、たとえば、データ層は UI レイヤーに変更することがなく複数のデータベースをアクセス可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-148">Layers can be swapped out, for example the data layer may access multiple databases without requiring changes to the UI layer.</span></span>

<span data-ttu-id="b6ae2-149">サーバーレスは、1 つまたは複数のレイヤーを実装するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-149">Serverless may be used to implement one or more layers.</span></span>

## <a name="microservices"></a><span data-ttu-id="b6ae2-150">マイクロサービス</span><span class="sxs-lookup"><span data-stu-id="b6ae2-150">Microservices</span></span>

<span data-ttu-id="b6ae2-151">**[マイクロ サービス](https://docs.microsoft.com/azure/architecture/guide/architecture-styles/microservices)** アーキテクチャが含まれる共通の特徴を含みます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-151">**[Microservices](https://docs.microsoft.com/azure/architecture/guide/architecture-styles/microservices)** architectures contain common characteristics that include:</span></span>

* <span data-ttu-id="b6ae2-152">アプリケーションは、いくつかの小さなサービスで構成されます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-152">Applications are composed of several small services.</span></span>
* <span data-ttu-id="b6ae2-153">各サービスは、独自のプロセスで実行されます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-153">Each service runs in its own process.</span></span>
* <span data-ttu-id="b6ae2-154">サービスは、ビジネス ドメインの周囲に配置されます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-154">Services are aligned around business domains.</span></span>
* <span data-ttu-id="b6ae2-155">サービスは、通常、トランスポートとして HTTP を使用して軽量の Api 経由で通信します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-155">Services communicate over lightweight APIs, typically using HTTP as the transport.</span></span>
* <span data-ttu-id="b6ae2-156">サービスのデプロイし、は個別にアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-156">Services can be deployed and upgraded independently.</span></span>
* <span data-ttu-id="b6ae2-157">サービスが 1 つのデータ ストアに依存します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-157">Services aren't dependent on a single data store.</span></span>
* <span data-ttu-id="b6ae2-158">システムはエラーを考慮して設計されていて、アプリには、特定のサービスが失敗する場合でも引き続きを実行できます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-158">The system is designed with failure in mind, and the app may still run even when certain services fail.</span></span>

<span data-ttu-id="b6ae2-159">マイクロ サービスは、他のアーキテクチャのアプローチを相互に排他的にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-159">Microservices don't have to be mutually exclusive to other architecture approaches.</span></span> <span data-ttu-id="b6ae2-160">たとえば、N 層アーキテクチャでは、中間層のマイクロ サービスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-160">For example, an N-Tier architecture may use microservices for the middle tier.</span></span> <span data-ttu-id="b6ae2-161">さまざまなコンテナーに IIS ホスト上の仮想ディレクトリからの方法でマイクロ サービスを実装することもできます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-161">It's also possible to implement microservices in a variety of ways, from virtual directories on IIS hosts to containers.</span></span> <span data-ttu-id="b6ae2-162">マイクロ サービスの特性となってサーバーレスの実装に特に適しています。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-162">The characteristics of microservices make them especially ideal for serverless implementations.</span></span>

![マイクロサービス アーキテクチャ](./media/microservices-architecture.png)

<span data-ttu-id="b6ae2-164">マイクロ サービス アーキテクチャの利点は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-164">The pros of microservices architectures include:</span></span>

* <span data-ttu-id="b6ae2-165">リファクタリングは、1 つのサービスに分離では多くの場合です。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-165">Refactoring is often isolated to a single service.</span></span>
* <span data-ttu-id="b6ae2-166">サービスは、それぞれ個別にアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-166">Services can be upgraded independently of each other.</span></span>
* <span data-ttu-id="b6ae2-167">回復性と弾力性は、個々 のサービスのニーズに合わせて調整できます。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-167">Resiliency and elasticity can be tuned to the demands of individual services.</span></span>
* <span data-ttu-id="b6ae2-168">開発がさまざまなチームおよびプラットフォーム間で並列に発生します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-168">Development can happen in parallel across disparate teams and platforms.</span></span>
* <span data-ttu-id="b6ae2-169">分離サービスの包括的なテストを記述しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-169">It's easier to write comprehensive tests for isolated services.</span></span>

<span data-ttu-id="b6ae2-170">マイクロ サービスなど、独自の課題が付属します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-170">Microservices come with their own challenges, including:</span></span>

* <span data-ttu-id="b6ae2-171">どのようなサービスを利用し、これらを呼び出す方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-171">Determining what services are available and how to call them.</span></span>
* <span data-ttu-id="b6ae2-172">サービスのライフ サイクルを管理します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-172">Managing the lifecycle of services.</span></span>
* <span data-ttu-id="b6ae2-173">サービスをまとめる方法でアプリケーション全体について理解します。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-173">Understanding how services fit together in the overall application.</span></span>
* <span data-ttu-id="b6ae2-174">完全なシステムは、異なるサービス間で行われた呼び出しのテスト。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-174">Full system testing of calls made across disparate services.</span></span>

<span data-ttu-id="b6ae2-175">最終的には、すべての後で説明するサーバーレスのメリットを利用することを含め、これらの課題に対応するソリューションがあります。</span><span class="sxs-lookup"><span data-stu-id="b6ae2-175">Ultimately there are solutions to address all of these challenges, including tapping into the benefits of serverless that are discussed later.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="b6ae2-176">[前へ](index.md)
>[次へ](architecture-deployment-approaches.md)</span><span class="sxs-lookup"><span data-stu-id="b6ae2-176">[Previous](index.md)
[Next](architecture-deployment-approaches.md)</span></span>