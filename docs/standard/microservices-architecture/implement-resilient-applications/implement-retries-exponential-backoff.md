---
title: エクスポネンシャル バックオフを含む再試行を実装する
description: エクスポネンシャル バックオフを含む再試行を実装する方法について説明します。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/16/2018
ms.openlocfilehash: 421a4535888f432974c764b238c06b5b323aefb3
ms.sourcegitcommit: 542aa405b295955eb055765f33723cb8b588d0d0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "54362081"
---
# <a name="implement-retries-with-exponential-backoff"></a>エクスポネンシャル バックオフを含む再試行を実装する

[*エクスポネンシャル バックオフを含む再試行*](/azure/architecture/patterns/retry)は、最大再試行回数に達するまで、指数関数的に増加する待機時間で操作を再試行する手法です ([エクスポネンシャル バックオフ](https://en.wikipedia.org/wiki/Exponential_backoff))。 この手法を利用すると、何らかの理由でクラウド リソースが数秒以上断続的に使用できなくなる可能性があります。 たとえば、オーケストレーターは、負荷分散のためにコンテナーをクラスター内の別ノードに移動している可能性があります。 その間は、一部の要求が失敗する可能性があります。 また、SQL Azure のようなデータベースで、負荷分散のためにデータベースを別のサーバーに移動しているときに、データベースを数秒間使用できなくなる例もあります。

エクスポネンシャル バックオフを使用する再試行ロジックを実装するには、さまざまなアプローチがあります。

>[!div class="step-by-step"]
>[前へ](partial-failure-strategies.md)
>[次へ](implement-resilient-entity-framework-core-sql-connections.md)