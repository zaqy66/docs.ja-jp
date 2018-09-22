---
title: 基本的な型 (f#)
description: F# 言語で使用される基本的な基本的な型を検出します。
ms.date: 07/09/2018
ms.openlocfilehash: 8f948d066323527b09b1d3f9f4167b95b1c875cf
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2018
ms.locfileid: "46584647"
---
# <a name="basic-types"></a><span data-ttu-id="3cb9d-103">基本的な型</span><span class="sxs-lookup"><span data-stu-id="3cb9d-103">Basic types</span></span>

<span data-ttu-id="3cb9d-104">このトピックでは、f# 言語で定義されている基本的な型を使用します。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-104">This topic lists the basic types that are defined in the F# language.</span></span> <span data-ttu-id="3cb9d-105">これらの型は、最も基本的な f# でほぼすべての f# プログラムの基礎を形成します。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-105">These types are the most fundamental in F#, forming the basis of nearly every F# program.</span></span> <span data-ttu-id="3cb9d-106">.NET プリミティブ型のスーパー セットです。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-106">They are a superset of .NET primitive types.</span></span>

|<span data-ttu-id="3cb9d-107">型</span><span class="sxs-lookup"><span data-stu-id="3cb9d-107">Type</span></span>|<span data-ttu-id="3cb9d-108">.NET 型</span><span class="sxs-lookup"><span data-stu-id="3cb9d-108">.NET type</span></span>|<span data-ttu-id="3cb9d-109">説明</span><span class="sxs-lookup"><span data-stu-id="3cb9d-109">Description</span></span>|
|----|---------|-----------|
|`bool`|<xref:System.Boolean>|<span data-ttu-id="3cb9d-110">有効な値は、`true` と `false` です。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-110">Possible values are `true` and `false`.</span></span>|
|`byte`|<xref:System.Byte>|<span data-ttu-id="3cb9d-111">0 から 255 の値です。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-111">Values from 0 to 255.</span></span>|
|`sbyte`|<xref:System.SByte>|<span data-ttu-id="3cb9d-112">-128 から 127 の値です。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-112">Values from -128 to 127.</span></span>|
|`int16`|<xref:System.Int16>|<span data-ttu-id="3cb9d-113">-32768 から 32767 の値です。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-113">Values from -32768 to 32767.</span></span>|
|`uint16`|<xref:System.UInt16>|<span data-ttu-id="3cb9d-114">0 から 65535 の値です。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-114">Values from 0 to 65535.</span></span>|
|`int`|<xref:System.Int32>|<span data-ttu-id="3cb9d-115">-2,147, 483,648 から 2,147, 483,647 の値です。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-115">Values from -2,147,483,648 to 2,147,483,647.</span></span>|
|`uint32`|<xref:System.UInt32>|<span data-ttu-id="3cb9d-116">0 から 4,294,967,295 の値です。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-116">Values from 0 to 4,294,967,295.</span></span>|
|`int64`|<xref:System.Int64>|<span data-ttu-id="3cb9d-117">9,223,372,036,854,775,807-9,223,372,036,854,775,808 から値です。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-117">Values from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.</span></span>|
|`uint64`|<xref:System.UInt64>|<span data-ttu-id="3cb9d-118">0 から 18,446,744,073,709,551,615 の値です。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-118">Values from 0 to 18,446,744,073,709,551,615.</span></span>|
|`nativeint`|<xref:System.IntPtr>|<span data-ttu-id="3cb9d-119">符号付き整数としてのネイティブ ポインターです。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-119">A native pointer as a signed integer.</span></span>|
|`unativeint`|<xref:System.UIntPtr>|<span data-ttu-id="3cb9d-120">符号なし整数としてのネイティブ ポインターです。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-120">A native pointer as an unsigned integer.</span></span>|
|`char`|<xref:System.Char>|<span data-ttu-id="3cb9d-121">Unicode 文字の値。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-121">Unicode character values.</span></span>|
|`string`|<xref:System.String>|<span data-ttu-id="3cb9d-122">Unicode テキスト。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-122">Unicode text.</span></span>|
|`decimal`|<xref:System.Decimal>|<span data-ttu-id="3cb9d-123">浮動小数点、少なくとも 28 の有効桁数を持つデータ型です。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-123">A floating point data type that has at least 28 significant digits.</span></span>|
|`unit`|<span data-ttu-id="3cb9d-124">該当なし</span><span class="sxs-lookup"><span data-stu-id="3cb9d-124">not applicable</span></span>|<span data-ttu-id="3cb9d-125">実際の値がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-125">Indicates the absence of an actual value.</span></span> <span data-ttu-id="3cb9d-126">型が示される 1 つだけの仮引数の値を持つ`()`します。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-126">The type has only one formal value, which is denoted `()`.</span></span> <span data-ttu-id="3cb9d-127">単位の値、`()`値が必要なが実際の値が使用可能なまたは意味のプレース ホルダーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-127">The unit value, `()`, is often used as a placeholder where a value is needed but no real value is available or makes sense.</span></span>|
|`void`|<xref:System.Void>|<span data-ttu-id="3cb9d-128">ないことを示します型または値。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-128">Indicates no type or value.</span></span>|
|<span data-ttu-id="3cb9d-129">`float32`, `single`</span><span class="sxs-lookup"><span data-stu-id="3cb9d-129">`float32`, `single`</span></span>|<xref:System.Single>|<span data-ttu-id="3cb9d-130">32 ビット浮動小数点型。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-130">A 32-bit floating point type.</span></span>|
|<span data-ttu-id="3cb9d-131">`float`, `double`</span><span class="sxs-lookup"><span data-stu-id="3cb9d-131">`float`, `double`</span></span>|<xref:System.Double>|<span data-ttu-id="3cb9d-132">64 ビット浮動小数点型。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-132">A 64-bit floating point type.</span></span>|

>[!NOTE]
<span data-ttu-id="3cb9d-133">使用して、64 ビット整数型の整数が大きすぎると計算を行うことができます、 [bigint](https://msdn.microsoft.com/library/dc8be18d-4042-46c4-b136-2f21a84f6efa)型。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-133">You can perform computations with integers too big for the 64-bit integer type by using the [bigint](https://msdn.microsoft.com/library/dc8be18d-4042-46c4-b136-2f21a84f6efa) type.</span></span> <span data-ttu-id="3cb9d-134">`bigint` 基本的な型であるとは見なされません省略形は`System.Numerics.BigInteger`します。</span><span class="sxs-lookup"><span data-stu-id="3cb9d-134">`bigint` is not considered a basic type; it is an abbreviation for `System.Numerics.BigInteger`.</span></span>

## <a name="see-also"></a><span data-ttu-id="3cb9d-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="3cb9d-135">See also</span></span>

- [<span data-ttu-id="3cb9d-136">F# 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="3cb9d-136">F# Language Reference</span></span>](index.md)
