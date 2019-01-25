---
title: LocalServiceSecuritySettings
ms.date: 03/30/2017
ms.assetid: 490aa0e5-5242-4f8d-b505-5ec6287633b4
ms.openlocfilehash: 5c68706c5dcec3a5b0ec62bb9cfbea4e1496b4f6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574600"
---
# <a name="localservicesecuritysettings"></a><span data-ttu-id="81ee4-102">LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="81ee4-102">LocalServiceSecuritySettings</span></span>
<span data-ttu-id="81ee4-103">LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="81ee4-103">LocalServiceSecuritySettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81ee4-104">構文</span><span class="sxs-lookup"><span data-stu-id="81ee4-104">Syntax</span></span>  
  
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
  
## <a name="methods"></a><span data-ttu-id="81ee4-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="81ee4-105">Methods</span></span>  
 <span data-ttu-id="81ee4-106">LocalServiceSecuritySettings クラスで定義されるメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="81ee4-106">The LocalServiceSecuritySettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="81ee4-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="81ee4-107">Properties</span></span>  
 <span data-ttu-id="81ee4-108">LocalServiceSecuritySettings クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="81ee4-108">The LocalServiceSecuritySettings class has the following properties:</span></span>  
  
### <a name="detectreplays"></a><span data-ttu-id="81ee4-109">DetectReplays</span><span class="sxs-lookup"><span data-stu-id="81ee4-109">DetectReplays</span></span>  
 <span data-ttu-id="81ee4-110">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="81ee4-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="81ee4-111">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-112">チャネルに対するリプレイ攻撃を検出し、自動的に処理するかどうかを指定するブール値です。</span><span class="sxs-lookup"><span data-stu-id="81ee4-112">A Boolean value that specifies whether replay attacks against the channel are detected and dealt with automatically.</span></span>  
  
### <a name="inactivitytimeout"></a><span data-ttu-id="81ee4-113">InactivityTimeout</span><span class="sxs-lookup"><span data-stu-id="81ee4-113">InactivityTimeout</span></span>  
 <span data-ttu-id="81ee4-114">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="81ee4-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="81ee4-115">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-116">サービスがサポートする保留状態のセキュリティ セッションの最大数。</span><span class="sxs-lookup"><span data-stu-id="81ee4-116">The maximum number of pending security sessions that the service supports.</span></span>  
  
### <a name="issuedcookielifetime"></a><span data-ttu-id="81ee4-117">IssuedCookieLifetime</span><span class="sxs-lookup"><span data-stu-id="81ee4-117">IssuedCookieLifetime</span></span>  
 <span data-ttu-id="81ee4-118">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="81ee4-118">Data type: datetime</span></span>  
  
 <span data-ttu-id="81ee4-119">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-120">すべての新しいセキュリティ クッキーに対して発行する有効期間を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="81ee4-120">A TimeSpan that specifies the lifetime issued to all new security cookies.</span></span>  
  
### <a name="maxcachedcookies"></a><span data-ttu-id="81ee4-121">MaxCachedCookies</span><span class="sxs-lookup"><span data-stu-id="81ee4-121">MaxCachedCookies</span></span>  
 <span data-ttu-id="81ee4-122">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="81ee4-122">Data type: sint32</span></span>  
  
 <span data-ttu-id="81ee4-123">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-124">キャッシュできるクッキーの最大数。</span><span class="sxs-lookup"><span data-stu-id="81ee4-124">The maximum number of cookies that can be cached.</span></span>  
  
### <a name="maxclockskew"></a><span data-ttu-id="81ee4-125">MaxClockSkew</span><span class="sxs-lookup"><span data-stu-id="81ee4-125">MaxClockSkew</span></span>  
 <span data-ttu-id="81ee4-126">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="81ee4-126">Data type: datetime</span></span>  
  
 <span data-ttu-id="81ee4-127">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-128">通信している双方の 2 つのシステム クロックのずれの最長時間を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="81ee4-128">A TimeSpan that specifies the maximum time difference between the system clocks of the two communicating parties.</span></span>  
  
### <a name="maxpendingsessions"></a><span data-ttu-id="81ee4-129">MaxPendingSessions</span><span class="sxs-lookup"><span data-stu-id="81ee4-129">MaxPendingSessions</span></span>  
 <span data-ttu-id="81ee4-130">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="81ee4-130">Data type: sint32</span></span>  
  
 <span data-ttu-id="81ee4-131">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-132">サービスにおける保留状態の接続の最大数です。</span><span class="sxs-lookup"><span data-stu-id="81ee4-132">The maximum number of pending connections on the service.</span></span>  
  
### <a name="maxstatefulnegotiations"></a><span data-ttu-id="81ee4-133">MaxStatefulNegotiations</span><span class="sxs-lookup"><span data-stu-id="81ee4-133">MaxStatefulNegotiations</span></span>  
 <span data-ttu-id="81ee4-134">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="81ee4-134">Data type: sint32</span></span>  
  
 <span data-ttu-id="81ee4-135">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-136">同時にアクティブにできるセキュリティ ネゴシエーションの数。</span><span class="sxs-lookup"><span data-stu-id="81ee4-136">The number of security negotiations that can be active concurrently.</span></span>  
  
### <a name="negotiationtimeout"></a><span data-ttu-id="81ee4-137">NegotiationTimeout</span><span class="sxs-lookup"><span data-stu-id="81ee4-137">NegotiationTimeout</span></span>  
 <span data-ttu-id="81ee4-138">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="81ee4-138">Data type: datetime</span></span>  
  
 <span data-ttu-id="81ee4-139">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-140">サーバーとクライアント間のセキュリティ ネゴシエーション フェーズの最大継続時間を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="81ee4-140">A TimeSpan that specifies the maximum duration for the security negotiation phase between server and client.</span></span>  
  
### <a name="reconnecttransportonfailure"></a><span data-ttu-id="81ee4-141">ReconnectTransportOnFailure</span><span class="sxs-lookup"><span data-stu-id="81ee4-141">ReconnectTransportOnFailure</span></span>  
 <span data-ttu-id="81ee4-142">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="81ee4-142">Data type: boolean</span></span>  
  
 <span data-ttu-id="81ee4-143">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-144">WS-ReliableMessaging を使用した接続が、トランスポート エラーの後再接続を試みるかどうかを指定するブール値です。</span><span class="sxs-lookup"><span data-stu-id="81ee4-144">A Boolean value that specifies whether connections using WS-Reliable messaging attempt to reconnect after transport failures.</span></span>  
  
### <a name="replaycachesize"></a><span data-ttu-id="81ee4-145">ReplayCacheSize</span><span class="sxs-lookup"><span data-stu-id="81ee4-145">ReplayCacheSize</span></span>  
 <span data-ttu-id="81ee4-146">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="81ee4-146">Data type: sint32</span></span>  
  
 <span data-ttu-id="81ee4-147">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-148">リプレイ検証で使用されるキャッシュ済みの nonce の数。</span><span class="sxs-lookup"><span data-stu-id="81ee4-148">The number of cached nonces used for replay detection.</span></span>  
  
### <a name="replaywindow"></a><span data-ttu-id="81ee4-149">ReplayWindow</span><span class="sxs-lookup"><span data-stu-id="81ee4-149">ReplayWindow</span></span>  
 <span data-ttu-id="81ee4-150">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="81ee4-150">Data type: datetime</span></span>  
  
 <span data-ttu-id="81ee4-151">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-152">個別のメッセージの nonce の有効期間を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="81ee4-152">A TimeSpan that specifies the duration in which individual message nonces are valid.</span></span>  
  
### <a name="sessionkeyrenewalinterval"></a><span data-ttu-id="81ee4-153">SessionKeyRenewalInterval</span><span class="sxs-lookup"><span data-stu-id="81ee4-153">SessionKeyRenewalInterval</span></span>  
 <span data-ttu-id="81ee4-154">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="81ee4-154">Data type: datetime</span></span>  
  
 <span data-ttu-id="81ee4-155">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-156">イニシエーターがセキュリティ セッションのキーを更新するまでの期間を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="81ee4-156">A TimeSpan that specifies the duration after which the initiator renews the key for the security session.</span></span>  
  
### <a name="sessionkeyrolloverinterval"></a><span data-ttu-id="81ee4-157">SessionKeyRolloverInterval</span><span class="sxs-lookup"><span data-stu-id="81ee4-157">SessionKeyRolloverInterval</span></span>  
 <span data-ttu-id="81ee4-158">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="81ee4-158">Data type: datetime</span></span>  
  
 <span data-ttu-id="81ee4-159">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-159">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-160">キーの更新中に、前のセッション キーが受信メッセージで有効な時間間隔を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="81ee4-160">A TimeSpan that specifies the time interval a previous session key is valid on incoming messages during a key renewal.</span></span>  
  
### <a name="timestampvalidityduration"></a><span data-ttu-id="81ee4-161">TimestampValidityDuration</span><span class="sxs-lookup"><span data-stu-id="81ee4-161">TimestampValidityDuration</span></span>  
 <span data-ttu-id="81ee4-162">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="81ee4-162">Data type: datetime</span></span>  
  
 <span data-ttu-id="81ee4-163">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="81ee4-163">Access type: Read-only</span></span>  
  
 <span data-ttu-id="81ee4-164">タイムスタンプの有効期間を指定する TimeSpan です。</span><span class="sxs-lookup"><span data-stu-id="81ee4-164">A TimeSpan that specifies the duration in which a time stamp is valid.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="81ee4-165">必要条件</span><span class="sxs-lookup"><span data-stu-id="81ee4-165">Requirements</span></span>  
  
|<span data-ttu-id="81ee4-166">MOF</span><span class="sxs-lookup"><span data-stu-id="81ee4-166">MOF</span></span>|<span data-ttu-id="81ee4-167">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="81ee4-167">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="81ee4-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="81ee4-168">Namespace</span></span>|<span data-ttu-id="81ee4-169">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="81ee4-169">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="81ee4-170">関連項目</span><span class="sxs-lookup"><span data-stu-id="81ee4-170">See also</span></span>
- <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
