---
title: ISOF (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 5b2b0d34-d0a7-4bcd-baf2-58aa8456d00b
ms.openlocfilehash: 72443060584eaca5aa8c1ea19393dfc043722c90
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54731544"
---
# <a name="isof-entity-sql"></a><span data-ttu-id="33ce0-102">ISOF (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="33ce0-102">ISOF (Entity SQL)</span></span>
<span data-ttu-id="33ce0-103">式の型が指定の型であるか、またはそのサブタイプであるかを判断します。</span><span class="sxs-lookup"><span data-stu-id="33ce0-103">Determines whether the type of an expression is of the specified type or one of its subtypes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="33ce0-104">構文</span><span class="sxs-lookup"><span data-stu-id="33ce0-104">Syntax</span></span>  
  
```  
expression IS [ NOT ] OF ( [ ONLY ] type )  
```  
  
## <a name="arguments"></a><span data-ttu-id="33ce0-105">引数</span><span class="sxs-lookup"><span data-stu-id="33ce0-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="33ce0-106">型を判断するための任意の有効なクエリ式。</span><span class="sxs-lookup"><span data-stu-id="33ce0-106">Any valid query expression to determine the type of.</span></span>  
  
 <span data-ttu-id="33ce0-107">NOT</span><span class="sxs-lookup"><span data-stu-id="33ce0-107">NOT</span></span>  
 <span data-ttu-id="33ce0-108">IS OF の EDM.Boolean の結果を否定します。</span><span class="sxs-lookup"><span data-stu-id="33ce0-108">Negates the EDM.Boolean result of IS OF.</span></span>  
  
 <span data-ttu-id="33ce0-109">ONLY</span><span class="sxs-lookup"><span data-stu-id="33ce0-109">ONLY</span></span>  
 <span data-ttu-id="33ce0-110">`true` が `expression` 型であり、そのサブタイプでない場合に限り、IS OF が `type` を返すことを指定します。</span><span class="sxs-lookup"><span data-stu-id="33ce0-110">Specifies that IS OF returns `true` only if `expression` is of type `type` and not any of one its subtypes.</span></span>  
  
 `type`  
 <span data-ttu-id="33ce0-111">`expression` を判定するための型。</span><span class="sxs-lookup"><span data-stu-id="33ce0-111">The type to test `expression` against.</span></span> <span data-ttu-id="33ce0-112">型は名前空間で修飾する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33ce0-112">The type must be namespace-qualified.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="33ce0-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="33ce0-113">Return Value</span></span>  
 <span data-ttu-id="33ce0-114">`true` が型 T で、T が基本データ型または `expression` の派生型である場合は、`type` となります。`expression` が実行時に null である場合は null となり、それ以外の場合は `false` となります。</span><span class="sxs-lookup"><span data-stu-id="33ce0-114">`true` if `expression` is of type T and T is either a base type, or a derived type of `type`; null if `expression` is null at runtime; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="33ce0-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="33ce0-115">Remarks</span></span>  
 <span data-ttu-id="33ce0-116">式`expression IS NOT OF (type)`と`expression IS NOT OF (ONLY type)`を構文的に等価`NOT (expression IS OF (type))`と`NOT (expression IS OF (ONLY type))`、それぞれします。</span><span class="sxs-lookup"><span data-stu-id="33ce0-116">The expressions `expression IS NOT OF (type)` and `expression IS NOT OF (ONLY type)` are syntactically equivalent to `NOT (expression IS OF (type))` and `NOT (expression IS OF (ONLY type))`, respectively.</span></span>  
  
 <span data-ttu-id="33ce0-117">次の表に、いくつかの通常およびコーナー パターンにおける `IS OF` 演算子の動作を示します。</span><span class="sxs-lookup"><span data-stu-id="33ce0-117">The following table shows the behavior of `IS OF` operator over some typical- and corner patterns.</span></span> <span data-ttu-id="33ce0-118">すべての例外はクライアント側にスローされてから、プロバイダーが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="33ce0-118">All exceptions are thrown from the client side before the provider gets invoked:</span></span>  
  
|<span data-ttu-id="33ce0-119">パターン</span><span class="sxs-lookup"><span data-stu-id="33ce0-119">Pattern</span></span>|<span data-ttu-id="33ce0-120">動作</span><span class="sxs-lookup"><span data-stu-id="33ce0-120">Behavior</span></span>|  
|-------------|--------------|  
|<span data-ttu-id="33ce0-121">null IS OF (EntityType)</span><span class="sxs-lookup"><span data-stu-id="33ce0-121">null IS OF (EntityType)</span></span>|<span data-ttu-id="33ce0-122">スロー</span><span class="sxs-lookup"><span data-stu-id="33ce0-122">Throws</span></span>|  
|<span data-ttu-id="33ce0-123">null IS OF (ComplexType)</span><span class="sxs-lookup"><span data-stu-id="33ce0-123">null IS OF (ComplexType)</span></span>|<span data-ttu-id="33ce0-124">スロー</span><span class="sxs-lookup"><span data-stu-id="33ce0-124">Throws</span></span>|  
|<span data-ttu-id="33ce0-125">null IS OF (RowType)</span><span class="sxs-lookup"><span data-stu-id="33ce0-125">null IS OF (RowType)</span></span>|<span data-ttu-id="33ce0-126">スロー</span><span class="sxs-lookup"><span data-stu-id="33ce0-126">Throws</span></span>|  
|<span data-ttu-id="33ce0-127">TREAT (null AS EntityType) IS OF (EntityType)</span><span class="sxs-lookup"><span data-stu-id="33ce0-127">TREAT (null AS EntityType) IS OF (EntityType)</span></span>|<span data-ttu-id="33ce0-128">DBNull を返します。</span><span class="sxs-lookup"><span data-stu-id="33ce0-128">Returns DBNull</span></span>|  
|<span data-ttu-id="33ce0-129">TREAT (null AS ComplexType) IS OF (ComplexType)</span><span class="sxs-lookup"><span data-stu-id="33ce0-129">TREAT (null AS ComplexType) IS OF (ComplexType)</span></span>|<span data-ttu-id="33ce0-130">スロー</span><span class="sxs-lookup"><span data-stu-id="33ce0-130">Throws</span></span>|  
|<span data-ttu-id="33ce0-131">TREAT (null AS RowType) IS OF (RowType)</span><span class="sxs-lookup"><span data-stu-id="33ce0-131">TREAT (null AS RowType) IS OF (RowType)</span></span>|<span data-ttu-id="33ce0-132">スロー</span><span class="sxs-lookup"><span data-stu-id="33ce0-132">Throws</span></span>|  
|<span data-ttu-id="33ce0-133">EntityType IS OF (EntityType)</span><span class="sxs-lookup"><span data-stu-id="33ce0-133">EntityType IS OF (EntityType)</span></span>|<span data-ttu-id="33ce0-134">true または false を返します。</span><span class="sxs-lookup"><span data-stu-id="33ce0-134">Returns true/false</span></span>|  
|<span data-ttu-id="33ce0-135">ComplexType IS OF (ComplexType)</span><span class="sxs-lookup"><span data-stu-id="33ce0-135">ComplexType IS OF (ComplexType)</span></span>|<span data-ttu-id="33ce0-136">スロー</span><span class="sxs-lookup"><span data-stu-id="33ce0-136">Throws</span></span>|  
|<span data-ttu-id="33ce0-137">RowType IS OF (RowType)</span><span class="sxs-lookup"><span data-stu-id="33ce0-137">RowType IS OF (RowType)</span></span>|<span data-ttu-id="33ce0-138">スロー</span><span class="sxs-lookup"><span data-stu-id="33ce0-138">Throws</span></span>|  
  
## <a name="example"></a><span data-ttu-id="33ce0-139">例</span><span class="sxs-lookup"><span data-stu-id="33ce0-139">Example</span></span>  
 <span data-ttu-id="33ce0-140">次[!INCLUDE[esql](../../../../../../includes/esql-md.md)]クエリが、IS OF 演算子を使用して、クエリ式の種類を判断し、TREAT 演算子を使用して、Course 型のオブジェクトを OnsiteCourse 型のオブジェクトのコレクションに変換します。</span><span class="sxs-lookup"><span data-stu-id="33ce0-140">The following [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query uses the IS OF operator to determine the type of a query expression, and then uses the TREAT operator to convert an object of the type Course to a collection of objects of the type OnsiteCourse.</span></span> <span data-ttu-id="33ce0-141">このクエリは、 [School モデル](https://msdn.microsoft.com/library/859a9587-81ea-4a45-9bc0-f8d330e1adac)に基づいています。</span><span class="sxs-lookup"><span data-stu-id="33ce0-141">The query is based on the [School Model](https://msdn.microsoft.com/library/859a9587-81ea-4a45-9bc0-f8d330e1adac).</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#TREAT_ISOF](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#treat_isof)]  
  
## <a name="see-also"></a><span data-ttu-id="33ce0-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="33ce0-142">See also</span></span>
- [<span data-ttu-id="33ce0-143">Entity SQL リファレンス</span><span class="sxs-lookup"><span data-stu-id="33ce0-143">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
