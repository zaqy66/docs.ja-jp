---
title: 空間関数
ms.date: 03/30/2017
ms.assetid: 90cb177d-88a0-45be-97e8-3b306283c6e0
ms.openlocfilehash: 09402633c5e7f591a534992fc92655e6a2d1d88d
ms.sourcegitcommit: c6f69b0cf149f6b54483a6d5c2ece222913f43ce
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2019
ms.locfileid: "55904474"
---
# <a name="spatial-functions"></a><span data-ttu-id="f1ada-102">空間関数</span><span class="sxs-lookup"><span data-stu-id="f1ada-102">Spatial Functions</span></span>
<span data-ttu-id="f1ada-103">空間型のリテラル形式はありません。</span><span class="sxs-lookup"><span data-stu-id="f1ada-103">There is no literal format for spatial types.</span></span> <span data-ttu-id="f1ada-104">ただし、Well-Known Text 形式の文字列を使用して呼び出す正規の Entity Framework 関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="f1ada-104">However, you can use canonical Entity Framework functions that you call using strings in Well-Known Text format.</span></span> <span data-ttu-id="f1ada-105">たとえば、次の関数呼び出しでは、ジオメトリ ポイントが作成されます。</span><span class="sxs-lookup"><span data-stu-id="f1ada-105">For example, the following function call creates a geometry point:</span></span>  
  
```  
GeometryFromText('POINT (43 -73)')  
```  
  
 <span data-ttu-id="f1ada-106"><xref:System.Data.Common.CommandTrees.ExpressionBuilder.Spatial.SpatialEdmFunctions>メソッドがある空間に関する正規 Entity Framework メソッドすべて。</span><span class="sxs-lookup"><span data-stu-id="f1ada-106">The <xref:System.Data.Common.CommandTrees.ExpressionBuilder.Spatial.SpatialEdmFunctions> methods have all spatial canonical Entity Framework methods.</span></span> <span data-ttu-id="f1ada-107">目的のメソッドをクリックすると、関数に渡す必要のあるパラメーターを確認できます。</span><span class="sxs-lookup"><span data-stu-id="f1ada-107">Click on a method of interest to see what parameters should be passed to a function.</span></span>
