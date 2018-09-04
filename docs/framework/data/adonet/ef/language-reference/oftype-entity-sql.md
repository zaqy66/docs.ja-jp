---
title: OFTYPE (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 6d259ca7-bbf0-40f8-a154-181d25c0d67e
ms.openlocfilehash: c90950e11cbfca7a49b505c1654d08be504990e1
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43564654"
---
# <a name="oftype-entity-sql"></a><span data-ttu-id="08c4c-102">OFTYPE (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="08c4c-102">OFTYPE (Entity SQL)</span></span>
<span data-ttu-id="08c4c-103">クエリ式を使用して、指定された型のオブジェクトのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="08c4c-103">Returns a collection of objects from a query expression that is of a specific type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08c4c-104">構文</span><span class="sxs-lookup"><span data-stu-id="08c4c-104">Syntax</span></span>  
  
```  
OFTYPE ( expression, [ONLY] test_type )  
```  
  
## <a name="arguments"></a><span data-ttu-id="08c4c-105">引数</span><span class="sxs-lookup"><span data-stu-id="08c4c-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="08c4c-106">オブジェクトのコレクションを返す任意の有効なクエリ式。</span><span class="sxs-lookup"><span data-stu-id="08c4c-106">Any valid query expression that returns a collection of objects.</span></span>  
  
 `test_type`  
 <span data-ttu-id="08c4c-107">`expression` から返される各オブジェクトを判定するための型。</span><span class="sxs-lookup"><span data-stu-id="08c4c-107">The type to test each object returned by `expression` against.</span></span> <span data-ttu-id="08c4c-108">型は名前空間で修飾する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08c4c-108">The type must be qualified by a namespace.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="08c4c-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="08c4c-109">Return Value</span></span>  
 <span data-ttu-id="08c4c-110">`test_type`型であるか、 `test_type`の基本データ型または派生型であるオブジェクトのコレクション。</span><span class="sxs-lookup"><span data-stu-id="08c4c-110">A collection of objects that are of type `test_type`, or a base type or derived type of `test_type`.</span></span> <span data-ttu-id="08c4c-111">ONLY を指定した場合、 `test_type` のインスタンスまたは空のコレクションのみ返されます。</span><span class="sxs-lookup"><span data-stu-id="08c4c-111">If ONLY is specified, only instances of the `test_type` or an empty collection will be returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="08c4c-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="08c4c-112">Remarks</span></span>  
 <span data-ttu-id="08c4c-113">`OFTYPE` 式は、コレクションの各要素の型を判定するための式です。</span><span class="sxs-lookup"><span data-stu-id="08c4c-113">An `OFTYPE` expression specifies a type expression that is issued to perform a type test against each element of a collection.</span></span>  <span data-ttu-id="08c4c-114">`OFTYPE` 式では、指定された型の新しいコレクションが生成されます。生成されたコレクションには、指定された型と同じか、そのサブタイプの要素だけが格納されます。</span><span class="sxs-lookup"><span data-stu-id="08c4c-114">The `OFTYPE` expression produces a new collection of the specified type containing only those elements that were either equivalent to that type or a sub-type of it.</span></span>  
  
 <span data-ttu-id="08c4c-115">`OFTYPE` 式は、次のクエリ式の省略形です。</span><span class="sxs-lookup"><span data-stu-id="08c4c-115">An `OFTYPE` expression is an abbreviation of the following query expression:</span></span>  
  
```  
select value treat(t as T) from ts as t where t is of (T)  
```  
  
 <span data-ttu-id="08c4c-116">Manager が Employee のサブタイプである場合、次の式からは、従業員 (employee) のコレクションのうち、マネージャー (manager) のコレクションだけが返されます。</span><span class="sxs-lookup"><span data-stu-id="08c4c-116">Given that a Manager is a subtype of Employee, the following expression produces a collection of only managers from a collection of employees:</span></span>  
  
```  
OfType(employees, NamespaceName.Manager)  
```  
  
 <span data-ttu-id="08c4c-117">型フィルターを使用してコレクションをアップ キャストすることもできます。</span><span class="sxs-lookup"><span data-stu-id="08c4c-117">It is also possible to up cast a collection using the type filter:</span></span>  
  
```  
OfType(executives, NamespaceName.Manager)  
```  
  
 <span data-ttu-id="08c4c-118">すべての企業幹部はマネージャーであるので、結果のコレクションには元の企業幹部がすべて含まれたままですが、コレクションはマネージャーのコレクションとして型指定されています。</span><span class="sxs-lookup"><span data-stu-id="08c4c-118">Since all executives are managers, the resulting collection still contains all the original executives, though the collection is now typed as a collection of managers.</span></span>  
  
 <span data-ttu-id="08c4c-119">次の表は、いくつかのパターンにおける `OFTYPE` 演算子の動作を示しています。</span><span class="sxs-lookup"><span data-stu-id="08c4c-119">The following table shows the behavior of the `OFTYPE` operator over some patterns.</span></span> <span data-ttu-id="08c4c-120">すべての例外はクライアント側にスローされてから、プロバイダーが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08c4c-120">All exceptions are thrown from the client side before the provider is invoked:</span></span>  
  
|<span data-ttu-id="08c4c-121">パターン</span><span class="sxs-lookup"><span data-stu-id="08c4c-121">Pattern</span></span>|<span data-ttu-id="08c4c-122">動作</span><span class="sxs-lookup"><span data-stu-id="08c4c-122">Behavior</span></span>|  
|-------------|--------------|  
|<span data-ttu-id="08c4c-123">OFTYPE(Collection(EntityType), EntityType)</span><span class="sxs-lookup"><span data-stu-id="08c4c-123">OFTYPE(Collection(EntityType), EntityType)</span></span>|<span data-ttu-id="08c4c-124">Collection(EntityType)</span><span class="sxs-lookup"><span data-stu-id="08c4c-124">Collection(EntityType)</span></span>|  
|<span data-ttu-id="08c4c-125">OFTYPE(Collection(ComplexType), ComplexType)</span><span class="sxs-lookup"><span data-stu-id="08c4c-125">OFTYPE(Collection(ComplexType), ComplexType)</span></span>|<span data-ttu-id="08c4c-126">スロー</span><span class="sxs-lookup"><span data-stu-id="08c4c-126">Throws</span></span>|  
|<span data-ttu-id="08c4c-127">OFTYPE(Collection(RowType), RowType)</span><span class="sxs-lookup"><span data-stu-id="08c4c-127">OFTYPE(Collection(RowType), RowType)</span></span>|<span data-ttu-id="08c4c-128">スロー</span><span class="sxs-lookup"><span data-stu-id="08c4c-128">Throws</span></span>|  
  
## <a name="example"></a><span data-ttu-id="08c4c-129">例</span><span class="sxs-lookup"><span data-stu-id="08c4c-129">Example</span></span>  
 <span data-ttu-id="08c4c-130">次の [!INCLUDE[esql](../../../../../../includes/esql-md.md)] クエリでは、OFTYPE 演算子を使用して、Course オブジェクトのコレクションから OnsiteCourse オブジェクトのコレクションを取得して返します。</span><span class="sxs-lookup"><span data-stu-id="08c4c-130">The following [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query uses the OFTYPE operator to return a collection of OnsiteCourse objects from a collection of Course objects.</span></span> <span data-ttu-id="08c4c-131">クエリに基づいていますが、 [School モデル](https://msdn.microsoft.com/library/859a9587-81ea-4a45-9bc0-f8d330e1adac)します。</span><span class="sxs-lookup"><span data-stu-id="08c4c-131">The query is based on the [School Model](https://msdn.microsoft.com/library/859a9587-81ea-4a45-9bc0-f8d330e1adac).</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#OFTYPE](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#oftype)]  
  
## <a name="see-also"></a><span data-ttu-id="08c4c-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="08c4c-132">See Also</span></span>  
 [<span data-ttu-id="08c4c-133">Entity SQL リファレンス</span><span class="sxs-lookup"><span data-stu-id="08c4c-133">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
