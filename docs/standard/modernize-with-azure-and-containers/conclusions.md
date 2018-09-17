---
title: まとめ
description: Azure クラウドおよび Windows コンテナーで既存の .NET アプリケーションを近代化 |結論
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/26/2017
ms.openlocfilehash: af6151d04622c72acdb7f27ebb220bf611418b4c
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2018
ms.locfileid: "45743970"
---
# <a name="conclusions"></a>まとめ

- コンテナー ベースのソリューションは、最終的にはコスト削減のメリットを提供します。 コンテナーは、運用環境での依存関係の欠落によって引き起こされる不整合を削除するための展開に関する問題の解決策です。 これらの問題を削除して、開発/テスト、DevOps、および運用操作大幅に向上します。

- Docker コンテナーは、サーバー ベースのアプリケーションまたはサービスの配置の標準的な単位になっています。

- 運用環境では、拡張性の高い Windows コンテナー ベースのアプリケーションをホストする (Service Fabric、または Kubernetes) などのオーケストレーターを使用する必要があります。

- コンテナーをホストする azure Vm は、クラウドで小規模な開発/テスト環境を作成する高速で簡単な方法です。

- 既存のアプリケーションを Azure から、リレーショナル データベースを移行する場合に、既定で azure SQL Database マネージ インスタンスがお勧めします。

- Visual Studio 2017 と Image2Docker は、作業の開始の学習曲線を向上させることにより、Windows コンテナーで既存の .NET アプリケーションを最新化を開始するための基本的なツールです。

- 実稼働環境でコンテナー化されたアプリケーションを配置するときに作成または DevOps の文化と CI/CD パイプラインで、Azure DevOps サービスや Jenkins などの DevOps ツールを採用するは常に。

- Microsoft Azure では、Windows コンテナー、クラウド インフラストラクチャおよび PaaS サービスで、既存の .NET Framework アプリケーションを近代化する最も包括的な完全な環境を提供します。

>[!div class="step-by-step"]
[前へ](walkthroughs-technical-get-started-overview.md)