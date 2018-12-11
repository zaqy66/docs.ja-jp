---
title: 一般的なコンテナー設計の原則
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 8aa388c7c19f532829d64208a48b6e556e43d802
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152878"
---
# <a name="common-container-design-principles"></a><span data-ttu-id="c8740-103">一般的なコンテナー設計の原則</span><span class="sxs-lookup"><span data-stu-id="c8740-103">Common container design principles</span></span>

<span data-ttu-id="c8740-104">今後、開発プロセスには、コンテナーを使用する方法に関して触れていくつかの基本的な概念があります。</span><span class="sxs-lookup"><span data-stu-id="c8740-104">Ahead of getting into the development process there are a few basic concepts worth mentioning with regard to how you use containers.</span></span>

## <a name="container-equals-a-process"></a><span data-ttu-id="c8740-105">コンテナー プロセスに等しい</span><span class="sxs-lookup"><span data-stu-id="c8740-105">Container equals a process</span></span>

<span data-ttu-id="c8740-106">コンテナー モデルでは、コンテナーは、1 つのプロセスを表します。</span><span class="sxs-lookup"><span data-stu-id="c8740-106">In the container model, a container represents a single process.</span></span> <span data-ttu-id="c8740-107">コンテナー プロセス境界として定義すると、スケール、またはバッチから、プロセスに使用するプリミティブの作成を開始します。</span><span class="sxs-lookup"><span data-stu-id="c8740-107">By defining a container as a process boundary, you begin to create the primitives used to scale, or batch-off, processes.</span></span> <span data-ttu-id="c8740-108">Docker コンテナーを実行すると表示されます、 [ENTRYPOINT](https://docs.docker.com/engine/reference/builder/#/entrypoint)定義します。</span><span class="sxs-lookup"><span data-stu-id="c8740-108">When you run a Docker container, you'll see an [ENTRYPOINT](https://docs.docker.com/engine/reference/builder/#/entrypoint) definition.</span></span> <span data-ttu-id="c8740-109">これは、プロセスとコンテナーの有効期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="c8740-109">This defines the process and the lifetime of the container.</span></span> <span data-ttu-id="c8740-110">プロセスが完了したら、コンテナーのライフ サイクルが終了します。</span><span class="sxs-lookup"><span data-stu-id="c8740-110">When the process completes, the container life cycle ends.</span></span> <span data-ttu-id="c8740-111">Web サーバー、およびバッチ ジョブは、Microsoft Azure として実装される可能性がありますなどの有効期間が短いプロセスなどの実行時間の長いプロセスがある[WebJobs](https://azure.microsoft.com/documentation/articles/websites-webjobs-resources/)します。</span><span class="sxs-lookup"><span data-stu-id="c8740-111">There are long-running processes, such as web servers, and short-lived processes, such as batch jobs, which might have been implemented as Microsoft Azure [WebJobs](https://azure.microsoft.com/documentation/articles/websites-webjobs-resources/).</span></span> <span data-ttu-id="c8740-112">プロセスが失敗した場合、コンテナーが終了し、Orchestrator が引き継ぎます。</span><span class="sxs-lookup"><span data-stu-id="c8740-112">If the process fails, the container ends, and the orchestrator takes over.</span></span> <span data-ttu-id="c8740-113">オーケストレーターが実行されている 5 つのインスタンスを保持するように指示し、1 つが失敗した場合、オーケストレーターは、失敗した処理を置換する別のコンテナーを作成します。</span><span class="sxs-lookup"><span data-stu-id="c8740-113">If the orchestrator was instructed to keep five instances running and one fails, the orchestrator will create another container to replace the failed process.</span></span> <span data-ttu-id="c8740-114">バッチ ジョブで、プロセスはパラメーターを指定して開始されます。</span><span class="sxs-lookup"><span data-stu-id="c8740-114">In a batch job, the process is started with parameters.</span></span> <span data-ttu-id="c8740-115">プロセスが完了すると、作業が完了します。</span><span class="sxs-lookup"><span data-stu-id="c8740-115">When the process completes, the work is complete.</span></span>

<span data-ttu-id="c8740-116">複数のプロセスを 1 つのコンテナーで実行されている必要があるシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="c8740-116">You might find a scenario in which you want multiple processes running in a single container.</span></span> <span data-ttu-id="c8740-117">任意のアーキテクチャのドキュメントはありません、"never、"は常にも、「常時」。</span><span class="sxs-lookup"><span data-stu-id="c8740-117">In any architecture document, there's never a "never," nor is there always an "always."</span></span> <span data-ttu-id="c8740-118">一般的なパターンは複数のプロセスを必要とするシナリオでは、使用する[スーパーバイザー](http://supervisord.org/)します。</span><span class="sxs-lookup"><span data-stu-id="c8740-118">For scenarios requiring multiple processes, a common pattern is to use [Supervisor](http://supervisord.org/).</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="c8740-119">[前へ](design-docker-applications.md)
>[次へ](monolithic-applications.md)</span><span class="sxs-lookup"><span data-stu-id="c8740-119">[Previous](design-docker-applications.md)
[Next](monolithic-applications.md)</span></span>