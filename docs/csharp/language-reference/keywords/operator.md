---
title: operator キーワード (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- operator_CSharpKeyword
- operator
helpviewer_keywords:
- operator keyword [C#]
ms.assetid: 59218cce-e90e-42f6-a6bb-30300981b86a
ms.openlocfilehash: c3bfada235993670bf158fe9803a09707b2b3251
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42929873"
---
# <a name="operator-c-reference"></a><span data-ttu-id="a8494-102">operator (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="a8494-102">operator (C# Reference)</span></span>

<span data-ttu-id="a8494-103">`operator` キーワードを使用して、組み込みの演算子をオーバーロードしたり、クラスまたは構造体宣言内でユーザー定義の変換を行ったりすることができます。</span><span class="sxs-lookup"><span data-stu-id="a8494-103">Use the `operator` keyword to overload a built-in operator or to provide a user-defined conversion in a class or struct declaration.</span></span>

## <a name="example"></a><span data-ttu-id="a8494-104">例</span><span class="sxs-lookup"><span data-stu-id="a8494-104">Example</span></span>

<span data-ttu-id="a8494-105">小数を処理する非常に簡単なクラスを次に示します。</span><span class="sxs-lookup"><span data-stu-id="a8494-105">The following is a very simplified class for fractional numbers.</span></span> <span data-ttu-id="a8494-106">このクラスは、小数の加算および乗算を実行するために `+` 演算子および `*` 演算子をオーバーロードします。また、`Fraction` 型を `double` 型に変換する変換演算子も提供します。</span><span class="sxs-lookup"><span data-stu-id="a8494-106">It overloads the `+` and `*` operators to perform fractional addition and multiplication, and also provides a conversion operator that converts a `Fraction` type to a `double` type.</span></span>

[!code-csharp[csrefKeywordsConversion#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsConversion/CS/csrefKeywordsConversion.cs#6)]

## <a name="c-language-specification"></a><span data-ttu-id="a8494-107">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="a8494-107">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="a8494-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8494-108">See also</span></span>

- [<span data-ttu-id="a8494-109">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="a8494-109">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="a8494-110">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="a8494-110">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="a8494-111">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="a8494-111">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="a8494-112">implicit</span><span class="sxs-lookup"><span data-stu-id="a8494-112">implicit</span></span>](implicit.md)
- [<span data-ttu-id="a8494-113">explicit</span><span class="sxs-lookup"><span data-stu-id="a8494-113">explicit</span></span>](explicit.md)
- [<span data-ttu-id="a8494-114">方法: 構造体間にユーザー定義の変換を実装する</span><span class="sxs-lookup"><span data-stu-id="a8494-114">How to: Implement User-Defined Conversions Between Structs</span></span>](../../programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)
