---
title: ServiceDebugBehavior
ms.date: 03/30/2017
ms.assetid: a5ec9061-1e95-43fb-b0d9-dbd0a7bc3c44
ms.openlocfilehash: 68b2350f257bc95d8e17f4b9049d67c7f67becae
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452863"
---
# <a name="servicedebugbehavior"></a><span data-ttu-id="3e333-102">ServiceDebugBehavior</span><span class="sxs-lookup"><span data-stu-id="3e333-102">ServiceDebugBehavior</span></span>
<span data-ttu-id="3e333-103">ServiceDebugBehavior</span><span class="sxs-lookup"><span data-stu-id="3e333-103">ServiceDebugBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e333-104">構文</span><span class="sxs-lookup"><span data-stu-id="3e333-104">Syntax</span></span>  
  
```csharp
class ServiceDebugBehavior : Behavior  
{  
  boolean HttpHelpPageEnabled;  
  string HttpHelpPageUrl;  
  boolean HttpsHelpPageEnabled;  
  string HttpsHelpPageUrl;  
  boolean IncludeExceptionDetailInFaults;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="3e333-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="3e333-105">Methods</span></span>  
 <span data-ttu-id="3e333-106">ServiceDebugBehavior クラスで定義されるメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="3e333-106">The ServiceDebugBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="3e333-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e333-107">Properties</span></span>  
 <span data-ttu-id="3e333-108">ServiceDebugBehavior クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="3e333-108">The ServiceDebugBehavior class has the following properties:</span></span>  
  
### <a name="httphelppageenabled"></a><span data-ttu-id="3e333-109">HttpHelpPageEnabled</span><span class="sxs-lookup"><span data-stu-id="3e333-109">HttpHelpPageEnabled</span></span>  
 <span data-ttu-id="3e333-110">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="3e333-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="3e333-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3e333-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3e333-112">`HttpGetUrl` 属性によって制御されるアドレスで、サービスが WSDL を公開するかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="3e333-112">Controls whether the service publishes its WSDL at the address controlled by the `HttpGetUrl` attribute.</span></span>  
  
### <a name="httphelppageurl"></a><span data-ttu-id="3e333-113">HttpHelpPageUrl</span><span class="sxs-lookup"><span data-stu-id="3e333-113">HttpHelpPageUrl</span></span>  
 <span data-ttu-id="3e333-114">データ型: string</span><span class="sxs-lookup"><span data-stu-id="3e333-114">Data type: string</span></span>  
  
 <span data-ttu-id="3e333-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3e333-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3e333-116">HTTP を使用した取得のために、サービス WSDL が公開される場所を設定します。</span><span class="sxs-lookup"><span data-stu-id="3e333-116">Sets the location at which the service WSDL is published for retrieval using HTTP.</span></span>  
  
### <a name="httpshelppageenabled"></a><span data-ttu-id="3e333-117">HttpsHelpPageEnabled</span><span class="sxs-lookup"><span data-stu-id="3e333-117">HttpsHelpPageEnabled</span></span>  
 <span data-ttu-id="3e333-118">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="3e333-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="3e333-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3e333-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3e333-120">`HttpsGetUrl` 属性によって制御されるアドレスで、サービスが HTTPS を介して WSDL を公開するかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="3e333-120">Controls whether the service publishes its WSDL over HTTPS at the address controlled by the `HttpsGetUrl` attribute.</span></span>  
  
### <a name="httpshelppageurl"></a><span data-ttu-id="3e333-121">HttpsHelpPageUrl</span><span class="sxs-lookup"><span data-stu-id="3e333-121">HttpsHelpPageUrl</span></span>  
 <span data-ttu-id="3e333-122">データ型: string</span><span class="sxs-lookup"><span data-stu-id="3e333-122">Data type: string</span></span>  
  
 <span data-ttu-id="3e333-123">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3e333-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3e333-124">HTTPS を使用した取得のために、サービス WSDL が公開される場所を設定します。</span><span class="sxs-lookup"><span data-stu-id="3e333-124">Sets the location at which the service WSDL is published for retrieval using HTTPS.</span></span>  
  
### <a name="includeexceptiondetailinfaults"></a><span data-ttu-id="3e333-125">IncludeExceptionDetailInFaults</span><span class="sxs-lookup"><span data-stu-id="3e333-125">IncludeExceptionDetailInFaults</span></span>  
 <span data-ttu-id="3e333-126">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="3e333-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="3e333-127">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3e333-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3e333-128">デバッグの目的でクライアントに返される SOAP エラーの詳細に、マネージド例外情報を含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3e333-128">Specifies whether to include managed exception information in the detail of SOAP faults returned to the clients for debugging purposes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3e333-129">必要条件</span><span class="sxs-lookup"><span data-stu-id="3e333-129">Requirements</span></span>  
  
|<span data-ttu-id="3e333-130">MOF</span><span class="sxs-lookup"><span data-stu-id="3e333-130">MOF</span></span>|<span data-ttu-id="3e333-131">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="3e333-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3e333-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e333-132">Namespace</span></span>|<span data-ttu-id="3e333-133">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="3e333-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3e333-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e333-134">See Also</span></span>  
 <xref:System.ServiceModel.Description.ServiceDebugBehavior>
