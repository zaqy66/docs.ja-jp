---
title: TransportBindingElement
ms.date: 03/30/2017
ms.assetid: 54ecfbee-53c0-410c-a7fa-a98f2e40c545
ms.openlocfilehash: 79d8b1f4a5127ca36eb57954cff6ee6a97e55e41
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50182659"
---
# <a name="transportbindingelement"></a><span data-ttu-id="3a64a-102">TransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="3a64a-102">TransportBindingElement</span></span>
<span data-ttu-id="3a64a-103">TransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="3a64a-103">TransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a64a-104">構文</span><span class="sxs-lookup"><span data-stu-id="3a64a-104">Syntax</span></span>  
  
```csharp
class TransportBindingElement : BindingElement  
{  
  boolean ManualAddressing;  
  sint64 MaxBufferPoolSize;  
  sint64 MaxReceivedMessageSize;  
  string Scheme;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="3a64a-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="3a64a-105">Methods</span></span>  
 <span data-ttu-id="3a64a-106">TransportBindingElement クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="3a64a-106">The TransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="3a64a-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3a64a-107">Properties</span></span>  
 <span data-ttu-id="3a64a-108">TransportBindingElement クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="3a64a-108">The TransportBindingElement class has the following properties:</span></span>  
  
### <a name="manualaddressing"></a><span data-ttu-id="3a64a-109">ManualAddressing</span><span class="sxs-lookup"><span data-stu-id="3a64a-109">ManualAddressing</span></span>  
 <span data-ttu-id="3a64a-110">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="3a64a-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="3a64a-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3a64a-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a64a-112">メッセージのアドレス指定をユーザーが制御するかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="3a64a-112">A boolean value that specifies whether the user wants to take control of message addressing.</span></span>  
  
### <a name="maxbufferpoolsize"></a><span data-ttu-id="3a64a-113">MaxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="3a64a-113">MaxBufferPoolSize</span></span>  
 <span data-ttu-id="3a64a-114">データ型 : sint64</span><span class="sxs-lookup"><span data-stu-id="3a64a-114">Data type: sint64</span></span>  
  
 <span data-ttu-id="3a64a-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3a64a-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a64a-116">バインディングに使用するバッファー プールの最大サイズ。</span><span class="sxs-lookup"><span data-stu-id="3a64a-116">The maximum buffer pool size for the binding.</span></span>  
  
### <a name="maxreceivedmessagesize"></a><span data-ttu-id="3a64a-117">MaxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="3a64a-117">MaxReceivedMessageSize</span></span>  
 <span data-ttu-id="3a64a-118">データ型 : sint64</span><span class="sxs-lookup"><span data-stu-id="3a64a-118">Data type: sint64</span></span>  
  
 <span data-ttu-id="3a64a-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3a64a-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a64a-120">このバインディングで処理されるメッセージの最大サイズ。</span><span class="sxs-lookup"><span data-stu-id="3a64a-120">The maximum size for a message that is processed by this binding.</span></span>  
  
### <a name="scheme"></a><span data-ttu-id="3a64a-121">Scheme</span><span class="sxs-lookup"><span data-stu-id="3a64a-121">Scheme</span></span>  
 <span data-ttu-id="3a64a-122">データ型: string</span><span class="sxs-lookup"><span data-stu-id="3a64a-122">Data type: string</span></span>  
  
 <span data-ttu-id="3a64a-123">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3a64a-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a64a-124">トランスポートの URI スキーム。</span><span class="sxs-lookup"><span data-stu-id="3a64a-124">The URI scheme for the transport.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a64a-125">必要条件</span><span class="sxs-lookup"><span data-stu-id="3a64a-125">Requirements</span></span>  
  
|<span data-ttu-id="3a64a-126">MOF</span><span class="sxs-lookup"><span data-stu-id="3a64a-126">MOF</span></span>|<span data-ttu-id="3a64a-127">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="3a64a-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3a64a-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a64a-128">Namespace</span></span>|<span data-ttu-id="3a64a-129">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="3a64a-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3a64a-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="3a64a-130">See Also</span></span>  
 <xref:System.ServiceModel.Channels.TransportBindingElement>
