---
title: エクスポネンシャル バックオフを含む再試行を実装する
description: コンテナー化された .NET アプリケーションの .NET マイクロサービス アーキテクチャ | エクスポネンシャル バックオフを含む再試行を実装する
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 06/08/2018
ms.openlocfilehash: e0758ee8fe28cb45ecd35ad07ddc738c12614973
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53148770"
---
# <a name="implement-retries-with-exponential-backoff"></a>エクスポネンシャル バックオフを含む再試行を実装する

[*エクスポネンシャル バックオフを含む再試行*](https://docs.microsoft.com/azure/architecture/patterns/retry)は、最大再試行回数に達するまで、指数関数的に増加する待機時間で操作を再試行しようとする手法です ([エクスポネンシャル バックオフ](https://en.wikipedia.org/wiki/Exponential_backoff))。 この手法を利用すると、何らかの理由でクラウド リソースが数秒以上断続的に使用できなくなる可能性があります。 たとえば、オーケストレーターは、負荷分散のためにコンテナーをクラスター内の別ノードに移動している可能性があります。 その間は、一部の要求が失敗する可能性があります。 また、SQL Azure のようなデータベースで、負荷分散のためにデータベースを別のサーバーに移動しているときに、データベースを数秒間使用できなくなる例もあります。

エクスポネンシャル バックオフを使用する再試行ロジックを実装するには、さまざまなアプローチがあります。

>[!div class="step-by-step"]
>[前へ](partial-failure-strategies.md)
>[次へ](implement-resilient-entity-framework-core-sql-connections.md)