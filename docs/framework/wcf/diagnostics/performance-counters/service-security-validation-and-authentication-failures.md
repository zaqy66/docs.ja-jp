---
title: 'サービス : セキュリティ検証と認証エラー'
ms.date: 03/30/2017
ms.assetid: 55c98268-b1ad-459d-851b-25ef52248187
ms.openlocfilehash: ba8da3ae6be6bd089690359f19e153da1e0b54fc
ms.sourcegitcommit: 5fd80619c760fa8c25d33a6f5661247cb65da465
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2018
ms.locfileid: "50744250"
---
# <a name="service-security-validation-and-authentication-failures"></a>サービス : セキュリティ検証と認証エラー
カウンター名 : セキュリティ検証と認証エラー  
  
## <a name="description"></a>説明  
 このカウンターは、"承認されていないセキュリティ呼び出し" カウンターでカウントの対象とならないセキュリティ上の問題が原因でメッセージが拒否されるたびにインクリメントされます。 この問題には、次のようなものがあります。  
  
-   メッセージからクライアント トークンを読み取ることができない。  
  
-   クライアント トークンが認証に失敗した (例 : 無効なパスワード)。  
  
-   署名の検証に失敗した (例 : メッセージが改ざんされた)。  
  
-   メッセージが以前のメッセージと重複する。この現象はリプレイ攻撃中に発生することがあります。  
  
-   復号化に失敗した。  
  
-   一部の必須要素 (タイムスタンプ、暗号化データ ブロックなど) がメッセージにない。  
  
-   TLSNEGO/SPNEGO ハンドシェイク中にエラーが発生した。
