---
title: Docker アプリケーションを設計します。
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/21/2017
ms.openlocfilehash: d02cec0595024eb7bd7c0ac46df093359680da74
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53155380"
---
# <a name="design-docker-applications"></a><span data-ttu-id="9b29c-103">Docker アプリケーションを設計します。</span><span class="sxs-lookup"><span data-stu-id="9b29c-103">Design Docker applications</span></span>

<span data-ttu-id="9b29c-104">第 1 章には、コンテナーと Docker に関する基本的な概念が導入されました。</span><span class="sxs-lookup"><span data-stu-id="9b29c-104">Chapter 1 introduced the fundamental concepts regarding containers and Docker.</span></span> <span data-ttu-id="9b29c-105">その情報は、開始に必要な情報の基本的なレベルです。</span><span class="sxs-lookup"><span data-stu-id="9b29c-105">That information is the basic level of information you need to get started.</span></span> <span data-ttu-id="9b29c-106">ただし、1 つのサービスまたはコンテナーではなく複数のサービスで構成され、複雑なエンタープライズ アプリケーションを指定できます。</span><span class="sxs-lookup"><span data-stu-id="9b29c-106">But, enterprise applications can be complex and composed of multiple services instead of a single service or container.</span></span> <span data-ttu-id="9b29c-107">これらの省略可能なユース ケースでは、オーケストレーションの概念デザイン、サービス指向アーキテクチャ (SOA) より高度なマイクロ サービスの概念とコンテナーに追加の手法を把握する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b29c-107">For those optional use cases, you need to know additional approaches to design, such as Service-Oriented Architecture (SOA) and the more advanced microservices concepts and container orchestration concepts.</span></span> <span data-ttu-id="9b29c-108">このドキュメントのスコープはマイクロ サービスに限定されませんが、Docker アプリケーションのライフ サイクルそのため、ことはできませんを参照してくださいマイクロ サービス アーキテクチャの詳細も正規サンパウロ、バック グラウンド タスクまたはジョブ、コンテナーと Docker を使用したりもためモノリシック アプリケーション展開のアプローチです。</span><span class="sxs-lookup"><span data-stu-id="9b29c-108">The scope of this document is not limited to microservices but to any Docker application life cycle, therefore, it does not explore microservices architecture in depth because you also can use containers and Docker with regular SAO, background tasks or jobs, or even with monolithic application deployment approaches.</span></span>

<span data-ttu-id="9b29c-109">ただし、アプリケーションのライフ サイクル、DevOps に入る前に、設計を行う方法を知るし、アプリケーションと、デザインの選択肢は何を構築を必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b29c-109">However, before we get into the application life cycle and DevOps, it is important to know how you are going to design and construct your application and what are your design choices.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="9b29c-110">[前へ](index.md)
>[次へ](common-container-design-principles.md)</span><span class="sxs-lookup"><span data-stu-id="9b29c-110">[Previous](index.md)
[Next](common-container-design-principles.md)</span></span>