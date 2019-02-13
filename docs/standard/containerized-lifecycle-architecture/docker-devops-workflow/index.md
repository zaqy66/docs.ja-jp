---
title: Microsoft ツールを使用した Docker アプリケーション DevOps ワークフロー
description: Microsoft のツールを使用して Microsoft プラットフォームとツールの DevOps ワークフローにコンテナー化された Docker アプリケーション ライフ サイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: a2d88dda9f3560675fcb6826960c6e76fa7daf92
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219076"
---
# <a name="docker-application-devops-workflow-with-microsoft-tools"></a>Microsoft ツールを使用した Docker アプリケーション DevOps ワークフロー

Microsoft Visual Studio、Azure DevOps サービス、Team Foundation Server、および Application Insights での開発と IT 運用チーム プロジェクトを管理し、迅速にビルド、テスト、および展開するツールを提供する包括的なエコシステムを提供します。コンテナー化されたアプリケーション。

Visual Studio Team Foundation Server、オンプレミス、と共に、クラウドでの Azure DevOps サービスを開発チームできます生産的ビルド、テスト、およびコンテナー化されたアプリケーションを任意のプラットフォーム (Windows または Linux) をリリースします。

マイクロソフトのツールは、コンテナー化されたアプリケーションの特定の実装のパイプラインを自動化できます: Docker、.NET Core、またはその他のプラットフォームで任意の組み合わせ、グローバル ビルドと継続的インテグレーション (CI) および Azure DevOps サービスまたはチームでのテストからFoundation Server に継続的デプロイ (CD) Docker 環境 (開発、ステージング、運用)、および開発チームが Application Insights でのサービスに関する分析情報を送信します。 すべてのコードのコミットでビルド (CI) を開始して、特定のコンテナー化された環境 (CD) に自動的にサービスを展開できます。

開発者およびテスト担当者は、Microsoft Azure のテンプレートを使用して、Docker に基づく運用環境のような開発とテストの環境を、簡単かつ迅速にプロビジョニングできます。

コンテナー化アプリケーションの開発は、ビジネスが複雑であり、拡張のニーズがあればあるほど、着実に複雑になります。 このよい例は、マイクロサービス アーキテクチャに基づいたアプリケーションです。 プロジェクトには、このような環境で成功のライフ サイクル全体を自動化する必要があります: テレメトリの収集とバージョンを管理する必要がありますも、ビルドと展開、だけでなく、します。 Azure DevOps サービスと Azure は次の機能を提供します。

-   Azure DevOps Services と Team Foundation Server ソース コード管理 (Git または Team Foundation バージョン管理に基づく)、アジャイル計画 (アジャイル、スクラム、CMMI がサポートされています)、CI、リリース管理、およびアジャイル チームの他のツール。

-   Azure DevOps Services と Team Foundation Server には、使用して簡単にできます構築 CI、ビルド、テスト、配信、リリース管理パイプライン マイクロ サービスの 1 つ目とサード パーティの拡張機能の増加し、強力なエコシステムが含まれます。

-   Azure DevOps サービスのビルド パイプラインの一部として自動テストを実行します。

-   Azure DevOps サービスは複数の環境への配信を使用した DevOps ライフ サイクル、実稼働環境でだけでなく、テストに対してもを強化できる A を含む/B 実験、[カナリア リリース](https://martinfowler.com/bliki/CanaryRelease.html)など。

-   組織は、Azure Container Registry に格納されたプライベート イメージから Docker コンテナーを、Azure Resource Manager テンプレートと既に使い慣れているツールを使用して、(Data、PaaS などの) Azure コンポーネントの任意の依存関係と共に簡単にプロビジョニングできます。

>[!div class="step-by-step"]
>[前へ](../design-develop-containerized-apps/build-aspnet-core-applications-linux-containers-aks-kubernetes.md)
>[次へ](docker-application-outer-loop-devops-workflow.md)