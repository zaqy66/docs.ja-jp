---
title: ServiceToEndpointAssociation
ms.date: 03/30/2017
ms.assetid: 03c3cd15-e1b2-4dc2-bdc2-59fdccdae110
ms.openlocfilehash: 3d23a3ee10c47e04ea7bdba202ea5063c0d84fac
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452710"
---
# <a name="servicetoendpointassociation"></a><span data-ttu-id="679b5-102">ServiceToEndpointAssociation</span><span class="sxs-lookup"><span data-stu-id="679b5-102">ServiceToEndpointAssociation</span></span>
<span data-ttu-id="679b5-103">エンドポイントにサービスを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="679b5-103">Maps a service to an endpoint.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="679b5-104">構文</span><span class="sxs-lookup"><span data-stu-id="679b5-104">Syntax</span></span>  
  
```csharp
class ServiceToEndpointAssociation  
{  
  Service ref;  
  Endpoint ref;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="679b5-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="679b5-105">Methods</span></span>  
 <span data-ttu-id="679b5-106">ServiceToEndpointAssociation クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="679b5-106">The ServiceToEndpointAssociation class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="679b5-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="679b5-107">Properties</span></span>  
 <span data-ttu-id="679b5-108">ServiceToEndpointAssociation クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="679b5-108">The ServiceToEndpointAssociation class has the following properties:</span></span>  
  
### <a name="ref"></a><span data-ttu-id="679b5-109">ref</span><span class="sxs-lookup"><span data-stu-id="679b5-109">ref</span></span>  
 <span data-ttu-id="679b5-110">データ型 : Service</span><span class="sxs-lookup"><span data-stu-id="679b5-110">Data type: Service</span></span>  
  
 <span data-ttu-id="679b5-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="679b5-111">Access type: Read-only</span></span>  
<span data-ttu-id="679b5-112">修飾子: キー</span><span class="sxs-lookup"><span data-stu-id="679b5-112">Qualifiers: Key</span></span>  
  
 <span data-ttu-id="679b5-113">エンドポイントに関連付けられるサービス。</span><span class="sxs-lookup"><span data-stu-id="679b5-113">The service associated with the endpoint.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="679b5-114">ref</span><span class="sxs-lookup"><span data-stu-id="679b5-114">ref</span></span>  
 <span data-ttu-id="679b5-115">データ型 : Endpoint</span><span class="sxs-lookup"><span data-stu-id="679b5-115">Data type: Endpoint</span></span>  
  
 <span data-ttu-id="679b5-116">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="679b5-116">Access type: Read-only</span></span>  
<span data-ttu-id="679b5-117">修飾子: キー</span><span class="sxs-lookup"><span data-stu-id="679b5-117">Qualifiers: Key</span></span>  
  
 <span data-ttu-id="679b5-118">サービスに関連付けられるエンドポイント。</span><span class="sxs-lookup"><span data-stu-id="679b5-118">The endpoint associated with the service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="679b5-119">必要条件</span><span class="sxs-lookup"><span data-stu-id="679b5-119">Requirements</span></span>  
  
|<span data-ttu-id="679b5-120">MOF</span><span class="sxs-lookup"><span data-stu-id="679b5-120">MOF</span></span>|<span data-ttu-id="679b5-121">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="679b5-121">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="679b5-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="679b5-122">Namespace</span></span>|<span data-ttu-id="679b5-123">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="679b5-123">Defined in root\ServiceModel</span></span>|
