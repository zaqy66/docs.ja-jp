---
title: 一般的なコンテナー設計の原則
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 3af174279e8b6f56a10413817b05ef68cfcabea5
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50202179"
---
# <a name="common-container-design-principles"></a>一般的なコンテナー設計の原則

今後、開発プロセスには、コンテナーを使用する方法に関して触れていくつかの基本的な概念があります。

## <a name="container-equals-a-process"></a>コンテナー プロセスに等しい

コンテナー モデルでは、コンテナーは、1 つのプロセスを表します。 コンテナー プロセス境界として定義すると、スケール、またはバッチから、プロセスに使用するプリミティブの作成を開始します。 Docker コンテナーを実行すると表示されます、 [ENTRYPOINT](https://docs.docker.com/engine/reference/builder/#/entrypoint)定義します。 これは、プロセスとコンテナーの有効期間を定義します。 プロセスが完了したら、コンテナーのライフ サイクルが終了します。 Web サーバー、およびバッチ ジョブは、Microsoft Azure として実装される可能性がありますなどの有効期間が短いプロセスなどの実行時間の長いプロセスがある[WebJobs](https://azure.microsoft.com/documentation/articles/websites-webjobs-resources/)します。 プロセスが失敗した場合、コンテナーが終了し、Orchestrator が引き継ぎます。 オーケストレーターが実行されている 5 つのインスタンスを保持するように指示し、1 つが失敗した場合、オーケストレーターは、失敗した処理を置換する別のコンテナーを作成します。 バッチ ジョブで、プロセスはパラメーターを指定して開始されます。 プロセスが完了すると、作業が完了します。

複数のプロセスを 1 つのコンテナーで実行されている必要があるシナリオがあります。 任意のアーキテクチャのドキュメントはありません、"never、"は常にも、「常時」。 一般的なパターンは複数のプロセスを必要とするシナリオでは、使用する[スーパーバイザー](http://supervisord.org/)します。


>[!div class="step-by-step"]
[前へ](design-docker-applications.md)
[次へ](monolithic-applications.md)
