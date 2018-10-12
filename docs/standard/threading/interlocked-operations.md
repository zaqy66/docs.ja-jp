---
title: インタロックされた操作
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Interlocked class, about Interlocked class
- threading [.NET Framework], Interlocked class
ms.assetid: cbda7114-c752-4f3e-ada1-b1e8dd262f2b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 069a95656e7ceaf454c01c47d61ff391bcbed2fe
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2018
ms.locfileid: "46538886"
---
# <a name="interlocked-operations"></a><span data-ttu-id="4f146-102">インタロックされた操作</span><span class="sxs-lookup"><span data-stu-id="4f146-102">Interlocked operations</span></span>

<span data-ttu-id="4f146-103"><xref:System.Threading.Interlocked?displayProperty=nameWithType> クラスでは、複数のスレッドによって共有されている変数へのアクセスを同期するメソッドが提供されます。</span><span class="sxs-lookup"><span data-stu-id="4f146-103">The <xref:System.Threading.Interlocked?displayProperty=nameWithType> class provides methods that synchronize access to a variable that is shared by multiple threads.</span></span> <span data-ttu-id="4f146-104">この変数が共有メモリにある場合、さまざまなプロセスのスレッドがこのメカニズムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f146-104">The threads of different processes can use this mechanism if the variable is in shared memory.</span></span> <span data-ttu-id="4f146-105">インタロックされた操作はアトミックです。つまり、その操作全体が 1 つの単位のため、同じ変数の別の操作によって中断されることはありません。</span><span class="sxs-lookup"><span data-stu-id="4f146-105">Interlocked operations are atomic — that is, the entire operation is a unit that cannot be interrupted by another operation on the same variable.</span></span> <span data-ttu-id="4f146-106">これは、メモリ アドレスから値を読み込んだ後、変更して格納できるようになる前にスレッドを中断できるプリエンプティブ マルチスレッドのオペレーティング システムで重要です。</span><span class="sxs-lookup"><span data-stu-id="4f146-106">This is important in operating systems with preemptive multithreading, where a thread can be suspended after loading a value from a memory address, but before having the chance to alter it and store it.</span></span>  
  
 <span data-ttu-id="4f146-107"><xref:System.Threading.Interlocked> クラスでは次の操作が提供されます。</span><span class="sxs-lookup"><span data-stu-id="4f146-107">The <xref:System.Threading.Interlocked> class provides the following operations:</span></span>  
  
-   <span data-ttu-id="4f146-108"><xref:System.Threading.Interlocked.Add%2A?displayProperty=nameWithType> メソッドは変数に整数値を追加して、変数の新しい値を返します。</span><span class="sxs-lookup"><span data-stu-id="4f146-108">The <xref:System.Threading.Interlocked.Add%2A?displayProperty=nameWithType> method adds an integer value to a variable and returns the new value of the variable.</span></span>  
  
-   <span data-ttu-id="4f146-109"><xref:System.Threading.Interlocked.Read%2A?displayProperty=nameWithType> メソッドはアトミック操作として 64 ビットの整数値を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="4f146-109">The <xref:System.Threading.Interlocked.Read%2A?displayProperty=nameWithType> method reads a 64-bit integer value as an atomic operation.</span></span> <span data-ttu-id="4f146-110">これは、64 ビット整数の読み取りが通常はアトミック操作ではない 32 ビット オペレーティング システムでは有用です。</span><span class="sxs-lookup"><span data-stu-id="4f146-110">This is useful on 32-bit operating systems, where reading a 64-bit integer is not ordinarily an atomic operation.</span></span>  
  
-   <span data-ttu-id="4f146-111"><xref:System.Threading.Interlocked.Increment%2A?displayProperty=nameWithType> および <xref:System.Threading.Interlocked.Decrement%2A?displayProperty=nameWithType> メソッドは変数をインクリメントまたはデクリメントして、結果の値を返します。</span><span class="sxs-lookup"><span data-stu-id="4f146-111">The <xref:System.Threading.Interlocked.Increment%2A?displayProperty=nameWithType> and <xref:System.Threading.Interlocked.Decrement%2A?displayProperty=nameWithType> methods increment or decrement a variable and return the resulting value.</span></span>  
  
-   <span data-ttu-id="4f146-112"><xref:System.Threading.Interlocked.Exchange%2A?displayProperty=nameWithType> メソッドは、指定された変数で値をアトミックに変換して値を返し、それを新しい値で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="4f146-112">The <xref:System.Threading.Interlocked.Exchange%2A?displayProperty=nameWithType> method performs an atomic exchange of the value in a specified variable, returning that value and replacing it with a new value.</span></span> <span data-ttu-id="4f146-113">任意の参照型の変数に対してこのメソッドの汎用 <xref:System.Threading.Interlocked.Exchange%60%601%28%60%600%40%2C%60%600%29> オーバーロードを使用して交換を実行します。</span><span class="sxs-lookup"><span data-stu-id="4f146-113">Use a generic <xref:System.Threading.Interlocked.Exchange%60%601%28%60%600%40%2C%60%600%29> overload of this method to perform the exchange on a variable of any reference type.</span></span>  
  
-   <span data-ttu-id="4f146-114"><xref:System.Threading.Interlocked.CompareExchange%2A?displayProperty=nameWithType> メソッドでも 2 つの値を変換しますが、比較結果によって異なります。</span><span class="sxs-lookup"><span data-stu-id="4f146-114">The <xref:System.Threading.Interlocked.CompareExchange%2A?displayProperty=nameWithType> method also exchanges two values, but contingent on the result of a comparison.</span></span> <span data-ttu-id="4f146-115">任意の参照型の変数に対してこのメソッドの汎用 <xref:System.Threading.Interlocked.CompareExchange%60%601%28%60%600%40%2C%60%600%2C%60%600%29> オーバーロードを使用して交換を実行します。</span><span class="sxs-lookup"><span data-stu-id="4f146-115">Use a generic <xref:System.Threading.Interlocked.CompareExchange%60%601%28%60%600%40%2C%60%600%2C%60%600%29> overload of this method to perform the exchange on a variable of any reference type.</span></span>  
  
 <span data-ttu-id="4f146-116">最新のプロセッサでは、<xref:System.Threading.Interlocked> クラスのメソッドを単一の命令で実装できる場合もよくあります。</span><span class="sxs-lookup"><span data-stu-id="4f146-116">On modern processors, the methods of the <xref:System.Threading.Interlocked> class can often be implemented by a single instruction.</span></span> <span data-ttu-id="4f146-117">このため、非常にパフォーマンスの高い同期を行うことができ、それらを使用して、スピン ロックのようなより高レベルの同期メカニズムを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="4f146-117">Thus, they provide very high-performance synchronization and can be used to build higher-level synchronization mechanisms, like spin locks.</span></span>  
  
 <span data-ttu-id="4f146-118"><xref:System.Threading.Monitor> クラスと <xref:System.Threading.Interlocked> クラスを組み合わせて使用する例については、「[Monitor クラス](https://msdn.microsoft.com/library/33fe4aef-b44b-42fd-9e72-c908e39e75db)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f146-118">For an example that uses the <xref:System.Threading.Monitor> and <xref:System.Threading.Interlocked> classes in combination, see [Monitors](https://msdn.microsoft.com/library/33fe4aef-b44b-42fd-9e72-c908e39e75db).</span></span>  
  
## <a name="compareexchange-example"></a><span data-ttu-id="4f146-119">CompareExchange の例</span><span class="sxs-lookup"><span data-stu-id="4f146-119">CompareExchange example</span></span>

 <span data-ttu-id="4f146-120"><xref:System.Threading.Interlocked.CompareExchange%2A> メソッドを使用して、単純なインクリメントまたはデクリメントよりも複雑な計算を保護できます。</span><span class="sxs-lookup"><span data-stu-id="4f146-120">The <xref:System.Threading.Interlocked.CompareExchange%2A> method can be used to protect computations that are more complicated than simple increment and decrement.</span></span> <span data-ttu-id="4f146-121">次の例は、浮動小数点数として格納されている現在の合計に対して加算を行うスレッドセーフ メソッドを示しています </span><span class="sxs-lookup"><span data-stu-id="4f146-121">The following example demonstrates a thread-safe method that adds to a running total stored as a floating point number.</span></span> <span data-ttu-id="4f146-122">(整数の場合は、<xref:System.Threading.Interlocked.Add%2A> メソッドがより単純なソリューションとなります)。完全なコード例については、単精度と倍精度浮動小数点引数 (<xref:System.Threading.Interlocked.CompareExchange%28System.Single%40%2CSystem.Single%2CSystem.Single%29> と <xref:System.Threading.Interlocked.CompareExchange%28System.Double%40%2CSystem.Double%2CSystem.Double%29>) を受け取る <xref:System.Threading.Interlocked.CompareExchange%2A> のオーバーロードを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f146-122">(For integers, the <xref:System.Threading.Interlocked.Add%2A> method is a simpler solution.) For complete code examples, see the overloads of <xref:System.Threading.Interlocked.CompareExchange%2A> that take single-precision and double-precision floating-point arguments (<xref:System.Threading.Interlocked.CompareExchange%28System.Single%40%2CSystem.Single%2CSystem.Single%29> and <xref:System.Threading.Interlocked.CompareExchange%28System.Double%40%2CSystem.Double%2CSystem.Double%29>).</span></span>  
  
 [!code-cpp[Conceptual.Interlocked#1](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.interlocked/cpp/source1.cpp#1)]
 [!code-csharp[Conceptual.Interlocked#1](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.interlocked/cs/source1.cs#1)]
 [!code-vb[Conceptual.Interlocked#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.interlocked/vb/source1.vb#1)]  
  
## <a name="untyped-overloads-of-exchange-and-compareexchange"></a><span data-ttu-id="4f146-123">Exchange および CompareExchange の型指定されていないオーバーロード</span><span class="sxs-lookup"><span data-stu-id="4f146-123">Untyped overloads of Exchange and CompareExchange</span></span>

 <span data-ttu-id="4f146-124"><xref:System.Threading.Interlocked.Exchange%2A> および <xref:System.Threading.Interlocked.CompareExchange%2A>メソッドには、<xref:System.Object> 型の引数を受け取るオーバーロードがあります。</span><span class="sxs-lookup"><span data-stu-id="4f146-124">The <xref:System.Threading.Interlocked.Exchange%2A> and <xref:System.Threading.Interlocked.CompareExchange%2A> methods have overloads that take arguments of type <xref:System.Object>.</span></span> <span data-ttu-id="4f146-125">各オーバーロードの最初の引数は `ref Object` (Visual Basic では `ByRef … As Object`) であり、タイプ セーフを確保するために、この引数に渡される変数は <xref:System.Object> のように厳密に型指定される必要があります。これらのメソッドを呼び出すときに、単に最初の引数を型 <xref:System.Object> にキャストするだけでは不十分です。</span><span class="sxs-lookup"><span data-stu-id="4f146-125">The first argument of each of these overloads is `ref Object` (`ByRef … As Object` in Visual Basic), and type safety requires the variable passed to this argument to be typed strictly as <xref:System.Object>; you cannot simply cast the first argument to type <xref:System.Object> when calling these methods.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4f146-126">.NET Framework Version 2.0 以降では、<xref:System.Threading.Interlocked.Exchange%2A> と <xref:System.Threading.Interlocked.CompareExchange%2A> メソッドの汎用オーバーロードを使用して、厳密に型指定された変数を変換します。</span><span class="sxs-lookup"><span data-stu-id="4f146-126">In the .NET Framework version 2.0 and later, use the generic overloads of the <xref:System.Threading.Interlocked.Exchange%2A> and <xref:System.Threading.Interlocked.CompareExchange%2A> methods to exchange strongly typed variables.</span></span>  
  
 <span data-ttu-id="4f146-127">一度だけ設定できる `ClassA` 型のプロパティのコード例を次に示します。このプロパティは、.NET Framework Version 1.0 または 1.1 で実装できます。</span><span class="sxs-lookup"><span data-stu-id="4f146-127">The following code example shows a property of type `ClassA` that can be set only once, as it might be implemented in the .NET Framework version 1.0 or 1.1.</span></span>  
  
 [!code-cpp[Conceptual.Interlocked#2](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.interlocked/cpp/source2.cpp#2)]
 [!code-csharp[Conceptual.Interlocked#2](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.interlocked/cs/source2.cs#2)]
 [!code-vb[Conceptual.Interlocked#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.interlocked/vb/source2.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="4f146-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f146-128">See also</span></span>

- <xref:System.Threading.Interlocked?displayProperty=nameWithType>  
- <xref:System.Threading.Monitor?displayProperty=nameWithType>  
- [<span data-ttu-id="4f146-129">スレッド化</span><span class="sxs-lookup"><span data-stu-id="4f146-129">Threading</span></span>](index.md)  
- [<span data-ttu-id="4f146-130">スレッド処理オブジェクトと機能</span><span class="sxs-lookup"><span data-stu-id="4f146-130">Threading objects and features</span></span>](threading-objects-and-features.md)
