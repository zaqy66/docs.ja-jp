---
title: Docker に関する用語
description: Docker を使用する場合は、毎日が使用したいくつかの基本的な用語について説明します。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 1514a2199efe52a411f61649fc21e906bba5b13c
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56218724"
---
# <a name="docker-terminology"></a>Docker に関する用語

このセクションでは、用語と定義する必要がありますを理解する Docker を深く掘り下げる前に一覧表示されます (その他の定義を参照してください、広範な[用語集](https://docs.docker.com/glossary/)で Docker によって提供される<https://docs.docker.com/glossary/>:。

-   **コンテナー イメージ** のすべての依存関係とコンテナーを作成するために必要な情報を使用してパッケージ。 イメージには、すべての依存関係 (フレームワークなど) と展開と、コンテナー ランタイムによって使用される構成が含まれます。 通常は、イメージから派生する複数の基本イメージをレイヤー積み重ねられているコンテナーのファイル システムを形成する他の一番上にある 1 つ。 作成された後、イメージは変更できません。

-   **コンテナー** Docker イメージのインスタンス。 コンテナーは、1 つのアプリケーション、プロセス、またはサービス用のランタイムを表します。 Docker イメージをランタイム環境、および標準的な一連の命令の内容で構成されます。 サービスを拡大縮小する場合は、同じイメージからコンテナーの複数のインスタンスを作成します。 または、バッチ ジョブは、インスタンスごとに異なるパラメーターを渡す、同じイメージから複数のコンテナーを作成できます。

-   **タグ** マークまたはラベルをさまざまなイメージまたは (バージョン番号または移行先の環境) に応じて、同じイメージのバージョンを識別できるようにイメージを適用することができます。

-   **Dockerfile** Docker イメージをビルドする方法の手順を含むテキスト ファイル。

-   **ビルド** 情報と、イメージがビルド フォルダー内の他のファイルおよびその Dockerfile によって提供されるコンテキストに基づいて、コンテナー イメージをビルドするアクションです。 Docker の docker ビルド コマンドを使用してイメージを構築できます。

-   **リポジトリ (リポジトリとも呼ばれます)** イメージ バージョンを示すタグが付いた関連の Docker イメージのコレクション。 いくつかのリポジトリには、特定のイメージ (軽い) ランタイムのみを含むイメージ (重い) Sdk を含むイメージなどの複数のバリエーションが含まれます。 これにします。 そのようなバリアントは、タグでマーク付けすることができます。 1 つのリポジトリには、Linux イメージと Windows イメージなどのプラットフォーム バリアントを含めることができます。

-   **レジストリ** リポジトリへのアクセスを提供するサービスです。 ほとんどのパブリック イメージの既定のレジストリは [Docker Hub](https://hub.docker.com/) です (Docker によって組織として所有されている)。 レジストリには、通常、複数のチームからのリポジトリが含まれています。 企業には、多くの場合、プライベート レジストリを作成したイメージ保存および管理があります。 *Azure Container Registry*別の例を示します。

-   **Docker Hub** イメージをアップロードし、作業中にパブリック レジストリです。 Docker Hub は、Docker イメージ ホスティング、パブリックまたはプライベート レジストリ、ビルド トリガーおよび Web フック、さらに GitHub および Bitbucket との統合を提供します。

-   **Azure Container Registry** Docker イメージと Azure では、そのコンポーネントを操作するためのパブリック リソースです。 これは、Azure で利用しているデプロイに近く、アクセスに対する制御権を付与するレジストリです。これにより、Azure Active Directory のグループとアクセス許可が使用できるようになります。

-   **Docker Trusted Registry (DTR)** をインストールすることができます (Docker) からの Docker レジストリ サービス、オンプレミス組織のデータ センターとネットワーク内にあります。 そのようにします。 企業内で管理する必要があるプライベート イメージにおいて便利です。 Docker Trusted Registry は Docker Datacenter 製品の一部として含められています。 詳細についてを参照してください[ https://docs.docker.com/docker-trusted-registry/overview/](https://docs.docker.com/docker-trusted-registry/overview/)します。

-   **Docker Community Edition (CE)** Windows および macOS の構築、実行、およびコンテナーをローカルにテスト用の開発ツール。 Docker for Windows CE は、Linux コンテナーと Windows コンテナーの両方に開発環境を提供します。 Windows 上の Linux Docker ホストがに基づいて、 [HYPER-V](https://www.microsoft.com/en-us/server-cloud/solutions/virtualization.aspx) VM。 Windows コンテナーのホストは、Windows に直接基づいています。 Docker CE for Mac は、Apple Hypervisor フレームワークに基づいて、 [xhyve ハイパーバイザー](https://github.com/mist64/xhyve)、Mac OS x. Docker Windows の CE では for Mac、Linux Docker ホスト VM を提供する、Oracle VirtualBox に基づく Docker Toolbox を置き換えます。

-   **Docker Enterprise Edition (EE)** Linux と Windows 開発用 Docker ツールのエンタープライズ規模のバージョン。

-   **Compose** コマンド ライン ツールと YAML ファイル形式を定義すると、複数のコンテナー アプリケーションを実行しているメタデータを使用します。 複数のイメージに基づく単一のアプリケーションを定義するには、環境に応じて値をオーバーライドできる 1 つまたは複数の .yml ファイルを使用します。 1 つのコマンドを使用して全体の複数のコンテナー アプリケーションを展開するには、定義を作成した後 (docker-compose を)、Docker ホストでイメージごとにコンテナーを作成します。

-   **クラスター** の Docker ホストの場合と同様、1 つの仮想 Docker ホストのサービスの複数のインスタンスに対応できるように公開されているコレクション、クラスター内で複数のホストに分散します。 Docker Swarm、Mesosphere DC/OS、Kubernetes、および Azure Service Fabric を使用して、Docker クラスターを作成することができます。 (クラスターを管理するために Docker Swarm を使用する場合、通常はそのクラスターをクラスターとしてではなく "*スウォーム*" として参照します)。

-   **Orchestrator** クラスターと Docker ホストの管理を簡素化するツール。 オーケストレーターを使用して、イメージ、コンテナー、および CLI またはグラフィカル ユーザー インターフェイスを使用してホストを管理できます。 コンテナー ネットワーク、構成、負荷分散、サービス検出、高可用性、Docker ホストの構成などを管理することができます。 オーケストレーターは、ノードのコレクション全体にわたりワークロードの実行、配布、スケーリング、修復を担当します。 通常、オーケストレーター製品は、Mesosphere DC/OS、Kubernetes、Docker Swarm、Azure Service Fabric などのクラスター インフラストラクチャを提供する製品です。

>[!div class="step-by-step"]
>[前へ](what-is-docker.md)
>[次へ](docker-containers-images-and-registries.md)