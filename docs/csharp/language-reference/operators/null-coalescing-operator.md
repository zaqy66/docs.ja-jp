---
title: ?? 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ??_CSharpKeyword
helpviewer_keywords:
- coalesce operator [C#]
- ?? operator [C#]
- conditional-AND operator (&&) [C#]
ms.assetid: 088b1f0d-c1af-4fe1-b4b8-196fd5ea9132
ms.openlocfilehash: b96fe4790aac7ff5ff5394cbaaeaddc1e334e96c
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333214"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="65556-103">??</span><span class="sxs-lookup"><span data-stu-id="65556-103">??</span></span> <span data-ttu-id="65556-104">operator (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="65556-104">operator (C# Reference)</span></span>

<span data-ttu-id="65556-105">`??` 演算子は、null 合体演算子と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="65556-105">The `??` operator is called the null-coalescing operator.</span></span>  <span data-ttu-id="65556-106">左側のオペランドが null 値でない場合には左側のオペランドを返し、null 値である場合には右側のオペランドを返します。</span><span class="sxs-lookup"><span data-stu-id="65556-106">It returns the left-hand operand if the operand is not null; otherwise it returns the right hand operand.</span></span>

## <a name="remarks"></a><span data-ttu-id="65556-107">コメント</span><span class="sxs-lookup"><span data-stu-id="65556-107">Remarks</span></span>

<span data-ttu-id="65556-108">null 許容型は、型のドメインの値を表すことができ、値は未定義でもかまいません (その場合、値は null になります)。</span><span class="sxs-lookup"><span data-stu-id="65556-108">A nullable type can represent a value from the type’s domain, or the value can be undefined (in which case the value is null).</span></span> <span data-ttu-id="65556-109">`??` 演算子の構文を使用して、左側のオペランドが null 許容型でその値が null である場合に、適切な値 (右側のオペランド) を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="65556-109">You can use the `??` operator’s syntactic expressiveness to return an appropriate value (the right hand operand) when the left operand has a nullable type whose value is null.</span></span> <span data-ttu-id="65556-110">`??` 演算子を使用せずに、null 非許容値型に対して null 許容値型を割り当てると、コンパイル時にエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="65556-110">If you try to assign a nullable value type to a non-nullable value type without using the `??` operator, you will generate a compile-time error.</span></span> <span data-ttu-id="65556-111">null 許容値型が定義されていない場合にキャストを使用すると、`InvalidOperationException` 例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="65556-111">If you use a cast, and the nullable value type is currently undefined, an `InvalidOperationException` exception will be thrown.</span></span>

<span data-ttu-id="65556-112">詳細については、「[Null 許容型](../../programming-guide/nullable-types/index.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65556-112">For more information, see [Nullable Types](../../programming-guide/nullable-types/index.md).</span></span>

<span data-ttu-id="65556-113">?? の結果は、</span><span class="sxs-lookup"><span data-stu-id="65556-113">The result of a ??</span></span> <span data-ttu-id="65556-114">たとえ両方の引数が定数であった場合でも、定数とは見なされません。</span><span class="sxs-lookup"><span data-stu-id="65556-114">operator is not considered to be a constant even if both its arguments are constants.</span></span>

## <a name="example"></a><span data-ttu-id="65556-115">例</span><span class="sxs-lookup"><span data-stu-id="65556-115">Example</span></span>

[!code-csharp[csRefOperators#53](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#53)]

## <a name="c-language-specification"></a><span data-ttu-id="65556-116">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="65556-116">C# language specification</span></span>

<span data-ttu-id="65556-117">詳細については、「[C# 言語仕様](../language-specification/index.md)」の [null 合体演算子](~/_csharplang/spec/expressions.md#the-null-coalescing-operator)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="65556-117">For more information, see [The null coalescing operator](~/_csharplang/spec/expressions.md#the-null-coalescing-operator) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="65556-118">言語仕様は、C# の構文と使用法に関する信頼性のある情報源です。</span><span class="sxs-lookup"><span data-stu-id="65556-118">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="65556-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="65556-119">See also</span></span>

- [<span data-ttu-id="65556-120">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="65556-120">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="65556-121">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="65556-121">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="65556-122">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="65556-122">C# operators</span></span>](index.md)
- [<span data-ttu-id="65556-123">Null 許容型</span><span class="sxs-lookup"><span data-stu-id="65556-123">Nullable Types</span></span>](../../programming-guide/nullable-types/index.md)
- [<span data-ttu-id="65556-124">'Lifted' の正確な意味</span><span class="sxs-lookup"><span data-stu-id="65556-124">What Exactly Does 'Lifted' mean?</span></span>](https://blogs.msdn.microsoft.com/ericlippert/2007/06/27/what-exactly-does-lifted-mean/)