---
title: . 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ._CSharpKeyword
helpviewer_keywords:
- member access operator (.) [C#]
- . operator [C#]
- dot operator (.) [C#]
ms.assetid: a1f54b52-b686-4ae5-a48e-a2a9ebd0eb7b
ms.openlocfilehash: a59f69d0349a054c8c2a5b701b8f63df113a6580
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333721"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="ef4f2-103">.</span><span class="sxs-lookup"><span data-stu-id="ef4f2-103">.</span></span> <span data-ttu-id="ef4f2-104">演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="ef4f2-104">operator (C# Reference)</span></span>

<span data-ttu-id="ef4f2-105">ドット演算子 (`.`) は、メンバー アクセスに使用されます。</span><span class="sxs-lookup"><span data-stu-id="ef4f2-105">The dot operator (`.`) is used for member access.</span></span> <span data-ttu-id="ef4f2-106">ドット演算子は、型または名前空間のメンバーを指定します。</span><span class="sxs-lookup"><span data-stu-id="ef4f2-106">The dot operator specifies a member of a type or namespace.</span></span> <span data-ttu-id="ef4f2-107">たとえば、ドット演算子は、.NET Framework クラス ライブラリ内の特定のメソッドにアクセスするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ef4f2-107">For example, the dot operator is used to access specific methods within the .NET Framework class libraries:</span></span>

[!code-csharp[csRefOperators#16](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#16)]

<span data-ttu-id="ef4f2-108">たとえば、次のクラスを考えてみます。</span><span class="sxs-lookup"><span data-stu-id="ef4f2-108">For example, consider the following class:</span></span>

[!code-csharp[csRefOperators#17](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#17)]

[!code-csharp[csRefOperators#18](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#18)]

<span data-ttu-id="ef4f2-109">`s` 変数には 2 つのメンバー (`a` と `b`) があり、それらにアクセスするために、ドット演算子を使用します。</span><span class="sxs-lookup"><span data-stu-id="ef4f2-109">The variable `s` has two members, `a` and `b`; to access them, use the dot operator:</span></span>

[!code-csharp[csRefOperators#19](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#19)]

<span data-ttu-id="ef4f2-110">ドットは、修飾名を形成するためにも使用されます。この修飾名は、たとえば、属している名前空間やインターフェイスを指定する名前です。</span><span class="sxs-lookup"><span data-stu-id="ef4f2-110">The dot is also used to form qualified names, which are names that specify the namespace or interface, for example, to which they belong.</span></span>

[!code-csharp[csRefOperators#20](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#20)]

<span data-ttu-id="ef4f2-111">using ディレクティブを使用すると、名前の修飾をオプションにすることができます。</span><span class="sxs-lookup"><span data-stu-id="ef4f2-111">The using directive makes some name qualification optional:</span></span>

[!code-csharp[csRefOperators#21](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#21)]

<span data-ttu-id="ef4f2-112">ただし、識別子があいまいな場合は、修飾する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef4f2-112">But when an identifier is ambiguous, it must be qualified:</span></span>

[!code-csharp[csRefOperators#22](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#22)]

## <a name="c-language-specification"></a><span data-ttu-id="ef4f2-113">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="ef4f2-113">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="ef4f2-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="ef4f2-114">See also</span></span>

- [<span data-ttu-id="ef4f2-115">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="ef4f2-115">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="ef4f2-116">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="ef4f2-116">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="ef4f2-117">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="ef4f2-117">C# Operators</span></span>](index.md)