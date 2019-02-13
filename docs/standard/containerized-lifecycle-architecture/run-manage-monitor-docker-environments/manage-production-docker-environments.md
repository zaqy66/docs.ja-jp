---
title: 運用環境の Docker 環境を管理します。
description: コンテナー ベースの実稼働環境を管理する重要な点を把握するを取得します。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 54e2b999f744600d3b6853442bb9ccca004f4e76
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219491"
---
# <a name="manage-production-docker-environments"></a>運用環境の Docker 環境を管理します。

クラスターの管理とオーケストレーションは、ホストのグループを制御するためのプロセスです。 追加して、クラスターでは、ホストとコンテナーの現在の状態に関する情報を取得し、開始およびプロセスの停止からホストを削除する必要があります。 クラスターの管理とオーケストレーションは、スケジューラは、クラスター内の各ホストへのアクセスをサービスのスケジュールを設定するにがある必要なためにのスケジューリングに密接に関連付けします。 このため、両方の目的で、同じツールがよく使用されます。

## <a name="container-service-and-management-tools"></a>コンテナー サービスと管理ツール

Container Service では、人気のオープン ソース コンテナーのクラスタ リングやオーケストレーション ソリューションの迅速なデプロイを提供します。 Docker イメージを使用して、アプリケーション コンテナーが完全に移植可能であることを確認します。 DC OS/(Mesosphere と Apache Mesos 利用) をデプロイするコンテナー サービスを使用して、Docker Swarm クラスターを Azure Resource Manager テンプレートまたは数千にこれらのアプリケーションをスケーリングできることを確認する Azure portal を使用: 数万も — のコンテナー。

Azure 仮想マシン スケール セットを使用してこれらのクラスターを展開して、クラスターを Azure のネットワークおよび記憶域サービスの利用します。 コンテナー サービスにアクセスするには、Azure サブスクリプションを必要があります。 Container service では、オーケストレーション レイヤーなど、アプリケーションの移植性を維持しながら Azure のエンタープライズ級の機能を活用がかかります。

表 6-1 は、オーケストレーター、スケジューラ、クラスタ リングのプラットフォームに関連する、一般的な管理ツールを一覧表示します。

表 6-1:Docker の管理ツール


| 管理ツール      | 説明           | 関連するオーケストレーター |
|-----------------------|-----------------------|-----------------------|
| Container Service\(Azure portal での UI の管理) | [Container Service](https://azure.microsoft.com/services/container-service/) 、簡単に取得できるは、開始する方法[Azure でコンテナーのクラスターのデプロイ](https://docs.microsoft.com/azure/container-service/dcos-swarm/container-service-deployment)Mesosphere DC/OS、Kubernetes、Docker Swarm などのよく使われるオーケストレーターに基づきます。 <br /><br /> Container Service では、これらのプラットフォームの構成を最適化します。 だけ、サイズ、ホストの数と、オーケストレーター ツールの選択肢を選択する必要があり、コンテナー サービスが他のすべてを処理します。 | Mesosphere DC/OS <br /><br /> Kubernetes <br /><br /> Docker Swarm |
| Docker ユニバーサル コントロール プレーン\(オンプレミスまたはクラウド) | [Docker ユニバーサル コントロール プレーン](https://docs.docker.com/v1.11/ucp/overview/)は Docker からエンタープライズ グレードのクラスター管理ソリューションです。 1 つの場所から、クラスター全体を管理できます。 <br /><br /> Docker ユニバーサル コントロール プレーンは、Docker Swarm、Docker ユニバーサル コントロール プレーン Docker Trusted Registry を提供する Docker Datacenter をという名前の商用製品の一部として含まれています。 <br /><br /> Docker Datacenter では、オンプレミスにインストールされていることができます。 または Azure のようなパブリック クラウドからプロビジョニングします。 | Docker Swarm\(Container Service でサポートされている) |
| Docker Cloud\(Tutum; クラウド SaaS とも呼ばれます) | [Docker Cloud](https://docs.docker.com/docker-cloud/)ビルドとテストの機能を設定して、ホスト インフラストラクチャの管理に役立つツールは Dockerized アプリケーション イメージとオーケストレーションの機能と Docker レジストリを提供するホストされる管理サービス (SaaS)具体的なインフラストラクチャをイメージの展開を自動化するのに役立つ機能を展開します。 SaaS の Docker クラウド アカウントは、Docker Swarm クラスターを実行して Container Service のインフラストラクチャに接続できます。 | Docker Swarm\(Container Service でサポートされている) |
| Mesosphere Marathon\(オンプレミスまたはクラウド) | [Marathon](https://mesosphere.github.io/marathon/docs/marathon-ui.html) Mesosphere の DC/OS と Apache Mesos は、運用環境レベルのコンテナー オーケストレーションとスケジューラ プラットフォーム。 <br /><br /> Mesos で動作する (DC/OS は Apache Mesos に基づく) コントロールの実行時間の長いサービスを示し、[プロセスとコンテナーの管理用の web UI](https://mesosphere.github.io/marathon/docs/marathon-ui.html)。 Web UI の管理ツールを提供します | Mesosphere DC/OS\(Mesos を Apache に基づき、Container Service でサポートされている) |
| Google Kubernetes | [Kubernetes](https://kubernetes.io/docs/user-guide/ui/#dashboard-access)調整、スケジュール、およびクラスター インフラストラクチャにまたがます。 これはコンテナー中心のインフラストラクチャを提供するホストのクラスターのデプロイ、スケーリング、およびアプリケーション コンテナーの操作を自動化するため、オープン ソース プラットフォーム。 | Google Kubernetes\(Container Service でサポートされている) |

## <a name="azure-service-fabric"></a>Azure Service Fabric

クラスターのデプロイと管理に関する別の選択肢では、Azure Service Fabric です。 [Service Fabric](https://azure.microsoft.com/services/service-fabric/)開発者と同様にコンテナーのオーケストレーションを含む Microsoft のマイクロ サービス プラットフォームは拡張性の高いマイクロ サービス アプリケーションを構築するモデルをプログラミングします。 Service Fabric では、現在のバージョンの Linux プレビューでは、Docker をサポートと、 [Linux 上の Service Fabric プレビュー](https://docs.microsoft.com/azure/service-fabric/service-fabric-deploy-anywhere)、および Windows コンテナーの[次のリリースで](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview)します。

Service Fabric 管理ツールを次に示します。

-   [Service Fabric 用に azure ポータル](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-creation-via-portal)クラスター関連の操作 (作成/更新/削除)、クラスターまたはインフラストラクチャ (Vm、ロード バランサー、ネットワークなど) の構成

-   [Azure Service Fabric Explorer](https://docs.microsoft.com/azure/service-fabric/service-fabric-visualizing-your-cluster) insights と Service Fabric クラスターのノード/vm の観点から、アプリケーションとサービスの観点からの特定の操作を提供する特殊な web UI ツールです。

>[!div class="step-by-step"]
>[前へ](run-microservices-based-applications-in-production.md)
>[次へ](monitor-containerized-application-services.md)