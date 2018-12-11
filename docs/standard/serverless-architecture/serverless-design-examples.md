---
title: サーバーレス設計の例 - サーバーレス アプリ
description: さまざまなスケジュール設定とファイルのトリガーおよびストリーム プロセスにイベント ベースの処理からのサーバーレス アーキテクチャでサポートされるシナリオについて説明します。
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: cf46c601ac6aa401c7c37bd64c1f8981589ebd2e
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53146713"
---
# <a name="serverless-design-examples"></a>サーバーレスの設計例

存在している多くのデザイン パターンがないサーバーレス。 このセクションでは、サーバーレスを使用する一般的なシナリオをキャプチャします。 どのような共通のあるすべての例は、イベントのトリガーとビジネス ロジックの基本的な組み合わせです。

## <a name="scheduling"></a>スケジュール設定

タスクのスケジュール設定は、一般的な関数です。 次の図は、適切な整合性チェックがない従来のデータベースを示します。 データベースを定期的に削除する必要があります。 サーバーレスの関数は、無効なデータを検索し、それをクリーンアップします。 トリガーは、スケジュールに従って、コードを実行するタイマーです。

![サーバーレスのスケジュール設定](./media/serverless-scheduling.png)

## <a name="command-and-query-responsibility-segregation-cqrs"></a>コマンドとクエリ責務分離 (CQRS)

コマンドとクエリ責務分離 (CQRS) は、データの読み取り (またはクエリを実行する) のさまざまなインターフェイスとデータを変更する操作を提供するパターンです。 これは、いくつかの一般的な問題を説明します。 従来の作成読み取り更新プログラムの削除 (CRUD) ベースのシステムでの競合が、同じデータ ストアに大量の読み取りと書き込みの両方から発生します。 ロックし、頻繁に発生する可能性があります、読み取りが大幅に低下します。 多くの場合、別のエンティティからデータを組み合わせる必要があります、複合ドメインのオブジェクトと読み取り操作のいくつかのようにデータが表示されます。

CQRS を使用して、読み取りは、使用される方法は、データをモデル化する特別な「フラット化された」エンティティになる場合があります。 格納する方法とは異なる、読み取りが処理されます。 たとえば、データベースは、子のアドレス レコードを含むヘッダー レコードとして連絡先を格納することがあります、読み取りはヘッダーとアドレスのプロパティの両方を持つエンティティを含めることができます。 読み取りモデルを作成するさまざまな方法はあります。 これは、ビューから具体化可能性があります。 更新操作は、2 つの異なるモデルの更新をトリガーし、単一のイベントとしてカプセル化する可能性があります。 読み取りと書き込みの別個のモデルが存在します。

![CQRS の例](./media/cqrs-example.png)

サーバーなしの分離のエンドポイントを提供することで、CQRS パターンに対応できます。 1 つのサーバーレス関数はクエリや読み取りに対応し、別のサーバーレス関数または関数のセットは、更新操作を処理します。 サーバーレス関数読み取りモデルに最新の状態を保持する必要もあり、データベースのによってトリガーできます[変更フィード](https://docs.microsoft.com/azure/cosmos-db/change-feed)します。 フロント エンド開発に必要なエンドポイントへの接続に簡単になります。 イベントの処理は、バックエンドで処理されます。 このモデルは、さまざまな操作の異なるチームで動作するため、大規模なプロジェクトにもスケーリングもします。

## <a name="event-based-processing"></a>イベント ベースの処理

メッセージ ベースのシステムでは、多くの場合、キューまたは処理するパブリッシャー/サブスクライバーのトピックにイベントが収集されます。 これらのイベントは、ビジネス ロジックの一部を実行するサーバーレス関数をトリガーできます。 イベント ベースの処理の例は、イベント ソース システムです。 「イベント」は、タスクを完了のマークに発生します。 イベントによってトリガーされるサーバーレスの関数は、適切なデータベースのドキュメントを更新します。 2 番目のサーバーレス関数は、システムの読み取りモデルを更新するのにイベントを使用することがあります。 [Azure Event Grid](https://docs.microsoft.com/azure/event-grid/overview)サブスクライバーとしての関数とイベントを統合する方法を提供します。

> イベントは、情報メッセージです。 詳細については、次を参照してください。[イベント ソーシング パターン](https://docs.microsoft.com/azure/architecture/patterns/event-sourcing)します。

## <a name="file-triggers-and-transformations"></a>ファイルのトリガーと変換

抽出、変換、および読み込み (ETL) は、共通のビジネス関数。 サーバーレスは優れたソリューション ETL パイプラインの一部としてトリガーされるようにコードを許容するためです。 個々 のコード コンポーネントは、さまざまな側面に対処できます。 サーバーレス関数を 1 つがファイルをダウンロード、変換を適用する別および別のデータを読み込みます。 コードをテストし、個別に、デプロイが簡単に維持し、必要に応じて拡大縮小します。

![サーバーレスのファイルのトリガーと変換](./media/serverless-file-triggers.png)

図では、「クール ストレージ」に解析されるデータを提供[Azure Stream Analytics](https://docs.microsoft.com/azure/stream-analytics)します。 データ ストリーム内に発生した問題は、異常に対処する Azure 関数をトリガーします。

## <a name="asynchronous-background-processing-and-messaging"></a>非同期のバック グラウンド処理とメッセージング

非同期メッセージングとバック グラウンド処理は、プロセスを待たずに開始するためにアプリケーションを許可します。 非同期処理の例は、OCR アプリです。 イメージが送信され、処理待ちのキューします。 テキストを抽出するイメージをスキャンするされ、時間がかかる場合があります、通知が完了したらが送信されます。 サーバーレスには、呼び出しと、このシナリオでは、結果の両方を処理できます。

## <a name="web-apps-and-apis"></a>Web アプリと Api

一般的なシナリオのサーバーレスは N 層アプリケーション、web アプリの UI レイヤーが最もよくものです。 シングル ページ アプリケーション (SPA) の人気は最近急騰しています。 SPA アプリでは、1 つのページを表示し、ページ全体を再度読み込まなくても、新しい UI を動的に表示するには、API 呼び出しと、返されるデータに依存します。 クライアント側のレンダリングでは、エンドユーザーにはるかに高速より応答性の高いアプリケーションを提供します。

HTTP 呼び出しによってトリガーされるサーバーレスのエンドポイントは、API 要求を処理するために使用できます。 たとえば、ad のサービス会社では、カスタム広告を要求するユーザー プロファイル情報を使ってサーバーレス関数を呼び出すことができます。 サーバーレスの関数は、カスタム ad を返し、web ページに表示します。

![サーバーレス web API](./media/serverless-web-api.png)

## <a name="data-pipeline"></a>データ パイプライン

サーバーレスの関数は、データ パイプラインを容易にするために使用できます。 この例では、ファイルは、テーブル内のデータ行を CSV ファイル内のデータを変換する関数をトリガーします。 構成されたテーブルには、analytics をエンドユーザーに提示する Power BI ダッシュ ボードができます。

![サーバーレス データ パイプライン](./media/serverless-data-pipeline.png)

## <a name="stream-processing"></a>Stream の処理

デバイスとセンサーを多くの場合、リアルタイムで処理する必要があるデータのストリームを生成します。 メッセージとストリームからキャプチャできるテクノロジがいくつか[Event Hubs](https://docs.microsoft.com/azure/event-hubs/event-hubs-what-is-event-hubs)と[IoT Hub](https://docs.microsoft.com/azure/iot-hub)に[Service Bus](/service-bus)します。 トランスポートに関係なくサーバーレスでやり取りされるメッセージとデータのストリームを処理するための最適なメカニズムです。 サーバーレスは、大量のデータの需要に合わせて迅速にスケールできます。 サーバーレス コードでは、データと出力の処理と分析を構造化された形式で解析するビジネス ロジックを適用できます。

![サーバーレスのストリーム処理](./media/serverless-stream-processing.png)

## <a name="api-gateway"></a>API ゲートウェイ

API ゲートウェイは、単一のエントリ ポイントをクライアントに提供し、バックエンド サービスに要求をインテリジェントにルーティングします。 サービスのセットを管理すると便利です。 バージョン管理を処理して、クライアントをさまざまな環境を簡単に接続することで開発を簡略化します。 サーバーレスでは、API ゲートウェイ経由で 1 つのフロント エンドを提示しながら、バック エンドが個々 のマイクロ サービスのスケーリングを処理できます。

![サーバーレス API ゲートウェイ](./media/serverless-api-gateway.png)

## <a name="recommended-resources"></a>推奨リソース

* [Azure Event Grid](https://docs.microsoft.com/azure/event-grid/overview)
* [Azure IoT Hub](https://docs.microsoft.com/azure/iot-hub)
* [分散データ管理に関する課題とソリューション](../microservices-architecture/architect-microservice-container-applications/distributed-data-management.md)
* [マイクロ サービスの設計: マイクロ サービス境界を識別します。](https://docs.microsoft.com/azure/architecture/microservices/microservice-boundaries)
* [Event Hubs](https://docs.microsoft.com/azure/event-hubs/event-hubs-what-is-event-hubs)
* [イベント ソーシング パターン](https://docs.microsoft.com/azure/architecture/patterns/event-sourcing)
* [直流高速度遮断器パターンの実装](../microservices-architecture/implement-resilient-applications/implement-circuit-breaker-pattern.md)
* [IoT Hub](https://docs.microsoft.com/azure/iot-hub)
* [Service Bus](https://docs.microsoft.com/azure/service-bus)
* [Change feed サポートを Azure Cosmos DB での操作](https://docs.microsoft.com/azure/cosmos-db/change-feed)

>[!div class="step-by-step"]
>[前へ](serverless-architecture-considerations.md)
>[次へ](azure-serverless-platform.md)