---
title: volatile - C# リファレンス
ms.custom: seodec18
ms.date: 10/24/2018
f1_keywords:
- volatile_CSharpKeyword
- volatile
helpviewer_keywords:
- volatile keyword [C#]
ms.assetid: 78089bc7-7b38-4cfd-9e49-87ac036af009
ms.openlocfilehash: 6ae5445de69e987826fb58ff50ca8d47c11eb53c
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245494"
---
# <a name="volatile-c-reference"></a><span data-ttu-id="89c32-102">volatile (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="89c32-102">volatile (C# Reference)</span></span>

<span data-ttu-id="89c32-103">`volatile` キーワードは、同時に実行されている複数のスレッドによって、フィールドが変更される可能性があることを示します。</span><span class="sxs-lookup"><span data-stu-id="89c32-103">The `volatile` keyword indicates that a field might be modified by multiple threads that are executing at the same time.</span></span> <span data-ttu-id="89c32-104">コンパイラ、ランタイム システム、さらにはハードウェアで、パフォーマンスを上げる目的でメモリの場所との読み書きを再整理できます。</span><span class="sxs-lookup"><span data-stu-id="89c32-104">The compiler, the runtime system, and even hardware may rearrange reads and writes to memory locations for performance reasons.</span></span> <span data-ttu-id="89c32-105">`volatile` が宣言されているフィールドはこのような最適化の対象になりません。</span><span class="sxs-lookup"><span data-stu-id="89c32-105">Fields that are declared `volatile` are not subject to these optimizations.</span></span> <span data-ttu-id="89c32-106">`volatile` 修飾子を追加することで、すべてのスレッドによって、他のスレッドにより実行される volatile 書き込みがその実行順序どおりに観察されます。</span><span class="sxs-lookup"><span data-stu-id="89c32-106">Adding the `volatile` modifier ensures that all threads will observe volatile writes performed by any other thread in the order in which they were performed.</span></span> <span data-ttu-id="89c32-107">volatile 書き込みの単一の全体的順序がすべての実行スレッドから認識される保証はありません。</span><span class="sxs-lookup"><span data-stu-id="89c32-107">There is no guarantee of a single total ordering of volatile writes as seen from all threads of execution.</span></span>
  
<span data-ttu-id="89c32-108">`volatile` キーワードは次の型のフィールドに使用できます。</span><span class="sxs-lookup"><span data-stu-id="89c32-108">The `volatile` keyword can be applied to fields of these types:</span></span>  
  
- <span data-ttu-id="89c32-109">参照型。</span><span class="sxs-lookup"><span data-stu-id="89c32-109">Reference types.</span></span>  
- <span data-ttu-id="89c32-110">ポインター型 (unsafe コンテキスト内)。</span><span class="sxs-lookup"><span data-stu-id="89c32-110">Pointer types (in an unsafe context).</span></span> <span data-ttu-id="89c32-111">ポインター自体は volatile にできますが、ポインターが指しているオブジェクトは volatile にできません。</span><span class="sxs-lookup"><span data-stu-id="89c32-111">Note that although the pointer itself can be volatile, the object that it points to cannot.</span></span> <span data-ttu-id="89c32-112">つまり、"volatile を指すポインター" は宣言できません。</span><span class="sxs-lookup"><span data-stu-id="89c32-112">In other words, you cannot declare a "pointer to volatile."</span></span>  
- <span data-ttu-id="89c32-113">`sbyte`、`byte`、`short`、`ushort`、`int`、`uint`、`char`、`float`、`bool` など、単純型。</span><span class="sxs-lookup"><span data-stu-id="89c32-113">Simple types such as `sbyte`, `byte`, `short`, `ushort`, `int`, `uint`, `char`, `float`, and `bool`.</span></span>  
- <span data-ttu-id="89c32-114">基本型が `byte`、`sbyte`、`short`、`ushort`、`int`、`uint` のいずれかの `enum` 型。</span><span class="sxs-lookup"><span data-stu-id="89c32-114">An `enum` type with one of the following base types: `byte`, `sbyte`, `short`, `ushort`, `int`, or `uint`.</span></span>  
- <span data-ttu-id="89c32-115">参照型であることが判明しているジェネリック型パラメーター。</span><span class="sxs-lookup"><span data-stu-id="89c32-115">Generic type parameters known to be reference types.</span></span>
- <span data-ttu-id="89c32-116"><xref:System.IntPtr> および <xref:System.UIntPtr>。</span><span class="sxs-lookup"><span data-stu-id="89c32-116"><xref:System.IntPtr> and <xref:System.UIntPtr>.</span></span>  

<span data-ttu-id="89c32-117">`double` や `long` など、その他の型には `volatile` を指定できません。そのような型のフィールドに対する読み書きはアトミックになるとは限らないためです。</span><span class="sxs-lookup"><span data-stu-id="89c32-117">Other types, including `double` and `long`, cannot be marked `volatile` because reads and writes to fields of those types cannot be guaranteed to be atomic.</span></span> <span data-ttu-id="89c32-118">そのような型のフィールドへのマルチスレッド アクセスを保護するために、<xref:System.Threading.Interlocked> クラス メンバーを使用するか、[`lock`](lock-statement.md) ステートメントでアクセスを保護します。</span><span class="sxs-lookup"><span data-stu-id="89c32-118">To protect multi-threaded access to those types of fields, use the <xref:System.Threading.Interlocked> class members or protect access using the [`lock`](lock-statement.md) statement.</span></span>

<span data-ttu-id="89c32-119">`volatile` キーワードは `class` または `struct` のフィールドにのみ適用できます。</span><span class="sxs-lookup"><span data-stu-id="89c32-119">The `volatile` keyword can only be applied to fields of a `class` or `struct`.</span></span> <span data-ttu-id="89c32-120">ローカル変数を `volatile` として宣言することはできません。</span><span class="sxs-lookup"><span data-stu-id="89c32-120">Local variables cannot be declared `volatile`.</span></span>
  
## <a name="example"></a><span data-ttu-id="89c32-121">例</span><span class="sxs-lookup"><span data-stu-id="89c32-121">Example</span></span>

<span data-ttu-id="89c32-122">次の例は、public のフィールド変数を `volatile` として宣言する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="89c32-122">The following example shows how to declare a public field variable as `volatile`.</span></span>  
  
[!code-csharp[declareVolatile](~/samples/snippets/csharp/language-reference/keywords/volatile/Program.cs#Declaration)]

<span data-ttu-id="89c32-123">次の例は、補助スレッドつまりワーカー スレッドを作成および使用して、プライマリ スレッドとの並行処理を実行する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="89c32-123">The following example demonstrates how an auxiliary or worker thread can be created and used to perform processing in parallel with that of the primary thread.</span></span> <span data-ttu-id="89c32-124">マルチスレッドについて詳しくは、「[マネージド スレッド処理](../../../standard/threading/index.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="89c32-124">For more information about multithreading, see [Managed Threading](../../../standard/threading/index.md).</span></span>
  
[!code-csharp[declareVolatile](~/samples/snippets/csharp/language-reference/keywords/volatile/Program.cs#Volatile)]

<span data-ttu-id="89c32-125">`volatile` 修飾子を `_shouldStop` の宣言に追加することで、(前述のコードにある抜粋に似た) 同じ結果が常に得られます。</span><span class="sxs-lookup"><span data-stu-id="89c32-125">With the `volatile` modifier added to the declaration of `_shouldStop` in place, you'll always get the same results (similar to the excerpt shown in the preceding code).</span></span> <span data-ttu-id="89c32-126">しかしながら、この修飾子が `_shouldStop` メンバーになければ、動作は予測できません。</span><span class="sxs-lookup"><span data-stu-id="89c32-126">However, without that modifier on the `_shouldStop` member, the behavior is unpredictable.</span></span> <span data-ttu-id="89c32-127">`DoWork` メソッドでメンバー アクセスが最適化されることがありますが、古いデータが読み取られます。</span><span class="sxs-lookup"><span data-stu-id="89c32-127">The `DoWork` method may optimize the member access, resulting in reading stale data.</span></span> <span data-ttu-id="89c32-128">マルチスレッド プログラミングの性質上、古い読み取りの数は予測できません。</span><span class="sxs-lookup"><span data-stu-id="89c32-128">Because of the nature of multi-threaded programming, the number of stale reads is unpredictable.</span></span> <span data-ttu-id="89c32-129">プログラムを実行するたびに若干異なる結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="89c32-129">Different runs of the program will produce somewhat different results.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="89c32-130">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="89c32-130">C# Language Specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="89c32-131">参照</span><span class="sxs-lookup"><span data-stu-id="89c32-131">See Also</span></span>

- [<span data-ttu-id="89c32-132">C# 言語仕様: volatile キーワード</span><span class="sxs-lookup"><span data-stu-id="89c32-132">C# language specification: volatile keyword</span></span>](../../../../_csharplang/spec/classes.md#volatile-fields)
- [<span data-ttu-id="89c32-133">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="89c32-133">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="89c32-134">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="89c32-134">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="89c32-135">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="89c32-135">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="89c32-136">修飾子</span><span class="sxs-lookup"><span data-stu-id="89c32-136">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="89c32-137">lock ステートメント</span><span class="sxs-lookup"><span data-stu-id="89c32-137">lock statement</span></span>](lock-statement.md)
- <span data-ttu-id="89c32-138"><xref:System.Threading.Interlocked> クラス</span><span class="sxs-lookup"><span data-stu-id="89c32-138"><xref:System.Threading.Interlocked> class</span></span>
