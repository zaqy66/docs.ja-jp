---
title: Microsoft ツールを使用した Docker アプリケーション devops ワークフロー
description: Microsoft プラットフォームでのコンテナー化された Docker アプリケーションのライフサイクルと Microsoft ツールでの Toolsdevops ワークフロー
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: a78b6cbae88dcc39d7452a67a2bc5239135dedf9
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53128441"
---
# <a name="docker-application-devops-workflow-with-microsoft-tools"></a><span data-ttu-id="8b229-103">Microsoft ツールを使用した Docker アプリケーション DevOps ワークフロー</span><span class="sxs-lookup"><span data-stu-id="8b229-103">Docker application DevOps workflow with Microsoft tools</span></span>

<span data-ttu-id="8b229-104">Microsoft Visual Studio、Azure DevOps サービス、Team Foundation Server、および Application Insights での開発と IT 運用チーム プロジェクトを管理し、迅速にビルド、テスト、および展開するツールを提供する包括的なエコシステムを提供します。コンテナー化されたアプリケーション。</span><span class="sxs-lookup"><span data-stu-id="8b229-104">Microsoft Visual Studio, Azure DevOps Services, Team Foundation Server, and Application Insights provide a comprehensive ecosystem for development and IT operations that give your team the tools to manage projects and rapidly build, test, and deploy containerized applications.</span></span>

<span data-ttu-id="8b229-105">Visual Studio Team Foundation Server、オンプレミス、と共に、クラウドでの Azure DevOps サービスを開発チームできます生産的ビルド、テスト、およびコンテナー化されたアプリケーションを任意のプラットフォーム (Windows または Linux) をリリースします。</span><span class="sxs-lookup"><span data-stu-id="8b229-105">With Visual Studio and Azure DevOps Services in the cloud, along with Team Foundation Server on-premises, development teams can productively build, test, and release containerized applications directed toward any platform (Windows or Linux).</span></span>

<span data-ttu-id="8b229-106">マイクロソフトのツールは、コンテナー化されたアプリケーションの特定の実装のパイプラインを自動化できます: Docker、.NET Core、またはその他のプラットフォームで任意の組み合わせ、グローバル ビルドと継続的インテグレーション (CI) および Azure DevOps サービスまたはチームでのテストからFoundation Server に継続的デプロイ (CD) Docker 環境 (開発、ステージング、運用)、および開発チームが Application Insights でのサービスに関する分析情報を送信します。</span><span class="sxs-lookup"><span data-stu-id="8b229-106">Microsoft tools can automate the pipeline for specific implementations of containerized applications—Docker, .NET Core, or any combination with other platforms—from global builds and Continuous Integration (CI) and tests with Azure DevOps Services or Team Foundation Server, to Continuous Deployment (CD) to Docker environments (Development, Staging, Production), and to transmit analytics information about the services to the development team through Application Insights.</span></span> <span data-ttu-id="8b229-107">すべてのコードのコミットでビルド (CI) を開始して、特定のコンテナー化された環境 (CD) に自動的にサービスを展開できます。</span><span class="sxs-lookup"><span data-stu-id="8b229-107">Every code commit can initiate a build (CI) and automatically deploy the services to specific containerized environments (CD).</span></span>

<span data-ttu-id="8b229-108">開発者およびテスト担当者は、Microsoft Azure のテンプレートを使用して、Docker に基づく運用環境のような開発とテストの環境を、簡単かつ迅速にプロビジョニングできます。</span><span class="sxs-lookup"><span data-stu-id="8b229-108">Developers and testers can easily and quickly provision production-like development and test environments based on Docker by using templates in Microsoft Azure.</span></span>

<span data-ttu-id="8b229-109">コンテナー化アプリケーションの開発は、ビジネスが複雑であり、拡張のニーズがあればあるほど、着実に複雑になります。</span><span class="sxs-lookup"><span data-stu-id="8b229-109">The complexity of containerized application development increases steadily depending on the business complexity and scalability needs.</span></span> <span data-ttu-id="8b229-110">このよい例は、マイクロサービス アーキテクチャに基づいたアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="8b229-110">A good example of this are applications based on microservices architectures.</span></span> <span data-ttu-id="8b229-111">プロジェクトには、このような環境で成功のライフ サイクル全体を自動化する必要があります: テレメトリの収集とバージョンを管理する必要がありますも、ビルドと展開、だけでなく、します。</span><span class="sxs-lookup"><span data-stu-id="8b229-111">To succeed in such an environment, your project must automate the entire life cycle—not only the build and deployment, but it also must manage versions along with the collection of telemetry.</span></span> <span data-ttu-id="8b229-112">Azure DevOps サービスと Azure は次の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="8b229-112">Azure DevOps Services and Azure offer the following capabilities:</span></span>

-   <span data-ttu-id="8b229-113">Azure DevOps Services と Team Foundation Server ソース コード管理 (Git または Team Foundation バージョン管理に基づく)、アジャイル計画 (アジャイル、スクラム、CMMI がサポートされています)、CI、リリース管理、およびアジャイル チームの他のツール。</span><span class="sxs-lookup"><span data-stu-id="8b229-113">Azure DevOps Services/Team Foundation Server source code management (based on Git or Team Foundation Version Control), Agile planning (Agile, Scrum, and CMMI are supported), CI, release management, and other tools for Agile teams.</span></span>

-   <span data-ttu-id="8b229-114">Azure DevOps Services と Team Foundation Server には、使用して簡単にできます構築 CI、ビルド、テスト、配信、リリース管理パイプライン マイクロ サービスの 1 つ目とサード パーティの拡張機能の増加し、強力なエコシステムが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8b229-114">Azure DevOps Services/Team Foundation Server include a powerful and growing ecosystem of first- and third-party extensions with which you easily can construct a CI, build, test, delivery, and release management pipeline for microservices.</span></span>

-   <span data-ttu-id="8b229-115">Azure DevOps サービスのビルド パイプラインの一部として自動テストを実行します。</span><span class="sxs-lookup"><span data-stu-id="8b229-115">Run automated tests as part of your build pipeline in Azure DevOps Services.</span></span>

-   <span data-ttu-id="8b229-116">Azure DevOps サービスは複数の環境への配信を使用した DevOps ライフ サイクル、実稼働環境でだけでなく、テストに対してもを強化できる A を含む/B 実験、[カナリア リリース](https://martinfowler.com/bliki/CanaryRelease.html)など。</span><span class="sxs-lookup"><span data-stu-id="8b229-116">Azure DevOps Services can tighten the DevOps life cycle with delivery to multiple environments, not just for production environments, but also for testing, including A/B experimentation, [canary releases](https://martinfowler.com/bliki/CanaryRelease.html), and so on.</span></span>

-   <span data-ttu-id="8b229-117">組織は、Azure Container Registry に格納されたプライベート イメージから Docker コンテナーを、Azure Resource Manager テンプレートと既に使い慣れているツールを使用して、(Data、PaaS などの) Azure コンポーネントの任意の依存関係と共に簡単にプロビジョニングできます。</span><span class="sxs-lookup"><span data-stu-id="8b229-117">Organizations easily can provision Docker containers from private images stored in Azure Container Registry along with any dependency on Azure components (Data, PaaS, etc.) using Azure Resource Manager templates with tools with which they are already comfortable working.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="8b229-118">[前へ](../design-develop-containerized-apps/set-up-windows-containers-with-powershell.md)
>[次へ](docker-application-outer-loop-devops-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="8b229-118">[Previous](../design-develop-containerized-apps/set-up-windows-containers-with-powershell.md)
[Next](docker-application-outer-loop-devops-workflow.md)</span></span>