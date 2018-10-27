---
title: PeerTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 40bf6be2-8087-4cb3-a66c-408d53eb9269
ms.openlocfilehash: 58bf07b0429ca2435b5aae3683ef69951a10003e
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50185184"
---
# <a name="peertransportbindingelement"></a><span data-ttu-id="07b5c-102">PeerTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="07b5c-102">PeerTransportBindingElement</span></span>
<span data-ttu-id="07b5c-103">PeerTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="07b5c-103">PeerTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07b5c-104">構文</span><span class="sxs-lookup"><span data-stu-id="07b5c-104">Syntax</span></span>  
  
```csharp
class PeerTransportBindingElement : TransportBindingElement  
{  
  string ListenIPAddress;  
  sint32 Port;  
  PeerSecuritySettings Security;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="07b5c-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="07b5c-105">Methods</span></span>  
 <span data-ttu-id="07b5c-106">PeerTransportBindingElement クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="07b5c-106">The PeerTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="07b5c-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="07b5c-107">Properties</span></span>  
 <span data-ttu-id="07b5c-108">PeerTransportBindingElement クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="07b5c-108">The PeerTransportBindingElement class has the following properties:</span></span>  
  
### <a name="listenipaddress"></a><span data-ttu-id="07b5c-109">ListenIPAddress</span><span class="sxs-lookup"><span data-stu-id="07b5c-109">ListenIPAddress</span></span>  
 <span data-ttu-id="07b5c-110">データ型: string</span><span class="sxs-lookup"><span data-stu-id="07b5c-110">Data type: string</span></span>  
  
 <span data-ttu-id="07b5c-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="07b5c-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="07b5c-112">ピア ノードがメッセージをリッスンする IP アドレスです。</span><span class="sxs-lookup"><span data-stu-id="07b5c-112">The IP address on which the peer node listens for messages.</span></span>  
  
### <a name="port"></a><span data-ttu-id="07b5c-113">ポート</span><span class="sxs-lookup"><span data-stu-id="07b5c-113">Port</span></span>  
 <span data-ttu-id="07b5c-114">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="07b5c-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="07b5c-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="07b5c-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="07b5c-116">このバインディングがピア チャネル メッセージを処理するネットワーク インターフェイス ポートです。</span><span class="sxs-lookup"><span data-stu-id="07b5c-116">The network interface port on which this binding processes peer channel messages.</span></span>  
  
### <a name="security"></a><span data-ttu-id="07b5c-117">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="07b5c-117">Security</span></span>  
 <span data-ttu-id="07b5c-118">データ型 : PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="07b5c-118">Data type: PeerSecuritySettings</span></span>  
  
 <span data-ttu-id="07b5c-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="07b5c-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="07b5c-120">ピア トランスポートのセキュリティ設定です。</span><span class="sxs-lookup"><span data-stu-id="07b5c-120">Peer transport security settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="07b5c-121">必要条件</span><span class="sxs-lookup"><span data-stu-id="07b5c-121">Requirements</span></span>  
  
|<span data-ttu-id="07b5c-122">MOF</span><span class="sxs-lookup"><span data-stu-id="07b5c-122">MOF</span></span>|<span data-ttu-id="07b5c-123">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="07b5c-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="07b5c-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="07b5c-124">Namespace</span></span>|<span data-ttu-id="07b5c-125">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="07b5c-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="07b5c-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="07b5c-126">See Also</span></span>  
 <xref:System.ServiceModel.Channels.PeerTransportBindingElement>
