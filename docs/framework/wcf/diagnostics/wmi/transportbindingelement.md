---
title: TransportBindingElement
ms.date: 03/30/2017
ms.assetid: 54ecfbee-53c0-410c-a7fa-a98f2e40c545
ms.openlocfilehash: 303e5523befb68c65bc50ee3933af58897929363
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54668454"
---
# <a name="transportbindingelement"></a><span data-ttu-id="98820-102">TransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="98820-102">TransportBindingElement</span></span>
<span data-ttu-id="98820-103">TransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="98820-103">TransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="98820-104">構文</span><span class="sxs-lookup"><span data-stu-id="98820-104">Syntax</span></span>  
  
```csharp
class TransportBindingElement : BindingElement  
{  
  boolean ManualAddressing;  
  sint64 MaxBufferPoolSize;  
  sint64 MaxReceivedMessageSize;  
  string Scheme;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="98820-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="98820-105">Methods</span></span>  
 <span data-ttu-id="98820-106">TransportBindingElement クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="98820-106">The TransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="98820-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="98820-107">Properties</span></span>  
 <span data-ttu-id="98820-108">TransportBindingElement クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="98820-108">The TransportBindingElement class has the following properties:</span></span>  
  
### <a name="manualaddressing"></a><span data-ttu-id="98820-109">ManualAddressing</span><span class="sxs-lookup"><span data-stu-id="98820-109">ManualAddressing</span></span>  
 <span data-ttu-id="98820-110">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="98820-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="98820-111">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="98820-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="98820-112">メッセージのアドレス指定をユーザーが制御するかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="98820-112">A boolean value that specifies whether the user wants to take control of message addressing.</span></span>  
  
### <a name="maxbufferpoolsize"></a><span data-ttu-id="98820-113">MaxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="98820-113">MaxBufferPoolSize</span></span>  
 <span data-ttu-id="98820-114">データ型 : sint64</span><span class="sxs-lookup"><span data-stu-id="98820-114">Data type: sint64</span></span>  
  
 <span data-ttu-id="98820-115">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="98820-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="98820-116">バインディングに使用するバッファー プールの最大サイズ。</span><span class="sxs-lookup"><span data-stu-id="98820-116">The maximum buffer pool size for the binding.</span></span>  
  
### <a name="maxreceivedmessagesize"></a><span data-ttu-id="98820-117">MaxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="98820-117">MaxReceivedMessageSize</span></span>  
 <span data-ttu-id="98820-118">データ型 : sint64</span><span class="sxs-lookup"><span data-stu-id="98820-118">Data type: sint64</span></span>  
  
 <span data-ttu-id="98820-119">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="98820-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="98820-120">このバインディングで処理されるメッセージの最大サイズ。</span><span class="sxs-lookup"><span data-stu-id="98820-120">The maximum size for a message that is processed by this binding.</span></span>  
  
### <a name="scheme"></a><span data-ttu-id="98820-121">Scheme</span><span class="sxs-lookup"><span data-stu-id="98820-121">Scheme</span></span>  
 <span data-ttu-id="98820-122">データ型: string</span><span class="sxs-lookup"><span data-stu-id="98820-122">Data type: string</span></span>  
  
 <span data-ttu-id="98820-123">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="98820-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="98820-124">トランスポートの URI スキーム。</span><span class="sxs-lookup"><span data-stu-id="98820-124">The URI scheme for the transport.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="98820-125">必要条件</span><span class="sxs-lookup"><span data-stu-id="98820-125">Requirements</span></span>  
  
|<span data-ttu-id="98820-126">MOF</span><span class="sxs-lookup"><span data-stu-id="98820-126">MOF</span></span>|<span data-ttu-id="98820-127">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="98820-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="98820-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="98820-128">Namespace</span></span>|<span data-ttu-id="98820-129">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="98820-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="98820-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="98820-130">See also</span></span>
- <xref:System.ServiceModel.Channels.TransportBindingElement>
