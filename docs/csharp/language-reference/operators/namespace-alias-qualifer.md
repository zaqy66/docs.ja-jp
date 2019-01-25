---
title: ':: 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ::_CSharpKeyword
helpviewer_keywords:
- ':: operator [C#]'
- 'namespaces [C#], :: operator'
- namespace alias qualifier operator (::) [C#]
ms.assetid: 698b5a73-85cf-4e0e-9e8e-6496887f8527
ms.openlocfilehash: 2618131f27271e7c06cb6d425fc22b5bd9750c49
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333318"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="6f4ac-102">:: 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="6f4ac-102">:: operator (C# Reference)</span></span>

<span data-ttu-id="6f4ac-103">名前空間エイリアス修飾子 (`::`) を使用して識別子を検索できます。</span><span class="sxs-lookup"><span data-stu-id="6f4ac-103">The namespace alias qualifier (`::`) is used to look up identifiers.</span></span> <span data-ttu-id="6f4ac-104">この例に示すように、常に 2 つの識別子の間に配置します。</span><span class="sxs-lookup"><span data-stu-id="6f4ac-104">It is always positioned between two identifiers, as in this example:</span></span>

[!code-csharp[csRefOperators#27](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#27)]

<span data-ttu-id="6f4ac-105">`::` 演算子は、"*using 別名ディレクティブ*" と一緒に使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="6f4ac-105">The `::` operator can also be used with a *using alias directive*:</span></span>

```csharp
// using Col=System.Collections.Generic;
var numbers = new Col::List<int> { 1, 2, 3 };
```

## <a name="remarks"></a><span data-ttu-id="6f4ac-106">コメント</span><span class="sxs-lookup"><span data-stu-id="6f4ac-106">Remarks</span></span>

<span data-ttu-id="6f4ac-107">名前空間エイリアス修飾子として `global` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6f4ac-107">The namespace alias qualifier can be `global`.</span></span> <span data-ttu-id="6f4ac-108">これにより、エイリアスを使用した名前空間ではなく、グローバル名前空間で検索が実行されます。</span><span class="sxs-lookup"><span data-stu-id="6f4ac-108">This invokes a lookup in the global namespace, rather than an aliased namespace.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="6f4ac-109">詳細情報</span><span class="sxs-lookup"><span data-stu-id="6f4ac-109">For more information</span></span>

<span data-ttu-id="6f4ac-110">`::` 演算子の使用例については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f4ac-110">For an example of how to use the `::` operator, see the following section:</span></span>

- [<span data-ttu-id="6f4ac-111">方法: グローバル名前空間エイリアスを使用する</span><span class="sxs-lookup"><span data-stu-id="6f4ac-111">How to: Use the Global Namespace Alias</span></span>](../../programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)

## <a name="c-language-specification"></a><span data-ttu-id="6f4ac-112">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="6f4ac-112">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="6f4ac-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f4ac-113">See also</span></span>

- [<span data-ttu-id="6f4ac-114">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="6f4ac-114">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="6f4ac-115">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="6f4ac-115">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="6f4ac-116">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="6f4ac-116">C# operators</span></span>](index.md)
- [<span data-ttu-id="6f4ac-117">名前空間キーワード</span><span class="sxs-lookup"><span data-stu-id="6f4ac-117">Namespace Keywords</span></span>](../keywords/namespace-keywords.md)
- [<span data-ttu-id="6f4ac-118">演算子 .</span><span class="sxs-lookup"><span data-stu-id="6f4ac-118">. operator</span></span>](member-access-operator.md)
- [<span data-ttu-id="6f4ac-119">extern エイリアス</span><span class="sxs-lookup"><span data-stu-id="6f4ac-119">extern alias</span></span>](../keywords/extern-alias.md)