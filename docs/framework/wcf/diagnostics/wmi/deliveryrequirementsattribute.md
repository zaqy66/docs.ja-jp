---
title: DeliveryRequirementsAttribute
ms.date: 03/30/2017
ms.assetid: 40c5435c-a325-4cf8-9dd0-d6e24b4a56a3
ms.openlocfilehash: 7bfc03299fffc8070a7d8a4b3885706ea861bdf6
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/26/2018
ms.locfileid: "50042897"
---
# <a name="deliveryrequirementsattribute"></a><span data-ttu-id="03703-102">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="03703-102">DeliveryRequirementsAttribute</span></span>
<span data-ttu-id="03703-103">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="03703-103">DeliveryRequirementsAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="03703-104">構文</span><span class="sxs-lookup"><span data-stu-id="03703-104">Syntax</span></span>  
  
```csharp
class DeliveryRequirementsAttribute : Behavior  
{  
  string QueuedDeliveryRequirements;  
  boolean RequireOrderedDelivery;  
  string TargetContract;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="03703-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="03703-105">Methods</span></span>  
 <span data-ttu-id="03703-106">DeliveryRequirementsAttribute クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="03703-106">The DeliveryRequirementsAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="03703-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="03703-107">Properties</span></span>  
 <span data-ttu-id="03703-108">DeliveryRequirementsAttribute クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="03703-108">The DeliveryRequirementsAttribute class has the following properties:</span></span>  
  
### <a name="queueddeliveryrequirements"></a><span data-ttu-id="03703-109">QueuedDeliveryRequirements</span><span class="sxs-lookup"><span data-stu-id="03703-109">QueuedDeliveryRequirements</span></span>  
 <span data-ttu-id="03703-110">データ型: string</span><span class="sxs-lookup"><span data-stu-id="03703-110">Data type: string</span></span>  
  
 <span data-ttu-id="03703-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="03703-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="03703-112">サービスのバインドがコントラクトをサポートするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="03703-112">Specifies whether the binding for a service supports contracts.</span></span>  
  
### <a name="requireordereddelivery"></a><span data-ttu-id="03703-113">RequireOrderedDelivery</span><span class="sxs-lookup"><span data-stu-id="03703-113">RequireOrderedDelivery</span></span>  
 <span data-ttu-id="03703-114">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="03703-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="03703-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="03703-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="03703-116">バインディングが順序付きメッセージをサポートするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="03703-116">Specifies whether the binding supports ordered messages.</span></span>  
  
### <a name="targetcontract"></a><span data-ttu-id="03703-117">TargetContract</span><span class="sxs-lookup"><span data-stu-id="03703-117">TargetContract</span></span>  
 <span data-ttu-id="03703-118">データ型: string</span><span class="sxs-lookup"><span data-stu-id="03703-118">Data type: string</span></span>  
  
 <span data-ttu-id="03703-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="03703-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="03703-120">適用先となるコントラクトです。</span><span class="sxs-lookup"><span data-stu-id="03703-120">The contract to which it applies.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="03703-121">必要条件</span><span class="sxs-lookup"><span data-stu-id="03703-121">Requirements</span></span>  
  
|<span data-ttu-id="03703-122">MOF</span><span class="sxs-lookup"><span data-stu-id="03703-122">MOF</span></span>|<span data-ttu-id="03703-123">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="03703-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="03703-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="03703-124">Namespace</span></span>|<span data-ttu-id="03703-125">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="03703-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="03703-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="03703-126">See Also</span></span>  
 <xref:System.ServiceModel.DeliveryRequirementsAttribute>
