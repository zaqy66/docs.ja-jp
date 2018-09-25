---
title: 'サービス : セキュリティ検証と認証エラー'
ms.date: 03/30/2017
ms.assetid: 55c98268-b1ad-459d-851b-25ef52248187
author: BrucePerlerMS
ms.openlocfilehash: 4c74cb1962bbc0f03ac33d8fcc7b10052bec8273
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47077293"
---
# <a name="service-security-validation-and-authentication-failures"></a><span data-ttu-id="dfdac-102">サービス : セキュリティ検証と認証エラー</span><span class="sxs-lookup"><span data-stu-id="dfdac-102">Service: Security Validation and Authentication Failures</span></span>
<span data-ttu-id="dfdac-103">カウンター名 : セキュリティ検証と認証エラー</span><span class="sxs-lookup"><span data-stu-id="dfdac-103">Counter name: Security Validation and Authentication Failures</span></span>  
  
## <a name="description"></a><span data-ttu-id="dfdac-104">説明</span><span class="sxs-lookup"><span data-stu-id="dfdac-104">Description</span></span>  
 <span data-ttu-id="dfdac-105">このカウンターは、"承認されていないセキュリティ呼び出し" カウンターでカウントの対象とならないセキュリティ上の問題が原因でメッセージが拒否されるたびにインクリメントされます。</span><span class="sxs-lookup"><span data-stu-id="dfdac-105">This counter is incremented whenever a message is rejected due to a security problem not covered by the "Security Calls Not Authorized" counter.</span></span> <span data-ttu-id="dfdac-106">この問題には、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="dfdac-106">Such problems include:</span></span>  
  
-   <span data-ttu-id="dfdac-107">メッセージからクライアント トークンを読み取ることができない。</span><span class="sxs-lookup"><span data-stu-id="dfdac-107">Client token cannot be read from the message.</span></span>  
  
-   <span data-ttu-id="dfdac-108">クライアント トークンが認証に失敗した (例 : 無効なパスワード)。</span><span class="sxs-lookup"><span data-stu-id="dfdac-108">Client token has failed authentication (for example,, bad password).</span></span>  
  
-   <span data-ttu-id="dfdac-109">署名の検証に失敗した (例 : メッセージが改ざんされた)。</span><span class="sxs-lookup"><span data-stu-id="dfdac-109">Signature verification has failed (for example,, the message has been tampered).</span></span>  
  
-   <span data-ttu-id="dfdac-110">メッセージが以前のメッセージと重複する。この現象はリプレイ攻撃中に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="dfdac-110">The message is a duplicate from a previous one, which can happen during a replay attack.</span></span>  
  
-   <span data-ttu-id="dfdac-111">復号化に失敗した。</span><span class="sxs-lookup"><span data-stu-id="dfdac-111">A decryption failure has occurred.</span></span>  
  
-   <span data-ttu-id="dfdac-112">一部の必須要素 (タイムスタンプ、暗号化データ ブロックなど) がメッセージにない。</span><span class="sxs-lookup"><span data-stu-id="dfdac-112">Some required elements (for example,, missing timestamp or encrypted data block) are missing from the message.</span></span>  
  
-   <span data-ttu-id="dfdac-113">TLSNEGO/SPNEGO ハンドシェイク中にエラーが発生した。</span><span class="sxs-lookup"><span data-stu-id="dfdac-113">Errors have occurred during TLSNEGO/SPNEGO handshake.</span></span>
