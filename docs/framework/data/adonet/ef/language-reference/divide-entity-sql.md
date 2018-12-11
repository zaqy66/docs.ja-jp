---
title: '- (除算)(Entity SQL)'
ms.date: 03/30/2017
ms.assetid: ef48c368-f3ed-4275-8ada-4e9649781262
ms.openlocfilehash: 38feaf4509ea2ed2838efe4daa257cdff144e863
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53147698"
---
# <a name="-divide-entity-sql"></a><span data-ttu-id="1e0af-102">/ (除算) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="1e0af-102">/ (Divide) (Entity SQL)</span></span>
<span data-ttu-id="1e0af-103">1 つの値を別の値で除算します。</span><span class="sxs-lookup"><span data-stu-id="1e0af-103">Divides one number by another.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1e0af-104">構文</span><span class="sxs-lookup"><span data-stu-id="1e0af-104">Syntax</span></span>  
  
```  
dividend / divisor  
```  
  
## <a name="arguments"></a><span data-ttu-id="1e0af-105">引数</span><span class="sxs-lookup"><span data-stu-id="1e0af-105">Arguments</span></span>  
 `dividend`  
 <span data-ttu-id="1e0af-106">除算する数値式。</span><span class="sxs-lookup"><span data-stu-id="1e0af-106">The numeric expression to divide.</span></span> <span data-ttu-id="1e0af-107">`dividend` は、任意の数値データ型の有効な式です。</span><span class="sxs-lookup"><span data-stu-id="1e0af-107">`dividend` is any valid expression of any one of the numeric data types.</span></span>  
  
 `divisor`  
 <span data-ttu-id="1e0af-108">被除数を除算する数値式。</span><span class="sxs-lookup"><span data-stu-id="1e0af-108">The numeric expression to divide the dividend by.</span></span> <span data-ttu-id="1e0af-109">`divisor` は、任意の数値データ型の有効な式です。</span><span class="sxs-lookup"><span data-stu-id="1e0af-109">`divisor` is any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="1e0af-110">戻り値の型</span><span class="sxs-lookup"><span data-stu-id="1e0af-110">Result Types</span></span>  
 <span data-ttu-id="1e0af-111">2 つの引数の暗黙の型の昇格の結果であるデータ型。</span><span class="sxs-lookup"><span data-stu-id="1e0af-111">The data type that results from the implicit type promotion of the two arguments.</span></span> <span data-ttu-id="1e0af-112">暗黙的な型の上位変換の詳細については、次を参照してください。[型システム](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md)します。</span><span class="sxs-lookup"><span data-stu-id="1e0af-112">For more information about implicit type promotion, see [Type System](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1e0af-113">例</span><span class="sxs-lookup"><span data-stu-id="1e0af-113">Example</span></span>  
 <span data-ttu-id="1e0af-114">次の Entity SQL クエリを使用して、/算術演算子を別の 1 つの数値を除算します。</span><span class="sxs-lookup"><span data-stu-id="1e0af-114">The following Entity SQL query uses the / arithmetic operator to divide one number by another.</span></span> <span data-ttu-id="1e0af-115">このクエリは、AdventureWorks Sales Model に基づいています。</span><span class="sxs-lookup"><span data-stu-id="1e0af-115">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="1e0af-116">このクエリをコンパイルして実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1e0af-116">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="1e0af-117">」の手順に従って[方法。StructuralType 結果を返すクエリを実行](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md)します。</span><span class="sxs-lookup"><span data-stu-id="1e0af-117">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="1e0af-118">次のクエリを引数として `ExecuteStructuralTypeQuery` メソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="1e0af-118">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#DIVIDE](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#divide)]  
  
## <a name="see-also"></a><span data-ttu-id="1e0af-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="1e0af-119">See Also</span></span>  
 [<span data-ttu-id="1e0af-120">Entity SQL リファレンス</span><span class="sxs-lookup"><span data-stu-id="1e0af-120">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
