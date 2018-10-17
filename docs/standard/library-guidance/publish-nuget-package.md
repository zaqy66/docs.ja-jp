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
# <a name="publishing-a-nuget-package"></a><span data-ttu-id="52042-103">NuGet パッケージを公開します。</span><span class="sxs-lookup"><span data-stu-id="52042-103">Publishing a NuGet package</span></span>

<span data-ttu-id="52042-104">NuGet パッケージは、発行され、パッケージ リポジトリから使用します。</span><span class="sxs-lookup"><span data-stu-id="52042-104">NuGet packages are published and consumed from package repositories.</span></span> <span data-ttu-id="52042-105">NuGet.org が既知で使用されているリポジトリで最も広く中には、NuGet パッケージを公開する多くの場所があります。</span><span class="sxs-lookup"><span data-stu-id="52042-105">While NuGet.org is the most widely known and used repository, there are many places to publish NuGet packages:</span></span>

* <span data-ttu-id="52042-106">**[NuGet.org](https://www.nuget.org/)** は NuGet パッケージのプライマリ、オンラインのリポジトリです。</span><span class="sxs-lookup"><span data-stu-id="52042-106">**[NuGet.org](https://www.nuget.org/)** is the primary online repository for NuGet packages.</span></span> <span data-ttu-id="52042-107">NuGet.org のすべてのパッケージは、すべてのユーザーに公開します。</span><span class="sxs-lookup"><span data-stu-id="52042-107">All packages on NuGet.org are publicly available to everyone.</span></span> <span data-ttu-id="52042-108">既定では、Visual Studio は、パッケージ ソースとして NuGet.org を持つし、多くの開発者の NuGet.org には、のみのパッケージ リポジトリとやり取りします。</span><span class="sxs-lookup"><span data-stu-id="52042-108">By default, Visual Studio has NuGet.org as a package source and for many developers NuGet.org is the only package repository they'll interact with.</span></span> <span data-ttu-id="52042-109">NuGet.org では、安定したパッケージとのコミュニティからのフィードバックを対象とするプレリリース パッケージを発行する最適な場所です。</span><span class="sxs-lookup"><span data-stu-id="52042-109">NuGet.org is the best place to publish stable packages and pre-release packages that you want community feedback on.</span></span>

* <span data-ttu-id="52042-110">**[MyGet](https://myget.org/)** リポジトリ サービス サポート[無料のカスタム パッケージは、オープン ソース プロジェクトのフィード](https://www.myget.org/opensource)します。</span><span class="sxs-lookup"><span data-stu-id="52042-110">**[MyGet](https://myget.org/)** repository service supports [free custom package feeds for open-source projects](https://www.myget.org/opensource).</span></span> <span data-ttu-id="52042-111">MyGet パブリック カスタム フィードとは、CI サービスによって作成されたプレリリース パッケージを発行するに最適です。</span><span class="sxs-lookup"><span data-stu-id="52042-111">A MyGet public custom feed is an ideal place to publish pre-release packages created by your CI service.</span></span> <span data-ttu-id="52042-112">MyGet はまた、プライベート フィードを商用提供します。</span><span class="sxs-lookup"><span data-stu-id="52042-112">MyGet also provides private feeds commercially.</span></span>

* <span data-ttu-id="52042-113">A **[ローカル フィード](/nuget/hosting-packages/local-feeds)** パッケージ リポジトリなどのフォルダーを扱うことができますになり、 `*.nupkg` NuGet によってアクセスできるフォルダー内のファイル。</span><span class="sxs-lookup"><span data-stu-id="52042-113">A **[local feed](/nuget/hosting-packages/local-feeds)** allows you to treat a folder like a package repository and makes the `*.nupkg` files in the folder accessible by NuGet.</span></span> <span data-ttu-id="52042-114">ローカル フィードは、NuGet パッケージを NuGet.org に公開する前にテストに便利です。</span><span class="sxs-lookup"><span data-stu-id="52042-114">A local feed is useful for testing a NuGet package before publishing it to NuGet.org.</span></span>

> [!NOTE]
> <span data-ttu-id="52042-115">NuGet.org[を削除するパッケージを許可しない](/nuget/policies/deleting-packages)アップロードしたら。</span><span class="sxs-lookup"><span data-stu-id="52042-115">NuGet.org [does not allow a package to be deleted](/nuget/policies/deleting-packages) once it is uploaded.</span></span> <span data-ttu-id="52042-116">UI で公開しないようににパッケージが一覧表示にすることができますが、`*.nupkg`復元で引き続きダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="52042-116">A package can be unlisted so that it is not publicly visible in the UI but the `*.nupkg` can still be downloaded on restore.</span></span> <span data-ttu-id="52042-117">また、nuget.org では、重複するパッケージのバージョンは許可されません。</span><span class="sxs-lookup"><span data-stu-id="52042-117">Also, nuget.org does not allow duplicate package versions.</span></span> <span data-ttu-id="52042-118">不正なパッケージを一覧から削除する必要があるエラーで NuGet パッケージを修正するには、バージョン番号をインクリメントし、パッケージの新しいバージョンを発行します。</span><span class="sxs-lookup"><span data-stu-id="52042-118">To correct a NuGet package with an error you have to unlist the incorrect package, increment the version number and publish a new version of the package.</span></span>

<span data-ttu-id="52042-119">**✔️ は**[安定版パッケージとプレリリース パッケージを発行](/nuget/create-packages/publish-a-package)NuGet.org にコミュニティからのフィードバックをします。</span><span class="sxs-lookup"><span data-stu-id="52042-119">**✔️ DO** [publish stable packages and pre-release packages](/nuget/create-packages/publish-a-package) you want community feedback on to NuGet.org.</span></span>

<span data-ttu-id="52042-120">**✔️ をご検討ください**継続的インテグレーション ビルドからフィードを MyGet にプレリリース パッケージを発行します。</span><span class="sxs-lookup"><span data-stu-id="52042-120">**✔️ CONSIDER** publishing pre-release packages to a MyGet feed from a continuous integration build.</span></span>

<span data-ttu-id="52042-121">**✔️ をご検討ください**ローカル フィードまたは MyGet を使用して、開発環境でパッケージをテストします。</span><span class="sxs-lookup"><span data-stu-id="52042-121">**✔️ CONSIDER** testing packages in your development environment using a local feed or MyGet.</span></span> <span data-ttu-id="52042-122">パッケージの動作を確認し、NuGet.org に公開します。</span><span class="sxs-lookup"><span data-stu-id="52042-122">Check the package works then publish it to NuGet.org.</span></span>

## <a name="nugetorg-security"></a><span data-ttu-id="52042-123">NuGet.org のセキュリティ</span><span class="sxs-lookup"><span data-stu-id="52042-123">NuGet.org security</span></span>

<span data-ttu-id="52042-124">悪意のあるユーザーが NuGet アカウントへのアクセスし、悪意のあるバージョンのライブラリをアップロードすることはできませんに重要です。</span><span class="sxs-lookup"><span data-stu-id="52042-124">It's important that bad actors can't access your NuGet account and upload a malicious version of your library.</span></span> <span data-ttu-id="52042-125">パッケージが発行されたときに、NuGet.org は 2 要素認証と電子メールの通知を提供します。</span><span class="sxs-lookup"><span data-stu-id="52042-125">NuGet.org offers two-factor authentication and email notifications when a package is published.</span></span> <span data-ttu-id="52042-126">NuGet.org にログインした後でこれらの機能を有効にする、**アカウント設定**ページ。</span><span class="sxs-lookup"><span data-stu-id="52042-126">Enable these features after logging into NuGet.org on the **Account settings** page.</span></span>

<span data-ttu-id="52042-127">![alt テキスト](./media/publish-nuget-package/nuget-2fa.png "NuGet アカウントのセキュリティ")</span><span class="sxs-lookup"><span data-stu-id="52042-127">![alt text](./media/publish-nuget-package/nuget-2fa.png "NuGet Account Security")</span></span>

<span data-ttu-id="52042-128">**✔️ は**NuGet へのサインインに Microsoft アカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="52042-128">**✔️ DO** use a Microsoft account to sign in to NuGet.</span></span>

<span data-ttu-id="52042-129">**✔️ は**NuGet にアクセスするための 2 要素認証を有効にします。</span><span class="sxs-lookup"><span data-stu-id="52042-129">**✔️ DO** enable two-factor authentication for accessing NuGet.</span></span>

<span data-ttu-id="52042-130">**✔️ は**パッケージが発行されたときに電子メール通知を有効にします。</span><span class="sxs-lookup"><span data-stu-id="52042-130">**✔️ DO** enable email notification when a package is published.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="52042-131">[前へ](./sourcelink.md)
[次へ](./versioning.md)</span><span class="sxs-lookup"><span data-stu-id="52042-131">[Previous](./sourcelink.md)
[Next](./versioning.md)</span></span>
