---
title: Null 条件演算子 (Visual Basic)
ms.date: 10/19/2018
helpviewer_keywords:
- null-conditional operators [Visual Basic]
- ?. operator [Visual Basic]
- ?[] operator [C#]
- ?[] operator [Visual Basic]
ms.openlocfilehash: c29362a1e335e18b66821919e266b1ce57774692
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50195993"
---
# <a name="-and--null-conditional-operators-visual-basic"></a><span data-ttu-id="05b84-102">?.</span><span class="sxs-lookup"><span data-stu-id="05b84-102">?.</span></span> <span data-ttu-id="05b84-103">そして。() null 条件演算子 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="05b84-103">and ?() null-conditional operators (Visual Basic)</span></span>

<span data-ttu-id="05b84-104">Null の左側のオペランドの値をテスト (`Nothing`) メンバー アクセスを実行する前に (`?.`) またはインデックス (`?()`); の操作を返します。`Nothing`に左側のオペランドが評価された場合`Nothing`します。</span><span class="sxs-lookup"><span data-stu-id="05b84-104">Tests the value of the left-hand operand for null (`Nothing`) before performing a member access (`?.`) or index (`?()`) operation; returns `Nothing` if the left-hand operand evaluates to `Nothing`.</span></span> <span data-ttu-id="05b84-105">値の型を返すことが通常は、式の null 条件演算子を返すことに注意してください、<xref:System.Nullable%601>します。</span><span class="sxs-lookup"><span data-stu-id="05b84-105">Note that, in the expressions that would ordinarily return value types, the null-conditional operator returns a <xref:System.Nullable%601>.</span></span>

<span data-ttu-id="05b84-106">これらの演算子を使用して、データ構造を下って場合は特に、null のチェックを処理するには、少ないコードを記述するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="05b84-106">These operators help you write less code to handle null checks, especially when descending into data structures.</span></span> <span data-ttu-id="05b84-107">例えば:</span><span class="sxs-lookup"><span data-stu-id="05b84-107">For example:</span></span>

```vb
Dim length As Integer? = customers?.Length  ' Nothing if customers is Nothing  
Dim first As Customer = customers?(0)  ' Nothing if customers is Nothing  
Dim count As Integer? = customers?(0)?.Orders?.Count()  ' Nothing if customers, the first customer, or Orders is Nothing  
```

<span data-ttu-id="05b84-108">比較については、null 条件演算子を使用せず、これらの式の最初の代替のコードは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="05b84-108">For comparison, the alternative code for the first of these expressions without a null-conditional operator is:</span></span>

```vb
Dim length As Integer
If customers IsNot Nothing Then
   length = customers.Length
End If
```

<span data-ttu-id="05b84-109">Null 条件演算子はショートサーキットです。</span><span class="sxs-lookup"><span data-stu-id="05b84-109">The null-conditional operators are short-circuiting.</span></span>  <span data-ttu-id="05b84-110">条件付きメンバー アクセスおよびインデックス操作のチェーン内の 1 つの操作は、何も返された場合、チェーンの実行の残りの部分を停止します。</span><span class="sxs-lookup"><span data-stu-id="05b84-110">If one operation in a chain of conditional member access and index operations returns Nothing, the rest of the chain’s execution stops.</span></span>  <span data-ttu-id="05b84-111">C(E) は次の例の場合は評価されません`A`、 `B`、または`C`Nothing に評価されます。</span><span class="sxs-lookup"><span data-stu-id="05b84-111">In the following example, C(E) isn't evaluated if `A`, `B`, or `C` evaluates to Nothing.</span></span>

```vb
A?.B?.C?(E);
```

<span data-ttu-id="05b84-112">Null 条件メンバー アクセスの別の用途では、はるかに少ないコードでスレッド セーフな方法でデリゲートを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="05b84-112">Another use for null-conditional member access is to invoke delegates in a thread-safe way with much less code.</span></span>  <span data-ttu-id="05b84-113">従来の方法には、次のようなコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="05b84-113">The old way requires code like the following:</span></span>  

```vb  
Dim handler = AddressOf(Me.PropertyChanged)  
If handler IsNot Nothing  
    Call handler(…)  
```

<span data-ttu-id="05b84-114">新しい方法は格段に単純です。</span><span class="sxs-lookup"><span data-stu-id="05b84-114">The new way is much simpler:</span></span>  

```vb
PropertyChanged?.Invoke(…)
```

<span data-ttu-id="05b84-115">コンパイラが `PropertyChanged` を評価するためのコードを一度しか生成せず、一時変数に結果が保持されるため、新しい方法はスレッド セーフです。</span><span class="sxs-lookup"><span data-stu-id="05b84-115">The new way is thread-safe because the compiler generates code to evaluate `PropertyChanged` one time only, keeping the result in a temporary variable.</span></span> <span data-ttu-id="05b84-116">null 条件デリゲート呼び出し構文 `PropertyChanged?(e)` がないため、`Invoke` メソッドを明示的に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="05b84-116">You need to explicitly call the `Invoke` method because there is no null-conditional delegate invocation syntax `PropertyChanged?(e)`.</span></span>  

## <a name="see-also"></a><span data-ttu-id="05b84-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="05b84-117">See also</span></span>

- [<span data-ttu-id="05b84-118">演算子 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="05b84-118">Operators (Visual Basic)</span></span>](index.md)
- [<span data-ttu-id="05b84-119">Visual Basic プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="05b84-119">Visual Basic Programming Guide</span></span>](../../../visual-basic/programming-guide/index.md)
- [<span data-ttu-id="05b84-120">Visual Basic の言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="05b84-120">Visual Basic Language Reference</span></span>](../../../visual-basic/language-reference/index.md)  
