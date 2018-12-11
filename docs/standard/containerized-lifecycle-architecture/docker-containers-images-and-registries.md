---
title: Docker コンテナー、イメージ、レジストリ
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: af235280c985d20f9e6a2ee6096edbe6c3aad63a
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53142750"
---
# <a name="docker-containers-images-and-registries"></a>Docker コンテナー、イメージ、レジストリ

Docker を使用する場合、およびその依存関係コンテナー イメージにアプリまたはサービス、およびパッケージを作成します。 イメージとは、アプリケーションまたはサービスと、その構成と依存関係の静的な表現です。

アプリケーションまたはサービスを実行するために、アプリケーションのイメージはインスタンス化され、コンテナーが作成されます。このコンテナーが Docker ホスト上で実行されます。 コンテナーは、最初に開発環境または PC でテストされます。

イメージのライブラリとして機能する、レジストリにイメージを格納します。 運用環境のオーケストレーターに展開する場合は、レジストリを作成する必要があります。 Docker は [Docker Hub](https://hub.docker.com/) 経由で公開レジストリを保守します。他のベンダーは、さまざまなイメージのコレクション用にレジストリを用意しています。 また、企業は自社の Docker イメージ用に非公開のレジストリをオンプレミスに持つことができます。

図 1-4 は、他のコンポーネントにイメージと Docker でレジストリを関連付ける方法を示しています。 また、ベンダーから提供される複数のレジストリも示しています。

![](./media/image4.png)

図 1-4:Docker の用語と概念の分類

レジストリにイメージを配置する、フレームワーク レベルの依存関係のすべてを含む、静的で不変アプリケーション ビットを格納できます。 バージョンことができますと複数の環境でイメージを展開し、したがって一貫した展開ユニットを提供します。

プライベート イメージ レジストリは、オンプレミスでホストされているか、クラウドでは、次の状況をお勧めします。

-   機密保持のためにイメージを一般公開して共有することができない場合。

-   イメージと選択した展開環境間のネットワーク待機時間を最小限に抑えたい場合。 など、実稼働環境が Azure の場合は、おそらくするネットワーク待機時間が最小限になるように、Azure Container Registry にイメージを保存します。 同様に、実稼働環境がオンプレミスの場合は、同じローカル ネットワーク内でオンプレミスの Docker Trusted Registry を使用できるようにする方法があります。

>[!div class="step-by-step"]
>[前へ](docker-terminology.md)
>[次へ](Docker-application-lifecycle/index.md)