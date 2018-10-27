---
title: OperationBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 8c9b0755-9e83-411f-bdcb-61a586022797
ms.openlocfilehash: 6266713307846ab953299370835726958196fac1
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50185340"
---
# <a name="operationbehaviorattribute"></a><span data-ttu-id="57804-102">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="57804-102">OperationBehaviorAttribute</span></span>
<span data-ttu-id="57804-103">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="57804-103">OperationBehaviorAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57804-104">構文</span><span class="sxs-lookup"><span data-stu-id="57804-104">Syntax</span></span>  
  
```csharp
class OperationBehaviorAttribute : Behavior  
{  
  boolean AutoDisposeParameters;  
  string Impersonation;  
  string ReleaseInstanceMode;  
  boolean TransactionAutoComplete;  
  boolean TransactionScopeRequired;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="57804-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="57804-105">Methods</span></span>  
 <span data-ttu-id="57804-106">OperationBehaviorAttribute クラスで定義されるメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="57804-106">The OperationBehaviorAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="57804-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="57804-107">Properties</span></span>  
 <span data-ttu-id="57804-108">OperationBehaviorAttribute クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="57804-108">The OperationBehaviorAttribute class has the following properties:</span></span>  
  
### <a name="autodisposeparameters"></a><span data-ttu-id="57804-109">AutoDisposeParameters</span><span class="sxs-lookup"><span data-stu-id="57804-109">AutoDisposeParameters</span></span>  
 <span data-ttu-id="57804-110">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="57804-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="57804-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="57804-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57804-112">パラメーターの自動破棄機能の状態です。</span><span class="sxs-lookup"><span data-stu-id="57804-112">The state of the auto-dispose feature for parameters.</span></span>  
  
### <a name="impersonation"></a><span data-ttu-id="57804-113">偽装</span><span class="sxs-lookup"><span data-stu-id="57804-113">Impersonation</span></span>  
 <span data-ttu-id="57804-114">データ型: string</span><span class="sxs-lookup"><span data-stu-id="57804-114">Data type: string</span></span>  
  
 <span data-ttu-id="57804-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="57804-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57804-116">操作がサポートする、呼び出し元の偽装レベルを示します。</span><span class="sxs-lookup"><span data-stu-id="57804-116">Indicates the level of caller impersonation that the operation supports.</span></span>  
  
### <a name="releaseinstancemode"></a><span data-ttu-id="57804-117">ReleaseInstanceMode</span><span class="sxs-lookup"><span data-stu-id="57804-117">ReleaseInstanceMode</span></span>  
 <span data-ttu-id="57804-118">データ型: string</span><span class="sxs-lookup"><span data-stu-id="57804-118">Data type: string</span></span>  
  
 <span data-ttu-id="57804-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="57804-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57804-120">操作の呼び出し過程のどの時点でオブジェクトをリサイクルするかを示します。</span><span class="sxs-lookup"><span data-stu-id="57804-120">Indicates when in the course of an operation invocation to recycle the object.</span></span>  
  
### <a name="transactionautocomplete"></a><span data-ttu-id="57804-121">TransactionAutoComplete</span><span class="sxs-lookup"><span data-stu-id="57804-121">TransactionAutoComplete</span></span>  
 <span data-ttu-id="57804-122">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="57804-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="57804-123">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="57804-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57804-124">未処理の例外が発生しなかった場合に、現在のトランザクションを自動的にコミットするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="57804-124">Indicates whether to automatically commit the current transaction if no unhandled exceptions occur.</span></span>  
  
### <a name="transactionscoperequired"></a><span data-ttu-id="57804-125">TransactionScopeRequired</span><span class="sxs-lookup"><span data-stu-id="57804-125">TransactionScopeRequired</span></span>  
 <span data-ttu-id="57804-126">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="57804-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="57804-127">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="57804-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57804-128">操作がトランザクションを必要とするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="57804-128">Indicates whether the operation requires a transaction.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57804-129">必要条件</span><span class="sxs-lookup"><span data-stu-id="57804-129">Requirements</span></span>  
  
|<span data-ttu-id="57804-130">MOF</span><span class="sxs-lookup"><span data-stu-id="57804-130">MOF</span></span>|<span data-ttu-id="57804-131">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="57804-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="57804-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="57804-132">Namespace</span></span>|<span data-ttu-id="57804-133">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="57804-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="57804-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="57804-134">See Also</span></span>  
 <xref:System.ServiceModel.OperationBehaviorAttribute>
