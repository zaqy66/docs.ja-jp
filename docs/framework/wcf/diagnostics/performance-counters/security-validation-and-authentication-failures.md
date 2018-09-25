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
# <a name="security-validation-and-authentication-failures"></a><span data-ttu-id="4b267-102">セキュリティ検証と認証エラー</span><span class="sxs-lookup"><span data-stu-id="4b267-102">Security Validation and Authentication Failures</span></span>
<span data-ttu-id="4b267-103">カウンター名 : セキュリティ検証と認証エラー</span><span class="sxs-lookup"><span data-stu-id="4b267-103">Counter name: Security Validation and Authentication Failures</span></span>  
  
## <a name="description"></a><span data-ttu-id="4b267-104">説明</span><span class="sxs-lookup"><span data-stu-id="4b267-104">Description</span></span>  
 <span data-ttu-id="4b267-105">このカウンターは、"承認されていないセキュリティ呼び出し" カウンターでカウントの対象とならないセキュリティ上の問題が原因でメッセージが拒否されるたびにインクリメントされます。</span><span class="sxs-lookup"><span data-stu-id="4b267-105">This counter is incremented whenever a message is rejected due to a security problem not covered by the "Security Calls Not Authorized" counter.</span></span> <span data-ttu-id="4b267-106">この問題には、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="4b267-106">Such problems include:</span></span>  
  
-   <span data-ttu-id="4b267-107">メッセージからクライアント トークンを読み取ることができない。</span><span class="sxs-lookup"><span data-stu-id="4b267-107">Client token cannot be read from the message.</span></span>  
  
-   <span data-ttu-id="4b267-108">クライアント トークンが認証に失敗した (例 : 無効なパスワード)。</span><span class="sxs-lookup"><span data-stu-id="4b267-108">Client token has failed authentication (for example, bad password).</span></span>  
  
-   <span data-ttu-id="4b267-109">署名の検証に失敗した (例 : メッセージが改ざんされた)。</span><span class="sxs-lookup"><span data-stu-id="4b267-109">Signature verification has failed (for example, the message has been tampered).</span></span>  
  
-   <span data-ttu-id="4b267-110">メッセージが以前のメッセージと重複する。この現象はリプレイ攻撃中に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="4b267-110">The message is a duplicate from a previous one, which can happen during a replay attack.</span></span>  
  
-   <span data-ttu-id="4b267-111">復号化に失敗した。</span><span class="sxs-lookup"><span data-stu-id="4b267-111">A decryption failure has occurred.</span></span>  
  
-   <span data-ttu-id="4b267-112">一部の必須要素 (タイムスタンプ、暗号化データ ブロックなど) がメッセージにない。</span><span class="sxs-lookup"><span data-stu-id="4b267-112">Some required elements (for example, missing timestamp or encrypted data block) are missing from the message.</span></span>  
  
-   <span data-ttu-id="4b267-113">TLSNEGO/SPNEGO ハンドシェイク中にエラーが発生した。</span><span class="sxs-lookup"><span data-stu-id="4b267-113">Errors have occurred during TLSNEGO/SPNEGO handshake.</span></span>
