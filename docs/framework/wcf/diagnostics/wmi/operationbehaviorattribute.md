---
title: OperationBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 8c9b0755-9e83-411f-bdcb-61a586022797
ms.openlocfilehash: d0bf59e6064748a045f761777a2f8f3e88f1cb5a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54504328"
---
# <a name="operationbehaviorattribute"></a><span data-ttu-id="35050-102">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="35050-102">OperationBehaviorAttribute</span></span>
<span data-ttu-id="35050-103">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="35050-103">OperationBehaviorAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35050-104">構文</span><span class="sxs-lookup"><span data-stu-id="35050-104">Syntax</span></span>  
  
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
  
## <a name="methods"></a><span data-ttu-id="35050-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="35050-105">Methods</span></span>  
 <span data-ttu-id="35050-106">OperationBehaviorAttribute クラスで定義されるメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="35050-106">The OperationBehaviorAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="35050-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="35050-107">Properties</span></span>  
 <span data-ttu-id="35050-108">OperationBehaviorAttribute クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="35050-108">The OperationBehaviorAttribute class has the following properties:</span></span>  
  
### <a name="autodisposeparameters"></a><span data-ttu-id="35050-109">AutoDisposeParameters</span><span class="sxs-lookup"><span data-stu-id="35050-109">AutoDisposeParameters</span></span>  
 <span data-ttu-id="35050-110">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="35050-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="35050-111">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="35050-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="35050-112">パラメーターの自動破棄機能の状態です。</span><span class="sxs-lookup"><span data-stu-id="35050-112">The state of the auto-dispose feature for parameters.</span></span>  
  
### <a name="impersonation"></a><span data-ttu-id="35050-113">偽装</span><span class="sxs-lookup"><span data-stu-id="35050-113">Impersonation</span></span>  
 <span data-ttu-id="35050-114">データ型: string</span><span class="sxs-lookup"><span data-stu-id="35050-114">Data type: string</span></span>  
  
 <span data-ttu-id="35050-115">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="35050-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="35050-116">操作がサポートする、呼び出し元の偽装レベルを示します。</span><span class="sxs-lookup"><span data-stu-id="35050-116">Indicates the level of caller impersonation that the operation supports.</span></span>  
  
### <a name="releaseinstancemode"></a><span data-ttu-id="35050-117">ReleaseInstanceMode</span><span class="sxs-lookup"><span data-stu-id="35050-117">ReleaseInstanceMode</span></span>  
 <span data-ttu-id="35050-118">データ型: string</span><span class="sxs-lookup"><span data-stu-id="35050-118">Data type: string</span></span>  
  
 <span data-ttu-id="35050-119">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="35050-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="35050-120">操作の呼び出し過程のどの時点でオブジェクトをリサイクルするかを示します。</span><span class="sxs-lookup"><span data-stu-id="35050-120">Indicates when in the course of an operation invocation to recycle the object.</span></span>  
  
### <a name="transactionautocomplete"></a><span data-ttu-id="35050-121">TransactionAutoComplete</span><span class="sxs-lookup"><span data-stu-id="35050-121">TransactionAutoComplete</span></span>  
 <span data-ttu-id="35050-122">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="35050-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="35050-123">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="35050-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="35050-124">未処理の例外が発生しなかった場合に、現在のトランザクションを自動的にコミットするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="35050-124">Indicates whether to automatically commit the current transaction if no unhandled exceptions occur.</span></span>  
  
### <a name="transactionscoperequired"></a><span data-ttu-id="35050-125">TransactionScopeRequired</span><span class="sxs-lookup"><span data-stu-id="35050-125">TransactionScopeRequired</span></span>  
 <span data-ttu-id="35050-126">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="35050-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="35050-127">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="35050-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="35050-128">操作がトランザクションを必要とするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="35050-128">Indicates whether the operation requires a transaction.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="35050-129">必要条件</span><span class="sxs-lookup"><span data-stu-id="35050-129">Requirements</span></span>  
  
|<span data-ttu-id="35050-130">MOF</span><span class="sxs-lookup"><span data-stu-id="35050-130">MOF</span></span>|<span data-ttu-id="35050-131">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="35050-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="35050-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="35050-132">Namespace</span></span>|<span data-ttu-id="35050-133">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="35050-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="35050-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="35050-134">See also</span></span>
- <xref:System.ServiceModel.OperationBehaviorAttribute>
