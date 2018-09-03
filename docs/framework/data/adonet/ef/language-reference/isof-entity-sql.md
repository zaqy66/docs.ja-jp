---
title: ISOF (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 5b2b0d34-d0a7-4bcd-baf2-58aa8456d00b
ms.openlocfilehash: dbea0c3a0087c88bf5ffda7b921764b8a0f9f21d
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2018
ms.locfileid: "43465448"
---
# <a name="isof-entity-sql"></a><span data-ttu-id="fa874-102">ISOF (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="fa874-102">ISOF (Entity SQL)</span></span>
<span data-ttu-id="fa874-103">式の型が指定の型であるか、またはそのサブタイプであるかを判断します。</span><span class="sxs-lookup"><span data-stu-id="fa874-103">Determines whether the type of an expression is of the specified type or one of its subtypes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa874-104">構文</span><span class="sxs-lookup"><span data-stu-id="fa874-104">Syntax</span></span>  
  
```  
expression IS [ NOT ] OF ( [ ONLY ] type )  
```  
  
## <a name="arguments"></a><span data-ttu-id="fa874-105">引数</span><span class="sxs-lookup"><span data-stu-id="fa874-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="fa874-106">型を判断するための任意の有効なクエリ式。</span><span class="sxs-lookup"><span data-stu-id="fa874-106">Any valid query expression to determine the type of.</span></span>  
  
 <span data-ttu-id="fa874-107">NOT</span><span class="sxs-lookup"><span data-stu-id="fa874-107">NOT</span></span>  
 <span data-ttu-id="fa874-108">IS OF の EDM.Boolean の結果を否定します。</span><span class="sxs-lookup"><span data-stu-id="fa874-108">Negates the EDM.Boolean result of IS OF.</span></span>  
  
 <span data-ttu-id="fa874-109">ONLY</span><span class="sxs-lookup"><span data-stu-id="fa874-109">ONLY</span></span>  
 <span data-ttu-id="fa874-110">`true` が `expression` 型であり、そのサブタイプでない場合に限り、IS OF が `type` を返すことを指定します。</span><span class="sxs-lookup"><span data-stu-id="fa874-110">Specifies that IS OF returns `true` only if `expression` is of type `type` and not any of one its subtypes.</span></span>  
  
 `type`  
 <span data-ttu-id="fa874-111">`expression` を判定するための型。</span><span class="sxs-lookup"><span data-stu-id="fa874-111">The type to test `expression` against.</span></span> <span data-ttu-id="fa874-112">型は名前空間で修飾する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa874-112">The type must be namespace-qualified.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fa874-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="fa874-113">Return Value</span></span>  
 <span data-ttu-id="fa874-114">`true` が型 T で、T が基本データ型または `expression` の派生型である場合は、`type` となります。`expression` が実行時に null である場合は null となり、それ以外の場合は `false` となります。</span><span class="sxs-lookup"><span data-stu-id="fa874-114">`true` if `expression` is of type T and T is either a base type, or a derived type of `type`; null if `expression` is null at runtime; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fa874-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="fa874-115">Remarks</span></span>  
 <span data-ttu-id="fa874-116">式`expression IS NOT OF (type)`と`expression IS NOT OF (ONLY type)`を構文的に等価`NOT (expression IS OF (type))`と`NOT (expression IS OF (ONLY type))`、それぞれします。</span><span class="sxs-lookup"><span data-stu-id="fa874-116">The expressions `expression IS NOT OF (type)` and `expression IS NOT OF (ONLY type)` are syntactically equivalent to `NOT (expression IS OF (type))` and `NOT (expression IS OF (ONLY type))`, respectively.</span></span>  
  
 <span data-ttu-id="fa874-117">次の表に、いくつかの通常およびコーナー パターンにおける `IS OF` 演算子の動作を示します。</span><span class="sxs-lookup"><span data-stu-id="fa874-117">The following table shows the behavior of `IS OF` operator over some typical- and corner patterns.</span></span> <span data-ttu-id="fa874-118">すべての例外はクライアント側にスローされてから、プロバイダーが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fa874-118">All exceptions are thrown from the client side before the provider gets invoked:</span></span>  
  
|<span data-ttu-id="fa874-119">パターン</span><span class="sxs-lookup"><span data-stu-id="fa874-119">Pattern</span></span>|<span data-ttu-id="fa874-120">動作</span><span class="sxs-lookup"><span data-stu-id="fa874-120">Behavior</span></span>|  
|-------------|--------------|  
|<span data-ttu-id="fa874-121">null IS OF (EntityType)</span><span class="sxs-lookup"><span data-stu-id="fa874-121">null IS OF (EntityType)</span></span>|<span data-ttu-id="fa874-122">スロー</span><span class="sxs-lookup"><span data-stu-id="fa874-122">Throws</span></span>|  
|<span data-ttu-id="fa874-123">null IS OF (ComplexType)</span><span class="sxs-lookup"><span data-stu-id="fa874-123">null IS OF (ComplexType)</span></span>|<span data-ttu-id="fa874-124">スロー</span><span class="sxs-lookup"><span data-stu-id="fa874-124">Throws</span></span>|  
|<span data-ttu-id="fa874-125">null IS OF (RowType)</span><span class="sxs-lookup"><span data-stu-id="fa874-125">null IS OF (RowType)</span></span>|<span data-ttu-id="fa874-126">スロー</span><span class="sxs-lookup"><span data-stu-id="fa874-126">Throws</span></span>|  
|<span data-ttu-id="fa874-127">TREAT (null AS EntityType) IS OF (EntityType)</span><span class="sxs-lookup"><span data-stu-id="fa874-127">TREAT (null AS EntityType) IS OF (EntityType)</span></span>|<span data-ttu-id="fa874-128">DBNull を返します。</span><span class="sxs-lookup"><span data-stu-id="fa874-128">Returns DBNull</span></span>|  
|<span data-ttu-id="fa874-129">TREAT (null AS ComplexType) IS OF (ComplexType)</span><span class="sxs-lookup"><span data-stu-id="fa874-129">TREAT (null AS ComplexType) IS OF (ComplexType)</span></span>|<span data-ttu-id="fa874-130">スロー</span><span class="sxs-lookup"><span data-stu-id="fa874-130">Throws</span></span>|  
|<span data-ttu-id="fa874-131">TREAT (null AS RowType) IS OF (RowType)</span><span class="sxs-lookup"><span data-stu-id="fa874-131">TREAT (null AS RowType) IS OF (RowType)</span></span>|<span data-ttu-id="fa874-132">スロー</span><span class="sxs-lookup"><span data-stu-id="fa874-132">Throws</span></span>|  
|<span data-ttu-id="fa874-133">EntityType IS OF (EntityType)</span><span class="sxs-lookup"><span data-stu-id="fa874-133">EntityType IS OF (EntityType)</span></span>|<span data-ttu-id="fa874-134">true または false を返します。</span><span class="sxs-lookup"><span data-stu-id="fa874-134">Returns true/false</span></span>|  
|<span data-ttu-id="fa874-135">ComplexType IS OF (ComplexType)</span><span class="sxs-lookup"><span data-stu-id="fa874-135">ComplexType IS OF (ComplexType)</span></span>|<span data-ttu-id="fa874-136">スロー</span><span class="sxs-lookup"><span data-stu-id="fa874-136">Throws</span></span>|  
|<span data-ttu-id="fa874-137">RowType IS OF (RowType)</span><span class="sxs-lookup"><span data-stu-id="fa874-137">RowType IS OF (RowType)</span></span>|<span data-ttu-id="fa874-138">スロー</span><span class="sxs-lookup"><span data-stu-id="fa874-138">Throws</span></span>|  
  
## <a name="example"></a><span data-ttu-id="fa874-139">例</span><span class="sxs-lookup"><span data-stu-id="fa874-139">Example</span></span>  
 <span data-ttu-id="fa874-140">次[!INCLUDE[esql](../../../../../../includes/esql-md.md)]クエリが、IS OF 演算子を使用して、クエリ式の種類を判断し、TREAT 演算子を使用して、Course 型のオブジェクトを OnsiteCourse 型のオブジェクトのコレクションに変換します。</span><span class="sxs-lookup"><span data-stu-id="fa874-140">The following [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query uses the IS OF operator to determine the type of a query expression, and then uses the TREAT operator to convert an object of the type Course to a collection of objects of the type OnsiteCourse.</span></span> <span data-ttu-id="fa874-141">クエリに基づいていますが、 [School モデル](https://msdn.microsoft.com/library/859a9587-81ea-4a45-9bc0-f8d330e1adac)します。</span><span class="sxs-lookup"><span data-stu-id="fa874-141">The query is based on the [School Model](https://msdn.microsoft.com/library/859a9587-81ea-4a45-9bc0-f8d330e1adac).</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#TREAT_ISOF](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#treat_isof)]  
  
## <a name="see-also"></a><span data-ttu-id="fa874-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa874-142">See Also</span></span>  
 [<span data-ttu-id="fa874-143">Entity SQL リファレンス</span><span class="sxs-lookup"><span data-stu-id="fa874-143">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
