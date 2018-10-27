---
title: ServiceMetadataBehavior
ms.date: 03/30/2017
ms.assetid: 0f194476-72f1-467e-bdce-674306316e64
ms.openlocfilehash: 19a04b6432f1ecc38a3b906b7e677175863134db
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188834"
---
# <a name="servicemetadatabehavior"></a><span data-ttu-id="be940-102">ServiceMetadataBehavior</span><span class="sxs-lookup"><span data-stu-id="be940-102">ServiceMetadataBehavior</span></span>
<span data-ttu-id="be940-103">ServiceMetadataBehavior</span><span class="sxs-lookup"><span data-stu-id="be940-103">ServiceMetadataBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be940-104">構文</span><span class="sxs-lookup"><span data-stu-id="be940-104">Syntax</span></span>  
  
```csharp
class ServiceMetadataBehavior : Behavior  
{  
  string ExternalMetadataLocation;  
  boolean HttpGetEnabled;  
  string HttpGetUrl;  
  boolean HttpsGetEnabled;  
  string HttpsGetUrl;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="be940-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="be940-105">Methods</span></span>  
 <span data-ttu-id="be940-106">ServiceMetadataBehavior クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="be940-106">The ServiceMetadataBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="be940-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="be940-107">Properties</span></span>  
 <span data-ttu-id="be940-108">ServiceMetadataBehavior クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="be940-108">The ServiceMetadataBehavior class has the following properties:</span></span>  
  
### <a name="externalmetadatalocation"></a><span data-ttu-id="be940-109">ExternalMetadataLocation</span><span class="sxs-lookup"><span data-stu-id="be940-109">ExternalMetadataLocation</span></span>  
 <span data-ttu-id="be940-110">データ型: string</span><span class="sxs-lookup"><span data-stu-id="be940-110">Data type: string</span></span>  
  
 <span data-ttu-id="be940-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="be940-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="be940-112">サービスがメタデータ要求をリダイレクトする場所を設定します。</span><span class="sxs-lookup"><span data-stu-id="be940-112">Sets the location to which the service redirects metadata requests.</span></span>  
  
### <a name="httpgetenabled"></a><span data-ttu-id="be940-113">HttpGetEnabled</span><span class="sxs-lookup"><span data-stu-id="be940-113">HttpGetEnabled</span></span>  
 <span data-ttu-id="be940-114">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="be940-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="be940-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="be940-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="be940-116">`HttpGetUrl` 属性によって制御されるアドレスで、サービスが WSDL を公開するかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="be940-116">Controls whether the service publishes its WSDL at the address controlled by the `HttpGetUrl` attribute.</span></span>  
  
### <a name="httpgeturl"></a><span data-ttu-id="be940-117">HttpGetUrl</span><span class="sxs-lookup"><span data-stu-id="be940-117">HttpGetUrl</span></span>  
 <span data-ttu-id="be940-118">データ型: string</span><span class="sxs-lookup"><span data-stu-id="be940-118">Data type: string</span></span>  
  
 <span data-ttu-id="be940-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="be940-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="be940-120">HTTP を使用した取得のために、サービス WSDL が公開される場所を設定します。</span><span class="sxs-lookup"><span data-stu-id="be940-120">Sets the location at which the service WSDL is published for retrieval using HTTP.</span></span>  
  
### <a name="httpsgetenabled"></a><span data-ttu-id="be940-121">HttpsGetEnabled</span><span class="sxs-lookup"><span data-stu-id="be940-121">HttpsGetEnabled</span></span>  
 <span data-ttu-id="be940-122">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="be940-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="be940-123">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="be940-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="be940-124">`HttpsGetUrl` 属性によって制御されるアドレスで、サービスが HTTPS を介して WSDL を公開するかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="be940-124">Controls whether the service publishes its WSDL over HTTPS at the address controlled by the `HttpsGetUrl` attribute.</span></span>  
  
### <a name="httpsgeturl"></a><span data-ttu-id="be940-125">HttpsGetUrl</span><span class="sxs-lookup"><span data-stu-id="be940-125">HttpsGetUrl</span></span>  
 <span data-ttu-id="be940-126">データ型: string</span><span class="sxs-lookup"><span data-stu-id="be940-126">Data type: string</span></span>  
  
 <span data-ttu-id="be940-127">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="be940-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="be940-128">HTTPS を使用した取得のために、サービス WSDL が公開される場所を設定します。</span><span class="sxs-lookup"><span data-stu-id="be940-128">Sets the location at which the service WSDL is published for retrieval using HTTPS.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="be940-129">必要条件</span><span class="sxs-lookup"><span data-stu-id="be940-129">Requirements</span></span>  
  
|<span data-ttu-id="be940-130">MOF</span><span class="sxs-lookup"><span data-stu-id="be940-130">MOF</span></span>|<span data-ttu-id="be940-131">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="be940-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="be940-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="be940-132">Namespace</span></span>|<span data-ttu-id="be940-133">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="be940-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="be940-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="be940-134">See Also</span></span>  
 <xref:System.ServiceModel.Description.ServiceMetadataBehavior>
