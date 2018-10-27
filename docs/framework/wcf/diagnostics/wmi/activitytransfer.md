---
title: ActivityTransfer
ms.date: 03/30/2017
ms.assetid: fc40ef17-2a92-4ce2-853c-6ba8e5d571f3
ms.openlocfilehash: 936e870c1ec991e2e33acf8a08ccc93975989679
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2018
ms.locfileid: "50034429"
---
# <a name="activitytransfer"></a><span data-ttu-id="830c6-102">ActivityTransfer</span><span class="sxs-lookup"><span data-stu-id="830c6-102">ActivityTransfer</span></span>
<span data-ttu-id="830c6-103">アクティビティ転送イベント</span><span class="sxs-lookup"><span data-stu-id="830c6-103">Activity Transfer Event</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="830c6-104">構文</span><span class="sxs-lookup"><span data-stu-id="830c6-104">Syntax</span></span>  
  
```csharp
class ActivityTransfer : WSAT_TraceEvent  
{  
  object ActivityID;  
  object RelatedActivityID;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="830c6-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="830c6-105">Methods</span></span>  
 <span data-ttu-id="830c6-106">ActivityTransfer クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="830c6-106">The ActivityTransfer class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="830c6-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="830c6-107">Properties</span></span>  
 <span data-ttu-id="830c6-108">ActivityTransfer クラスには次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="830c6-108">The ActivityTransfer class has the following properties:</span></span>  
  
### <a name="activityid"></a><span data-ttu-id="830c6-109">ActivityID</span><span class="sxs-lookup"><span data-stu-id="830c6-109">ActivityID</span></span>  
  
-   <span data-ttu-id="830c6-110">データ型: object</span><span class="sxs-lookup"><span data-stu-id="830c6-110">Data type: object</span></span>  
    <span data-ttu-id="830c6-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="830c6-111">Access type: Read-only</span></span>  
  
-   <span data-ttu-id="830c6-112">アクティビティ ID</span><span class="sxs-lookup"><span data-stu-id="830c6-112">Activity ID</span></span>  
  
### <a name="relatedactivityid"></a><span data-ttu-id="830c6-113">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="830c6-113">RelatedActivityID</span></span>  
  
-   <span data-ttu-id="830c6-114">データ型: object</span><span class="sxs-lookup"><span data-stu-id="830c6-114">Data type: object</span></span>  
    <span data-ttu-id="830c6-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="830c6-115">Access type: Read-only</span></span>  
  
-   <span data-ttu-id="830c6-116">関連アクティビティ ID</span><span class="sxs-lookup"><span data-stu-id="830c6-116">Related Activity ID</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="830c6-117">要件</span><span class="sxs-lookup"><span data-stu-id="830c6-117">Requirements</span></span>  
  
|<span data-ttu-id="830c6-118">MOF</span><span class="sxs-lookup"><span data-stu-id="830c6-118">MOF</span></span>|<span data-ttu-id="830c6-119">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="830c6-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="830c6-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="830c6-120">Namespace</span></span>|<span data-ttu-id="830c6-121">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="830c6-121">Defined in root\ServiceModel.</span></span>|
