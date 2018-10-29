---
title: サービス
ms.date: 03/30/2017
ms.assetid: 999806e1-6376-409e-b998-b0af391adfe7
ms.openlocfilehash: c59672b3b7617d9c28d99f7d534b6e7f2f2e9fbb
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50196909"
---
# <a name="service"></a><span data-ttu-id="7600d-102">サービス</span><span class="sxs-lookup"><span data-stu-id="7600d-102">Service</span></span>
<span data-ttu-id="7600d-103">サービス</span><span class="sxs-lookup"><span data-stu-id="7600d-103">Service</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7600d-104">構文</span><span class="sxs-lookup"><span data-stu-id="7600d-104">Syntax</span></span>  
  
```csharp
class Service  
{  
  string BaseAddresses[];  
  Behavior Behaviors[];  
  string ConfigurationName;  
  string CounterInstanceName;  
  string DistinguishedName;  
  string Extensions[];  
  string Metadata[];  
  string Name;  
  string Namespace;  
  datetime Opened;  
  Channel OutgoingChannels[];  
  sint32 ProcessId;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="7600d-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="7600d-105">Methods</span></span>  
 <span data-ttu-id="7600d-106">Service クラスで定義されているメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="7600d-106">The Service class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="7600d-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7600d-107">Properties</span></span>  
 <span data-ttu-id="7600d-108">Service クラスには次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="7600d-108">The Service class has the following properties:</span></span>  
  
### <a name="baseaddresses"></a><span data-ttu-id="7600d-109">BaseAddresses</span><span class="sxs-lookup"><span data-stu-id="7600d-109">BaseAddresses</span></span>  
 <span data-ttu-id="7600d-110">データ型 : string array</span><span class="sxs-lookup"><span data-stu-id="7600d-110">Data type: string array</span></span>  
  
 <span data-ttu-id="7600d-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7600d-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7600d-112">サービスによって使用されるベース アドレスです。</span><span class="sxs-lookup"><span data-stu-id="7600d-112">The base addresses used by the service.</span></span>  
  
### <a name="behaviors"></a><span data-ttu-id="7600d-113">ビヘイビアー</span><span class="sxs-lookup"><span data-stu-id="7600d-113">Behaviors</span></span>  
 <span data-ttu-id="7600d-114">データ型 : Behavior array</span><span class="sxs-lookup"><span data-stu-id="7600d-114">Data type: Behavior array</span></span>  
  
 <span data-ttu-id="7600d-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7600d-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7600d-116">このサービスに関連付けられている動作です。</span><span class="sxs-lookup"><span data-stu-id="7600d-116">The behaviors associated with this service.</span></span>  
  
### <a name="configurationname"></a><span data-ttu-id="7600d-117">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7600d-117">ConfigurationName</span></span>  
 <span data-ttu-id="7600d-118">データ型: string</span><span class="sxs-lookup"><span data-stu-id="7600d-118">Data type: string</span></span>  
  
 <span data-ttu-id="7600d-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7600d-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7600d-120">ServiceElement_BehaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="7600d-120">ServiceElement_BehaviorConfiguration</span></span>  
  
### <a name="counterinstancename"></a><span data-ttu-id="7600d-121">CounterInstanceName</span><span class="sxs-lookup"><span data-stu-id="7600d-121">CounterInstanceName</span></span>  
 <span data-ttu-id="7600d-122">データ型: string</span><span class="sxs-lookup"><span data-stu-id="7600d-122">Data type: string</span></span>  
  
 <span data-ttu-id="7600d-123">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7600d-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7600d-124">サービスのパフォーマンス カウンターのインスタンスのインスタンス名です。</span><span class="sxs-lookup"><span data-stu-id="7600d-124">Instance name of the instance of the performance counters of the service.</span></span>  
  
### <a name="distinguishedname"></a><span data-ttu-id="7600d-125">DistinguishedName</span><span class="sxs-lookup"><span data-stu-id="7600d-125">DistinguishedName</span></span>  
 <span data-ttu-id="7600d-126">データ型: string</span><span class="sxs-lookup"><span data-stu-id="7600d-126">Data type: string</span></span>  
  
 <span data-ttu-id="7600d-127">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7600d-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7600d-128">アドレスでのサービス名です。</span><span class="sxs-lookup"><span data-stu-id="7600d-128">Service name at the address.</span></span>  
  
### <a name="extensions"></a><span data-ttu-id="7600d-129">拡張機能</span><span class="sxs-lookup"><span data-stu-id="7600d-129">Extensions</span></span>  
 <span data-ttu-id="7600d-130">データ型 : string array</span><span class="sxs-lookup"><span data-stu-id="7600d-130">Data type: string array</span></span>  
  
 <span data-ttu-id="7600d-131">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7600d-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7600d-132">サービス インスタンスの拡張に対するインスタンス コンテキストです。</span><span class="sxs-lookup"><span data-stu-id="7600d-132">The instance contexts for the extensions of the service instance.</span></span>  
  
### <a name="metadata"></a><span data-ttu-id="7600d-133">メタデータ</span><span class="sxs-lookup"><span data-stu-id="7600d-133">Metadata</span></span>  
 <span data-ttu-id="7600d-134">データ型 : string array</span><span class="sxs-lookup"><span data-stu-id="7600d-134">Data type: string array</span></span>  
  
 <span data-ttu-id="7600d-135">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7600d-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7600d-136">サービス メタデータの設定です。</span><span class="sxs-lookup"><span data-stu-id="7600d-136">The service metadata settings.</span></span>  
  
### <a name="name"></a><span data-ttu-id="7600d-137">名前</span><span class="sxs-lookup"><span data-stu-id="7600d-137">Name</span></span>  
 <span data-ttu-id="7600d-138">データ型: string</span><span class="sxs-lookup"><span data-stu-id="7600d-138">Data type: string</span></span>  
  
 <span data-ttu-id="7600d-139">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7600d-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7600d-140">このサービスの一意の名前。</span><span class="sxs-lookup"><span data-stu-id="7600d-140">The unique name of this service.</span></span>  
  
### <a name="namespace"></a><span data-ttu-id="7600d-141">名前空間</span><span class="sxs-lookup"><span data-stu-id="7600d-141">Namespace</span></span>  
 <span data-ttu-id="7600d-142">データ型: string</span><span class="sxs-lookup"><span data-stu-id="7600d-142">Data type: string</span></span>  
  
 <span data-ttu-id="7600d-143">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7600d-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7600d-144">サービスの名前空間です。</span><span class="sxs-lookup"><span data-stu-id="7600d-144">The namespace of the service.</span></span>  
  
### <a name="opened"></a><span data-ttu-id="7600d-145">Opened</span><span class="sxs-lookup"><span data-stu-id="7600d-145">Opened</span></span>  
 <span data-ttu-id="7600d-146">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="7600d-146">Data type: datetime</span></span>  
  
 <span data-ttu-id="7600d-147">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7600d-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7600d-148">サービスが開かれた時刻です。</span><span class="sxs-lookup"><span data-stu-id="7600d-148">The time the service was opened.</span></span>  
  
### <a name="outgoingchannels"></a><span data-ttu-id="7600d-149">OutgoingChannels</span><span class="sxs-lookup"><span data-stu-id="7600d-149">OutgoingChannels</span></span>  
 <span data-ttu-id="7600d-150">データ型 : Channel 配列</span><span class="sxs-lookup"><span data-stu-id="7600d-150">Data type: Channel array</span></span>  
  
 <span data-ttu-id="7600d-151">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7600d-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7600d-152">サービス インスタンスから送信しているチャネルです。</span><span class="sxs-lookup"><span data-stu-id="7600d-152">The channels that are outgoing from the service instance.</span></span>  
  
### <a name="processid"></a><span data-ttu-id="7600d-153">ProcessId</span><span class="sxs-lookup"><span data-stu-id="7600d-153">ProcessId</span></span>  
 <span data-ttu-id="7600d-154">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="7600d-154">Data type: sint32</span></span>  
  
 <span data-ttu-id="7600d-155">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7600d-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7600d-156">サービスをホストするプロセスのプロセス ID です。</span><span class="sxs-lookup"><span data-stu-id="7600d-156">The process id of the process that hosts the service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7600d-157">必要条件</span><span class="sxs-lookup"><span data-stu-id="7600d-157">Requirements</span></span>  
  
|<span data-ttu-id="7600d-158">MOF</span><span class="sxs-lookup"><span data-stu-id="7600d-158">MOF</span></span>|<span data-ttu-id="7600d-159">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="7600d-159">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="7600d-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="7600d-160">Namespace</span></span>|<span data-ttu-id="7600d-161">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="7600d-161">Defined in root\ServiceModel</span></span>|
