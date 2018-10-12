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
# <a name="lock-statement-c-reference"></a>lock ステートメント (C# リファレンス)

`lock` キーワードは、ステートメント ブロックをクリティカル セクションとして指定します。このためには、特定のオブジェクトの相互排他ロックを取得し、ステートメントを実行して、ロックを解放します。 次の例では、`lock` ステートメントが使用されています。

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

詳細については、「[スレッドの同期](../../programming-guide/concepts/threading/thread-synchronization.md)」を参照してください。

## <a name="remarks"></a>コメント

`lock` キーワードは、コードのクリティカル セクションに複数のスレッドが同時に進入することを防ぐ働きをします。 これから実行しようとしているコードがロックされている場合、別のスレッドは、そのオブジェクトが解放されるまで待機 (ブロック) 状態になります。

スレッド処理については、「[スレッド処理](../../programming-guide/concepts/threading/index.md)」を参照してください。

`lock` キーワードは、ブロックの先頭で <xref:System.Threading.Monitor.Enter%2A> を呼び出し、ブロックの末尾で <xref:System.Threading.Monitor.Exit%2A> を呼び出します。 `lock` ステートメントの実行を待っているスレッドを <xref:System.Threading.Thread.Interrupt%2A> で中断すると、<xref:System.Threading.ThreadInterruptedException> がスローされます。

一般に、`public` 型 (つまり、コードの制御が及ばないインスタンス) をロックすることは避けてください。 `lock (this)`、`lock (typeof (MyType))`、`lock ("myLock")` は、このガイドラインに違反する代表的なコンストラクトです。

- `lock (this)` は、このインスタンスにパブリックにアクセスできる場合に問題となります。

- `lock (typeof (MyType))` は、`MyType` にパブリックにアクセスできる場合に問題となります。

- `lock("myLock")` が問題となる理由は、同じ文字列を使用するコードがプロセス内に他にも存在した場合、そのコードも同じロックを共有するためです。

`private` オブジェクトを定義してロックの適用対象を限定するか、`private static` オブジェクト変数を定義して、すべてのインスタンスに共通するデータを保護することをお勧めします。

`lock` ステートメントの本体で [await](await.md) キーワードを使用することはできません。

## <a name="example---threads-without-locking"></a>例: ロックを使用しないスレッド

次のサンプルでは、C# でロックされていないスレッドの簡単な使用例を示しています。

[!code-csharp[csrefKeywordsFixedLock#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsFixedLock/CS/csrefKeywordsFixedLock.cs#5)]

## <a name="example---threads-using-locking"></a>例: ロックを使用するスレッド

次のサンプルでは、スレッドと `lock` を使用しています。 `lock` ステートメントが存在する限り、このステートメント ブロックはクリティカル セクションとなり、`balance` が負の数になることはありません。

[!code-csharp[csrefKeywordsFixedLock#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsFixedLock/CS/csrefKeywordsFixedLock.cs#6)]

## <a name="c-language-specification"></a>C# 言語仕様

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>関連項目

- <xref:System.Reflection.MethodImplAttributes>
- <xref:System.Threading.Mutex>
- <xref:System.Threading.Monitor>
- [C# リファレンス](../../language-reference/index.md)
- [C# プログラミング ガイド](../../programming-guide/index.md)
- [スレッド化](../../programming-guide/concepts/threading/index.md)
- [C# のキーワード](index.md)
- [ステートメントのキーワード](statement-keywords.md)
- [インタロックされた操作](../../../standard/threading/interlocked-operations.md)
- [AutoResetEvent](../../../standard/threading/autoresetevent.md)
- [スレッドの同期](../../programming-guide/concepts/threading/thread-synchronization.md)