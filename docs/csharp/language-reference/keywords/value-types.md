---
title: 値型 (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- cs.valuetypes
helpviewer_keywords:
- value types [C#]
- types [C#], value types
- C# language, value types
ms.assetid: 471eb994-2958-49d5-a6be-19b4313f80a3
ms.openlocfilehash: 3bbaea9247d975c27ed6f49dedb749312f675296
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43487066"
---
# <a name="value-types-c-reference"></a><span data-ttu-id="a9602-102">値型 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="a9602-102">Value Types (C# Reference)</span></span>
<span data-ttu-id="a9602-103">値型は、次の 2 つの主要なカテゴリで構成されます。</span><span class="sxs-lookup"><span data-stu-id="a9602-103">The value types consist of two main categories:</span></span>  
  
-   [<span data-ttu-id="a9602-104">構造体</span><span class="sxs-lookup"><span data-stu-id="a9602-104">Structs</span></span>](../../../csharp/language-reference/keywords/struct.md)  
  
-   [<span data-ttu-id="a9602-105">列挙型</span><span class="sxs-lookup"><span data-stu-id="a9602-105">Enumerations</span></span>](../../../csharp/language-reference/keywords/enum.md)  
  
 <span data-ttu-id="a9602-106">構造体は、次のカテゴリに分類されます。</span><span class="sxs-lookup"><span data-stu-id="a9602-106">Structs fall into these categories:</span></span>  
  
-   <span data-ttu-id="a9602-107">数値型</span><span class="sxs-lookup"><span data-stu-id="a9602-107">Numeric types</span></span>  
  
    -   [<span data-ttu-id="a9602-108">整数型</span><span class="sxs-lookup"><span data-stu-id="a9602-108">Integral types</span></span>](../../../csharp/language-reference/keywords/integral-types-table.md)  
  
    -   [<span data-ttu-id="a9602-109">浮動小数点型</span><span class="sxs-lookup"><span data-stu-id="a9602-109">Floating-point types</span></span>](../../../csharp/language-reference/keywords/floating-point-types-table.md)  
  
-   [<span data-ttu-id="a9602-110">bool</span><span class="sxs-lookup"><span data-stu-id="a9602-110">bool</span></span>](../../../csharp/language-reference/keywords/bool.md)  
  
-   <span data-ttu-id="a9602-111">ユーザー定義の構造体</span><span class="sxs-lookup"><span data-stu-id="a9602-111">User defined structs.</span></span>  
  
## <a name="main-features-of-value-types"></a><span data-ttu-id="a9602-112">値型の主な機能</span><span class="sxs-lookup"><span data-stu-id="a9602-112">Main Features of Value Types</span></span>  
 <span data-ttu-id="a9602-113">値型に基づく変数には、値が直接含まれます。</span><span class="sxs-lookup"><span data-stu-id="a9602-113">Variables that are based on value types directly contain values.</span></span> <span data-ttu-id="a9602-114">ある値型の変数を別の変数に代入することで、含まれている値がコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a9602-114">Assigning one value type variable to another copies the contained value.</span></span> <span data-ttu-id="a9602-115">これは、オブジェクトそのものではなく、参照をオブジェクトにコピーする、参照型の変数の代入とは異なります。</span><span class="sxs-lookup"><span data-stu-id="a9602-115">This differs from the assignment of reference type variables, which copies a reference to the object but not the object itself.</span></span>  
  
 <span data-ttu-id="a9602-116">すべての値型が <xref:System.ValueType?displayProperty=nameWithType> から暗黙的に派生されます。</span><span class="sxs-lookup"><span data-stu-id="a9602-116">All value types are derived implicitly from the <xref:System.ValueType?displayProperty=nameWithType>.</span></span>  
  
 <span data-ttu-id="a9602-117">参照型とは異なり、値型から新しい型を派生することはできません。</span><span class="sxs-lookup"><span data-stu-id="a9602-117">Unlike with reference types, you cannot derive a new type from a value type.</span></span> <span data-ttu-id="a9602-118">ただし、参照型の場合と同様に、構造体はインターフェイスを実装できます。</span><span class="sxs-lookup"><span data-stu-id="a9602-118">However, like reference types, structs can implement interfaces.</span></span>  
  
 <span data-ttu-id="a9602-119">参照型とは異なり、値型に `null` 値を含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="a9602-119">Unlike reference types, a value type cannot contain the `null` value.</span></span> <span data-ttu-id="a9602-120">ただし、[null 許容型](../../../csharp/programming-guide/nullable-types/index.md)機能では、値型の `null` への代入が許可されます。</span><span class="sxs-lookup"><span data-stu-id="a9602-120">However, the [nullable types](../../../csharp/programming-guide/nullable-types/index.md) feature does allow for value types to be assigned to `null`.</span></span>  
  
 <span data-ttu-id="a9602-121">各値型には、その型の既定値を初期化する暗黙の既定のコンストラクターがあります。</span><span class="sxs-lookup"><span data-stu-id="a9602-121">Each value type has an implicit default constructor that initializes the default value of that type.</span></span> <span data-ttu-id="a9602-122">値型の既定値の詳細については、「[既定値の一覧表](../../../csharp/language-reference/keywords/default-values-table.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9602-122">For information about default values of value types, see [Default Values Table](../../../csharp/language-reference/keywords/default-values-table.md).</span></span>  
  
## <a name="main-features-of-simple-types"></a><span data-ttu-id="a9602-123">単純型の主な機能</span><span class="sxs-lookup"><span data-stu-id="a9602-123">Main Features of Simple Types</span></span>  
 <span data-ttu-id="a9602-124">C# 言語に不可欠なすべての単純型は、.NET Framework システム型のエイリアスです。</span><span class="sxs-lookup"><span data-stu-id="a9602-124">All of the simple types -- those integral to the C# language -- are aliases of the .NET Framework System types.</span></span> <span data-ttu-id="a9602-125">たとえば、[int](../../../csharp/language-reference/keywords/int.md) は <xref:System.Int32?displayProperty=nameWithType> のエイリアスです。</span><span class="sxs-lookup"><span data-stu-id="a9602-125">For example, [int](../../../csharp/language-reference/keywords/int.md) is an alias of <xref:System.Int32?displayProperty=nameWithType>.</span></span> <span data-ttu-id="a9602-126">エイリアスの完全な一覧については、「[組み込み型の一覧表](../../../csharp/language-reference/keywords/built-in-types-table.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9602-126">For a complete list of aliases, see [Built-In Types Table](../../../csharp/language-reference/keywords/built-in-types-table.md).</span></span>  
  
 <span data-ttu-id="a9602-127">オペランドがすべて単純型の定数式は、コンパイル時に評価されます。</span><span class="sxs-lookup"><span data-stu-id="a9602-127">Constant expressions, whose operands are all simple type constants, are evaluated at compilation time.</span></span>  
  
 <span data-ttu-id="a9602-128">単純型はリテラルを使用して初期化できます。</span><span class="sxs-lookup"><span data-stu-id="a9602-128">Simple types can be initialized by using literals.</span></span> <span data-ttu-id="a9602-129">たとえば、'A' は `char` 型のリテラルで、2001 は `int` 型のリテラルです。</span><span class="sxs-lookup"><span data-stu-id="a9602-129">For example, 'A' is a literal of the type `char` and 2001 is a literal of the type `int`.</span></span>  
  
## <a name="initializing-value-types"></a><span data-ttu-id="a9602-130">値型の初期化</span><span class="sxs-lookup"><span data-stu-id="a9602-130">Initializing Value Types</span></span>  
 <span data-ttu-id="a9602-131">C# では、ローカル変数を使用する前に初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9602-131">Local variables in C# must be initialized before they are used.</span></span> <span data-ttu-id="a9602-132">たとえば、次の例のように、初期化せずにローカル変数を宣言した場合、</span><span class="sxs-lookup"><span data-stu-id="a9602-132">For example, you might declare a local variable without initialization as in the following example:</span></span>  
  
```csharp  
int myInt;  
```  
  
 <span data-ttu-id="a9602-133">初期化してからでないとこれを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="a9602-133">You cannot use it before you initialize it.</span></span> <span data-ttu-id="a9602-134">次のステートメントを使用して初期化できます。</span><span class="sxs-lookup"><span data-stu-id="a9602-134">You can initialize it using the following statement:</span></span>  
  
```csharp  
myInt = new int();  // Invoke default constructor for int type.  
```  
  
 <span data-ttu-id="a9602-135">このステートメントは、次のステートメントと同じです。</span><span class="sxs-lookup"><span data-stu-id="a9602-135">This statement is equivalent to the following statement:</span></span>  
  
```csharp  
myInt = 0;         // Assign an initial value, 0 in this example.  
```  
  
 <span data-ttu-id="a9602-136">もちろん、次の例のように、宣言と初期化を同じステートメントに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a9602-136">You can, of course, have the declaration and the initialization in the same statement as in the following examples:</span></span>  
  
```csharp  
int myInt = new int();  
```  
  
 <span data-ttu-id="a9602-137">または</span><span class="sxs-lookup"><span data-stu-id="a9602-137">–or–</span></span>  
  
```csharp  
int myInt = 0;  
```  
  
 <span data-ttu-id="a9602-138">[new](../../../csharp/language-reference/keywords/new.md) 演算子を使用すると、特定の型の既定のコンストラクターを呼び出し、既定値を変数に代入します。</span><span class="sxs-lookup"><span data-stu-id="a9602-138">Using the [new](../../../csharp/language-reference/keywords/new.md) operator calls the default constructor of the specific type and assigns the default value to the variable.</span></span> <span data-ttu-id="a9602-139">前の例では、既定のコンス トラクターが値 `0` を `myInt` に代入しました。</span><span class="sxs-lookup"><span data-stu-id="a9602-139">In the preceding example, the default constructor assigned the value `0` to `myInt`.</span></span> <span data-ttu-id="a9602-140">既定のコンストラクターの呼び出しにより値を代入する詳細については、「[既定値の一覧表](../../../csharp/language-reference/keywords/default-values-table.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9602-140">For more information about values assigned by calling default constructors, see [Default Values Table](../../../csharp/language-reference/keywords/default-values-table.md).</span></span>  
  
 <span data-ttu-id="a9602-141">ユーザー定義型では、[new](../../../csharp/language-reference/keywords/new.md) を使用して既定のコンストラクターを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a9602-141">With user-defined types, use [new](../../../csharp/language-reference/keywords/new.md) to invoke the default constructor.</span></span> <span data-ttu-id="a9602-142">たとえば、次のステートメントは、`Point` 構造体の既定のコンストラクターを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a9602-142">For example, the following statement invokes the default constructor of the `Point` struct:</span></span>  
  
```csharp  
Point p = new Point(); // Invoke default constructor for the struct.  
```  
  
 <span data-ttu-id="a9602-143">この呼び出しの後、構造体は明示的に代入されると見なされます。つまり、すべてのメンバーがその既定値に初期化されます。</span><span class="sxs-lookup"><span data-stu-id="a9602-143">After this call, the struct is considered to be definitely assigned; that is, all its members are initialized to their default values.</span></span>  
  
 <span data-ttu-id="a9602-144">new 演算子の詳細については、「[new](../../../csharp/language-reference/keywords/new.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9602-144">For more information about the new operator, see [new](../../../csharp/language-reference/keywords/new.md).</span></span>  
  
 <span data-ttu-id="a9602-145">数値型の出力の書式設定については、「[数値結果テーブルの書式設定](../../../csharp/language-reference/keywords/formatting-numeric-results-table.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9602-145">For information about formatting the output of numeric types, see [Formatting Numeric Results Table](../../../csharp/language-reference/keywords/formatting-numeric-results-table.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9602-146">参照</span><span class="sxs-lookup"><span data-stu-id="a9602-146">See Also</span></span>

- [<span data-ttu-id="a9602-147">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="a9602-147">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="a9602-148">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="a9602-148">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="a9602-149">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="a9602-149">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="a9602-150">型</span><span class="sxs-lookup"><span data-stu-id="a9602-150">Types</span></span>](../../../csharp/language-reference/keywords/types.md)  
- [<span data-ttu-id="a9602-151">型のリファレンス表</span><span class="sxs-lookup"><span data-stu-id="a9602-151">Reference Tables for Types</span></span>](../../../csharp/language-reference/keywords/reference-tables-for-types.md)  
- [<span data-ttu-id="a9602-152">参照型</span><span class="sxs-lookup"><span data-stu-id="a9602-152">Reference Types</span></span>](../../../csharp/language-reference/keywords/reference-types.md)  
- [<span data-ttu-id="a9602-153">Null 許容型</span><span class="sxs-lookup"><span data-stu-id="a9602-153">Nullable types</span></span>](../../programming-guide/nullable-types/index.md)  
