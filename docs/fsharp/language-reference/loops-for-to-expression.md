---
title: 'ループ: for...to 式 (F#)'
description: 参照してください方法 f# for….. ループ変数の値の範囲をループで反復処理する式に使用されます。
ms.date: 05/16/2016
ms.openlocfilehash: 8160fd30c4f3afe8bb6b58f468802ef1c0ef32ee
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "43800470"
---
# <a name="loops-forto-expression"></a><span data-ttu-id="57df6-103">ループ: for...to 式</span><span class="sxs-lookup"><span data-stu-id="57df6-103">Loops: for...to Expression</span></span>

<span data-ttu-id="57df6-104">`for...to`ループ変数の値の範囲をループで反復処理する式を使用します。</span><span class="sxs-lookup"><span data-stu-id="57df6-104">The `for...to` expression is used to iterate in a loop over a range of values of a loop variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="57df6-105">構文</span><span class="sxs-lookup"><span data-stu-id="57df6-105">Syntax</span></span>

```fsharp
for identifier = start [ to | downto ] finish do
    body-expression
```

## <a name="remarks"></a><span data-ttu-id="57df6-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="57df6-106">Remarks</span></span>

<span data-ttu-id="57df6-107">識別子の型の型から推論されます、*開始*と*完了*式。</span><span class="sxs-lookup"><span data-stu-id="57df6-107">The type of the identifier is inferred from the type of the *start* and *finish* expressions.</span></span> <span data-ttu-id="57df6-108">これらの式の型は、32 ビット整数である必要があります。</span><span class="sxs-lookup"><span data-stu-id="57df6-108">Types for these expressions must be 32-bit integers.</span></span>

<span data-ttu-id="57df6-109">式では技術的には、`for...to`は命令型プログラミング言語では、従来のステートメントのようにします。</span><span class="sxs-lookup"><span data-stu-id="57df6-109">Although technically an expression, `for...to` is more like a traditional statement in an imperative programming language.</span></span> <span data-ttu-id="57df6-110">戻り値の型、*式の本体*あります`unit`します。</span><span class="sxs-lookup"><span data-stu-id="57df6-110">The return type for the *body-expression* must be `unit`.</span></span> <span data-ttu-id="57df6-111">次の例では、さまざまな使用、`for...to`式。</span><span class="sxs-lookup"><span data-stu-id="57df6-111">The following examples show various uses of the `for...to` expression.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5101.fs)]

<span data-ttu-id="57df6-112">このコードの出力は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="57df6-112">The output of the previous code is as follows.</span></span>

```
1 2 3 4 5 6 7 8 9 10
10 9 8 7 6 5 4 3 2 1
2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18
```

## <a name="see-also"></a><span data-ttu-id="57df6-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="57df6-113">See also</span></span>

- [<span data-ttu-id="57df6-114">F# 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="57df6-114">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="57df6-115">ループ: `for...in` 式</span><span class="sxs-lookup"><span data-stu-id="57df6-115">Loops: `for...in` Expression</span></span>](loops-for-in-expression.md)
- [<span data-ttu-id="57df6-116">ループ: `while...do` 式</span><span class="sxs-lookup"><span data-stu-id="57df6-116">Loops: `while...do` Expression</span></span>](loops-while-do-expression.md)
