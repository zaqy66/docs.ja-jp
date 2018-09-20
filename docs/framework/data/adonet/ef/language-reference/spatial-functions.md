---
title: 空間関数
ms.date: 03/30/2017
ms.assetid: 90cb177d-88a0-45be-97e8-3b306283c6e0
ms.openlocfilehash: ad6b722e84aae40354e30434b107752d02352645
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2018
ms.locfileid: "45676150"
---
# <a name="spatial-functions"></a><span data-ttu-id="a7df4-102">空間関数</span><span class="sxs-lookup"><span data-stu-id="a7df4-102">Spatial Functions</span></span>
<span data-ttu-id="a7df4-103">空間型のリテラル形式はありません。</span><span class="sxs-lookup"><span data-stu-id="a7df4-103">There is no literal format for spatial types.</span></span> <span data-ttu-id="a7df4-104">ただし、Well-Known Text 形式の文字列を使用して呼び出す正規の Entity Framework 関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a7df4-104">However, you can use canonical Entity Framework functions that you call using strings in Well-Known Text format.</span></span> <span data-ttu-id="a7df4-105">たとえば、次の関数呼び出しでは、ジオメトリ ポイントが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a7df4-105">For example, the following function call creates a geometry point:</span></span>  
  
```  
GeometryFromText('POINT (43 -73)')  
```  
  
 <span data-ttu-id="a7df4-106">[SpatialEdmFunctions メソッド](https://msdn.microsoft.com/library/hh749531.aspx)ページは、空間に関する正規 Entity Framework メソッドすべてを一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7df4-106">The [SpatialEdmFunctions Methods](https://msdn.microsoft.com/library/hh749531.aspx) page lists all spatial canonical Entity Framework methods.</span></span> <span data-ttu-id="a7df4-107">目的のメソッドをクリックすると、関数に渡す必要のあるパラメーターを確認できます。</span><span class="sxs-lookup"><span data-stu-id="a7df4-107">Click on a method of interest to see what parameters should be passed to a function.</span></span>
