---
title: SOA アプリケーション
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 7f88daaf0787cf780e7ab9602f35ae4e6ab8308c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53155315"
---
# <a name="soa-applications"></a>SOA アプリケーション

SOA が過剰使用されている用語を使用してを別々 の人は多くの異なる要素。 少なくとも、共通分母、SOA、またはサービス指向、平均 (最も一般的な HTTP サービス) としてさまざまな種類に分類できる複数のサービスに分解して、アプリケーションのアーキテクチャの構造をそのなどのサブシステムが、または、階層化とそれ以外の場合。

今日では、コンテナー イメージに含まれるすべての依存関係のため、展開に関連する問題を解決する Docker コンテナーとしてそれらのサービスをデプロイできます。 ただし、Soa のスケール アウトする必要がある場合、そのに基づいて 1 つのインスタンスを展開する場合の課題が発生する可能性があります。 これは、Docker クラスタ リング ソフトウェアまたはオーケストレーターが支援する場所です。 マイクロ サービス アプローチを調べるとき、次のセクションで詳しくこれを確認します。

1 日の終わりには、コンテナーのクラスタ リング ソリューションは、両方の従来の SOA アーキテクチャまたはマイクロ サービスごとにそのデータ モデルが所有するより高度なマイクロ サービス アーキテクチャに便利です。 また、複数のデータベースに協力してくれたもスケール アウトできる SOA サービスによって共有モノリシック データベースでの作業ではなく、データ層。 ただし、データの分割に関する議論は、アーキテクチャと設計についてのみです。

>[!div class="step-by-step"]
>[前へ](state-and-data-in-docker-applications.md)
>[次へ](orchestrate-high-scalability-availability.md)