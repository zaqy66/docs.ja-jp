---
title: セキュリティ検証と認証エラー
ms.date: 03/30/2017
ms.assetid: 0d4e3666-dfc6-421c-baf8-9479c22f7050
author: BrucePerlerMS
ms.openlocfilehash: d13e94800d71c6f567c6aab61974e42b1a3f1706
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47070943"
---
# <a name="security-validation-and-authentication-failures"></a>セキュリティ検証と認証エラー
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
