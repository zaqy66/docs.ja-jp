---
title: ServiceTimeoutsBehavior
ms.date: 03/30/2017
ms.assetid: 4412525d-a3cc-4eae-b3e8-a50ce766d09d
ms.openlocfilehash: 1a5284915de739e95325234318842a4d1ab607be
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50196979"
---
# <a name="servicetimeoutsbehavior"></a><span data-ttu-id="26695-102">ServiceTimeoutsBehavior</span><span class="sxs-lookup"><span data-stu-id="26695-102">ServiceTimeoutsBehavior</span></span>
<span data-ttu-id="26695-103">ServiceTimeoutsBehavior</span><span class="sxs-lookup"><span data-stu-id="26695-103">ServiceTimeoutsBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26695-104">構文</span><span class="sxs-lookup"><span data-stu-id="26695-104">Syntax</span></span>  
  
```csharp
class ServiceTimeoutsBehavior : Behavior  
{  
  datetime TransactionTimeout;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="26695-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="26695-105">Methods</span></span>  
 <span data-ttu-id="26695-106">ServiceTimeoutsBehavior クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="26695-106">The ServiceTimeoutsBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="26695-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="26695-107">Properties</span></span>  
 <span data-ttu-id="26695-108">ServiceTimeoutsBehavior クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="26695-108">The ServiceTimeoutsBehavior class has the following property:</span></span>  
  
### <a name="transactiontimeout"></a><span data-ttu-id="26695-109">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="26695-109">TransactionTimeout</span></span>  
 <span data-ttu-id="26695-110">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="26695-110">Data type: datetime</span></span>  
  
 <span data-ttu-id="26695-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="26695-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="26695-112">トランザクションを完了しなければならない期間。</span><span class="sxs-lookup"><span data-stu-id="26695-112">The period within which a transaction must complete.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="26695-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="26695-113">Requirements</span></span>  
  
|<span data-ttu-id="26695-114">MOF</span><span class="sxs-lookup"><span data-stu-id="26695-114">MOF</span></span>|<span data-ttu-id="26695-115">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="26695-115">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="26695-116">Namespace</span><span class="sxs-lookup"><span data-stu-id="26695-116">Namespace</span></span>|<span data-ttu-id="26695-117">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="26695-117">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="26695-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="26695-118">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
