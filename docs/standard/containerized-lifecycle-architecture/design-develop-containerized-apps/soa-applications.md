---
title: SOA アプリケーション
description: コンテナーが SOA アプリケーションの配置オプションもあることに注意してください。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 353ba738143b7dcd92c7c75ac27ea6a7370f9da6
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/23/2019
ms.locfileid: "56745834"
---
# <a name="service-oriented-applications"></a>サービス指向アプリケーション

サービス指向アーキテクチャ (SOA) は、人によって異なる、さまざまなものの過剰使用されている用語をしました。 しかし、SOA がサブシステムなど、さまざまな種類にまたは他の場合、階層として分類できる (通常 HTTP サービス) としていくつかのサービスに分解して、アプリケーションのアーキテクチャを構築することを意味、共通の基準として。

今日では、コンテナー イメージの依存関係すべて含まれているため、展開に関連する問題を解決する Docker コンテナーとしてそれらのサービスをデプロイできます。 ただし、Soa を拡大する必要がある場合、そのに基づいて 1 つのインスタンスを展開する場合の課題が発生する可能性があります。 この課題は、Docker クラスタ リング ソフトウェアまたはオーケストレーターを使用して処理できます。 マイクロ サービス アプローチについて説明している場合、次のセクションで詳しくオーケストレーターについて説明します。

Docker コンテナーは、従来のサービス指向アーキテクチャと高度なマイクロサービス アーキテクチャの両方にとって便利な機能です (ただし、必須ではありません)。

1 日の終わりには、コンテナーのクラスタ リング ソリューションは、両方の従来の SOA アーキテクチャとマイクロ サービスごとにそのデータ モデルが所有するより高度なマイクロ サービス アーキテクチャに便利です。 複数のデータベースに協力してくれたもスケール アウトできます SOA サービスによって共有モノリシック データベースでの作業ではなく、データ層。 ただし、データの分割に関する議論は、アーキテクチャと設計についてのみです。

>[!div class="step-by-step"]
>[前へ](state-and-data-in-docker-applications.md)
>[次へ](orchestrate-high-scalability-availability.md)
