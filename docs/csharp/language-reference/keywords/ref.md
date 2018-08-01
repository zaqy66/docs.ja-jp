---
title: ref (C# リファレンス)
ms.date: 03/06/2018
f1_keywords:
- ref_CSharpKeyword
- ref
helpviewer_keywords:
- parameters [C#], ref
- ref keyword [C#]
ms.openlocfilehash: a72624d5702ec12bfda98d49a16474cc84205ff0
ms.sourcegitcommit: 70c76a12449439bac0f7a359866be5a0311ce960
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/25/2018
ms.locfileid: "39245753"
---
# <a name="ref-c-reference"></a><span data-ttu-id="765c1-102">ref (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="765c1-102">ref (C# Reference)</span></span>

<span data-ttu-id="765c1-103">`ref` キーワードは、参照渡しで渡される値を示します。</span><span class="sxs-lookup"><span data-stu-id="765c1-103">The `ref` keyword indicates a value that is passed by reference.</span></span> <span data-ttu-id="765c1-104">このキーワードは、4 つの異なるコンテキストで使用されます。</span><span class="sxs-lookup"><span data-stu-id="765c1-104">It is used in four different contexts:</span></span>

- <span data-ttu-id="765c1-105">メソッド シグネチャとメソッドの呼び出しで、参照によってメソッドに引数を渡します。</span><span class="sxs-lookup"><span data-stu-id="765c1-105">In a method signature and in a method call, to pass an argument to a method by reference.</span></span> <span data-ttu-id="765c1-106">詳細については、「[参照渡しで引数を渡す](#passing-an-argument-by-reference)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="765c1-106">See [Passing an argument by reference](#passing-an-argument-by-reference) for more information.</span></span>
- <span data-ttu-id="765c1-107">メソッド シグネチャで、参照渡しで呼び出し元に値を返します。</span><span class="sxs-lookup"><span data-stu-id="765c1-107">In a method signature, to return a value to the caller by reference.</span></span> <span data-ttu-id="765c1-108">詳細については、「[参照戻り値](#reference-return-values)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="765c1-108">See [Reference return values](#reference-return-values) for more information.</span></span>
- <span data-ttu-id="765c1-109">メンバーの本文で、参照戻り値が、呼び出し元によって変更される参照としてローカルに格納されること、または、通常はローカル変数が参照渡しによって別の値にアクセスすることを示します。</span><span class="sxs-lookup"><span data-stu-id="765c1-109">In a member body, to indicate that a reference return value is stored locally as a reference that the caller intends to modify or, in general, a local variable accesses another value by reference.</span></span> <span data-ttu-id="765c1-110">詳細については、「[ref ローカル変数](#ref-locals)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="765c1-110">See [Ref locals](#ref-locals) for more information.</span></span>
- <span data-ttu-id="765c1-111">`struct` の宣言で、`ref struct` または `ref readonly struct` を宣言します。</span><span class="sxs-lookup"><span data-stu-id="765c1-111">In a `struct` declaration to declare a `ref struct` or a `ref readonly struct`.</span></span> <span data-ttu-id="765c1-112">詳しくは、「[ref struct 宣言](#ref-struct-declarations)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="765c1-112">See [ref struct declarations](#ref-struct-declarations) for more information.</span></span>

## <a name="passing-an-argument-by-reference"></a><span data-ttu-id="765c1-113">参照渡しで引数を渡す</span><span class="sxs-lookup"><span data-stu-id="765c1-113">Passing an argument by reference</span></span>

<span data-ttu-id="765c1-114">メソッドのパラメーター リストで使用した場合、`ref` キーワードは、引数を値ではなく、参照によって渡すことを示します。</span><span class="sxs-lookup"><span data-stu-id="765c1-114">When used in a method's parameter list, the `ref` keyword indicates that an argument is passed by reference, not by value.</span></span> <span data-ttu-id="765c1-115">参照渡しで渡すことにより、呼び出されたメソッドの引数に対する変更が、呼び出し元のメソッドに反映されます。</span><span class="sxs-lookup"><span data-stu-id="765c1-115">The effect of passing by reference is that any change to the argument in the called method is reflected in the calling method.</span></span> <span data-ttu-id="765c1-116">たとえば、呼び出し元がローカル変数の式、または配列要素のアクセス式を渡し、呼び出されたメソッドが ref パラメーターが参照するオブジェクトを置き換える場合、メソッドが戻ったときに呼び出し元のローカル変数または配列要素は新しいオブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="765c1-116">For example, if the caller passes a local variable expression or an array element access expression, and the called method replaces the object to which the ref parameter refers, then the caller’s local variable or the array element now refers to the new object when the method returns.</span></span>

> [!NOTE]
> <span data-ttu-id="765c1-117">参照渡しの概念と参照型の概念を混同しないでください。</span><span class="sxs-lookup"><span data-stu-id="765c1-117">Do not confuse the concept of passing by reference with the concept of reference types.</span></span> <span data-ttu-id="765c1-118">2 つの概念は同じではありません。</span><span class="sxs-lookup"><span data-stu-id="765c1-118">The two concepts are not the same.</span></span> <span data-ttu-id="765c1-119">メソッドのパラメーターは、値型か参照型かどうかに関係なく、`ref` によって変更できます。</span><span class="sxs-lookup"><span data-stu-id="765c1-119">A method parameter can be modified by `ref` regardless of whether it is a value type or a reference type.</span></span> <span data-ttu-id="765c1-120">参照渡しで渡される場合、値型はボックス化されません。</span><span class="sxs-lookup"><span data-stu-id="765c1-120">There is no boxing of a value type when it is passed by reference.</span></span>  

<span data-ttu-id="765c1-121">`ref` パラメーターを使用するには、メソッド定義と呼び出し元のメソッドの両方が、次の例に示すように `ref` キーワードを明示的に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="765c1-121">To use a `ref` parameter, both the method definition and the calling method must explicitly use the `ref` keyword, as shown in the following example.</span></span>  

[!code-csharp-interactive[csrefKeywordsMethodParams#6](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/RefParameterModifier.cs#1)]

<span data-ttu-id="765c1-122">`ref` または `in` パラメーターに渡す引数は、渡す前に初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="765c1-122">An argument that is passed to a `ref` or `in` parameter must be initialized before it is passed.</span></span> <span data-ttu-id="765c1-123">これは、引数を渡す前に明示的に初期化する必要がない [out](out-parameter-modifier.md) パラメーターとは異なります。</span><span class="sxs-lookup"><span data-stu-id="765c1-123">This differs from [out](out-parameter-modifier.md) parameters, whose arguments do not have to be explicitly initialized before they are passed.</span></span>

<span data-ttu-id="765c1-124">クラスのメンバーは、`ref`、`in`、または `out` のみが異なるシグネチャを持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="765c1-124">Members of a class can't have signatures that differ only by `ref`, `in`, or `out`.</span></span> <span data-ttu-id="765c1-125">1 つの型の 2 つのメンバー間の唯一の違いが、1 つには `ref` パラメーターが存在し、もう 1 つには `out` または `in` パラメーターが存在することである場合、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="765c1-125">A compiler error occurs if the only difference between two members of a type is that one of them has a `ref` parameter and the other has an `out`, or `in` parameter.</span></span> <span data-ttu-id="765c1-126">たとえば、次のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="765c1-126">The following code, for example, doesn't compile.</span></span>  

```csharp
class CS0663_Example
{
    // Compiler error CS0663: "Cannot define overloaded 
    // methods that differ only on ref and out".
    public void SampleMethod(out int i) { }
    public void SampleMethod(ref int i) { }
}
```

<span data-ttu-id="765c1-127">ただし、次の例に示すように、1 つのメソッドに `ref`、`in` または `out` パラメーターがあり、もう 1 つのメソッドに値パラメーターがある場合、メソッドをオーバーロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="765c1-127">However, methods can be overloaded when one method has a `ref`, `in`, or `out` parameter and the other has a value parameter, as shown in the following example.</span></span>
  
[!code-csharp[csrefKeywordsMethodParams#6](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/RefParameterModifier.cs#2)]
  
 <span data-ttu-id="765c1-128">非表示やオーバーライドなど、シグネチャの一致が必要な他の状況では、`in`、`ref`、`out` はシグネチャの一部であり、互いに一致しません。</span><span class="sxs-lookup"><span data-stu-id="765c1-128">In other situations that require signature matching, such as hiding or overriding, `in`, `ref`, and `out` are part of the signature and don't match each other.</span></span>  
  
 <span data-ttu-id="765c1-129">プロパティは変数ではありません。</span><span class="sxs-lookup"><span data-stu-id="765c1-129">Properties are not variables.</span></span> <span data-ttu-id="765c1-130">プロパティはメソッドであり、`ref` パラメーターに渡すことはできません。</span><span class="sxs-lookup"><span data-stu-id="765c1-130">They are methods, and cannot be passed to `ref` parameters.</span></span>  
  
 <span data-ttu-id="765c1-131">配列を渡す方法については、「[ref と out を使用した配列の引き渡し](../../../csharp/programming-guide/arrays/passing-arrays-using-ref-and-out.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="765c1-131">For information about how to pass arrays, see [Passing Arrays Using ref and out](../../../csharp/programming-guide/arrays/passing-arrays-using-ref-and-out.md).</span></span>  
  
 <span data-ttu-id="765c1-132">次の種類のメソッドには、`ref`、`in`、`out` キーワードを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="765c1-132">You can't use the `ref`, `in`, and `out` keywords for the following kinds of methods:</span></span>  
  
- <span data-ttu-id="765c1-133">[async](../../../csharp/language-reference/keywords/async.md) 修飾子を使用して定義した Async メソッド。</span><span class="sxs-lookup"><span data-stu-id="765c1-133">Async methods, which you define by using the [async](../../../csharp/language-reference/keywords/async.md) modifier.</span></span>  
- <span data-ttu-id="765c1-134">[yield return](../../../csharp/language-reference/keywords/yield.md) または `yield break` ステートメントを含む Iterator メソッド。</span><span class="sxs-lookup"><span data-stu-id="765c1-134">Iterator methods, which include a [yield return](../../../csharp/language-reference/keywords/yield.md) or `yield break` statement.</span></span>  

## <a name="passing-an-argument-by-reference-an-example"></a><span data-ttu-id="765c1-135">参照渡しで引数を渡す: 使用例</span><span class="sxs-lookup"><span data-stu-id="765c1-135">Passing an argument by reference: An example</span></span>

<span data-ttu-id="765c1-136">前の例は、参照によって値型を渡す例でした。</span><span class="sxs-lookup"><span data-stu-id="765c1-136">The previous examples pass value types by reference.</span></span> <span data-ttu-id="765c1-137">`ref` キーワードを使用して、参照渡しで参照型を渡すこともできます。</span><span class="sxs-lookup"><span data-stu-id="765c1-137">You can also use the `ref` keyword to pass reference types by reference.</span></span> <span data-ttu-id="765c1-138">参照型を参照渡しで渡すと、呼び出されたメソッドは、参照パラメーターが呼び出し元で参照するオブジェクトに置換できます。</span><span class="sxs-lookup"><span data-stu-id="765c1-138">Passing a reference type by reference enables the called method to replace the object to which the reference parameter refers in the caller.</span></span> <span data-ttu-id="765c1-139">オブジェクトの格納場所は、参照パラメーターの値としてメソッドに渡されます。</span><span class="sxs-lookup"><span data-stu-id="765c1-139">The storage location of the object is passed to the method as the value of the reference parameter.</span></span> <span data-ttu-id="765c1-140">パラメーターの格納場所の値を変更する場合は (新しいオブジェクトをポイント)、呼び出し元が参照する格納場所を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="765c1-140">If you change the value in the storage location of the parameter (to point to a new object), you also change the storage location to which the caller refers.</span></span> <span data-ttu-id="765c1-141">次の例では、参照型のインスタンスを `ref` パラメーターとして渡します。</span><span class="sxs-lookup"><span data-stu-id="765c1-141">The following example passes an instance of a reference type as a `ref` parameter.</span></span>
  
[!code-csharp[csrefKeywordsMethodParams#6](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/RefParameterModifier.cs#3)]

<span data-ttu-id="765c1-142">参照型を値渡しまたは参照渡しで渡す方法の詳細については、「[参照型パラメーターの引き渡し](../../../csharp/programming-guide/classes-and-structs/passing-reference-type-parameters.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="765c1-142">For more information about how to pass reference types by value and by reference, see [Passing Reference-Type Parameters](../../../csharp/programming-guide/classes-and-structs/passing-reference-type-parameters.md).</span></span>
  
## <a name="reference-return-values"></a><span data-ttu-id="765c1-143">参照戻り値</span><span class="sxs-lookup"><span data-stu-id="765c1-143">Reference return values</span></span>

<span data-ttu-id="765c1-144">参照戻り値 (または ref 戻り値) は、メソッドから呼び出し元に参照渡しで返される値です。</span><span class="sxs-lookup"><span data-stu-id="765c1-144">Reference return values (or ref returns) are values that a method returns by reference to the caller.</span></span> <span data-ttu-id="765c1-145">つまり、呼び出し元はメソッドによって返される値を変更することができ、メソッドを格納するオブジェクトの状態にその変更が反映されます。</span><span class="sxs-lookup"><span data-stu-id="765c1-145">That is, the caller can modify the value returned by a method, and that change is reflected in the state of the object that contains the method.</span></span>

<span data-ttu-id="765c1-146">参照戻り値は `ref` キーワードを使用して以下に定義されます。</span><span class="sxs-lookup"><span data-stu-id="765c1-146">A reference return value is defined by using the `ref` keyword:</span></span>

- <span data-ttu-id="765c1-147">メソッド シグネチャ。</span><span class="sxs-lookup"><span data-stu-id="765c1-147">In the method signature.</span></span> <span data-ttu-id="765c1-148">たとえば、次のメソッド シグネチャは、`GetCurrentPrice` メソッドが参照渡しで <xref:System.Decimal> 値を返すことを示しています。</span><span class="sxs-lookup"><span data-stu-id="765c1-148">For example, the following method signature indicates that the `GetCurrentPrice` method returns a <xref:System.Decimal> value by reference.</span></span>

```csharp
public ref decimal GetCurrentValue()
```

- <span data-ttu-id="765c1-149">メソッドの `return` ステートメントで返される変数と `return` トークンの間。</span><span class="sxs-lookup"><span data-stu-id="765c1-149">Between the `return` token and the variable returned in a `return` statement in the method.</span></span> <span data-ttu-id="765c1-150">例:</span><span class="sxs-lookup"><span data-stu-id="765c1-150">For example:</span></span>

```csharp
return ref DecimalArray[0];
```

<span data-ttu-id="765c1-151">呼び出し元がオブジェクトの状態を変更するには、[ref ローカル変数](#ref-locals)として明示的に定義した変数に参照戻り値を格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="765c1-151">In order for the caller to modify the object's state, the reference return value must be stored to a variable that is explicitly defined as a [ref local](#ref-locals).</span></span>

<span data-ttu-id="765c1-152">例については、「[ref 戻り値と ref ローカル変数](#a-ref-returns-and-ref-locals-example)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="765c1-152">For an example, see [A ref returns and ref locals example](#a-ref-returns-and-ref-locals-example)</span></span>

## <a name="ref-locals"></a><span data-ttu-id="765c1-153">ref ローカル変数</span><span class="sxs-lookup"><span data-stu-id="765c1-153">Ref locals</span></span>

<span data-ttu-id="765c1-154">ref ローカル変数は、`return ref` を使用して返された値を参照するために使用します。</span><span class="sxs-lookup"><span data-stu-id="765c1-154">A ref local variable is used to refer to values returned using `return ref`.</span></span>  <span data-ttu-id="765c1-155">ref ローカル変数は、初期化して ref 戻り値に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="765c1-155">A ref local variable must be initialized and assigned to a ref return value.</span></span> <span data-ttu-id="765c1-156">ref ローカル変数の値に変更を加えると、参照渡しの値を返すメソッドのオブジェクトの状態に反映されます。</span><span class="sxs-lookup"><span data-stu-id="765c1-156">Any modifications to the value of the ref local are reflected in the state of the object whose method returned the value by reference.</span></span>

<span data-ttu-id="765c1-157">ref ローカル変数を定義するには、変数宣言の前と、参照渡しで値を返すメソッドの呼び出しの直前に、`ref` キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="765c1-157">You define a ref local by using the `ref` keyword before the variable declaration, as well as immediately before the call to the method that returns the value by reference.</span></span>

<span data-ttu-id="765c1-158">たとえば、次のステートメントは、`GetEstimatedValue` という名前のメソッドによって返される ref ローカル変数を定義しています。</span><span class="sxs-lookup"><span data-stu-id="765c1-158">For example, the following statement defines a ref local value that is returned by a method named `GetEstimatedValue`:</span></span>

```csharp
ref decimal estValue = ref Building.GetEstimatedValue();
```

<span data-ttu-id="765c1-159">同じ方法で、参照渡しの値にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="765c1-159">You can access a value by reference in the same way.</span></span> <span data-ttu-id="765c1-160">場合によっては、参照渡しの値へのアクセスによって負荷がかかる可能性があるコピー操作が回避され、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="765c1-160">In some cases, accessing a value by reference increases performance by avoiding a potentially expensive copy operation.</span></span> <span data-ttu-id="765c1-161">たとえば、次のステートメントは、値の参照に使用される ref ローカル値をどのように定義できるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="765c1-161">For example, the following statement shows how one can define a ref local value that is used to reference a value.</span></span>

```csharp
ref VeryLargeStruct reflocal = ref veryLargeStruct;
```

<span data-ttu-id="765c1-162">どちらの例も、`ref` キーワードは両方の位置で使用する必要があります。そうしないと、コンパイラ エラー CS8172 "値を使用して参照渡し変数を初期化することはできません" が生成されます。</span><span class="sxs-lookup"><span data-stu-id="765c1-162">Note that in both examples the `ref` keyword must be used in both places, or the compiler generates error CS8172, "Cannot initialize a by-reference variable with a value."</span></span>

## <a name="a-ref-returns-and-ref-locals-example"></a><span data-ttu-id="765c1-163">ref 戻り値と ref ローカル変数の使用例</span><span class="sxs-lookup"><span data-stu-id="765c1-163">A ref returns and ref locals example</span></span>

<span data-ttu-id="765c1-164">次の例は、`Title` と `Author` という 2 つの <xref:System.String> フィールドを持つ `Book` クラスを定義しています。</span><span class="sxs-lookup"><span data-stu-id="765c1-164">The following example defines a `Book` class that has two <xref:System.String> fields, `Title` and `Author`.</span></span> <span data-ttu-id="765c1-165">また、`Book` オブジェクトのプライベート配列を含む `BookCollection` クラスも定義しています。</span><span class="sxs-lookup"><span data-stu-id="765c1-165">It also defines a `BookCollection` class that includes a private array of `Book` objects.</span></span> <span data-ttu-id="765c1-166">個々のブック オブジェクトは、`GetBookByTitle` メソッドを呼び出すことによって参照渡しで返されます。</span><span class="sxs-lookup"><span data-stu-id="765c1-166">Individual book objects are returned by reference by calling its `GetBookByTitle` method.</span></span>

[!code-csharp[csrefKeywordsMethodParams#6](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/RefParameterModifier.cs#4)]

<span data-ttu-id="765c1-167">呼び出し元が `GetBookByTitle` によって返される値を ref ローカル変数として格納する場合、呼び出し元が戻り値に加えた変更が `BookCollection` オブジェクトに反映されます。次の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="765c1-167">When the caller stores the value returned by the `GetBookByTitle` method as a ref local, changes that the caller makes to the return value are reflected in the `BookCollection` object, as the following example shows.</span></span>

[!code-csharp[csrefKeywordsMethodParams#6](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/RefParameterModifier.cs#5)]

## <a name="ref-struct-declarations"></a><span data-ttu-id="765c1-168">ref struct 宣言</span><span class="sxs-lookup"><span data-stu-id="765c1-168">Ref struct declarations</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="765c1-169">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="765c1-169">C# Language Specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="765c1-170">関連項目</span><span class="sxs-lookup"><span data-stu-id="765c1-170">See also</span></span>

 [<span data-ttu-id="765c1-171">値の型による参照セマンティクス</span><span class="sxs-lookup"><span data-stu-id="765c1-171">Reference semantics with value types</span></span>](../../reference-semantics-with-value-types.md)  
 [<span data-ttu-id="765c1-172">パラメーターの引き渡し</span><span class="sxs-lookup"><span data-stu-id="765c1-172">Passing Parameters</span></span>](../../programming-guide/classes-and-structs/passing-parameters.md)  
 [<span data-ttu-id="765c1-173">メソッド パラメーター</span><span class="sxs-lookup"><span data-stu-id="765c1-173">Method Parameters</span></span>](method-parameters.md)  
 [<span data-ttu-id="765c1-174">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="765c1-174">C# Reference</span></span>](../index.md)  
 [<span data-ttu-id="765c1-175">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="765c1-175">C# Programming Guide</span></span>](../../programming-guide/index.md)  
 [<span data-ttu-id="765c1-176">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="765c1-176">C# Keywords</span></span>](index.md)
