---
title: Binding2
ms.date: 03/30/2017
ms.assetid: 09511c6c-5749-4bb0-874e-0f0be36bfe04
ms.openlocfilehash: 84e304f3dedcbd785d6238e6cb5eb142c288b995
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53149706"
---
# <a name="binding"></a><span data-ttu-id="1cc84-102">バインド</span><span class="sxs-lookup"><span data-stu-id="1cc84-102">Binding</span></span>
<span data-ttu-id="1cc84-103">wmi バインディング</span><span class="sxs-lookup"><span data-stu-id="1cc84-103">wmi Binding</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1cc84-104">構文</span><span class="sxs-lookup"><span data-stu-id="1cc84-104">Syntax</span></span>  
  
```csharp
class Binding  
{  
  BindingElement BindingElements[];  
  datetime CloseTimeout;  
  string Name;  
  string Namespace;  
  datetime OpenTimeout;  
  datetime ReceiveTimeout;  
  string Scheme;  
  datetime SendTimeout;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="1cc84-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="1cc84-105">Methods</span></span>  
 <span data-ttu-id="1cc84-106">Binding クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="1cc84-106">The Binding class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="1cc84-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cc84-107">Properties</span></span>  
 <span data-ttu-id="1cc84-108">Binding クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="1cc84-108">The Binding class has the following properties.</span></span>  
  
### <a name="bindingelements"></a><span data-ttu-id="1cc84-109">BindingElements</span><span class="sxs-lookup"><span data-stu-id="1cc84-109">BindingElements</span></span>  
 <span data-ttu-id="1cc84-110">データの種類:BindingElement 配列</span><span class="sxs-lookup"><span data-stu-id="1cc84-110">Data type: BindingElement array</span></span>  
  
 <span data-ttu-id="1cc84-111">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1cc84-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1cc84-112">バインディングによって実装されるバインド要素のコレクションです。</span><span class="sxs-lookup"><span data-stu-id="1cc84-112">The collection of binding elements implemented by the binding.</span></span>  
  
### <a name="closetimeout"></a><span data-ttu-id="1cc84-113">CloseTimeout</span><span class="sxs-lookup"><span data-stu-id="1cc84-113">CloseTimeout</span></span>  
 <span data-ttu-id="1cc84-114">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="1cc84-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="1cc84-115">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1cc84-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1cc84-116">クローズ操作が完了するまで待機する時間です。</span><span class="sxs-lookup"><span data-stu-id="1cc84-116">The interval of time provided for a close operation to complete.</span></span>  
  
### <a name="name"></a><span data-ttu-id="1cc84-117">名前</span><span class="sxs-lookup"><span data-stu-id="1cc84-117">Name</span></span>  
 <span data-ttu-id="1cc84-118">データ型: string</span><span class="sxs-lookup"><span data-stu-id="1cc84-118">Data type: string</span></span>  
  
 <span data-ttu-id="1cc84-119">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1cc84-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1cc84-120">バインディングの名前。</span><span class="sxs-lookup"><span data-stu-id="1cc84-120">The name of the binding.</span></span>  
  
### <a name="namespace"></a><span data-ttu-id="1cc84-121">名前空間</span><span class="sxs-lookup"><span data-stu-id="1cc84-121">Namespace</span></span>  
 <span data-ttu-id="1cc84-122">データ型: string</span><span class="sxs-lookup"><span data-stu-id="1cc84-122">Data type: string</span></span>  
  
 <span data-ttu-id="1cc84-123">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1cc84-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1cc84-124">バインディングの XML 名前空間。</span><span class="sxs-lookup"><span data-stu-id="1cc84-124">The XML namespace of the binding.</span></span>  
  
### <a name="opentimeout"></a><span data-ttu-id="1cc84-125">OpenTimeout</span><span class="sxs-lookup"><span data-stu-id="1cc84-125">OpenTimeout</span></span>  
 <span data-ttu-id="1cc84-126">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="1cc84-126">Data type: datetime</span></span>  
  
 <span data-ttu-id="1cc84-127">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1cc84-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1cc84-128">オープン操作が完了するまで待機する時間です。</span><span class="sxs-lookup"><span data-stu-id="1cc84-128">The interval of time provided for an open operation to complete.</span></span>  
  
### <a name="receivetimeout"></a><span data-ttu-id="1cc84-129">ReceiveTimeout</span><span class="sxs-lookup"><span data-stu-id="1cc84-129">ReceiveTimeout</span></span>  
 <span data-ttu-id="1cc84-130">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="1cc84-130">Data type: datetime</span></span>  
  
 <span data-ttu-id="1cc84-131">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1cc84-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1cc84-132">受信操作が完了するまで待機する時間です。</span><span class="sxs-lookup"><span data-stu-id="1cc84-132">The interval of time provided for a receive operation to complete.</span></span>  
  
### <a name="scheme"></a><span data-ttu-id="1cc84-133">Scheme</span><span class="sxs-lookup"><span data-stu-id="1cc84-133">Scheme</span></span>  
 <span data-ttu-id="1cc84-134">データ型: string</span><span class="sxs-lookup"><span data-stu-id="1cc84-134">Data type: string</span></span>  
  
 <span data-ttu-id="1cc84-135">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1cc84-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1cc84-136">このバインディングに組み込まれているチャネルおよびリスナー ファクトリによって使用される URI トランスポート スキームです。</span><span class="sxs-lookup"><span data-stu-id="1cc84-136">The URI transport scheme that is used by the channel and listener factories that are built by the binding.</span></span>  
  
### <a name="sendtimeout"></a><span data-ttu-id="1cc84-137">SendTimeout</span><span class="sxs-lookup"><span data-stu-id="1cc84-137">SendTimeout</span></span>  
 <span data-ttu-id="1cc84-138">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="1cc84-138">Data type: datetime</span></span>  
  
 <span data-ttu-id="1cc84-139">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1cc84-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1cc84-140">送信操作が完了するまで待機する時間です。</span><span class="sxs-lookup"><span data-stu-id="1cc84-140">The interval of time provided for a send operation to complete.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1cc84-141">必要条件</span><span class="sxs-lookup"><span data-stu-id="1cc84-141">Requirements</span></span>  
  
|<span data-ttu-id="1cc84-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1cc84-142">MOF</span></span>|<span data-ttu-id="1cc84-143">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="1cc84-143">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="1cc84-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="1cc84-144">Namespace</span></span>|<span data-ttu-id="1cc84-145">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="1cc84-145">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1cc84-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="1cc84-146">See Also</span></span>  
 <xref:System.ServiceModel.Channels.Binding>
