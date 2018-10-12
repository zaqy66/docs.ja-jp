---
title: Docker コンテナー用 .NET Core と .NET Framework の選択
description: '.NET マイクロサービス: コンテナー化された .NET アプリケーションのアーキテクチャ | Docker コンテナー用 .NET Core と .NET Framework の選択'
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/11/2018
ms.openlocfilehash: 9abff2614e4022408a069be25440196111db19ab
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2018
ms.locfileid: "46562110"
---
# <a name="choosing-between-net-core-and-net-framework-for-docker-containers"></a>Docker コンテナー用 .NET Core と .NET Framework の選択

.NET を使用してサーバー側のコンテナー化された Docker アプリケーションをビルドする場合に選択できるサポート対象のフレームワークには、[.NET Framework と .NET Core](https://www.microsoft.com/net/download) の 2 つがあります。 それらは多数の .NET プラットフォームのコンポーネントを共有しているため、両者でコードを共有できます。 ただし、それらには基本的な違いがあり、どちらのフレームワークを使用するかは実行内容によって決まります。 このセクションでは、それぞれのフレームワークを選択する場合のガイダンスを提供します。


>[!div class="step-by-step"]
[前へ](../container-docker-introduction/docker-containers-images-registries.md)
[次へ](general-guidance.md)
