---
title: + (追加)
ms.date: 03/30/2017
ms.assetid: 51769b02-a8f7-4177-9e99-bbd10e77092c
ms.openlocfilehash: a3c41ef8cf393a4d1b1deb362d6a3614558a34ba
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47086263"
---
# <a name="-add"></a><span data-ttu-id="71fcd-102">+ (加算)</span><span class="sxs-lookup"><span data-stu-id="71fcd-102">+ (Add)</span></span>
<span data-ttu-id="71fcd-103">2 つの値を加算します。</span><span class="sxs-lookup"><span data-stu-id="71fcd-103">Adds two numbers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="71fcd-104">構文</span><span class="sxs-lookup"><span data-stu-id="71fcd-104">Syntax</span></span>  
  
```  
expression + expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="71fcd-105">引数</span><span class="sxs-lookup"><span data-stu-id="71fcd-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="71fcd-106">任意の数値データ型の有効な式。</span><span class="sxs-lookup"><span data-stu-id="71fcd-106">Any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="71fcd-107">戻り値の型</span><span class="sxs-lookup"><span data-stu-id="71fcd-107">Result Types</span></span>  
 <span data-ttu-id="71fcd-108">2 つの引数の暗黙の型の昇格の結果であるデータ型。</span><span class="sxs-lookup"><span data-stu-id="71fcd-108">The data type that results from the implicit type promotion of the two arguments.</span></span> <span data-ttu-id="71fcd-109">暗黙的な型の上位変換の詳細については、次を参照してください。[型システム](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md)します。</span><span class="sxs-lookup"><span data-stu-id="71fcd-109">For more information about implicit type promotion, see [Type System](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="71fcd-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="71fcd-110">Remarks</span></span>  
 <span data-ttu-id="71fcd-111">EDM.String 型の場合は、値が連結されます。</span><span class="sxs-lookup"><span data-stu-id="71fcd-111">For EDM.String types, addition is concatenation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="71fcd-112">例</span><span class="sxs-lookup"><span data-stu-id="71fcd-112">Example</span></span>  
 <span data-ttu-id="71fcd-113">次の Entity SQL クエリでは、+ 算術演算子を使用して 2 つの数値を加算します。</span><span class="sxs-lookup"><span data-stu-id="71fcd-113">The following Entity SQL query uses the + arithmetic operator to add two numbers.</span></span> <span data-ttu-id="71fcd-114">このクエリは、AdventureWorks Sales Model に基づいています。</span><span class="sxs-lookup"><span data-stu-id="71fcd-114">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="71fcd-115">このクエリをコンパイルして実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="71fcd-115">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="71fcd-116">「 [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md)」の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="71fcd-116">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="71fcd-117">次のクエリを引数として `ExecuteStructuralTypeQuery` メソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="71fcd-117">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#ADD](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#add)]  
  
## <a name="see-also"></a><span data-ttu-id="71fcd-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="71fcd-118">See Also</span></span>  
 [<span data-ttu-id="71fcd-119">Entity SQL リファレンス</span><span class="sxs-lookup"><span data-stu-id="71fcd-119">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)  
 [<span data-ttu-id="71fcd-120">概念モデルの型 (CSDL)</span><span class="sxs-lookup"><span data-stu-id="71fcd-120">Conceptual Model Types (CSDL)</span></span>](https://msdn.microsoft.com/library/987b995f-e429-4569-9559-b4146744def4)
