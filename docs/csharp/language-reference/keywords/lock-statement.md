---
title: lock ステートメント (C# リファレンス)
description: C# lock ステートメントを使用し、共有リソースへのスレッド アクセスを同期します
ms.date: 08/28/2018
f1_keywords:
- lock_CSharpKeyword
- lock
helpviewer_keywords:
- lock keyword [C#]
ms.assetid: 656da1a4-707e-4ef6-9c6e-6d13b646af42
ms.openlocfilehash: 2b6fbfb2f81d7745c4effb9ea0087f34cc872a6c
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43858357"
---
# <a name="lock-statement-c-reference"></a><span data-ttu-id="681d6-103">lock ステートメント (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="681d6-103">lock statement (C# Reference)</span></span>

<span data-ttu-id="681d6-104">`lock` ステートメントは、指定のオブジェクトに対する相互排他ロックを取得し、ステートメント ブロックを実行してからロックを解放します。</span><span class="sxs-lookup"><span data-stu-id="681d6-104">The `lock` statement obtains the mutual-exclusion lock for a given object, executes a statement block, and then releases the lock.</span></span> <span data-ttu-id="681d6-105">ロックが保持されている間、ロックを保持するスレッドはロックを再度取得し、解放できます。</span><span class="sxs-lookup"><span data-stu-id="681d6-105">While a lock is held, the thread that holds the lock can again obtain and release the lock.</span></span> <span data-ttu-id="681d6-106">他のスレッドはブロックされてロックを取得できず、ロックが解放されるまで待機します。</span><span class="sxs-lookup"><span data-stu-id="681d6-106">Any other thread is blocked from obtaining the lock and waits until the lock is released.</span></span>

<span data-ttu-id="681d6-107">`lock` ステートメントの形式は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="681d6-107">The `lock` statement is of the form</span></span>

```csharp
lock (x)
{
    // Your code...
}
```

<span data-ttu-id="681d6-108">`x` は[参照型](reference-types.md)の式です。</span><span class="sxs-lookup"><span data-stu-id="681d6-108">where `x` is an expression of a [reference type](reference-types.md).</span></span> <span data-ttu-id="681d6-109">これは次にまったく等しくなります。</span><span class="sxs-lookup"><span data-stu-id="681d6-109">It's precisely equivalent to</span></span>

```csharp
object __lockObj = x;
bool __lockWasTaken = false;
try
{
    System.Threading.Monitor.Enter(__lockObj, ref __lockWasTaken);
    // Your code...
}
finally
{
    if (__lockWasTaken) System.Threading.Monitor.Exit(__lockObj);
}
```

<span data-ttu-id="681d6-110">このコードでは [try...finally](try-finally.md) ブロックが使用されているため、`lock` ステートメントの本文内で例外がスローされた場合でもロックは解放されます。</span><span class="sxs-lookup"><span data-stu-id="681d6-110">Since the code uses a [try...finally](try-finally.md) block, the lock is released even if an exception is thrown within the body of a `lock` statement.</span></span>

<span data-ttu-id="681d6-111">`lock` ステートメントの本体で [await](await.md) キーワードを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="681d6-111">You can't use the [await](await.md) keyword in the body of a `lock` statement.</span></span>

## <a name="remarks"></a><span data-ttu-id="681d6-112">コメント</span><span class="sxs-lookup"><span data-stu-id="681d6-112">Remarks</span></span>

<span data-ttu-id="681d6-113">共有リソースへのスレッド アクセスを同期する場合、専用オブジェクト インスタンス (`private readonly object balanceLock = new object();` など) またはコードの関連のない部分によってロック オブジェクトとして使用される可能性がない別のインスタンスをロックします。</span><span class="sxs-lookup"><span data-stu-id="681d6-113">When you synchronize thread access to shared resource, lock on a dedicated object instance (for example, `private readonly object balanceLock = new object();`) or another instance that is unlikely to be used as a lock object by unrelated parts of the code.</span></span> <span data-ttu-id="681d6-114">異なる共有リソースに対して同じロック オブジェクト インスタンスを使用することは避けてください。デッドロックやロックの競合が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="681d6-114">Avoid using the same lock object instance for different shared resources, as it might result in deadlock or lock contention.</span></span> <span data-ttu-id="681d6-115">特に以下の使用は避けてください。</span><span class="sxs-lookup"><span data-stu-id="681d6-115">In particular, avoid using</span></span>

- <span data-ttu-id="681d6-116">`this` (ロックとして呼び出し元に使用される可能性があります)。</span><span class="sxs-lookup"><span data-stu-id="681d6-116">`this` (might be used by the callers as a lock),</span></span>
- <span data-ttu-id="681d6-117"><xref:System.Type> インスタンス ([typeof](typeof.md) 演算子またはリフレクションによって取得される可能性があります)。</span><span class="sxs-lookup"><span data-stu-id="681d6-117"><xref:System.Type> instances (might be obtained by the [typeof](typeof.md) operator or reflection),</span></span>
- <span data-ttu-id="681d6-118">ロック オブジェクトとしての</span><span class="sxs-lookup"><span data-stu-id="681d6-118">string instances, including string literals,</span></span>

<span data-ttu-id="681d6-119">文字列インスタンス (文字列リテラルなど)。</span><span class="sxs-lookup"><span data-stu-id="681d6-119">as lock objects.</span></span>

## <a name="example"></a><span data-ttu-id="681d6-120">例</span><span class="sxs-lookup"><span data-stu-id="681d6-120">Example</span></span>

<span data-ttu-id="681d6-121">次の例では、専用 `balanceLock` インスタンスをロックすることでそのプライベート `balance` フィールドへのアクセスを同期する `Account` クラスが定義されます。</span><span class="sxs-lookup"><span data-stu-id="681d6-121">The following example defines an `Account` class that synchronizes access to its private `balance` field by locking on a dedicated `balanceLock` instance.</span></span> <span data-ttu-id="681d6-122">ロッキングに同じインスタンスを使用すると、2 つのスレッドが `Debit` または `Credit` メソッドを同時に呼び出すことによって `balance` フィールドを同時に更新することができなくなります。</span><span class="sxs-lookup"><span data-stu-id="681d6-122">Using the same instance for locking ensures that the `balance` field cannot be updated simultaneously by two threads attempting to call the `Debit` or `Credit` methods simultaneously.</span></span>

[!code-csharp[lock-statement-example](~/samples/snippets/csharp/keywords/LockStatementExample.cs)]

## <a name="c-language-specification"></a><span data-ttu-id="681d6-123">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="681d6-123">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="681d6-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="681d6-124">See also</span></span>

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.SpinLock?displayProperty=nameWithType>
- <xref:System.Threading.Interlocked?displayProperty=nameWithType>
- [<span data-ttu-id="681d6-125">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="681d6-125">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="681d6-126">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="681d6-126">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="681d6-127">ステートメントのキーワード</span><span class="sxs-lookup"><span data-stu-id="681d6-127">Statement Keywords</span></span>](statement-keywords.md)
- [<span data-ttu-id="681d6-128">インタロックされた操作</span><span class="sxs-lookup"><span data-stu-id="681d6-128">Interlocked operations</span></span>](../../../standard/threading/interlocked-operations.md)
- [<span data-ttu-id="681d6-129">同期プリミティブの概要</span><span class="sxs-lookup"><span data-stu-id="681d6-129">Overview of synchronization primitives</span></span>](../../../standard/threading/overview-of-synchronization-primitives.md)