---
title: 数値演算子および比較演算子
ms.date: 03/30/2017
ms.assetid: 25b4a26a-06f2-4f80-87a9-76705ed46197
ms.openlocfilehash: e2bdc55cd6c2203bc96d0766e5e53a57294d4d7e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54554713"
---
# <a name="numeric-and-comparison-operators"></a><span data-ttu-id="f8be8-102">数値演算子および比較演算子</span><span class="sxs-lookup"><span data-stu-id="f8be8-102">Numeric and Comparison Operators</span></span>
<span data-ttu-id="f8be8-103">算術演算子と比較演算子は、次の点を除いて、共通言語ランタイム (CLR) では期待どおりに動作します。</span><span class="sxs-lookup"><span data-stu-id="f8be8-103">Arithmetic and comparison operators work as expected in the common language runtime (CLR) except as follows:</span></span>  
  
-   <span data-ttu-id="f8be8-104">SQL では、浮動小数点数に対して剰余演算子がサポートされません。</span><span class="sxs-lookup"><span data-stu-id="f8be8-104">SQL does not support the modulus operator on floating-point numbers.</span></span>  
  
-   <span data-ttu-id="f8be8-105">SQL ではチェックされない算術はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="f8be8-105">SQL does not support unchecked arithmetic.</span></span>  
  
-   <span data-ttu-id="f8be8-106">インクリメント演算子とデクリメント演算子は、SQL に複製できない式で使用すると副作用があるため、SQL ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="f8be8-106">Increment and decrement operators cause side-effects when you use them in expressions that cannot be replicated in SQL and are, therefore, not supported.</span></span>  
  
## <a name="supported-operators"></a><span data-ttu-id="f8be8-107">サポートされる演算子</span><span class="sxs-lookup"><span data-stu-id="f8be8-107">Supported Operators</span></span>  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="f8be8-108">は、次の演算子をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f8be8-108">supports the following operators.</span></span>  
  
-   <span data-ttu-id="f8be8-109">基本算術演算子</span><span class="sxs-lookup"><span data-stu-id="f8be8-109">Basic arithmetic operators:</span></span>  
  
    -   `+`  
  
    -   <span data-ttu-id="f8be8-110">`-` (減算)</span><span class="sxs-lookup"><span data-stu-id="f8be8-110">`-` (subtraction)</span></span>  
  
    -   `*`  
  
    -   `/`  
  
    -   <span data-ttu-id="f8be8-111">Visual Basic 整数除算 (`\`)</span><span class="sxs-lookup"><span data-stu-id="f8be8-111">Visual Basic integer division (`\`)</span></span>  
  
    -   <span data-ttu-id="f8be8-112">`%` (Visual Basic `Mod`)</span><span class="sxs-lookup"><span data-stu-id="f8be8-112">`%` (Visual Basic `Mod`)</span></span>  
  
    -   `<<`  
  
    -   `>>`  
  
    -   <span data-ttu-id="f8be8-113">`-` (単項マイナス符号)</span><span class="sxs-lookup"><span data-stu-id="f8be8-113">`-` (unary negation)</span></span>  
  
-   <span data-ttu-id="f8be8-114">基本比較演算子</span><span class="sxs-lookup"><span data-stu-id="f8be8-114">Basic comparison operators:</span></span>  
  
    -   <span data-ttu-id="f8be8-115">Visual Basic `=` および C# `==`</span><span class="sxs-lookup"><span data-stu-id="f8be8-115">Visual Basic `=` and C# `==`</span></span>  
  
    -   <span data-ttu-id="f8be8-116">Visual Basic `<>` および C# `!=`</span><span class="sxs-lookup"><span data-stu-id="f8be8-116">Visual Basic `<>` and C# `!=`</span></span>  
  
    -   <span data-ttu-id="f8be8-117">Visual Basic `Is/IsNot`</span><span class="sxs-lookup"><span data-stu-id="f8be8-117">Visual Basic `Is/IsNot`</span></span>  
  
    -   `<`  
  
    -   `<=`  
  
    -   `>`  
  
    -   `>=`  
  
## <a name="see-also"></a><span data-ttu-id="f8be8-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8be8-118">See also</span></span>
- [<span data-ttu-id="f8be8-119">データ型と関数</span><span class="sxs-lookup"><span data-stu-id="f8be8-119">Data Types and Functions</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
- [<span data-ttu-id="f8be8-120">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="f8be8-120">C# Operators</span></span>](../../../../../../docs/csharp/language-reference/operators/index.md)
- [<span data-ttu-id="f8be8-121">演算子</span><span class="sxs-lookup"><span data-stu-id="f8be8-121">Operators</span></span>](../../../../../visual-basic/language-reference/operators/index.md)
