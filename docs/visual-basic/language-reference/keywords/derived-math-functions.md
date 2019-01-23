---
title: 数値演算関数の導出 (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- arithmetic operations, derived math functions
- cosecant function
- arcsecant function
- arccotangent function
- functions [Visual Basic], derived math functions
- inverse functions
- math functions, derived
- derived math functions
- cotangent function
- angles
- secant function
- trigonometric functions
- logarithms
- arccosecant function
- hyperbolic functions
- arcsine function
- degrees
- arccosine function
ms.assetid: 63e449d8-9444-44fb-8db1-6d9cf346e2aa
ms.openlocfilehash: 1273871faf65afdd1a894c03f13a2c93507c1b13
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505862"
---
# <a name="derived-math-functions-visual-basic"></a><span data-ttu-id="eef02-102">数値演算関数の導出 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="eef02-102">Derived Math Functions (Visual Basic)</span></span>
<span data-ttu-id="eef02-103">次の表はの組み込みの数学関数から派生可能な非組み込みの数学関数、<xref:System.Math?displayProperty=nameWithType>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="eef02-103">The following table shows non-intrinsic math functions that can be derived from the intrinsic math functions of the <xref:System.Math?displayProperty=nameWithType> object.</span></span> <span data-ttu-id="eef02-104">組み込みの数学関数を追加することでアクセスできる`Imports System.Math`ファイルまたはプロジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="eef02-104">You can access the intrinsic math functions by adding `Imports System.Math` to your file or project.</span></span>  
  
|<span data-ttu-id="eef02-105">関数</span><span class="sxs-lookup"><span data-stu-id="eef02-105">Function</span></span>|<span data-ttu-id="eef02-106">対応する派生</span><span class="sxs-lookup"><span data-stu-id="eef02-106">Derived equivalents</span></span>|  
|--------------|-------------------------|  
|<span data-ttu-id="eef02-107">Secant (Sec(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-107">Secant (Sec(x))</span></span>|<span data-ttu-id="eef02-108">1 / Cos(x)</span><span class="sxs-lookup"><span data-stu-id="eef02-108">1 / Cos(x)</span></span>|  
|<span data-ttu-id="eef02-109">余割 (Csc(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-109">Cosecant (Csc(x))</span></span>|<span data-ttu-id="eef02-110">1 / Sin(x)</span><span class="sxs-lookup"><span data-stu-id="eef02-110">1 / Sin(x)</span></span>|  
|<span data-ttu-id="eef02-111">コタンジェント (Ctan(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-111">Cotangent (Ctan(x))</span></span>|<span data-ttu-id="eef02-112">1 / Tan(x)</span><span class="sxs-lookup"><span data-stu-id="eef02-112">1 / Tan(x)</span></span>|  
|<span data-ttu-id="eef02-113">逆正弦 (Asin(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-113">Inverse sine (Asin(x))</span></span>|<span data-ttu-id="eef02-114">Atan(x / Sqrt(-x \* x + 1))</span><span class="sxs-lookup"><span data-stu-id="eef02-114">Atan(x / Sqrt(-x \* x + 1))</span></span>|  
|<span data-ttu-id="eef02-115">逆コサイン (Acos(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-115">Inverse cosine (Acos(x))</span></span>|<span data-ttu-id="eef02-116">Atan (-x/Sqrt (-x \* x + 1)) + 2 \* Atan(1)</span><span class="sxs-lookup"><span data-stu-id="eef02-116">Atan(-x / Sqrt(-x \* x + 1)) + 2 \* Atan(1)</span></span>|  
|<span data-ttu-id="eef02-117">逆正割 (Asec(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-117">Inverse secant (Asec(x))</span></span>|<span data-ttu-id="eef02-118">2 \* Atan(1) – Atan(Sign(x)/Sqrt (x \* x 1))</span><span class="sxs-lookup"><span data-stu-id="eef02-118">2 \* Atan(1) – Atan(Sign(x) / Sqrt(x \* x – 1))</span></span>|  
|<span data-ttu-id="eef02-119">逆の余割 (Acsc(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-119">Inverse cosecant (Acsc(x))</span></span>|<span data-ttu-id="eef02-120">Atan(Sign(x) / Sqrt(x \* x – 1))</span><span class="sxs-lookup"><span data-stu-id="eef02-120">Atan(Sign(x) / Sqrt(x \* x – 1))</span></span>|  
|<span data-ttu-id="eef02-121">逆余接 (Acot(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-121">Inverse cotangent (Acot(x))</span></span>|<span data-ttu-id="eef02-122">2 \* Atan(1) - Atan(x)</span><span class="sxs-lookup"><span data-stu-id="eef02-122">2 \* Atan(1) - Atan(x)</span></span>|  
|<span data-ttu-id="eef02-123">双曲線正弦 (Sinh(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-123">Hyperbolic sine (Sinh(x))</span></span>|<span data-ttu-id="eef02-124">(Exp(x) – Exp(-x)) / 2</span><span class="sxs-lookup"><span data-stu-id="eef02-124">(Exp(x) – Exp(-x)) / 2</span></span>|  
|<span data-ttu-id="eef02-125">双曲線余弦 (Cosh(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-125">Hyperbolic cosine (Cosh(x))</span></span>|<span data-ttu-id="eef02-126">(Exp(x) + Exp(-x)) / 2</span><span class="sxs-lookup"><span data-stu-id="eef02-126">(Exp(x) + Exp(-x)) / 2</span></span>|  
|<span data-ttu-id="eef02-127">ハイパーボリック タンジェント (Tanh(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-127">Hyperbolic tangent (Tanh(x))</span></span>|<span data-ttu-id="eef02-128">(Exp(x) – Exp(-x)) / (Exp(x) + Exp(-x))</span><span class="sxs-lookup"><span data-stu-id="eef02-128">(Exp(x) – Exp(-x)) / (Exp(x) + Exp(-x))</span></span>|  
|<span data-ttu-id="eef02-129">双曲線正割 (Sech(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-129">Hyperbolic secant (Sech(x))</span></span>|<span data-ttu-id="eef02-130">2 / (Exp(x) + Exp(-x))</span><span class="sxs-lookup"><span data-stu-id="eef02-130">2 / (Exp(x) + Exp(-x))</span></span>|  
|<span data-ttu-id="eef02-131">Hyperbolic cosecant (Csch(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-131">Hyperbolic cosecant (Csch(x))</span></span>|<span data-ttu-id="eef02-132">2 / (Exp(x) – Exp(-x))</span><span class="sxs-lookup"><span data-stu-id="eef02-132">2 / (Exp(x) – Exp(-x))</span></span>|  
|<span data-ttu-id="eef02-133">双曲線余接 (Coth(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-133">Hyperbolic cotangent (Coth(x))</span></span>|<span data-ttu-id="eef02-134">(Exp(x) + Exp(-x)) / (Exp(x) – Exp(-x))</span><span class="sxs-lookup"><span data-stu-id="eef02-134">(Exp(x) + Exp(-x)) / (Exp(x) – Exp(-x))</span></span>|  
|<span data-ttu-id="eef02-135">逆双曲線正弦 (Asinh(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-135">Inverse hyperbolic sine (Asinh(x))</span></span>|<span data-ttu-id="eef02-136">ログ (x + Sqrt (x \* x + 1))</span><span class="sxs-lookup"><span data-stu-id="eef02-136">Log(x + Sqrt(x \* x + 1))</span></span>|  
|<span data-ttu-id="eef02-137">逆双曲線余弦 (Acosh(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-137">Inverse hyperbolic cosine (Acosh(x))</span></span>|<span data-ttu-id="eef02-138">ログ (x + Sqrt (x \* x 1))</span><span class="sxs-lookup"><span data-stu-id="eef02-138">Log(x + Sqrt(x \* x – 1))</span></span>|  
|<span data-ttu-id="eef02-139">逆ハイパーボリック タンジェント (Atanh(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-139">Inverse hyperbolic tangent (Atanh(x))</span></span>|<span data-ttu-id="eef02-140">Log((1 + x) / (1 – x)) / 2</span><span class="sxs-lookup"><span data-stu-id="eef02-140">Log((1 + x) / (1 – x)) / 2</span></span>|  
|<span data-ttu-id="eef02-141">逆双曲線正割 (AsecH(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-141">Inverse hyperbolic secant (AsecH(x))</span></span>|<span data-ttu-id="eef02-142">Log ((Sqrt (-x \* x + 1) + 1)/x)</span><span class="sxs-lookup"><span data-stu-id="eef02-142">Log((Sqrt(-x \* x + 1) + 1) / x)</span></span>|  
|<span data-ttu-id="eef02-143">逆双曲線余割 (Acsch(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-143">Inverse hyperbolic cosecant (Acsch(x))</span></span>|<span data-ttu-id="eef02-144">Log((Sign(x) \* Sqrt (x \* x + 1) + 1)/x)</span><span class="sxs-lookup"><span data-stu-id="eef02-144">Log((Sign(x) \* Sqrt(x \* x + 1) + 1) / x)</span></span>|  
|<span data-ttu-id="eef02-145">逆双曲線余接 (Acoth(x))</span><span class="sxs-lookup"><span data-stu-id="eef02-145">Inverse hyperbolic cotangent (Acoth(x))</span></span>|<span data-ttu-id="eef02-146">Log((x + 1) / (x – 1)) / 2</span><span class="sxs-lookup"><span data-stu-id="eef02-146">Log((x + 1) / (x – 1)) / 2</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="eef02-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="eef02-147">See also</span></span>
- [<span data-ttu-id="eef02-148">数値演算関数</span><span class="sxs-lookup"><span data-stu-id="eef02-148">Math Functions</span></span>](../../../visual-basic/language-reference/functions/math-functions.md)
