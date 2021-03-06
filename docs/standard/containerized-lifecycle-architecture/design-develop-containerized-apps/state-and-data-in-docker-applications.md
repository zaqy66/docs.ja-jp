---
title: Docker アプリケーションの状態とデータ
description: コンテナー化されたアプリケーションの状態の保存に利用可能なオプションをについて説明します。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 1e30a545ba0003acb8b85dee9896d54934f0d737
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/23/2019
ms.locfileid: "56745999"
---
# <a name="state-and-data-in-docker-applications"></a>Docker アプリケーションの状態とデータ

ほとんどの場合、コンテナーはプロセスのインスタンスと考えることができます。 プロセスは永続的な状態を維持しません。 コンテナーは、そのローカル ストレージに書き込むことができます、メモリ内の 1 つの場所にあるは持続性のあると仮定した場合などと仮定すると、インスタンスが無期限に存在します。 インスタンスが複数存在する、プロセスと同様に、コンテナー イメージを前提とし、強制終了最終的にはコンテナー オーケストレーターで管理されている、その必要がありますと見なされますことが移動する可能性が 1 つのノードまたは VM 間。

Docker アプリケーションで永続的なデータを管理するには、次のソリューションを使用します。

Docker ホストから、[Docker ボリューム](https://docs.docker.com/engine/admin/volumes/)として: 

- **ボリューム**は Docker によって管理されるホスト ファイル システムの領域に格納されます。

- **バインド マウント**アクセスの Docker プロセスから制御することはできず、セキュリティ上の問題は、コンテナーが機密性の高い OS フォルダーにアクセスできますので、ホスト ファイル システム内の任意のフォルダーにマップできます。

- **tmpfs マウント**は、ホストのメモリ内にのみ存在していてファイル システムに決して書き込まれない仮想フォルダーに似ています。

リモート ストレージから: 

- [Azure Storage](https://azure.microsoft.com/documentation/services/storage/)最適な長期的な永続化ソリューションを提供するコンテナーの地理的に分散可能なのストレージを提供します。

- などのリレーショナル データベースがリモート[Azure SQL Database](https://azure.microsoft.com/services/sql-database/)などの NoSQL データベース[Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/introduction)、ようなキャッシュ サービス[Redis](https://redis.io/)します。

Docker コンテナーから:

- Docker には、*オーバーレイ ファイル システム*という機能があります。 この機能は、コンテナーのルート ファイル システムに更新された情報を格納するコピー オン ライト タスクを実装します。 その情報「レイアウトの上部に」コンテナーの基になる元のイメージ。 コンテナーがシステムから削除された場合、それらの変更は失われます。 そのため、ローカル ストレージ内のコンテナーの状態を保存することはできますが既定では、ステートレス、コンテナー設計の内部設置型と競合するこの機能に基づくシステムを設計します。

- ただし、Docker ボリュームは Docker でのローカルのデータを処理することをお勧めします。 詳細については、ストレージ コンテナーには、必要がある場合を確認[Docker 記憶装置ドライバー](https://docs.docker.com/engine/userguide/storagedriver/)と[イメージ、コンテナー、および記憶域ドライバーについて](https://docs.docker.com/engine/userguide/storagedriver/imagesandcontainers/)します。

次の例は、これらのオプションに関する追加情報を提供します。

**ボリューム**は、ホスト OS からコンテナー内のディレクトリにマップされたディレクトリです。 コンテナー内のコードがディレクトリへのアクセス権を持っている場合、それは実際にはホスト OS 上のディレクトリに対するアクセス権です。 このディレクトリはコンテナー自体の有効期間に関連付けられていません。さらにディレクトリは Docker によって管理され、ホスト マシンのコア機能から分離されています。 したがって、データ ボリュームは、コンテナーの有効期間とは独立してデータを保持するように設計されます。 Docker ホストからコンテナーまたはイメージを削除した場合、データ ボリュームに保持されているデータは削除されません。

ボリュームについては、名前を付けることも匿名 (既定) とすることもできます。 名前付きボリュームは、**データ ボリューム コンテナー**が進化したものです。これにより、コンテナー間でのデータの共有が簡単になります。 ボリュームには、その他のオプション間でのリモート ホストにデータを格納するためのボリューム ドライバーもサポートします。

**バインド マウント**長期間使用されているし、任意のフォルダーをコンテナーにマウント ポイントへのマッピングを許可します。 バインド マウントにはボリュームよりも多くの制限があるほか、重要なセキュリティ上の問題もあるため、ボリュームの方をお勧めします。

**`tmpfs` マウント**仮想フォルダーが、ホストのメモリ内にのみ live し、ファイル システムに書き込まれません。 これは、高速で安全ですがメモリを消費するため、非永続的なデータのためだけに用意されています。

図 4-5 に示すように、通常の Docker ボリュームは、コンテナー自体の外部 (ただし、ホスト サーバーまたは VM の物理的境界内) に格納できます。 ただし、Docker コンテナーは、あるホスト サーバーまたは VM から別のホスト サーバーまたは VM のボリュームにアクセスすることはできません。 つまり、これらのボリュームをリモート ホストをサポートしているボリューム ドライバーを達成できるが、異なる Docker ホスト上で実行されるコンテナー間で共有されるデータを管理することはできません。

![リモート ホストをサポートするリモート ドライバーを使用していない場合、コンテナー間でのボリュームの共有は同一ホスト内でのみ可能です。 ](./media/image5.png)

**図 4-5** コンテナーベースのアプリケーション向けのボリュームと外部データ ソース

さらに、オーケストレーターにより Docker コンテナーが管理される場合、クラスターによって実行される最適化に応じて、ホスト間でコンテナーが移動する可能性があります。 そのため、ビジネス データにデータ ボリュームを使用することはお勧めしません。 ただし、トレース ファイル、テンポラル ファイルなどを使用する優れたメカニズムはまたはと同様に、影響を与えないビジネス データの一貫性。

Azure SQL Database、Azure Cosmos DB のような**リモート データ ソースとキャッシュ**、または Redis のようなリモート キャッシュは、コンテナーなしで開発する場合と同じ方法でコンテナー化アプリケーションで使用できます。 これは、ビジネス アプリケーション データを格納する実績のある方法です。

**Azure Storage。** ビジネス データは、通常、外部リソースや Azure Storage などのデータベースに配置する必要があります。 Azure Storage では、クラウド内の次のサービスを提供します。

- BLOB ストレージには、非構造化オブジェクト データが格納されます。 BLOB は、ドキュメントやメディア ファイル (画像、オーディオ、ビデオ ファイル) など、任意の種類のテキストまたはバイナリ データの可能性があります。 BLOB ストレージは、オブジェクト ストレージとも呼ばれます。

- ファイル ストレージは、標準の SMB プロトコルを使用してレガシ アプリケーション用の共有ストレージを提供します。 Azure 仮想マシンとクラウド サービスは、マウントされた共有を介してアプリケーション コンポーネント全体でファイル データを共有できます。 オンプレミス アプリケーションには、ファイル サービス REST API を介して、共有内のファイル データにアクセスできます。

- テーブル ストレージには、構造化データセットが格納されます。 テーブル ストレージは NoSQL のキー属性データ ストアであり、迅速な開発と大量のデータへの高速アクセスが可能です。

**リレーショナル データベースと NoSQL データベース。** 外部データベースには、SQL Server、PostgreSQL、Oracle のようなリレーショナル データベースや、Azure Cosmos DB、MongoDB のような NoSQL データベースなど、多くの選択肢があります。これらのデータベースには、まったく別のトピックがあるため、このガイドの一部として説明はしません。

>[!div class="step-by-step"]
>[前へ](monolithic-applications.md)
>[次へ](soa-applications.md)
