---
title: SOA アプリケーション
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 7f88daaf0787cf780e7ab9602f35ae4e6ab8308c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53155315"
---
# <a name="soa-applications"></a><span data-ttu-id="f2e5b-103">SOA アプリケーション</span><span class="sxs-lookup"><span data-stu-id="f2e5b-103">SOA applications</span></span>

<span data-ttu-id="f2e5b-104">SOA が過剰使用されている用語を使用してを別々 の人は多くの異なる要素。</span><span class="sxs-lookup"><span data-stu-id="f2e5b-104">SOA was an overused term and meant so many different things to different people.</span></span> <span data-ttu-id="f2e5b-105">少なくとも、共通分母、SOA、またはサービス指向、平均 (最も一般的な HTTP サービス) としてさまざまな種類に分類できる複数のサービスに分解して、アプリケーションのアーキテクチャの構造をそのなどのサブシステムが、または、階層化とそれ以外の場合。</span><span class="sxs-lookup"><span data-stu-id="f2e5b-105">But at a minimum and as a common denominator, SOA, or service orientation, mean that you structure the architecture of your application by decomposing it in multiple services (most commonly as HTTP services) that can be classified in different types like subsystems or, in other cases, as tiers.</span></span>

<span data-ttu-id="f2e5b-106">今日では、コンテナー イメージに含まれるすべての依存関係のため、展開に関連する問題を解決する Docker コンテナーとしてそれらのサービスをデプロイできます。</span><span class="sxs-lookup"><span data-stu-id="f2e5b-106">Today, you can deploy those services as Docker containers, which solves deployment-related issues because all of the dependencies are included within the container image.</span></span> <span data-ttu-id="f2e5b-107">ただし、Soa のスケール アウトする必要がある場合、そのに基づいて 1 つのインスタンスを展開する場合の課題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f2e5b-107">However, when you need to scale-out SOAs, you might encounter challenges if you are deploying based on single instances.</span></span> <span data-ttu-id="f2e5b-108">これは、Docker クラスタ リング ソフトウェアまたはオーケストレーターが支援する場所です。</span><span class="sxs-lookup"><span data-stu-id="f2e5b-108">This is where a Docker clustering software or orchestrator will help you.</span></span> <span data-ttu-id="f2e5b-109">マイクロ サービス アプローチを調べるとき、次のセクションで詳しくこれを確認します。</span><span class="sxs-lookup"><span data-stu-id="f2e5b-109">We'll look at this in greater detail in the next section when we examine microservices approaches.</span></span>

<span data-ttu-id="f2e5b-110">1 日の終わりには、コンテナーのクラスタ リング ソリューションは、両方の従来の SOA アーキテクチャまたはマイクロ サービスごとにそのデータ モデルが所有するより高度なマイクロ サービス アーキテクチャに便利です。</span><span class="sxs-lookup"><span data-stu-id="f2e5b-110">At the end of the day, the container clustering solutions are useful for both a traditional SOA architecture or for a more advanced microservices architecture in which each microservice owns its data model.</span></span> <span data-ttu-id="f2e5b-111">また、複数のデータベースに協力してくれたもスケール アウトできる SOA サービスによって共有モノリシック データベースでの作業ではなく、データ層。</span><span class="sxs-lookup"><span data-stu-id="f2e5b-111">And, thanks to multiple databases, you also can scale-out the data tier instead of working with monolithic databases shared by the SOA services.</span></span> <span data-ttu-id="f2e5b-112">ただし、データの分割に関する議論は、アーキテクチャと設計についてのみです。</span><span class="sxs-lookup"><span data-stu-id="f2e5b-112">However, the discussion about splitting the data is purely about architecture and design.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="f2e5b-113">[前へ](state-and-data-in-docker-applications.md)
>[次へ](orchestrate-high-scalability-availability.md)</span><span class="sxs-lookup"><span data-stu-id="f2e5b-113">[Previous](state-and-data-in-docker-applications.md)
[Next](orchestrate-high-scalability-availability.md)</span></span>