---
title: '* 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 04/04/2018
f1_keywords:
- '*_CSharpKeyword'
helpviewer_keywords:
- multiplication operator (*) [C#]
- '* operator [C#]'
ms.assetid: abd9a5f0-9b24-431e-971a-09ee1c45c50e
ms.openlocfilehash: f4490c4632d9344eb879ea55c20787b838781d91
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333734"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="38bdd-102">\* 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="38bdd-102">\* operator (C# Reference)</span></span>

<span data-ttu-id="38bdd-103">乗算演算子 (`*`) は、そのオペランドの積を計算します。</span><span class="sxs-lookup"><span data-stu-id="38bdd-103">The multiplication operator (`*`) computes the product of its operands.</span></span> <span data-ttu-id="38bdd-104">すべての数値型には定義済みの乗算演算子があります。</span><span class="sxs-lookup"><span data-stu-id="38bdd-104">All numeric types have predefined multiplication operators.</span></span>

<span data-ttu-id="38bdd-105">また、`*` はポインターへの読み書きを可能にする逆参照演算子としても機能します。</span><span class="sxs-lookup"><span data-stu-id="38bdd-105">`*` also serves as the dereference operator, which allows reading and writing to a pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="38bdd-106">コメント</span><span class="sxs-lookup"><span data-stu-id="38bdd-106">Remarks</span></span>

<span data-ttu-id="38bdd-107">`*` 演算子は、ポインターの種類の宣言、およびポインターの逆参照にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="38bdd-107">The `*` operator is also used to declare pointer types and to dereference pointers.</span></span> <span data-ttu-id="38bdd-108">この演算子は、[unsafe](../keywords/unsafe.md) キーワードの使用によって示され、[/unsafe](../compiler-options/unsafe-compiler-option.md) コンパイラ オプションを必要とする、unsafe コンテキストでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="38bdd-108">This operator can only be used in unsafe contexts, denoted by the use of the [unsafe](../keywords/unsafe.md) keyword, and requiring the [/unsafe](../compiler-options/unsafe-compiler-option.md) compiler option.</span></span>  <span data-ttu-id="38bdd-109">逆参照演算子は、間接演算子とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="38bdd-109">The dereference operator is also known as the indirection operator.</span></span>

<span data-ttu-id="38bdd-110">ユーザー定義型は二項 `*` 演算子をオーバーロードできます (「[演算子](../keywords/operator.md)」を参照)。</span><span class="sxs-lookup"><span data-stu-id="38bdd-110">User-defined types can overload the binary `*` operator (see [operator](../keywords/operator.md)).</span></span> <span data-ttu-id="38bdd-111">二項演算子をオーバーロードすると、対応する代入演算子がある場合、これも暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="38bdd-111">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>

## <a name="example"></a><span data-ttu-id="38bdd-112">例</span><span class="sxs-lookup"><span data-stu-id="38bdd-112">Example</span></span>

[!code-csharp-interactive[csRefOperators#50](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#50)]

## <a name="example"></a><span data-ttu-id="38bdd-113">例</span><span class="sxs-lookup"><span data-stu-id="38bdd-113">Example</span></span>

[!code-csharp[csRefOperators#51](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#51)]

## <a name="see-also"></a><span data-ttu-id="38bdd-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="38bdd-114">See also</span></span>

- [<span data-ttu-id="38bdd-115">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="38bdd-115">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="38bdd-116">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="38bdd-116">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="38bdd-117">アンセーフ コードとポインター</span><span class="sxs-lookup"><span data-stu-id="38bdd-117">Unsafe Code and Pointers</span></span>](../../programming-guide/unsafe-code-pointers/index.md)
- [<span data-ttu-id="38bdd-118">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="38bdd-118">C# Operators</span></span>](index.md)