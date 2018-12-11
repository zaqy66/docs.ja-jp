---
title: Docker アプリケーションを設計します。
description: Microsoft プラットフォームとツールでコンテナー化された Docker アプリケーションのライフサイクル
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/21/2017
ms.openlocfilehash: d02cec0595024eb7bd7c0ac46df093359680da74
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53155380"
---
# <a name="design-docker-applications"></a>Docker アプリケーションを設計します。

第 1 章には、コンテナーと Docker に関する基本的な概念が導入されました。 その情報は、開始に必要な情報の基本的なレベルです。 ただし、1 つのサービスまたはコンテナーではなく複数のサービスで構成され、複雑なエンタープライズ アプリケーションを指定できます。 これらの省略可能なユース ケースでは、オーケストレーションの概念デザイン、サービス指向アーキテクチャ (SOA) より高度なマイクロ サービスの概念とコンテナーに追加の手法を把握する必要があります。 このドキュメントのスコープはマイクロ サービスに限定されませんが、Docker アプリケーションのライフ サイクルそのため、ことはできませんを参照してくださいマイクロ サービス アーキテクチャの詳細も正規サンパウロ、バック グラウンド タスクまたはジョブ、コンテナーと Docker を使用したりもためモノリシック アプリケーション展開のアプローチです。

ただし、アプリケーションのライフ サイクル、DevOps に入る前に、設計を行う方法を知るし、アプリケーションと、デザインの選択肢は何を構築を必要があります。

>[!div class="step-by-step"]
>[前へ](index.md)
>[次へ](common-container-design-principles.md)