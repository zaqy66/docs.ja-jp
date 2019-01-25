---
title: 信頼できるセッション
ms.date: 03/30/2017
f1_keywords:
- Windows Communication Foundation, sessions and instances
- WCF, sessions and instances
- sessions and instances [WCF]
helpviewer_keywords:
- instances [WCF]
- sessions [WCF]
ms.assetid: 143951b3-3aa0-4540-b4b7-d33e77e874a1
ms.openlocfilehash: 1d87f6f4d94763dc8f6ac7e929c22b17940097ca
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54735426"
---
# <a name="reliable-sessions"></a>信頼できるセッション

このセクションでは、どのような Windows Communication Foundation (WCF) 信頼できるセッションが、用途も、方法およびと 1 つを使用するバインド構成をサポートしのポインターのベスト プラクティスについて説明します。 このセクションの重要なポイントと関連するトピックの詳細について、次の表にまとめます。

信頼できるセッションが WCF には、エンドポイント間で送信されるメッセージが SOAP またはトランスポート中継ぎ局を介して転送して、1 回のみと、必要に応じて、送信された順序で配信されることを確認する機能が用意されています。

で WCF アプリケーションを信頼できるセッションを使用するには、既定またはオプションとして、信頼できるセッションをサポートして WCF でのシステム提供バインディングのいずれかを使用するか、セッションをサポートする独自のカスタム バインドを作成します。

## <a name="in-this-section"></a>このセクションの内容

[信頼できるセッションの概要](../../../../docs/framework/wcf/feature-details/reliable-sessions-overview.md)   
信頼できるセッションの概要、信頼できるセッションを使用する状況、信頼できるセッションをサポートする各種のバインディング、および動作のしくみについて説明します。

[方法: 信頼できるセッション内でメッセージを交換](../../../../docs/framework/wcf/feature-details/how-to-exchange-messages-within-a-reliable-session.md)   
構成で指定したカスタム バインドを使用して、HTTP 上で信頼できるセッションを作成する方法を説明します。

[方法: 信頼できるセッション内でメッセージをセキュリティ保護します。](../../../../docs/framework/wcf/feature-details/how-to-secure-messages-within-reliable-sessions.md)   
信頼できるセッションを保護する方法について説明します。

[方法: HTTPS で信頼できるセッションをカスタム バインディングを作成します。](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md)   
HTTPS 上で信頼できるセッションを作成する方法について説明します。

[信頼できるセッションのベスト プラクティス](../../../../docs/framework/wcf/feature-details/best-practices-for-reliable-sessions.md)   
信頼できるセッションの使用に関するベスト プラクティスについて説明します。

## <a name="reference"></a>参照

<xref:System.ServiceModel.ReliableSession>

## <a name="see-also"></a>関連項目

- [キューと信頼できるセッション](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md)
- [セッション、インスタンス化、およびコンカレンシー](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)
