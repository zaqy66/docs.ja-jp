---
title: 組み込み型の一覧表 - C# リファレンス
ms.custom: seodec18
description: C# の組み込み型のキーワード
ms.date: 08/17/2018
helpviewer_keywords:
- types [C#], built-in
- built-in C# types
ms.assetid: 54f901f2-bf2f-472c-ae8d-73e8ecfc57fe
ms.openlocfilehash: fae0cedfe8bf675dceb9cb9d5835d923cae8b4ab
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235629"
---
# <a name="built-in-types-table-c-reference"></a><span data-ttu-id="18ddd-103">組み込み型の一覧表 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="18ddd-103">Built-in types table (C# Reference)</span></span>

<span data-ttu-id="18ddd-104">次の表は、C# の組み込み型のキーワードを示しています。これは、<xref:System> 名前空間の定義済み型の別名です。</span><span class="sxs-lookup"><span data-stu-id="18ddd-104">The following table shows the keywords for built-in C# types, which are aliases of predefined types in the <xref:System> namespace.</span></span>  
  
|<span data-ttu-id="18ddd-105">C# 型</span><span class="sxs-lookup"><span data-stu-id="18ddd-105">C# type</span></span>|<span data-ttu-id="18ddd-106">.NET 型</span><span class="sxs-lookup"><span data-stu-id="18ddd-106">.NET type</span></span>|  
|--------------|-------------------------|  
|[<span data-ttu-id="18ddd-107">bool</span><span class="sxs-lookup"><span data-stu-id="18ddd-107">bool</span></span>](bool.md)|<xref:System.Boolean?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-108">byte</span><span class="sxs-lookup"><span data-stu-id="18ddd-108">byte</span></span>](byte.md)|<xref:System.Byte?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-109">sbyte</span><span class="sxs-lookup"><span data-stu-id="18ddd-109">sbyte</span></span>](sbyte.md)|<xref:System.SByte?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-110">char</span><span class="sxs-lookup"><span data-stu-id="18ddd-110">char</span></span>](char.md)|<xref:System.Char?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-111">decimal</span><span class="sxs-lookup"><span data-stu-id="18ddd-111">decimal</span></span>](decimal.md)|<xref:System.Decimal?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-112">double</span><span class="sxs-lookup"><span data-stu-id="18ddd-112">double</span></span>](double.md)|<xref:System.Double?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-113">float</span><span class="sxs-lookup"><span data-stu-id="18ddd-113">float</span></span>](float.md)|<xref:System.Single?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-114">int</span><span class="sxs-lookup"><span data-stu-id="18ddd-114">int</span></span>](int.md)|<xref:System.Int32?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-115">uint</span><span class="sxs-lookup"><span data-stu-id="18ddd-115">uint</span></span>](uint.md)|<xref:System.UInt32?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-116">long</span><span class="sxs-lookup"><span data-stu-id="18ddd-116">long</span></span>](long.md)|<xref:System.Int64?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-117">ulong</span><span class="sxs-lookup"><span data-stu-id="18ddd-117">ulong</span></span>](ulong.md)|<xref:System.UInt64?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-118">object</span><span class="sxs-lookup"><span data-stu-id="18ddd-118">object</span></span>](object.md)|<xref:System.Object?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-119">short</span><span class="sxs-lookup"><span data-stu-id="18ddd-119">short</span></span>](short.md)|<xref:System.Int16?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-120">ushort</span><span class="sxs-lookup"><span data-stu-id="18ddd-120">ushort</span></span>](ushort.md)|<xref:System.UInt16?displayProperty=nameWithType>|  
|[<span data-ttu-id="18ddd-121">string</span><span class="sxs-lookup"><span data-stu-id="18ddd-121">string</span></span>](string.md)|<xref:System.String?displayProperty=nameWithType>|  
  
## <a name="remarks"></a><span data-ttu-id="18ddd-122">コメント</span><span class="sxs-lookup"><span data-stu-id="18ddd-122">Remarks</span></span>

<span data-ttu-id="18ddd-123">表内の、`object` と `string` を除くすべての型が、単純型と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="18ddd-123">All of the types in the table, except `object` and `string`, are referred to as simple types.</span></span>  
  
<span data-ttu-id="18ddd-124">C# 型のキーワードと別名は相互に交換できます。</span><span class="sxs-lookup"><span data-stu-id="18ddd-124">The C# type keywords and their aliases are interchangeable.</span></span> <span data-ttu-id="18ddd-125">たとえば、整数の変数を宣言するには、次のいずれかの宣言を使用します。</span><span class="sxs-lookup"><span data-stu-id="18ddd-125">For example, you can declare an integer variable by using either of the following declarations:</span></span>  

```csharp
int x = 123;
System.Int32 y = 123;
```

<span data-ttu-id="18ddd-126">[typeof](typeof.md) 演算子を使用して、指定した型を表す <xref:System.Type?displayProperty=nameWithType> インスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="18ddd-126">Use the [typeof](typeof.md) operator to get the <xref:System.Type?displayProperty=nameWithType> instance that represents the specified type:</span></span>

```csharp
Type stringType = typeof(string);
Console.WriteLine(stringType.FullName);

Type doubleType = typeof(System.Double);
Console.WriteLine(doubleType.FullName);

// Output:
// System.String
// System.Double
```

## <a name="see-also"></a><span data-ttu-id="18ddd-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="18ddd-127">See also</span></span>

- [<span data-ttu-id="18ddd-128">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="18ddd-128">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="18ddd-129">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="18ddd-129">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="18ddd-130">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="18ddd-130">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="18ddd-131">型のリファレンス表</span><span class="sxs-lookup"><span data-stu-id="18ddd-131">Reference tables for types</span></span>](reference-tables-for-types.md)
- [<span data-ttu-id="18ddd-132">値型</span><span class="sxs-lookup"><span data-stu-id="18ddd-132">Value types</span></span>](value-types.md)
- [<span data-ttu-id="18ddd-133">参照型</span><span class="sxs-lookup"><span data-stu-id="18ddd-133">Reference types</span></span>](reference-types.md)
- [<span data-ttu-id="18ddd-134">既定値の一覧表</span><span class="sxs-lookup"><span data-stu-id="18ddd-134">Default values table</span></span>](default-values-table.md)
- [<span data-ttu-id="18ddd-135">dynamic</span><span class="sxs-lookup"><span data-stu-id="18ddd-135">dynamic</span></span>](dynamic.md)
