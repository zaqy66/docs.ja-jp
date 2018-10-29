---
title: チャネル クラス
ms.date: 03/30/2017
ms.assetid: d9fae2ca-209c-4341-a0f5-6b79d1a67776
ms.openlocfilehash: 108d5f8e3cd092863dbd48e2bb9d180798b091a4
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50197874"
---
# <a name="channel-class"></a><span data-ttu-id="b9d8d-102">チャネル クラス</span><span class="sxs-lookup"><span data-stu-id="b9d8d-102">Channel class</span></span>
<span data-ttu-id="b9d8d-103">チャネル</span><span class="sxs-lookup"><span data-stu-id="b9d8d-103">Channel</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9d8d-104">構文</span><span class="sxs-lookup"><span data-stu-id="b9d8d-104">Syntax</span></span>  
  
```csharp
class Channel  
{  
  string LocalAddress;  
  Endpoint ref;  
  string RemoteAddress;  
  string SessionId;  
  string Type;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="b9d8d-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="b9d8d-105">Methods</span></span>  
 <span data-ttu-id="b9d8d-106">チャネル クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="b9d8d-106">The Channel class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="b9d8d-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="b9d8d-107">Properties</span></span>  
 <span data-ttu-id="b9d8d-108">チャネル クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="b9d8d-108">The Channel class has the following properties.</span></span>  
  
### <a name="localaddress"></a><span data-ttu-id="b9d8d-109">LocalAddress</span><span class="sxs-lookup"><span data-stu-id="b9d8d-109">LocalAddress</span></span>  
 <span data-ttu-id="b9d8d-110">データ型: string</span><span class="sxs-lookup"><span data-stu-id="b9d8d-110">Data type: string</span></span>  
  
 <span data-ttu-id="b9d8d-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="b9d8d-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9d8d-112">チャネルのローカル エンドポイント。</span><span class="sxs-lookup"><span data-stu-id="b9d8d-112">The local endpoint for the channel.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="b9d8d-113">ref</span><span class="sxs-lookup"><span data-stu-id="b9d8d-113">ref</span></span>  
 <span data-ttu-id="b9d8d-114">データ型 : Endpoint</span><span class="sxs-lookup"><span data-stu-id="b9d8d-114">Data type: Endpoint</span></span>  
  
 <span data-ttu-id="b9d8d-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="b9d8d-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9d8d-116">チャネルが接続するエンドポイントへの参照。</span><span class="sxs-lookup"><span data-stu-id="b9d8d-116">A reference to the endpoint the channel connects to.</span></span>  
  
### <a name="remoteaddress"></a><span data-ttu-id="b9d8d-117">RemoteAddress</span><span class="sxs-lookup"><span data-stu-id="b9d8d-117">RemoteAddress</span></span>  
 <span data-ttu-id="b9d8d-118">データ型: string</span><span class="sxs-lookup"><span data-stu-id="b9d8d-118">Data type: string</span></span>  
  
 <span data-ttu-id="b9d8d-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="b9d8d-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9d8d-120">チャネルに関連するリモート アドレス。</span><span class="sxs-lookup"><span data-stu-id="b9d8d-120">The remote address associated with the channel.</span></span>  
  
### <a name="sessionid"></a><span data-ttu-id="b9d8d-121">SessionId</span><span class="sxs-lookup"><span data-stu-id="b9d8d-121">SessionId</span></span>  
 <span data-ttu-id="b9d8d-122">データ型: string</span><span class="sxs-lookup"><span data-stu-id="b9d8d-122">Data type: string</span></span>  
  
 <span data-ttu-id="b9d8d-123">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="b9d8d-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9d8d-124">現在のセッション ID (存在する場合)。</span><span class="sxs-lookup"><span data-stu-id="b9d8d-124">The current session Id, if any.</span></span>  
  
### <a name="type"></a><span data-ttu-id="b9d8d-125">種類</span><span class="sxs-lookup"><span data-stu-id="b9d8d-125">Type</span></span>  
 <span data-ttu-id="b9d8d-126">データ型: string</span><span class="sxs-lookup"><span data-stu-id="b9d8d-126">Data type: string</span></span>  
  
 <span data-ttu-id="b9d8d-127">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="b9d8d-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9d8d-128">チャネルの型。</span><span class="sxs-lookup"><span data-stu-id="b9d8d-128">The type of the channel.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b9d8d-129">要件</span><span class="sxs-lookup"><span data-stu-id="b9d8d-129">Requirements</span></span>  
  
|<span data-ttu-id="b9d8d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b9d8d-130">MOF</span></span>|<span data-ttu-id="b9d8d-131">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="b9d8d-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="b9d8d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9d8d-132">Namespace</span></span>|<span data-ttu-id="b9d8d-133">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="b9d8d-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b9d8d-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9d8d-134">See Also</span></span>  
 <xref:System.ServiceModel.Channels.ChannelBase>
