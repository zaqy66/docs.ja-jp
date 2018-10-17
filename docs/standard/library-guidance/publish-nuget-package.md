---
title: NuGet パッケージを公開します。
description: .NET ライブラリを NuGet に公開するための推奨されるベスト プラクティスです。
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 0602712311411ef3d59825bec8c5e550bc8d8265
ms.sourcegitcommit: d88024e6d6d8b242feae5f4007a709379355aa24
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2018
ms.locfileid: "49370323"
---
# <a name="publishing-a-nuget-package"></a>NuGet パッケージを公開します。

NuGet パッケージは、発行され、パッケージ リポジトリから使用します。 NuGet.org が既知で使用されているリポジトリで最も広く中には、NuGet パッケージを公開する多くの場所があります。

* **[NuGet.org](https://www.nuget.org/)** は NuGet パッケージのプライマリ、オンラインのリポジトリです。 NuGet.org のすべてのパッケージは、すべてのユーザーに公開します。 既定では、Visual Studio は、パッケージ ソースとして NuGet.org を持つし、多くの開発者の NuGet.org には、のみのパッケージ リポジトリとやり取りします。 NuGet.org では、安定したパッケージとのコミュニティからのフィードバックを対象とするプレリリース パッケージを発行する最適な場所です。

* **[MyGet](https://myget.org/)** リポジトリ サービス サポート[無料のカスタム パッケージは、オープン ソース プロジェクトのフィード](https://www.myget.org/opensource)します。 MyGet パブリック カスタム フィードとは、CI サービスによって作成されたプレリリース パッケージを発行するに最適です。 MyGet はまた、プライベート フィードを商用提供します。

* A **[ローカル フィード](/nuget/hosting-packages/local-feeds)** パッケージ リポジトリなどのフォルダーを扱うことができますになり、 `*.nupkg` NuGet によってアクセスできるフォルダー内のファイル。 ローカル フィードは、NuGet パッケージを NuGet.org に公開する前にテストに便利です。

> [!NOTE]
> NuGet.org[を削除するパッケージを許可しない](/nuget/policies/deleting-packages)アップロードしたら。 UI で公開しないようににパッケージが一覧表示にすることができますが、`*.nupkg`復元で引き続きダウンロードできます。 また、nuget.org では、重複するパッケージのバージョンは許可されません。 不正なパッケージを一覧から削除する必要があるエラーで NuGet パッケージを修正するには、バージョン番号をインクリメントし、パッケージの新しいバージョンを発行します。

**✔️ は**[安定版パッケージとプレリリース パッケージを発行](/nuget/create-packages/publish-a-package)NuGet.org にコミュニティからのフィードバックをします。

**✔️ をご検討ください**継続的インテグレーション ビルドからフィードを MyGet にプレリリース パッケージを発行します。

**✔️ をご検討ください**ローカル フィードまたは MyGet を使用して、開発環境でパッケージをテストします。 パッケージの動作を確認し、NuGet.org に公開します。

## <a name="nugetorg-security"></a>NuGet.org のセキュリティ

悪意のあるユーザーが NuGet アカウントへのアクセスし、悪意のあるバージョンのライブラリをアップロードすることはできませんに重要です。 パッケージが発行されたときに、NuGet.org は 2 要素認証と電子メールの通知を提供します。 NuGet.org にログインした後でこれらの機能を有効にする、**アカウント設定**ページ。

![alt テキスト](./media/publish-nuget-package/nuget-2fa.png "NuGet アカウントのセキュリティ")

**✔️ は**NuGet へのサインインに Microsoft アカウントを使用します。

**✔️ は**NuGet にアクセスするための 2 要素認証を有効にします。

**✔️ は**パッケージが発行されたときに電子メール通知を有効にします。

>[!div class="step-by-step"]
[前へ](./sourcelink.md)
[次へ](./versioning.md)
