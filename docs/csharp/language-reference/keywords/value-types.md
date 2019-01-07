---
title: 値型 - C# リファレンス
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- cs.valuetypes
helpviewer_keywords:
- value types [C#]
- types [C#], value types
- C# language, value types
ms.assetid: 471eb994-2958-49d5-a6be-19b4313f80a3
ms.openlocfilehash: 77aed78e7822e06b3b1e6c48b07790d93e09559c
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612726"
---
# <a name="value-types-c-reference"></a><span data-ttu-id="4665b-102">値型 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="4665b-102">Value types (C# Reference)</span></span>

<span data-ttu-id="4665b-103">2 種類の値型があります。</span><span class="sxs-lookup"><span data-stu-id="4665b-103">There are two kinds of value types:</span></span>

- [<span data-ttu-id="4665b-104">構造体</span><span class="sxs-lookup"><span data-stu-id="4665b-104">Structs</span></span>](struct.md)

- [<span data-ttu-id="4665b-105">列挙型</span><span class="sxs-lookup"><span data-stu-id="4665b-105">Enumerations</span></span>](enum.md)

## <a name="main-features-of-value-types"></a><span data-ttu-id="4665b-106">値型の主な機能</span><span class="sxs-lookup"><span data-stu-id="4665b-106">Main features of value types</span></span>

<span data-ttu-id="4665b-107">値型の変数には、その型の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4665b-107">A variable of a value type contains a value of the type.</span></span> <span data-ttu-id="4665b-108">たとえば、`int` 型の変数には値 `42` が含まれている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4665b-108">For example, a variable of the `int` type might contain the value `42`.</span></span> <span data-ttu-id="4665b-109">これは、オブジェクトとも呼ばれる型のインスタンスへの参照を含む参照型の変数とは異なります。</span><span class="sxs-lookup"><span data-stu-id="4665b-109">This differs from a variable of a reference type, which contains a reference to an instance of the type, also known as an object.</span></span> <span data-ttu-id="4665b-110">値型の変数に新しい値を割り当てると、その値はコピーされます。</span><span class="sxs-lookup"><span data-stu-id="4665b-110">When you assign a new value to a variable of a value type, that value is copied.</span></span> <span data-ttu-id="4665b-111">参照型の変数に新しい値を割り当てると、オブジェクト自体ではなく参照がコピーされます。</span><span class="sxs-lookup"><span data-stu-id="4665b-111">When you assign a new value to a variable of a reference type, the reference is copied, not the object itself.</span></span>

<span data-ttu-id="4665b-112">すべての値型が <xref:System.ValueType?displayProperty=nameWithType> から暗黙的に派生されます。</span><span class="sxs-lookup"><span data-stu-id="4665b-112">All value types are derived implicitly from the <xref:System.ValueType?displayProperty=nameWithType>.</span></span>

<span data-ttu-id="4665b-113">参照型とは異なり、値型から新しい型を派生することはできません。</span><span class="sxs-lookup"><span data-stu-id="4665b-113">Unlike with reference types, you cannot derive a new type from a value type.</span></span> <span data-ttu-id="4665b-114">ただし、参照型の場合と同様に、構造体はインターフェイスを実装できます。</span><span class="sxs-lookup"><span data-stu-id="4665b-114">However, like reference types, structs can implement interfaces.</span></span>

<span data-ttu-id="4665b-115">値型の変数は既定で `null` にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4665b-115">Value type variables cannot be `null` by default.</span></span> <span data-ttu-id="4665b-116">ただし、対応する [null 許容型](../../../csharp/programming-guide/nullable-types/index.md)の変数を `null` にすることはできます。</span><span class="sxs-lookup"><span data-stu-id="4665b-116">However, variables of the corresponding [nullable types](../../../csharp/programming-guide/nullable-types/index.md) can be `null`.</span></span>

<span data-ttu-id="4665b-117">各値型には、その型の既定値を初期化する暗黙の既定のコンストラクターがあります。</span><span class="sxs-lookup"><span data-stu-id="4665b-117">Each value type has an implicit default constructor that initializes the default value of that type.</span></span> <span data-ttu-id="4665b-118">値型の既定値の詳細については、「[既定値の一覧表](default-values-table.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4665b-118">For information about default values of value types, see [Default values table](default-values-table.md).</span></span>

## <a name="simple-types"></a><span data-ttu-id="4665b-119">単純型</span><span class="sxs-lookup"><span data-stu-id="4665b-119">Simple types</span></span>

<span data-ttu-id="4665b-120">*単純型*は、C# に用意されている定義済みの構造体型のセットであり、次の型を構成します。</span><span class="sxs-lookup"><span data-stu-id="4665b-120">The *simple types* are a set of predefined struct types provided by C# and comprise the following types:</span></span>

- <span data-ttu-id="4665b-121">[整数型](integral-types-table.md): 整数の数値型と [char](char.md) 型</span><span class="sxs-lookup"><span data-stu-id="4665b-121">[Integral types](integral-types-table.md): integer numeric types and the [char](char.md) type</span></span>
- [<span data-ttu-id="4665b-122">浮動小数点型</span><span class="sxs-lookup"><span data-stu-id="4665b-122">Floating-point types</span></span>](floating-point-types-table.md)
- [<span data-ttu-id="4665b-123">bool</span><span class="sxs-lookup"><span data-stu-id="4665b-123">bool</span></span>](bool.md)

<span data-ttu-id="4665b-124">単純型はキーワードで識別されますが、これらのキーワードは、<xref:System> 名前空間に事前に定義されている構造体型の単なるエイリアスです。</span><span class="sxs-lookup"><span data-stu-id="4665b-124">The simple types are identified through keywords, but these keywords are simply aliases for predefined struct types in the <xref:System> namespace.</span></span> <span data-ttu-id="4665b-125">たとえば、[int](int.md) は <xref:System.Int32?displayProperty=nameWithType> のエイリアスです。</span><span class="sxs-lookup"><span data-stu-id="4665b-125">For example, [int](int.md) is an alias of <xref:System.Int32?displayProperty=nameWithType>.</span></span> <span data-ttu-id="4665b-126">エイリアスの完全な一覧については、「[組み込み型の一覧表](built-in-types-table.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4665b-126">For a complete list of aliases, see [Built-in types table](built-in-types-table.md).</span></span>

<span data-ttu-id="4665b-127">単純型は、ある追加の操作を許可している点で、他の構造体型とは異なります。</span><span class="sxs-lookup"><span data-stu-id="4665b-127">The simple types differ from other struct types in that they permit certain additional operations:</span></span>

- <span data-ttu-id="4665b-128">単純型はリテラルを使用して初期化できます。</span><span class="sxs-lookup"><span data-stu-id="4665b-128">Simple types can be initialized by using literals.</span></span> <span data-ttu-id="4665b-129">たとえば、`'A'` は `char` 型のリテラルで、`2001` は `int` 型のリテラルです。</span><span class="sxs-lookup"><span data-stu-id="4665b-129">For example, `'A'` is a literal of the type `char` and `2001` is a literal of the type `int`.</span></span>

- <span data-ttu-id="4665b-130">単純型の定数は、[const](const.md) キーワードを使用して宣言できます。</span><span class="sxs-lookup"><span data-stu-id="4665b-130">You can declare constants of the simple types with the [const](const.md) keyword.</span></span> <span data-ttu-id="4665b-131">他の構造体型の定数を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="4665b-131">It's not possible to have constants of other struct types.</span></span>

- <span data-ttu-id="4665b-132">オペランドがすべて単純型の定数式は、コンパイル時に評価されます。</span><span class="sxs-lookup"><span data-stu-id="4665b-132">Constant expressions, whose operands are all simple type constants, are evaluated at compile time.</span></span>

<span data-ttu-id="4665b-133">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[単純型](~/_csharplang/spec/types.md#simple-types)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4665b-133">For more information, see the [Simple types](~/_csharplang/spec/types.md#simple-types) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="initializing-value-types"></a><span data-ttu-id="4665b-134">値型の初期化</span><span class="sxs-lookup"><span data-stu-id="4665b-134">Initializing value types</span></span>

<span data-ttu-id="4665b-135">C# では、ローカル変数を使用する前に初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4665b-135">Local variables in C# must be initialized before they are used.</span></span> <span data-ttu-id="4665b-136">たとえば、次の例のように、初期化せずにローカル変数を宣言した場合、</span><span class="sxs-lookup"><span data-stu-id="4665b-136">For example, you might declare a local variable without initialization as in the following example:</span></span>

```csharp
int myInt;
```

<span data-ttu-id="4665b-137">初期化してからでないとこれを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="4665b-137">You cannot use it before you initialize it.</span></span> <span data-ttu-id="4665b-138">次のステートメントを使用して初期化できます。</span><span class="sxs-lookup"><span data-stu-id="4665b-138">You can initialize it using the following statement:</span></span>

```csharp
myInt = new int();  // Invoke default constructor for int type.
```

<span data-ttu-id="4665b-139">このステートメントは、次のステートメントと同じです。</span><span class="sxs-lookup"><span data-stu-id="4665b-139">This statement is equivalent to the following statement:</span></span>

```csharp
myInt = 0;         // Assign an initial value, 0 in this example.
```

<span data-ttu-id="4665b-140">もちろん、次の例のように、宣言と初期化を同じステートメントに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4665b-140">You can, of course, have the declaration and the initialization in the same statement as in the following examples:</span></span>

```csharp
int myInt = new int();
```

<span data-ttu-id="4665b-141">または</span><span class="sxs-lookup"><span data-stu-id="4665b-141">–or–</span></span>

```csharp
int myInt = 0;
```

<span data-ttu-id="4665b-142">[new](new.md) 演算子を使用すると、特定の型の既定のコンストラクターを呼び出し、既定値を変数に代入します。</span><span class="sxs-lookup"><span data-stu-id="4665b-142">Using the [new](new.md) operator calls the default constructor of the specific type and assigns the default value to the variable.</span></span> <span data-ttu-id="4665b-143">前の例では、既定のコンス トラクターが値 `0` を `myInt` に代入しました。</span><span class="sxs-lookup"><span data-stu-id="4665b-143">In the preceding example, the default constructor assigned the value `0` to `myInt`.</span></span> <span data-ttu-id="4665b-144">既定のコンストラクターの呼び出しにより値を代入する詳細については、「[既定値の一覧表](default-values-table.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4665b-144">For more information about values assigned by calling default constructors, see [Default values table](default-values-table.md).</span></span>

<span data-ttu-id="4665b-145">ユーザー定義型では、[new](new.md) を使用して既定のコンストラクターを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4665b-145">With user-defined types, use [new](new.md) to invoke the default constructor.</span></span> <span data-ttu-id="4665b-146">たとえば、次のステートメントは、`Point` 構造体の既定のコンストラクターを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4665b-146">For example, the following statement invokes the default constructor of the `Point` struct:</span></span>

```csharp
Point p = new Point(); // Invoke default constructor for the struct.
```

<span data-ttu-id="4665b-147">この呼び出しの後、構造体は明示的に代入されると見なされます。つまり、すべてのメンバーがその既定値に初期化されます。</span><span class="sxs-lookup"><span data-stu-id="4665b-147">After this call, the struct is considered to be definitely assigned; that is, all its members are initialized to their default values.</span></span>

<span data-ttu-id="4665b-148">`new` 演算子の詳細については、「[new](new.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4665b-148">For more information about the `new` operator, see [new](new.md).</span></span>

<span data-ttu-id="4665b-149">数値型の出力の書式設定については、「[数値結果テーブルの書式設定](formatting-numeric-results-table.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4665b-149">For information about formatting the output of numeric types, see [Formatting numeric results table](formatting-numeric-results-table.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4665b-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="4665b-150">See also</span></span>

- [<span data-ttu-id="4665b-151">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="4665b-151">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="4665b-152">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="4665b-152">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="4665b-153">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="4665b-153">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="4665b-154">型</span><span class="sxs-lookup"><span data-stu-id="4665b-154">Types</span></span>](types.md)
- [<span data-ttu-id="4665b-155">型のリファレンス表</span><span class="sxs-lookup"><span data-stu-id="4665b-155">Reference tables for types</span></span>](reference-tables-for-types.md)
- [<span data-ttu-id="4665b-156">参照型</span><span class="sxs-lookup"><span data-stu-id="4665b-156">Reference Types</span></span>](reference-types.md)
- [<span data-ttu-id="4665b-157">Null 許容型</span><span class="sxs-lookup"><span data-stu-id="4665b-157">Nullable types</span></span>](../../programming-guide/nullable-types/index.md)