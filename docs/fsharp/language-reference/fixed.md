---
title: Fixed キーワード (f#)
description: F# を使用して、コレクションを回避するには、スタックにローカルがキーワードを 'fixed' することができます 'pin' 方法について説明します。
ms.date: 04/24/2017
ms.openlocfilehash: 1bf1b2ad67d2dd7f854e569cfca7c06e8aec7f4c
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44201414"
---
# <a name="the-fixed-keyword"></a><span data-ttu-id="44283-103">固定キーワード</span><span class="sxs-lookup"><span data-stu-id="44283-103">The Fixed Keyword</span></span>

<span data-ttu-id="44283-104">F# 4.1 が導入されています、`fixed`キーワードで、収集またはガベージ コレクション中に移動されないようにするには、スタックにローカルを「ピン留め」することができます。</span><span class="sxs-lookup"><span data-stu-id="44283-104">F# 4.1 introduces the `fixed` keyword, which allows you to "pin" a local onto the stack to prevent it from being collected or moved during garbage-collection.</span></span>  <span data-ttu-id="44283-105">低レベルのプログラミング シナリオに使用されます。</span><span class="sxs-lookup"><span data-stu-id="44283-105">It is used for low-level programming scenarios.</span></span>

## <a name="syntax"></a><span data-ttu-id="44283-106">構文</span><span class="sxs-lookup"><span data-stu-id="44283-106">Syntax</span></span>

```fsharp
use ptr = fixed expression
```

## <a name="remarks"></a><span data-ttu-id="44283-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="44283-107">Remarks</span></span>

<span data-ttu-id="44283-108">これは、ポインターを抽出し、収集されたり、ガベージ コレクション中に移動できない名前にバインドすることを許可する式の構文を拡張します。</span><span class="sxs-lookup"><span data-stu-id="44283-108">This extends the syntax of expressions to allow extracting a pointer and binding it to a name which is prevented from being collected or moved during garbage-collection.</span></span>  

<span data-ttu-id="44283-109">使用して式からのポインターが固定されて、`fixed`キーワードは、識別子を使用してにバインドされて、`use`キーワード。</span><span class="sxs-lookup"><span data-stu-id="44283-109">A pointer from an expression is fixed via the `fixed` keyword is bound to an identifier via the `use` keyword.</span></span>  <span data-ttu-id="44283-110">これのセマンティクスを使用したリソース管理に似ています、`use`キーワード。</span><span class="sxs-lookup"><span data-stu-id="44283-110">The semantics of this are similar to resource management via the `use` keyword.</span></span>  <span data-ttu-id="44283-111">ポインターは、スコープ内にあるし、修正が不要になったスコープ外に出ることが、中に固定されています。</span><span class="sxs-lookup"><span data-stu-id="44283-111">The pointer is fixed while it is in scope, and once it is out of scope, it is no longer fixed.</span></span>  <span data-ttu-id="44283-112">`fixed` コンテキストの外部で使用することはできません、`use`バインドします。</span><span class="sxs-lookup"><span data-stu-id="44283-112">`fixed` cannot be used outside the context of a `use` binding.</span></span>  <span data-ttu-id="44283-113">名前に、ポインターをバインドする必要があります`use`します。</span><span class="sxs-lookup"><span data-stu-id="44283-113">You must bind the pointer to a name with `use`.</span></span>

<span data-ttu-id="44283-114">使用`fixed`関数またはメソッドの式内で発生する必要があります。</span><span class="sxs-lookup"><span data-stu-id="44283-114">Use of `fixed` must occur within an expression in a function or a method.</span></span>  <span data-ttu-id="44283-115">これは、スクリプト レベルまたはモジュール レベルのスコープで使用できません。</span><span class="sxs-lookup"><span data-stu-id="44283-115">It cannot be used at a script-level or module-level scope.</span></span>

<span data-ttu-id="44283-116">ポインターのすべてのコードのようにこれは安全でない機能で、使用時に警告が生成されます。</span><span class="sxs-lookup"><span data-stu-id="44283-116">Like all pointer code, this is an unsafe feature and will emit a warning when used.</span></span>

## <a name="example"></a><span data-ttu-id="44283-117">例</span><span class="sxs-lookup"><span data-stu-id="44283-117">Example</span></span>

```fsharp
open Microsoft.FSharp.NativeInterop

type Point = { mutable X: int; mutable Y: int}

let squareWithPointer (p: nativeptr<int>) =
    // Dereference the pointer at the 0th address.
    let mutable value = NativePtr.get p 0

    // Perform some work
    value <- value * value

    // Set the value in the pointer at the 0th address.
    NativePtr.set p 0 value

let pnt = { X = 1; Y = 2 }
printfn "pnt before - X: %d Y: %d" pnt.X pnt.Y // prints 1 and 2

// Note that the use of 'fixed' is inside a function.
// You cannot fix a pointer at a script-level or module-level scope.
let doPointerWork() =
    use ptr = fixed &pnt.Y

    // Square the Y value
    squareWithPointer ptr
    printfn "pnt after - X: %d Y: %d" pnt.X pnt.Y // prints 1 and 4

doPointerWork()
```

## <a name="see-also"></a><span data-ttu-id="44283-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="44283-118">See also</span></span>

- [<span data-ttu-id="44283-119">NativePtr モジュール</span><span class="sxs-lookup"><span data-stu-id="44283-119">NativePtr Module</span></span>](https://msdn.microsoft.com/visualfsharpdocs/conceptual/nativeinterop.nativeptr-module-%5Bfsharp%5D)
