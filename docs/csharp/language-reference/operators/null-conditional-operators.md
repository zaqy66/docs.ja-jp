---
title: Null 条件演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 04/03/2015
helpviewer_keywords:
- null-conditional operators [C#]
- ?. operator [C#]
- ?[] operator [C#]
ms.assetid: 9c7b2c8f-a785-44ca-836c-407bfb6d27f5
ms.openlocfilehash: 38298cded904cbfedeaf3c6b66c74d610d714902
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333240"
---
# <a name="-and--null-conditional-operators-c-and-visual-basic"></a><span data-ttu-id="c087f-102">?.</span><span class="sxs-lookup"><span data-stu-id="c087f-102">?.</span></span> <span data-ttu-id="c087f-103">および ?[] Null 条件演算子 (C# および Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c087f-103">and ?[] null-conditional operators (C# and Visual Basic)</span></span>

<span data-ttu-id="c087f-104">メンバー アクセス (`?.`) またはインデックス (`?[]`) 操作を実行する前に、左の演算子の値を null に対してテストします。左側のオペランドが `null` に評価される場合、`null` が返されます。</span><span class="sxs-lookup"><span data-stu-id="c087f-104">Tests the value of the left-hand operand for null before performing a member access (`?.`) or index (`?[]`) operation; returns `null` if the left-hand operand evaluates to `null`.</span></span>

<span data-ttu-id="c087f-105">これらの演算子を使用すると、null チェックの処理のために記述するコードを少なくすることができます (特に、データ構造を下っていく場合)。</span><span class="sxs-lookup"><span data-stu-id="c087f-105">These operators help you write less code to handle null checks, especially for descending into data structures.</span></span>

```csharp
int? length = customers?.Length; // null if customers is null
Customer first = customers?[0];  // null if customers is null
int? count = customers?[0]?.Orders?.Count();  // null if customers, the first customer, or Orders is null
```

<span data-ttu-id="c087f-106">Null 条件演算子はショートサーキットです。</span><span class="sxs-lookup"><span data-stu-id="c087f-106">The null-conditional operators are short-circuiting.</span></span>  <span data-ttu-id="c087f-107">条件付きのメンバー アクセスやインデックス操作のチェーンの 1 つの演算が null を返す場合、チェーンの実行の残りの部分は停止します。</span><span class="sxs-lookup"><span data-stu-id="c087f-107">If one operation in a chain of conditional member access and index operations returns null, the rest of the chain’s execution stops.</span></span>  <span data-ttu-id="c087f-108">次の例では、`A`、`B`、または `C` が null と評価された場合、`E` は実行されません。</span><span class="sxs-lookup"><span data-stu-id="c087f-108">In the following example, `E` doesn't execute if `A`, `B`, or `C` evaluates to null.</span></span>

```csharp
A?.B?.C?.Do(E);
A?.B?.C?[E];
```

<span data-ttu-id="c087f-109">null 条件メンバー アクセスの別の用途は、はるかに少ないコードのスレッド セーフな方法でデリゲートを呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="c087f-109">Another use for the null-conditional member access is invoking delegates in a thread-safe way with much less code.</span></span>  <span data-ttu-id="c087f-110">従来の方法には、次のようなコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="c087f-110">The old way requires code like the following:</span></span>

```csharp
var handler = this.PropertyChanged;
if (handler != null)
    handler(…);
```

<span data-ttu-id="c087f-111">新しい方法は格段に単純です。</span><span class="sxs-lookup"><span data-stu-id="c087f-111">The new way is much simpler:</span></span>

```csharp
PropertyChanged?.Invoke(…)
```

<span data-ttu-id="c087f-112">コンパイラが `PropertyChanged` を評価するためのコードを一度しか生成せず、一時変数に結果が保持されるため、新しい方法はスレッド セーフです。</span><span class="sxs-lookup"><span data-stu-id="c087f-112">The new way is thread-safe because the compiler generates code to evaluate `PropertyChanged` one time only, keeping the result in a temporary variable.</span></span> <span data-ttu-id="c087f-113">null 条件デリゲート呼び出し構文 `PropertyChanged?(e)` がないため、`Invoke` メソッドを明示的に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c087f-113">You need to explicitly call the `Invoke` method because there is no null-conditional delegate invocation syntax `PropertyChanged?(e)`.</span></span>

## <a name="language-specifications"></a><span data-ttu-id="c087f-114">言語仕様</span><span class="sxs-lookup"><span data-stu-id="c087f-114">Language specifications</span></span>

<span data-ttu-id="c087f-115">詳細については、「[C# 言語仕様](../language-specification/index.md)」の「[Null 条件演算子](~/_csharplang/spec/expressions.md#null-conditional-operator)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="c087f-115">For more information, see [Null-conditional operator](~/_csharplang/spec/expressions.md#null-conditional-operator) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="c087f-116">言語仕様は、C# の構文と使用法に関する信頼性のある情報源です。</span><span class="sxs-lookup"><span data-stu-id="c087f-116">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="c087f-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="c087f-117">See also</span></span>

- [<span data-ttu-id="c087f-118">?? (Null 合体演算子)</span><span class="sxs-lookup"><span data-stu-id="c087f-118">?? (null-coalescing operator)</span></span>](null-coalescing-operator.md)
- [<span data-ttu-id="c087f-119">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="c087f-119">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="c087f-120">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="c087f-120">C# Programming Guide</span></span>](../../programming-guide/index.md)