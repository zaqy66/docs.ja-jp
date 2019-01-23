---
title: オンライン ステータスとオフライン ステータスの追加
ms.date: 03/30/2017
ms.assetid: 05e5f51d-81b6-4c17-b364-9dda447a5fce
ms.openlocfilehash: 6a04648e4251774538d298b35d1d655e09e03495
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54591901"
---
# <a name="adding-online-and-offline-status"></a>オンライン ステータスとオフライン ステータスの追加
多くの場合、アプリケーションではピア チャネル接続のステータスについて明確な詳細情報を監視することが重要です。 この情報は、`GetProperty` インターフェイスの実装で <xref:System.ServiceModel.IOnlineStatus> メソッドを呼び出すことで取得できます。 このインターフェイスを実装するオブジェクトは、接続ステータスを監視したり、`OnOnline` や `OnOffline` などのイベント ハンドラーを登録したりできるため、オンライン ステータスに変化があると即座に反応できます。  
  
 ピア チャネル インフラストラクチャでは、クライアントが少なくとも 1 つのピアに接続されているとオンラインと見なされ、そうでない場合はオフラインと見なされます。 このことは、開発中のアプリケーションをデバッグする際や、エンド ユーザーに詳細情報を表示する際に特に役立ちます。  
  
> [!NOTE]
>  オンライン イベント ハンドラーでは、メッセージを送信する前に、まず、ノードが開いていることを確認する必要があります。  
  
## <a name="see-also"></a>関連項目
- [ピア チャネル アプリケーションの構築](../../../../docs/framework/wcf/feature-details/building-a-peer-channel-application.md)
