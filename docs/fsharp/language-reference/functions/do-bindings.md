---
title: do バインド (F#)
description: F# の 'do' のバインドを使用する方法、関数または値を定義することがなくコードを実行について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: 78dbf8da0fe40b5af566ad98693df1109eede7e4
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "45973145"
---
# <a name="do-bindings"></a><span data-ttu-id="cf34d-103">do バインド</span><span class="sxs-lookup"><span data-stu-id="cf34d-103">do Bindings</span></span>

<span data-ttu-id="cf34d-104">A`do`関数または値を定義することがなくコードを実行するバインディングを使用します。</span><span class="sxs-lookup"><span data-stu-id="cf34d-104">A `do` binding is used to execute code without defining a function or value.</span></span> <span data-ttu-id="cf34d-105">またはバインドできるクラスを使用してを参照してください[`do`クラス内のバインディング](../members/do-bindings-in-classes.md)します。</span><span class="sxs-lookup"><span data-stu-id="cf34d-105">Also, do bindings can be used in classes, see [`do` Bindings in Classes](../members/do-bindings-in-classes.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf34d-106">構文</span><span class="sxs-lookup"><span data-stu-id="cf34d-106">Syntax</span></span>

```fsharp
[ attributes ]
[ do ]expression
```

## <a name="remarks"></a><span data-ttu-id="cf34d-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="cf34d-107">Remarks</span></span>

<span data-ttu-id="cf34d-108">使用して、`do`関数または値の定義とは別にコードを実行するときにバインディングします。</span><span class="sxs-lookup"><span data-stu-id="cf34d-108">Use a `do` binding when you want to execute code independently of a function or value definition.</span></span> <span data-ttu-id="cf34d-109">内の式を`do`バインディングを返す必要があります`unit`します。</span><span class="sxs-lookup"><span data-stu-id="cf34d-109">The expression in a `do` binding must return `unit`.</span></span> <span data-ttu-id="cf34d-110">最上位のコード`do`モジュールの初期化時にバインディングを実行します。</span><span class="sxs-lookup"><span data-stu-id="cf34d-110">Code in a top-level `do` binding is executed when the module is initialized.</span></span> <span data-ttu-id="cf34d-111">キーワード`do`は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="cf34d-111">The keyword `do` is optional.</span></span>

<span data-ttu-id="cf34d-112">属性は、最上位レベルに適用できる`do`バインドします。</span><span class="sxs-lookup"><span data-stu-id="cf34d-112">Attributes can be applied to a top-level `do` binding.</span></span> <span data-ttu-id="cf34d-113">たとえば、プログラムでは、COM 相互運用機能を使用する場合があります適用する、`STAThread`属性をプログラムします。</span><span class="sxs-lookup"><span data-stu-id="cf34d-113">For example, if your program uses COM interop, you might want to apply the `STAThread` attribute to your program.</span></span> <span data-ttu-id="cf34d-114">属性を使用してこれを行う、`do`バインド、次のコードに示すようにします。</span><span class="sxs-lookup"><span data-stu-id="cf34d-114">You can do this by using an attribute on a `do` binding, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet201.fs)]

## <a name="see-also"></a><span data-ttu-id="cf34d-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf34d-115">See also</span></span>

- [<span data-ttu-id="cf34d-116">F# 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="cf34d-116">F# Language Reference</span></span>](../index.md)
- [<span data-ttu-id="cf34d-117">関数</span><span class="sxs-lookup"><span data-stu-id="cf34d-117">Functions</span></span>](index.md)
