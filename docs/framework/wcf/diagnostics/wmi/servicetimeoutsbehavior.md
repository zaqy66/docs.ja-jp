---
title: ServiceTimeoutsBehavior
ms.date: 03/30/2017
ms.assetid: 4412525d-a3cc-4eae-b3e8-a50ce766d09d
ms.openlocfilehash: 1a5284915de739e95325234318842a4d1ab607be
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/26/2018
ms.locfileid: "50135246"
---
# <a name="servicetimeoutsbehavior"></a><span data-ttu-id="4f296-102">ServiceTimeoutsBehavior</span><span class="sxs-lookup"><span data-stu-id="4f296-102">ServiceTimeoutsBehavior</span></span>
<span data-ttu-id="4f296-103">ServiceTimeoutsBehavior</span><span class="sxs-lookup"><span data-stu-id="4f296-103">ServiceTimeoutsBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f296-104">構文</span><span class="sxs-lookup"><span data-stu-id="4f296-104">Syntax</span></span>  
  
```csharp
class ServiceTimeoutsBehavior : Behavior  
{  
  datetime TransactionTimeout;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="4f296-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="4f296-105">Methods</span></span>  
 <span data-ttu-id="4f296-106">ServiceTimeoutsBehavior クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="4f296-106">The ServiceTimeoutsBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="4f296-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f296-107">Properties</span></span>  
 <span data-ttu-id="4f296-108">ServiceTimeoutsBehavior クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="4f296-108">The ServiceTimeoutsBehavior class has the following property:</span></span>  
  
### <a name="transactiontimeout"></a><span data-ttu-id="4f296-109">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="4f296-109">TransactionTimeout</span></span>  
 <span data-ttu-id="4f296-110">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="4f296-110">Data type: datetime</span></span>  
  
 <span data-ttu-id="4f296-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="4f296-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="4f296-112">トランザクションを完了しなければならない期間。</span><span class="sxs-lookup"><span data-stu-id="4f296-112">The period within which a transaction must complete.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4f296-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="4f296-113">Requirements</span></span>  
  
|<span data-ttu-id="4f296-114">MOF</span><span class="sxs-lookup"><span data-stu-id="4f296-114">MOF</span></span>|<span data-ttu-id="4f296-115">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="4f296-115">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="4f296-116">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f296-116">Namespace</span></span>|<span data-ttu-id="4f296-117">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="4f296-117">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4f296-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f296-118">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
