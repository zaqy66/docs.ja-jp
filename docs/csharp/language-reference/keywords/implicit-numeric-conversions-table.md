---
title: 暗黙的な数値変換の一覧表 - C# リファレンス
ms.custom: seodec18
ms.date: 09/05/2018
helpviewer_keywords:
- conversions [C#], implicit numeric
- implicit numeric conversions [C#]
- numeric conversions [C#], implicit
- types [C#], implicit numeric conversions
ms.assetid: 72eb5a94-0491-48bf-8032-d7ebfdfeb8d8
ms.openlocfilehash: 703f60f48e1e569e0ffcab66ff7ccc91d4a49514
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2019
ms.locfileid: "56093555"
---
# <a name="implicit-numeric-conversions-table-c-reference"></a><span data-ttu-id="a766c-102">暗黙的な数値変換の一覧表 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="a766c-102">Implicit numeric conversions table (C# Reference)</span></span>

<span data-ttu-id="a766c-103">.NET 数値型間の定義済みの暗黙的な変換を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="a766c-103">The following table shows the predefined implicit conversions between .NET numeric types.</span></span>
  
|<span data-ttu-id="a766c-104">変換元</span><span class="sxs-lookup"><span data-stu-id="a766c-104">From</span></span>|<span data-ttu-id="a766c-105">終了</span><span class="sxs-lookup"><span data-stu-id="a766c-105">To</span></span>|  
|----------|--------|  
|[<span data-ttu-id="a766c-106">sbyte</span><span class="sxs-lookup"><span data-stu-id="a766c-106">sbyte</span></span>](sbyte.md)|<span data-ttu-id="a766c-107">`short`、`int`、`long`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="a766c-107">`short`, `int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a766c-108">byte</span><span class="sxs-lookup"><span data-stu-id="a766c-108">byte</span></span>](byte.md)|<span data-ttu-id="a766c-109">`short`、`ushort`、`int`、`uint`、`long`、`ulong`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="a766c-109">`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a766c-110">char</span><span class="sxs-lookup"><span data-stu-id="a766c-110">char</span></span>](char.md)|<span data-ttu-id="a766c-111">`ushort`、`int`、`uint`、`long`、`ulong`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="a766c-111">`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a766c-112">short</span><span class="sxs-lookup"><span data-stu-id="a766c-112">short</span></span>](short.md)|<span data-ttu-id="a766c-113">`int`、`long`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="a766c-113">`int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a766c-114">ushort</span><span class="sxs-lookup"><span data-stu-id="a766c-114">ushort</span></span>](ushort.md)|<span data-ttu-id="a766c-115">`int`、`uint`、`long`、`ulong`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="a766c-115">`int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a766c-116">int</span><span class="sxs-lookup"><span data-stu-id="a766c-116">int</span></span>](int.md)|<span data-ttu-id="a766c-117">`long`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="a766c-117">`long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a766c-118">uint</span><span class="sxs-lookup"><span data-stu-id="a766c-118">uint</span></span>](uint.md)|<span data-ttu-id="a766c-119">`long`、`ulong`、`float`、`double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="a766c-119">`long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a766c-120">long</span><span class="sxs-lookup"><span data-stu-id="a766c-120">long</span></span>](long.md)|<span data-ttu-id="a766c-121">`float`、 `double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="a766c-121">`float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a766c-122">ulong</span><span class="sxs-lookup"><span data-stu-id="a766c-122">ulong</span></span>](ulong.md)|<span data-ttu-id="a766c-123">`float`、 `double`、または `decimal`</span><span class="sxs-lookup"><span data-stu-id="a766c-123">`float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a766c-124">float</span><span class="sxs-lookup"><span data-stu-id="a766c-124">float</span></span>](float.md)|`double`|  
  
## <a name="remarks"></a><span data-ttu-id="a766c-125">解説</span><span class="sxs-lookup"><span data-stu-id="a766c-125">Remarks</span></span>  

- <span data-ttu-id="a766c-126">[整数型](integral-types-table.md)はすべて、あらゆる[浮動小数点型](floating-point-types-table.md)に暗黙的に変換できます。</span><span class="sxs-lookup"><span data-stu-id="a766c-126">Any [integral type](integral-types-table.md) is implicitly convertible to any [floating-point type](floating-point-types-table.md).</span></span>

- <span data-ttu-id="a766c-127">`int`、`uint`、`long`、または `ulong` から `float` への変換と `long` から `ulong` または `double` への変換では、有効桁数が失われる場合があります (絶対値ではありません)。</span><span class="sxs-lookup"><span data-stu-id="a766c-127">Precision but not magnitude might be lost in the conversions from `int`, `uint`, `long`, or `ulong` to `float` and from `long` or `ulong` to `double`.</span></span>  
  
- <span data-ttu-id="a766c-128">`char`、`byte`、`sbyte` 型への暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="a766c-128">There are no implicit conversions to the `char`, `byte`, and `sbyte` types.</span></span>  

- <span data-ttu-id="a766c-129">`double` および `decimal` 型からの暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="a766c-129">There are no implicit conversions from the `double` and `decimal` types.</span></span>
  
- <span data-ttu-id="a766c-130">`decimal` 型と `float` 型または `double` 型の間に暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="a766c-130">There are no implicit conversions between the `decimal` type and the `float` or `double` types.</span></span>  
  
- <span data-ttu-id="a766c-131">型 `int` の定数式の値 (整数リテラルで表される値など) は、それが変換先の型の範囲内にある場合、`sbyte`、`byte`、`short`、`ushort`、`uint`、`ulong` に変換できます。</span><span class="sxs-lookup"><span data-stu-id="a766c-131">A value of a constant expression of type `int` (for example, a value represented by an integral literal) can be converted to `sbyte`, `byte`, `short`, `ushort`, `uint`, or `ulong`, provided it's within the range of the destination type:</span></span>

  ```csharp
  byte a = 13;    // Compiles
  byte b = 300;   // CS0031: Constant value '300' cannot be converted to a 'byte'
  ```

<span data-ttu-id="a766c-132">明示的な変換に関する詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[Implicit conversions](~/_csharplang/spec/conversions.md#implicit-conversions)」 (明示的な変換) セクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a766c-132">For more information about implicit conversions, see the [Implicit conversions](~/_csharplang/spec/conversions.md#implicit-conversions) section of the [C# language specification](../language-specification/index.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a766c-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="a766c-133">See also</span></span>

- [<span data-ttu-id="a766c-134">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="a766c-134">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="a766c-135">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="a766c-135">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="a766c-136">整数型の一覧表</span><span class="sxs-lookup"><span data-stu-id="a766c-136">Integral types table</span></span>](integral-types-table.md)
- [<span data-ttu-id="a766c-137">浮動小数点型の一覧表</span><span class="sxs-lookup"><span data-stu-id="a766c-137">Floating-point types table</span></span>](floating-point-types-table.md)
- [<span data-ttu-id="a766c-138">組み込み型の一覧表</span><span class="sxs-lookup"><span data-stu-id="a766c-138">Built-in types table</span></span>](built-in-types-table.md)
- [<span data-ttu-id="a766c-139">明示的な数値変換の一覧表</span><span class="sxs-lookup"><span data-stu-id="a766c-139">Explicit numeric conversions table</span></span>](explicit-numeric-conversions-table.md)
- [<span data-ttu-id="a766c-140">キャストと型変換</span><span class="sxs-lookup"><span data-stu-id="a766c-140">Casting and type conversions</span></span>](../../programming-guide/types/casting-and-type-conversions.md)
