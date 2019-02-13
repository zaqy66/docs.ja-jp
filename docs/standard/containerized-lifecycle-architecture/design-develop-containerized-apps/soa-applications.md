---
title: SOA アプリケーション
description: コンテナーが SOA アプリケーションの配置オプションもあることに注意してください。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 4fd39e075c5730cf7fddb0138cdb5267a914c91f
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56221265"
---
# <a name="soa-applications"></a>SOA アプリケーション

SOA が過剰使用されている用語を使用してを別々 の人は多くの異なる要素。 少なくとも、共通分母、SOA、またはサービス指向、平均 (最も一般的な HTTP サービス) としてさまざまな種類に分類できる複数のサービスに分解して、アプリケーションのアーキテクチャの構造をそのなどのサブシステムが、または、階層化とそれ以外の場合。

今日では、コンテナー イメージに含まれるすべての依存関係のため、展開に関連する問題を解決する Docker コンテナーとしてそれらのサービスをデプロイできます。 ただし、Soa のスケール アウトする必要がある場合、そのに基づいて 1 つのインスタンスを展開する場合の課題が発生する可能性があります。 これは、Docker クラスタ リング ソフトウェアまたはオーケストレーターが支援する場所です。 マイクロ サービス アプローチを調べるとき、次のセクションで詳しくこれを確認します。

1 日の終わりには、コンテナーのクラスタ リング ソリューションは、両方の従来の SOA アーキテクチャまたはマイクロ サービスごとにそのデータ モデルが所有するより高度なマイクロ サービス アーキテクチャに便利です。 また、複数のデータベースに協力してくれたもスケール アウトできる SOA サービスによって共有モノリシック データベースでの作業ではなく、データ層。 ただし、データの分割に関する議論は、アーキテクチャと設計についてのみです。

>[!div class="step-by-step"]
>[前へ](state-and-data-in-docker-applications.md)
>[次へ](orchestrate-high-scalability-availability.md)