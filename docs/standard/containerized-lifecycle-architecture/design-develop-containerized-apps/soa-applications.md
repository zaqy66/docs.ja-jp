---
title: SOA アプリケーション
description: コンテナーが SOA アプリケーションの配置オプションもあることに注意してください。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 353ba738143b7dcd92c7c75ac27ea6a7370f9da6
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/23/2019
ms.locfileid: "56745834"
---
# <a name="service-oriented-applications"></a><span data-ttu-id="9bb29-103">サービス指向アプリケーション</span><span class="sxs-lookup"><span data-stu-id="9bb29-103">Service-oriented applications</span></span>

<span data-ttu-id="9bb29-104">サービス指向アーキテクチャ (SOA) は、人によって異なる、さまざまなものの過剰使用されている用語をしました。</span><span class="sxs-lookup"><span data-stu-id="9bb29-104">Service-Oriented Architecture (SOA) was an overused term that meant many different things to different people.</span></span> <span data-ttu-id="9bb29-105">しかし、SOA がサブシステムなど、さまざまな種類にまたは他の場合、階層として分類できる (通常 HTTP サービス) としていくつかのサービスに分解して、アプリケーションのアーキテクチャを構築することを意味、共通の基準として。</span><span class="sxs-lookup"><span data-stu-id="9bb29-105">But as a common denominator, SOA means that you structure the architecture of your application by decomposing it into several services (most commonly as HTTP services) that can be classified in different types like subsystems or, in other cases, as tiers.</span></span>

<span data-ttu-id="9bb29-106">今日では、コンテナー イメージの依存関係すべて含まれているため、展開に関連する問題を解決する Docker コンテナーとしてそれらのサービスをデプロイできます。</span><span class="sxs-lookup"><span data-stu-id="9bb29-106">Today, you can deploy those services as Docker containers, which solve deployment-related issues because all of the dependencies are included in the container image.</span></span> <span data-ttu-id="9bb29-107">ただし、Soa を拡大する必要がある場合、そのに基づいて 1 つのインスタンスを展開する場合の課題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9bb29-107">However, when you need to scale out SOAs, you might encounter challenges if you are deploying based on single instances.</span></span> <span data-ttu-id="9bb29-108">この課題は、Docker クラスタ リング ソフトウェアまたはオーケストレーターを使用して処理できます。</span><span class="sxs-lookup"><span data-stu-id="9bb29-108">This challenge can be handled using Docker clustering software or an orchestrator.</span></span> <span data-ttu-id="9bb29-109">マイクロ サービス アプローチについて説明している場合、次のセクションで詳しくオーケストレーターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9bb29-109">We'll look at orchestrators in greater detail in the next section, when we explore microservices approaches.</span></span>

<span data-ttu-id="9bb29-110">Docker コンテナーは、従来のサービス指向アーキテクチャと高度なマイクロサービス アーキテクチャの両方にとって便利な機能です (ただし、必須ではありません)。</span><span class="sxs-lookup"><span data-stu-id="9bb29-110">Docker containers are useful (but not required) for both traditional service-oriented architectures and the more advanced microservices architectures.</span></span>

<span data-ttu-id="9bb29-111">1 日の終わりには、コンテナーのクラスタ リング ソリューションは、両方の従来の SOA アーキテクチャとマイクロ サービスごとにそのデータ モデルが所有するより高度なマイクロ サービス アーキテクチャに便利です。</span><span class="sxs-lookup"><span data-stu-id="9bb29-111">At the end of the day, the container clustering solutions are useful for both a traditional SOA architecture and for a more advanced microservices architecture in which each microservice owns its data model.</span></span> <span data-ttu-id="9bb29-112">複数のデータベースに協力してくれたもスケール アウトできます SOA サービスによって共有モノリシック データベースでの作業ではなく、データ層。</span><span class="sxs-lookup"><span data-stu-id="9bb29-112">And thanks to multiple databases, you also can scale out the data tier instead of working with monolithic databases shared by the SOA services.</span></span> <span data-ttu-id="9bb29-113">ただし、データの分割に関する議論は、アーキテクチャと設計についてのみです。</span><span class="sxs-lookup"><span data-stu-id="9bb29-113">However, the discussion about splitting the data is purely about architecture and design.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="9bb29-114">[前へ](state-and-data-in-docker-applications.md)
>[次へ](orchestrate-high-scalability-availability.md)</span><span class="sxs-lookup"><span data-stu-id="9bb29-114">[Previous](state-and-data-in-docker-applications.md)
[Next](orchestrate-high-scalability-availability.md)</span></span>
