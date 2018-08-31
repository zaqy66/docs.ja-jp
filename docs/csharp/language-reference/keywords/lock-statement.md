---
title: lock ステートメント (C# リファレンス)
description: 'lock キーワードはスレッド処理で使用されます。 '
ms.date: 07/20/2015
f1_keywords:
- lock_CSharpKeyword
- lock
helpviewer_keywords:
- lock keyword [C#]
ms.assetid: 656da1a4-707e-4ef6-9c6e-6d13b646af42
ms.openlocfilehash: 6ed46837482642dfd7e1a96cd120fc18023c5e9f
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42931194"
---
# <a name="lock-statement-c-reference"></a><span data-ttu-id="346d8-103">lock ステートメント (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="346d8-103">lock statement (C# Reference)</span></span>

<span data-ttu-id="346d8-104">`lock` キーワードは、ステートメント ブロックをクリティカル セクションとして指定します。このためには、特定のオブジェクトの相互排他ロックを取得し、ステートメントを実行して、ロックを解放します。</span><span class="sxs-lookup"><span data-stu-id="346d8-104">The `lock` keyword marks a statement block as a critical section by obtaining the mutual-exclusion lock for a given object, executing a statement, and then releasing the lock.</span></span> <span data-ttu-id="346d8-105">次の例では、`lock` ステートメントが使用されています。</span><span class="sxs-lookup"><span data-stu-id="346d8-105">The following example includes a `lock` statement.</span></span>

```csharp
class Account
{
    decimal balance;
    private Object thisLock = new Object();

    public void Withdraw(decimal amount)
    {
        lock (thisLock)
        {
            if (amount > balance)
            {
                throw new Exception("Insufficient funds");
            }
            balance -= amount;
        }
    }
}
```

<span data-ttu-id="346d8-106">詳細については、「[スレッドの同期](../../programming-guide/concepts/threading/thread-synchronization.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="346d8-106">For more information, see [Thread Synchronization](../../programming-guide/concepts/threading/thread-synchronization.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="346d8-107">コメント</span><span class="sxs-lookup"><span data-stu-id="346d8-107">Remarks</span></span>

<span data-ttu-id="346d8-108">`lock` キーワードは、コードのクリティカル セクションに複数のスレッドが同時に進入することを防ぐ働きをします。</span><span class="sxs-lookup"><span data-stu-id="346d8-108">The `lock` keyword ensures that one thread does not enter a critical section of code while another thread is in the critical section.</span></span> <span data-ttu-id="346d8-109">これから実行しようとしているコードがロックされている場合、別のスレッドは、そのオブジェクトが解放されるまで待機 (ブロック) 状態になります。</span><span class="sxs-lookup"><span data-stu-id="346d8-109">If another thread tries to enter a locked code, it will wait, block, until the object is released.</span></span>

<span data-ttu-id="346d8-110">スレッド処理については、「[スレッド処理](../../programming-guide/concepts/threading/index.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="346d8-110">The section [Threading](../../programming-guide/concepts/threading/index.md) discusses threading.</span></span>

<span data-ttu-id="346d8-111">`lock` キーワードは、ブロックの先頭で <xref:System.Threading.Monitor.Enter%2A> を呼び出し、ブロックの末尾で <xref:System.Threading.Monitor.Exit%2A> を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="346d8-111">The `lock` keyword calls <xref:System.Threading.Monitor.Enter%2A> at the start of the block and <xref:System.Threading.Monitor.Exit%2A> at the end of the block.</span></span> <span data-ttu-id="346d8-112">`lock` ステートメントの実行を待っているスレッドを <xref:System.Threading.Thread.Interrupt%2A> で中断すると、<xref:System.Threading.ThreadInterruptedException> がスローされます。</span><span class="sxs-lookup"><span data-stu-id="346d8-112">A <xref:System.Threading.ThreadInterruptedException> is thrown if <xref:System.Threading.Thread.Interrupt%2A> interrupts a thread that is waiting to enter a `lock` statement.</span></span>

<span data-ttu-id="346d8-113">一般に、`public` 型 (つまり、コードの制御が及ばないインスタンス) をロックすることは避けてください。</span><span class="sxs-lookup"><span data-stu-id="346d8-113">In general, avoid locking on a `public` type, or instances beyond your code's control.</span></span> <span data-ttu-id="346d8-114">`lock (this)`、`lock (typeof (MyType))`、`lock ("myLock")` は、このガイドラインに違反する代表的なコンストラクトです。</span><span class="sxs-lookup"><span data-stu-id="346d8-114">The common constructs `lock (this)`, `lock (typeof (MyType))`, and `lock ("myLock")` violate this guideline:</span></span>

- <span data-ttu-id="346d8-115">`lock (this)` は、このインスタンスにパブリックにアクセスできる場合に問題となります。</span><span class="sxs-lookup"><span data-stu-id="346d8-115">`lock (this)` is a problem if the instance can be accessed publicly.</span></span>

- <span data-ttu-id="346d8-116">`lock (typeof (MyType))` は、`MyType` にパブリックにアクセスできる場合に問題となります。</span><span class="sxs-lookup"><span data-stu-id="346d8-116">`lock (typeof (MyType))` is a problem if `MyType` is publicly accessible.</span></span>

- <span data-ttu-id="346d8-117">`lock("myLock")` が問題となる理由は、同じ文字列を使用するコードがプロセス内に他にも存在した場合、そのコードも同じロックを共有するためです。</span><span class="sxs-lookup"><span data-stu-id="346d8-117">`lock("myLock")` is a problem because any other code in the process using the same string, will share the same lock.</span></span>

<span data-ttu-id="346d8-118">`private` オブジェクトを定義してロックの適用対象を限定するか、`private static` オブジェクト変数を定義して、すべてのインスタンスに共通するデータを保護することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="346d8-118">Best practice is to define a `private` object to lock on, or a `private static` object variable to protect data common to all instances.</span></span>

<span data-ttu-id="346d8-119">`lock` ステートメントの本体で [await](await.md) キーワードを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="346d8-119">You can't use the [await](await.md) keyword in the body of a `lock` statement.</span></span>

## <a name="example---threads-without-locking"></a><span data-ttu-id="346d8-120">例: ロックを使用しないスレッド</span><span class="sxs-lookup"><span data-stu-id="346d8-120">Example - Threads without locking</span></span>

<span data-ttu-id="346d8-121">次のサンプルでは、C# でロックされていないスレッドの簡単な使用例を示しています。</span><span class="sxs-lookup"><span data-stu-id="346d8-121">The following sample shows a simple use of threads without locking in C#:</span></span>

[!code-csharp[csrefKeywordsFixedLock#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsFixedLock/CS/csrefKeywordsFixedLock.cs#5)]

## <a name="example---threads-using-locking"></a><span data-ttu-id="346d8-122">例: ロックを使用するスレッド</span><span class="sxs-lookup"><span data-stu-id="346d8-122">Example - Threads using locking</span></span>

<span data-ttu-id="346d8-123">次のサンプルでは、スレッドと `lock` を使用しています。</span><span class="sxs-lookup"><span data-stu-id="346d8-123">The following sample uses threads and `lock`.</span></span> <span data-ttu-id="346d8-124">`lock` ステートメントが存在する限り、このステートメント ブロックはクリティカル セクションとなり、`balance` が負の数になることはありません。</span><span class="sxs-lookup"><span data-stu-id="346d8-124">As long as the `lock` statement is present, the statement block is a critical section and `balance` will never become a negative number:</span></span>

[!code-csharp[csrefKeywordsFixedLock#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsFixedLock/CS/csrefKeywordsFixedLock.cs#6)]

## <a name="c-language-specification"></a><span data-ttu-id="346d8-125">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="346d8-125">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="346d8-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="346d8-126">See also</span></span>

- <xref:System.Reflection.MethodImplAttributes>
- <xref:System.Threading.Mutex>
- <xref:System.Threading.Monitor>
- [<span data-ttu-id="346d8-127">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="346d8-127">C# Reference</span></span>](../../language-reference/index.md)
- [<span data-ttu-id="346d8-128">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="346d8-128">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="346d8-129">スレッド化</span><span class="sxs-lookup"><span data-stu-id="346d8-129">Threading</span></span>](../../programming-guide/concepts/threading/index.md)
- [<span data-ttu-id="346d8-130">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="346d8-130">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="346d8-131">ステートメントのキーワード</span><span class="sxs-lookup"><span data-stu-id="346d8-131">Statement Keywords</span></span>](statement-keywords.md)
- [<span data-ttu-id="346d8-132">インタロックされた操作</span><span class="sxs-lookup"><span data-stu-id="346d8-132">Interlocked Operations</span></span>](../../../standard/threading/interlocked-operations.md)
- [<span data-ttu-id="346d8-133">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="346d8-133">AutoResetEvent</span></span>](../../../standard/threading/autoresetevent.md)
- [<span data-ttu-id="346d8-134">スレッドの同期</span><span class="sxs-lookup"><span data-stu-id="346d8-134">Thread Synchronization</span></span>](../../programming-guide/concepts/threading/thread-synchronization.md)