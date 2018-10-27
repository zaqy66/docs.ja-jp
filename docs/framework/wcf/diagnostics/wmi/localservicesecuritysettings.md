---
title: LocalServiceSecuritySettings
ms.date: 03/30/2017
ms.assetid: 490aa0e5-5242-4f8d-b505-5ec6287633b4
ms.openlocfilehash: c1f3abe2d016ccab9b136752c4b2e6697ca59e66
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188847"
---
# <a name="localservicesecuritysettings"></a><span data-ttu-id="71c9b-102">LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="71c9b-102">LocalServiceSecuritySettings</span></span>
<span data-ttu-id="71c9b-103">LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="71c9b-103">LocalServiceSecuritySettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="71c9b-104">構文</span><span class="sxs-lookup"><span data-stu-id="71c9b-104">Syntax</span></span>  
  
```csharp
class LocalServiceSecuritySettings  
{  
  boolean DetectReplays;  
  datetime InactivityTimeout;  
  datetime IssuedCookieLifetime;  
  sint32 MaxCachedCookies;  
  datetime MaxClockSkew;  
  sint32 MaxPendingSessions;  
  sint32 MaxStatefulNegotiations;  
  datetime NegotiationTimeout;  
  boolean ReconnectTransportOnFailure;  
  sint32 ReplayCacheSize;  
  datetime ReplayWindow;  
  datetime SessionKeyRenewalInterval;  
  datetime SessionKeyRolloverInterval;  
  datetime TimestampValidityDuration;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="71c9b-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="71c9b-105">Methods</span></span>  
 <span data-ttu-id="71c9b-106">LocalServiceSecuritySettings クラスで定義されるメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="71c9b-106">The LocalServiceSecuritySettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="71c9b-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="71c9b-107">Properties</span></span>  
 <span data-ttu-id="71c9b-108">LocalServiceSecuritySettings クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="71c9b-108">The LocalServiceSecuritySettings class has the following properties:</span></span>  
  
### <a name="detectreplays"></a><span data-ttu-id="71c9b-109">DetectReplays</span><span class="sxs-lookup"><span data-stu-id="71c9b-109">DetectReplays</span></span>  
 <span data-ttu-id="71c9b-110">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="71c9b-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="71c9b-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-112">チャネルに対するリプレイ攻撃を検出し、自動的に処理するかどうかを指定するブール値です。</span><span class="sxs-lookup"><span data-stu-id="71c9b-112">A Boolean value that specifies whether replay attacks against the channel are detected and dealt with automatically.</span></span>  
  
### <a name="inactivitytimeout"></a><span data-ttu-id="71c9b-113">InactivityTimeout</span><span class="sxs-lookup"><span data-stu-id="71c9b-113">InactivityTimeout</span></span>  
 <span data-ttu-id="71c9b-114">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="71c9b-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="71c9b-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-116">サービスがサポートする保留状態のセキュリティ セッションの最大数。</span><span class="sxs-lookup"><span data-stu-id="71c9b-116">The maximum number of pending security sessions that the service supports.</span></span>  
  
### <a name="issuedcookielifetime"></a><span data-ttu-id="71c9b-117">IssuedCookieLifetime</span><span class="sxs-lookup"><span data-stu-id="71c9b-117">IssuedCookieLifetime</span></span>  
 <span data-ttu-id="71c9b-118">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="71c9b-118">Data type: datetime</span></span>  
  
 <span data-ttu-id="71c9b-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-120">すべての新しいセキュリティ クッキーに対して発行する有効期間を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="71c9b-120">A TimeSpan that specifies the lifetime issued to all new security cookies.</span></span>  
  
### <a name="maxcachedcookies"></a><span data-ttu-id="71c9b-121">MaxCachedCookies</span><span class="sxs-lookup"><span data-stu-id="71c9b-121">MaxCachedCookies</span></span>  
 <span data-ttu-id="71c9b-122">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="71c9b-122">Data type: sint32</span></span>  
  
 <span data-ttu-id="71c9b-123">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-124">キャッシュできるクッキーの最大数。</span><span class="sxs-lookup"><span data-stu-id="71c9b-124">The maximum number of cookies that can be cached.</span></span>  
  
### <a name="maxclockskew"></a><span data-ttu-id="71c9b-125">MaxClockSkew</span><span class="sxs-lookup"><span data-stu-id="71c9b-125">MaxClockSkew</span></span>  
 <span data-ttu-id="71c9b-126">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="71c9b-126">Data type: datetime</span></span>  
  
 <span data-ttu-id="71c9b-127">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-128">通信している双方の 2 つのシステム クロックのずれの最長時間を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="71c9b-128">A TimeSpan that specifies the maximum time difference between the system clocks of the two communicating parties.</span></span>  
  
### <a name="maxpendingsessions"></a><span data-ttu-id="71c9b-129">MaxPendingSessions</span><span class="sxs-lookup"><span data-stu-id="71c9b-129">MaxPendingSessions</span></span>  
 <span data-ttu-id="71c9b-130">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="71c9b-130">Data type: sint32</span></span>  
  
 <span data-ttu-id="71c9b-131">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-132">サービスにおける保留状態の接続の最大数です。</span><span class="sxs-lookup"><span data-stu-id="71c9b-132">The maximum number of pending connections on the service.</span></span>  
  
### <a name="maxstatefulnegotiations"></a><span data-ttu-id="71c9b-133">MaxStatefulNegotiations</span><span class="sxs-lookup"><span data-stu-id="71c9b-133">MaxStatefulNegotiations</span></span>  
 <span data-ttu-id="71c9b-134">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="71c9b-134">Data type: sint32</span></span>  
  
 <span data-ttu-id="71c9b-135">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-136">同時にアクティブにできるセキュリティ ネゴシエーションの数。</span><span class="sxs-lookup"><span data-stu-id="71c9b-136">The number of security negotiations that can be active concurrently.</span></span>  
  
### <a name="negotiationtimeout"></a><span data-ttu-id="71c9b-137">NegotiationTimeout</span><span class="sxs-lookup"><span data-stu-id="71c9b-137">NegotiationTimeout</span></span>  
 <span data-ttu-id="71c9b-138">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="71c9b-138">Data type: datetime</span></span>  
  
 <span data-ttu-id="71c9b-139">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-140">サーバーとクライアント間のセキュリティ ネゴシエーション フェーズの最大継続時間を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="71c9b-140">A TimeSpan that specifies the maximum duration for the security negotiation phase between server and client.</span></span>  
  
### <a name="reconnecttransportonfailure"></a><span data-ttu-id="71c9b-141">ReconnectTransportOnFailure</span><span class="sxs-lookup"><span data-stu-id="71c9b-141">ReconnectTransportOnFailure</span></span>  
 <span data-ttu-id="71c9b-142">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="71c9b-142">Data type: boolean</span></span>  
  
 <span data-ttu-id="71c9b-143">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-144">WS-ReliableMessaging を使用した接続が、トランスポート エラーの後再接続を試みるかどうかを指定するブール値です。</span><span class="sxs-lookup"><span data-stu-id="71c9b-144">A Boolean value that specifies whether connections using WS-Reliable messaging attempt to reconnect after transport failures.</span></span>  
  
### <a name="replaycachesize"></a><span data-ttu-id="71c9b-145">ReplayCacheSize</span><span class="sxs-lookup"><span data-stu-id="71c9b-145">ReplayCacheSize</span></span>  
 <span data-ttu-id="71c9b-146">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="71c9b-146">Data type: sint32</span></span>  
  
 <span data-ttu-id="71c9b-147">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-148">リプレイ検証で使用されるキャッシュ済みの nonce の数。</span><span class="sxs-lookup"><span data-stu-id="71c9b-148">The number of cached nonces used for replay detection.</span></span>  
  
### <a name="replaywindow"></a><span data-ttu-id="71c9b-149">ReplayWindow</span><span class="sxs-lookup"><span data-stu-id="71c9b-149">ReplayWindow</span></span>  
 <span data-ttu-id="71c9b-150">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="71c9b-150">Data type: datetime</span></span>  
  
 <span data-ttu-id="71c9b-151">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-152">個別のメッセージの nonce の有効期間を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="71c9b-152">A TimeSpan that specifies the duration in which individual message nonces are valid.</span></span>  
  
### <a name="sessionkeyrenewalinterval"></a><span data-ttu-id="71c9b-153">SessionKeyRenewalInterval</span><span class="sxs-lookup"><span data-stu-id="71c9b-153">SessionKeyRenewalInterval</span></span>  
 <span data-ttu-id="71c9b-154">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="71c9b-154">Data type: datetime</span></span>  
  
 <span data-ttu-id="71c9b-155">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-156">イニシエーターがセキュリティ セッションのキーを更新するまでの期間を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="71c9b-156">A TimeSpan that specifies the duration after which the initiator renews the key for the security session.</span></span>  
  
### <a name="sessionkeyrolloverinterval"></a><span data-ttu-id="71c9b-157">SessionKeyRolloverInterval</span><span class="sxs-lookup"><span data-stu-id="71c9b-157">SessionKeyRolloverInterval</span></span>  
 <span data-ttu-id="71c9b-158">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="71c9b-158">Data type: datetime</span></span>  
  
 <span data-ttu-id="71c9b-159">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-159">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-160">キーの更新中に、前のセッション キーが受信メッセージで有効な時間間隔を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="71c9b-160">A TimeSpan that specifies the time interval a previous session key is valid on incoming messages during a key renewal.</span></span>  
  
### <a name="timestampvalidityduration"></a><span data-ttu-id="71c9b-161">TimestampValidityDuration</span><span class="sxs-lookup"><span data-stu-id="71c9b-161">TimestampValidityDuration</span></span>  
 <span data-ttu-id="71c9b-162">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="71c9b-162">Data type: datetime</span></span>  
  
 <span data-ttu-id="71c9b-163">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="71c9b-163">Access type: Read-only</span></span>  
  
 <span data-ttu-id="71c9b-164">タイムスタンプの有効期間を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="71c9b-164">A TimeSpan that specifies the duration in which a time stamp is valid.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="71c9b-165">必要条件</span><span class="sxs-lookup"><span data-stu-id="71c9b-165">Requirements</span></span>  
  
|<span data-ttu-id="71c9b-166">MOF</span><span class="sxs-lookup"><span data-stu-id="71c9b-166">MOF</span></span>|<span data-ttu-id="71c9b-167">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="71c9b-167">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="71c9b-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="71c9b-168">Namespace</span></span>|<span data-ttu-id="71c9b-169">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="71c9b-169">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="71c9b-170">関連項目</span><span class="sxs-lookup"><span data-stu-id="71c9b-170">See Also</span></span>  
 <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
