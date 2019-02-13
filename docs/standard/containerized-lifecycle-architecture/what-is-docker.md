---
title: Docker について
description: Docker の理解に深く取得は、単純な例をここで役立つことがあります。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: c8300c964dfce0cc8e39478cc10ed7589dbca2c9
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56218555"
---
# <a name="what-is-docker"></a>Docker について

[Docker](https://www.docker.com/)は、[オープン ソース プロジェクト](https://github.com/docker/docker)クラウドまたはオンプレミスで実行できる移植可能な自己完結型コンテナーとしてのアプリケーションのデプロイを自動化するため (を参照してください図 1-2)。 Docker はまた、[会社](https://www.docker.com/)を促進およびこのテクノロジは、クラウド、Linux、および Windows のベンダーなどの Microsoft と共同で作業を開発します。

![](./media/image2.png)

図 1-2:Docker は、ハイブリッド クラウドのすべてのレイヤーでコンテナーを展開します。

Docker イメージ コンテナーは、Linux と Windows 上でネイティブに実行できます。 ただし、Windows イメージを Windows ホストでのみ実行でき、Linux イメージは、Linux ホスト、つまり、ホスト サーバーまたは VM でのみ実行できます。

開発者は、Windows、Linux、または macOS 上の開発環境を使用できます。 開発用コンピューターでは、開発者は、どの Docker イメージの配置、アプリとその依存関係を含む Docker ホストを実行します。 Linux または Mac 上で開発する場合は、Linux ベースの Docker ホストを使用し、Linux コンテナー専用のイメージを作成できます (Mac で作業する開発者はコードを編集したり、Docker コマンド ライン インターフェイスを実行\[CLI\]から macOS では、この記事の執筆時点、コンテナーが macOS 上で直接実行しないでください)。Windows 上で開発する場合は、Linux または Windows コンテナーのいずれかのイメージを作成できます。

開発環境でコンテナーをホストし、開発ツールを追加するために、Docker は Windows 用または macOS 用の [Docker Community Edition (CE)](https://www.docker.com/community-edition) をリリースしています。 これらの製品で、コンテナーをホストするために必要な VM (Docker ホスト) がインストールされます。 Docker は [Docker Enterprise Edition (EE) ](https://www.docker.com/enterprise-edition) もリリースしています。エンタープライズ開発向けに設計されており、大規模なビジネスクリティカル アプリケーションをビルドし、リリースし、運用環境で実行する IT チームに使用されています。

[Windows コンテナー](/virtualization/windowscontainers/about/)を実行するには、次の 2 つの種類のランタイムがあります。

-   **Windows Server コンテナー** このランタイムには、プロセスと名前空間の分離テクノロジによる分離性をアプリケーションが用意されています。 Windows Server コンテナーは、コンテナー ホストおよびホストで実行されているすべてのコンテナーとカーネルを共有します。

-   **HYPER-V コンテナー** 大幅に最適化された VM で各コンテナーを実行して、Windows Server コンテナーによって提供される分離でこれを展開します。 この構成では、コンテナー ホストのカーネルは、Hyper-V コンテナーと共有されず、分離性を提供します。

これらのコンテナー イメージは、同じ方法で作成され、同じ機能します。 違いは、イメージからコンテナーを作成する方法、HYPER-V コンテナーを実行するには、追加のパラメーターが必要です。 詳細については、「[Hyper-V コンテナー](/virtualization/windowscontainers/about/)」を参照してください。

## <a name="comparing-docker-containers-with-vms"></a>Vm での Docker コンテナーの比較

図 1-3 は、Vm と Docker の比較を示しています。 コンテナー。

コンテナーは、はるかに少ないリソースを必要とするため (たとえば、する必要はありません完全な OS)、簡単にデプロイされ、高速に起動します。 これにより、密度の高い、コストを減らす、同じハードウェア単位に、その他のサービスを実行できることを意味することが可能にします。

同じカーネルで実行されていることの副作用として、Vm よりも緩やかな分離を実現します。

イメージの主な目的は、異なる展開間で同じ環境 (依存関係) にすることです。 自分のコンピューターでデバッグし、同じ環境が保証されている別のコンピューターに展開できます。

コンテナー イメージは、アプリやサービスをパッケージ化し、信頼性が高く、再現可能な方法でデプロイする方法です。 この点で、Docker はテクノロジだけではありませんも、哲学やプロセス。

Docker を使用する場合と開発者を聞くことがない、「機能は私のコンピューターでは、なぜ実稼働環境ででしょうか。」 いることができます簡単に言えば「には、Docker で実行される」ためのサポートされている Docker 環境でパッケージ化された Docker アプリケーションを実行することができます、展開のすべての宛先 (開発、QA、ステージング、運用など。) にするためのものが、方法は、実行されます。

![](./media/image3.png)

図 1-3:従来の Vm を Docker コンテナーの比較

>[!div class="step-by-step"]
>[前へ](index.md)
>[次へ](docker-terminology.md)
