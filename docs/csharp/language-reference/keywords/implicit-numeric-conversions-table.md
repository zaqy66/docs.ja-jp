---
title: 暗黙的な数値変換の一覧表 (C# リファレンス)
ms.date: 09/05/2018
helpviewer_keywords:
- conversions [C#], implicit numeric
- implicit numeric conversions [C#]
- numeric conversions [C#], implicit
- types [C#], implicit numeric conversions
ms.assetid: 72eb5a94-0491-48bf-8032-d7ebfdfeb8d8
ms.openlocfilehash: c3c0153a0ae3e07839822c8bb978b1a09277bd53
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188704"
---
# <a name="implicit-numeric-conversions-table-c-reference"></a><span data-ttu-id="4786a-102">暗黙的な数値変換の一覧表 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="4786a-102">Implicit numeric conversions table (C# Reference)</span></span>

<span data-ttu-id="4786a-103">.NET 数値型間の定義済みの暗黙的な変換を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="4786a-103">The following table shows the predefined implicit conversions between .NET numeric types.</span></span>
  
|<span data-ttu-id="4786a-104">From</span><span class="sxs-lookup"><span data-stu-id="4786a-104">From</span></span>|<span data-ttu-id="4786a-105">終了</span><span class="sxs-lookup"><span data-stu-id="4786a-105">To</span></span>|  
|----------|--------|  
|[<span data-ttu-id="4786a-106">sbyte</span><span class="sxs-lookup"><span data-stu-id="4786a-106">sbyte</span></span>](sbyte.md)|<span data-ttu-id="4786a-107">`short`、`int`、`long`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="4786a-107">`short`, `int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="4786a-108">byte</span><span class="sxs-lookup"><span data-stu-id="4786a-108">byte</span></span>](byte.md)|<span data-ttu-id="4786a-109">`short`、`ushort`、`int`、`uint`、`long`、`ulong`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="4786a-109">`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="4786a-110">short</span><span class="sxs-lookup"><span data-stu-id="4786a-110">short</span></span>](short.md)|<span data-ttu-id="4786a-111">`int`、`long`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="4786a-111">`int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="4786a-112">ushort</span><span class="sxs-lookup"><span data-stu-id="4786a-112">ushort</span></span>](ushort.md)|<span data-ttu-id="4786a-113">`int`、`uint`、`long`、`ulong`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="4786a-113">`int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="4786a-114">int</span><span class="sxs-lookup"><span data-stu-id="4786a-114">int</span></span>](int.md)|<span data-ttu-id="4786a-115">`long`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="4786a-115">`long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="4786a-116">uint</span><span class="sxs-lookup"><span data-stu-id="4786a-116">uint</span></span>](uint.md)|<span data-ttu-id="4786a-117">`long`、`ulong`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="4786a-117">`long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="4786a-118">long</span><span class="sxs-lookup"><span data-stu-id="4786a-118">long</span></span>](long.md)|<span data-ttu-id="4786a-119">`float`、 `double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="4786a-119">`float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="4786a-120">char</span><span class="sxs-lookup"><span data-stu-id="4786a-120">char</span></span>](char.md)|<span data-ttu-id="4786a-121">`ushort`、`int`、`uint`、`long`、`ulong`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="4786a-121">`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="4786a-122">float</span><span class="sxs-lookup"><span data-stu-id="4786a-122">float</span></span>](float.md)|`double`|  
|[<span data-ttu-id="4786a-123">ulong</span><span class="sxs-lookup"><span data-stu-id="4786a-123">ulong</span></span>](ulong.md)|<span data-ttu-id="4786a-124">`float`、 `double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="4786a-124">`float`, `double`, or `decimal`</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4786a-125">コメント</span><span class="sxs-lookup"><span data-stu-id="4786a-125">Remarks</span></span>  

- <span data-ttu-id="4786a-126">[整数型](integral-types-table.md)はすべて、あらゆる[浮動小数点型](floating-point-types-table.md)に暗黙的に変換できます。</span><span class="sxs-lookup"><span data-stu-id="4786a-126">Any [integral type](integral-types-table.md) is implicitly convertible to any [floating-point type](floating-point-types-table.md).</span></span>

- <span data-ttu-id="4786a-127">`int`、`uint`、`long`、または `ulong` から `float` への変換と `long` から `ulong` または `double` への変換では、有効桁数が失われる場合があります (絶対値ではありません)。</span><span class="sxs-lookup"><span data-stu-id="4786a-127">Precision but not magnitude might be lost in the conversions from `int`, `uint`, `long`, or `ulong` to `float` and from `long` or `ulong` to `double`.</span></span>  
  
- <span data-ttu-id="4786a-128">`char` 型への暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="4786a-128">There are no implicit conversions to the `char` type.</span></span>  
  
- <span data-ttu-id="4786a-129">`float` 型、`double` 型、`decimal` 型の間に暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="4786a-129">There are no implicit conversions between the `float` and `double` types and the `decimal` type.</span></span>  
  
- <span data-ttu-id="4786a-130">型 `int` の定数式の値 (整数リテラルで表される値など) は、それが変換先の型の範囲内にある場合、`sbyte`、`byte`、`short`、`ushort`、`uint`、`ulong` に変換できます。</span><span class="sxs-lookup"><span data-stu-id="4786a-130">A value of a constant expression of type `int` (for example, a value represented by an integral literal) can be converted to `sbyte`, `byte`, `short`, `ushort`, `uint`, or `ulong`, provided it's within the range of the destination type:</span></span>

  ```csharp
  byte a = 13;    // Compiles
  byte b = 300;   // CS0031: Constant value '300' cannot be converted to a 'byte'
  ```

<span data-ttu-id="4786a-131">明示的な変換に関する詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[Implicit conversions](~/_csharplang/spec/conversions.md#implicit-conversions)」 (明示的な変換) セクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4786a-131">For more information about implicit conversions, see the [Implicit conversions](~/_csharplang/spec/conversions.md#implicit-conversions) section of the [C# language specification](../language-specification/index.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4786a-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="4786a-132">See also</span></span>

- [<span data-ttu-id="4786a-133">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="4786a-133">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="4786a-134">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="4786a-134">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="4786a-135">整数型の一覧表</span><span class="sxs-lookup"><span data-stu-id="4786a-135">Integral types table</span></span>](integral-types-table.md)
- [<span data-ttu-id="4786a-136">浮動小数点型の一覧表</span><span class="sxs-lookup"><span data-stu-id="4786a-136">Floating-point types table</span></span>](floating-point-types-table.md)
- [<span data-ttu-id="4786a-137">組み込み型の一覧表</span><span class="sxs-lookup"><span data-stu-id="4786a-137">Built-in types table</span></span>](built-in-types-table.md)
- [<span data-ttu-id="4786a-138">明示的な数値変換の一覧表</span><span class="sxs-lookup"><span data-stu-id="4786a-138">Explicit numeric conversions table</span></span>](explicit-numeric-conversions-table.md)
- [<span data-ttu-id="4786a-139">キャストと型変換</span><span class="sxs-lookup"><span data-stu-id="4786a-139">Casting and type conversions</span></span>](../../programming-guide/types/casting-and-type-conversions.md)
