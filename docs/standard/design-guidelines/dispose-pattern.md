---
title: Dispose パターン
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- Dispose method
- class library design guidelines [.NET Framework], Dispose method
- class library design guidelines [.NET Framework], Finalize method
- customizing Dispose method name
- Finalize method
ms.assetid: 31a6c13b-d6a2-492b-9a9f-e5238c983bcb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ff52e17cfe4a4236e4d165c0961ca3a23fed9a72
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43864645"
---
# <a name="dispose-pattern"></a><span data-ttu-id="b126f-102">Dispose パターン</span><span class="sxs-lookup"><span data-stu-id="b126f-102">Dispose Pattern</span></span>
<span data-ttu-id="b126f-103">すべてのプログラムは、実行の進行中に、メモリ、システムのハンドル、データベース接続など、1 つまたは複数のシステム リソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="b126f-103">All programs acquire one or more system resources, such as memory, system handles, or database connections, during the course of their execution.</span></span> <span data-ttu-id="b126f-104">開発者は、取得して使用後に解放する必要があるために、このようなシステム リソースを使用するには注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b126f-104">Developers have to be careful when using such system resources, because they must be released after they have been acquired and used.</span></span>  
  
 <span data-ttu-id="b126f-105">CLR では、自動メモリ管理のサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="b126f-105">The CLR provides support for automatic memory management.</span></span> <span data-ttu-id="b126f-106">マネージ メモリ (c# の演算子を使用して割り当てられたメモリ`new`) 明示的に解放する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b126f-106">Managed memory (memory allocated using the C# operator `new`) does not need to be explicitly released.</span></span> <span data-ttu-id="b126f-107">ガベージ コレクター (GC) によって自動的に解放されます。</span><span class="sxs-lookup"><span data-stu-id="b126f-107">It is released automatically by the garbage collector (GC).</span></span> <span data-ttu-id="b126f-108">これにより、メモリの解放の難しい面倒な作業から開発者を解放し、これまでにない生産性を .NET Framework によって提供される主な理由の 1 でしょう。</span><span class="sxs-lookup"><span data-stu-id="b126f-108">This frees developers from the tedious and difficult task of releasing memory and has been one of the main reasons for the unprecedented productivity afforded by the .NET Framework.</span></span>  
  
 <span data-ttu-id="b126f-109">残念ながら、マネージ メモリは、さまざまな種類のシステム リソースの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="b126f-109">Unfortunately, managed memory is just one of many types of system resources.</span></span> <span data-ttu-id="b126f-110">マネージ メモリ以外のリソースは、明示的に解放する必要がまだとアンマネージ リソースとして参照されます。</span><span class="sxs-lookup"><span data-stu-id="b126f-110">Resources other than managed memory still need to be released explicitly and are referred to as unmanaged resources.</span></span> <span data-ttu-id="b126f-111">GC は、具体的には設計されていません、このようなアンマネージ リソースの管理、開発者の手でアンマネージ リソースを管理する責任があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="b126f-111">The GC was specifically not designed to manage such unmanaged resources, which means that the responsibility for managing unmanaged resources lies in the hands of the developers.</span></span>  
  
 <span data-ttu-id="b126f-112">CLR では、アンマネージ リソースを解放するときにいくつかのヘルプを提供します。</span><span class="sxs-lookup"><span data-stu-id="b126f-112">The CLR provides some help in releasing unmanaged resources.</span></span> <span data-ttu-id="b126f-113"><xref:System.Object?displayProperty=nameWithType> 仮想メソッドを宣言<xref:System.Object.Finalize%2A>(ファイナライザーとも呼ばれます)、オブジェクトのメモリが GC によって解放され、アンマネージ リソースを解放をオーバーライドする前に、GC によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b126f-113"><xref:System.Object?displayProperty=nameWithType> declares a virtual method <xref:System.Object.Finalize%2A> (also called the finalizer) that is called by the GC before the object’s memory is reclaimed by the GC and can be overridden to release unmanaged resources.</span></span> <span data-ttu-id="b126f-114">ファイナライザーをオーバーライドする型は、ファイナライズ可能な型と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b126f-114">Types that override the finalizer are referred to as finalizable types.</span></span>  
  
 <span data-ttu-id="b126f-115">ファイナライザーはいくつかのクリーンアップのシナリオで有効になりますが、2 つの重要な欠点があります。</span><span class="sxs-lookup"><span data-stu-id="b126f-115">Although finalizers are effective in some cleanup scenarios, they have two significant drawbacks:</span></span>  
  
-   <span data-ttu-id="b126f-116">GC で検出されるオブジェクトがコレクションの対象である、ファイナライザーが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b126f-116">The finalizer is called when the GC detects that an object is eligible for collection.</span></span> <span data-ttu-id="b126f-117">これは未確定一定時間後、リソースは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="b126f-117">This happens at some undetermined period of time after the resource is not needed anymore.</span></span> <span data-ttu-id="b126f-118">開発者がでしたまたはリソースとリソースが実際には、ファイナライザーによってリリースときの時刻をリリースするまでの遅延がでプログラムが不足している多くのリソース (リソースを簡単に使い果たされる可能性) を取得または許容できない可能性があります。リソースの使用 (大規模なアンマネージ メモリ バッファーなど) に保持するコストがかかる場合です。</span><span class="sxs-lookup"><span data-stu-id="b126f-118">The delay between when the developer could or would like to release the resource and the time when the resource is actually released by the finalizer might be unacceptable in programs that acquire many scarce resources (resources that can be easily exhausted) or in cases in which resources are costly to keep in use (e.g., large unmanaged memory buffers).</span></span>  
  
-   <span data-ttu-id="b126f-119">CLR は、ファイナライザーを呼び出す必要がある、ときに、次のラウンドのガベージ コレクション (コレクション間で実行するファイナライザー) まで、オブジェクトのメモリのコレクションを延期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b126f-119">When the CLR needs to call a finalizer, it must postpone collection of the object’s memory until the next round of garbage collection (the finalizers run between collections).</span></span> <span data-ttu-id="b126f-120">これは、オブジェクトのメモリ (およびすべてのオブジェクトを参照) が、時間の長い期間に解放されないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="b126f-120">This means that the object’s memory (and all objects it refers to) will not be released for a longer period of time.</span></span>  
  
 <span data-ttu-id="b126f-121">そのため、ファイナライザーにのみ依存できない可能性がありますかを高パフォーマンスの高いシナリオで不足しているリソースを扱うとき、できるだけ迅速にアンマネージ リソースを解放する必要がある場合、多くのシナリオで適切な GC オーバーヘッドを追加しましたファイナライズは許されません。</span><span class="sxs-lookup"><span data-stu-id="b126f-121">Therefore, relying exclusively on finalizers might not be appropriate in many scenarios when it is important to reclaim unmanaged resources as quickly as possible, when dealing with scarce resources, or in highly performant scenarios in which the added GC overhead of finalization is unacceptable.</span></span>  
  
 <span data-ttu-id="b126f-122">フレームワークは、提供、<xref:System.IDisposable?displayProperty=nameWithType>不要なとすぐには、アンマネージ リソースを解放する手動の方法を開発者に提供するために実装するインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="b126f-122">The Framework provides the <xref:System.IDisposable?displayProperty=nameWithType> interface that should be implemented to provide the developer a manual way to release unmanaged resources as soon as they are not needed.</span></span> <span data-ttu-id="b126f-123">用意されています、<xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType>するように、GC が知ることができるメソッド オブジェクトが手動で破棄され、場合、オブジェクトのメモリを再要求できる前なくなった場合に、終了する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b126f-123">It also provides the <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType> method that can tell the GC that an object was manually disposed of and does not need to be finalized anymore, in which case the object’s memory can be reclaimed earlier.</span></span> <span data-ttu-id="b126f-124">実装する型、`IDisposable`インターフェイス破棄可能な型として参照されます。</span><span class="sxs-lookup"><span data-stu-id="b126f-124">Types that implement the `IDisposable` interface are referred to as disposable types.</span></span>  
  
 <span data-ttu-id="b126f-125">Dispose パターンは、使用状況とファイナライザーの実装を標準化するためのものと`IDisposable`インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="b126f-125">The Dispose Pattern is intended to standardize the usage and implementation of finalizers and the `IDisposable` interface.</span></span>  
  
 <span data-ttu-id="b126f-126">実装の複雑さを軽減するパターンの主な動機は、<xref:System.Object.Finalize%2A>と<xref:System.IDisposable.Dispose%2A>メソッド。</span><span class="sxs-lookup"><span data-stu-id="b126f-126">The main motivation for the pattern is to reduce the complexity of the implementation of the <xref:System.Object.Finalize%2A> and the <xref:System.IDisposable.Dispose%2A> methods.</span></span> <span data-ttu-id="b126f-127">複雑なメソッドがいくつかのコード パスが (相違点は、章の説明) を共有するという事実に由来します。</span><span class="sxs-lookup"><span data-stu-id="b126f-127">The complexity stems from the fact that the methods share some but not all code paths (the differences are described later in the chapter).</span></span> <span data-ttu-id="b126f-128">さらに、確定的なリソース管理のための言語サポートの進化に関連するパターンの一部の要素の歴史的な理由があります。</span><span class="sxs-lookup"><span data-stu-id="b126f-128">In addition, there are historical reasons for some elements of the pattern related to the evolution of language support for deterministic resource management.</span></span>  
  
 <span data-ttu-id="b126f-129">**✓ DO** 破棄可能な型のインスタンスを含む型で、基本的な Dispose パターンを実装します。</span><span class="sxs-lookup"><span data-stu-id="b126f-129">**✓ DO** implement the Basic Dispose Pattern on types containing instances of disposable types.</span></span> <span data-ttu-id="b126f-130">参照してください、 [Dispose パターンの基本的な](#basic_pattern)基本的なパターンの詳細セクション。</span><span class="sxs-lookup"><span data-stu-id="b126f-130">See the [Basic Dispose Pattern](#basic_pattern) section for details on the basic pattern.</span></span>  
  
 <span data-ttu-id="b126f-131">型が破棄可能なその他のオブジェクトの有効期間にわたって担当する場合は、開発者にも、それらを破棄する方法が必要があります。</span><span class="sxs-lookup"><span data-stu-id="b126f-131">If a type is responsible for the lifetime of other disposable objects, developers need a way to dispose of them, too.</span></span> <span data-ttu-id="b126f-132">コンテナーの使用`Dispose`メソッドは、これを可能にする便利な方法です。</span><span class="sxs-lookup"><span data-stu-id="b126f-132">Using the container’s `Dispose` method is a convenient way to make this possible.</span></span>  
  
 <span data-ttu-id="b126f-133">**✓ DO** 基本の Dispose パターンを実装し、保持しているリソースを明示的に解放できる必要があると、ファイナライザーがない型でファイナライザーを用意します。</span><span class="sxs-lookup"><span data-stu-id="b126f-133">**✓ DO** implement the Basic Dispose Pattern and provide a finalizer on types holding resources that need to be freed explicitly and that do not have finalizers.</span></span>  
  
 <span data-ttu-id="b126f-134">たとえば、アンマネージ メモリ バッファーに格納する型のパターンを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b126f-134">For example, the pattern should be implemented on types storing unmanaged memory buffers.</span></span> <span data-ttu-id="b126f-135">[ファイナライズ可能な型](#finalizable_types)に関連するファイナライザーを実装するガイドラインについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b126f-135">The [Finalizable Types](#finalizable_types) section discusses guidelines related to implementing finalizers.</span></span>  
  
 <span data-ttu-id="b126f-136">**✓ CONSIDER** 基本の Dispose パターンを実装するクラスでのリソースとアンマネージ自体を保持しないことや、破棄可能なオブジェクトは、実行のサブタイプをされている可能性がします。</span><span class="sxs-lookup"><span data-stu-id="b126f-136">**✓ CONSIDER** implementing the Basic Dispose Pattern on classes that themselves don’t hold unmanaged resources or disposable objects but are likely to have subtypes that do.</span></span>  
  
 <span data-ttu-id="b126f-137">これの良い例は、<xref:System.IO.Stream?displayProperty=nameWithType>クラス。</span><span class="sxs-lookup"><span data-stu-id="b126f-137">A great example of this is the <xref:System.IO.Stream?displayProperty=nameWithType> class.</span></span> <span data-ttu-id="b126f-138">すべてのリソースを保持しない抽象基本クラスが、そのサブクラスのほとんどの操作を行い、このため、このパターンを実装します。</span><span class="sxs-lookup"><span data-stu-id="b126f-138">Although it is an abstract base class that doesn’t hold any resources, most of its subclasses do and because of this, it implements this pattern.</span></span>  
  
<a name="basic_pattern"></a>   
## <a name="basic-dispose-pattern"></a><span data-ttu-id="b126f-139">基本的な Dispose パターン</span><span class="sxs-lookup"><span data-stu-id="b126f-139">Basic Dispose Pattern</span></span>  
 <span data-ttu-id="b126f-140">基本的なパターンの実装では、実装する必要があります、`System.IDisposable`インターフェイスと宣言する、`Dispose(bool)`間で共有するすべてのリソースのクリーンアップ ロジックを実装するメソッド、`Dispose`メソッドと省略可能な終了します。</span><span class="sxs-lookup"><span data-stu-id="b126f-140">The basic implementation of the pattern involves implementing the `System.IDisposable` interface and declaring the `Dispose(bool)` method that implements all resource cleanup logic to be shared between the `Dispose` method and the optional finalizer.</span></span>  
  
 <span data-ttu-id="b126f-141">次の例は、基本的なパターンの単純な実装を示しています。</span><span class="sxs-lookup"><span data-stu-id="b126f-141">The following example shows a simple implementation of the basic pattern:</span></span>  
  
```csharp
public class DisposableResourceHolder : IDisposable {  
  
    private SafeHandle resource; // handle to a resource  
  
    public DisposableResourceHolder() {  
        this.resource = ... // allocates the resource  
    }  
  
    public void Dispose() {  
        Dispose(true);  
        GC.SuppressFinalize(this);  
    }  
  
    protected virtual void Dispose(bool disposing) {  
        if (disposing) {  
            if (resource!= null) resource.Dispose();  
        }  
    }  
}  
```  
  
 <span data-ttu-id="b126f-142">ブール型パラメーター`disposing`から呼び出されたメソッドであるかどうかを示す、`IDisposable.Dispose`実装、それともファイナライザーか。</span><span class="sxs-lookup"><span data-stu-id="b126f-142">The Boolean parameter `disposing` indicates whether the method was invoked from the `IDisposable.Dispose` implementation or from the finalizer.</span></span> <span data-ttu-id="b126f-143">`Dispose(bool)`実装は、その他の参照オブジェクト (上記のサンプルのリソース フィールドなど) にアクセスする前に、パラメーターを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b126f-143">The `Dispose(bool)` implementation should check the parameter before accessing other reference objects (e.g., the resource field in the preceding sample).</span></span> <span data-ttu-id="b126f-144">このようなオブジェクトから、メソッドが呼び出された場合にのみアクセスする必要があります、`IDisposable.Dispose`実装 (ときに、`disposing`パラメーターが true に等しい)。</span><span class="sxs-lookup"><span data-stu-id="b126f-144">Such objects should only be accessed when the method is called from the `IDisposable.Dispose` implementation (when the `disposing` parameter is equal to true).</span></span> <span data-ttu-id="b126f-145">メソッドがファイナライザーから呼び出される場合 (`disposing`は false)、その他のオブジェクトへのアクセスはできません。</span><span class="sxs-lookup"><span data-stu-id="b126f-145">If the method is invoked from the finalizer (`disposing` is false), other objects should not be accessed.</span></span> <span data-ttu-id="b126f-146">理由は、予期しない順序でオブジェクトがファイナライズし、そのため、またはその依存関係のいずれかが既にファイナライズされていることです。</span><span class="sxs-lookup"><span data-stu-id="b126f-146">The reason is that objects are finalized in an unpredictable order and so they, or any of their dependencies, might already have been finalized.</span></span>  
  
 <span data-ttu-id="b126f-147">また、このセクションでは、Dispose パターンを実装しないベース クラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="b126f-147">Also, this section applies to classes with a base that does not already implement the Dispose Pattern.</span></span> <span data-ttu-id="b126f-148">既にパターンを実装するクラスを継承する場合はオーバーライドするだけで、`Dispose(bool)`追加のリソースのクリーンアップ ロジックを提供するメソッド。</span><span class="sxs-lookup"><span data-stu-id="b126f-148">If you are inheriting from a class that already implements the pattern, simply override the `Dispose(bool)` method to provide additional resource cleanup logic.</span></span>  
  
 <span data-ttu-id="b126f-149">**✓ DO** 宣言、`protected virtual void Dispose(bool disposing)`アンマネージ リソースの解放に関連するすべてのロジックを集中管理するメソッド。</span><span class="sxs-lookup"><span data-stu-id="b126f-149">**✓ DO** declare a `protected virtual void Dispose(bool disposing)` method to centralize all logic related to releasing unmanaged resources.</span></span>  
  
 <span data-ttu-id="b126f-150">このメソッドでは、すべてのリソースのクリーンアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="b126f-150">All resource cleanup should occur in this method.</span></span> <span data-ttu-id="b126f-151">メソッドは、両方のファイナライザーから、`IDisposable.Dispose`メソッド。</span><span class="sxs-lookup"><span data-stu-id="b126f-151">The method is called from both the finalizer and the `IDisposable.Dispose` method.</span></span> <span data-ttu-id="b126f-152">パラメーターは、ファイナライザーの内部から呼び出されている場合は false になります。</span><span class="sxs-lookup"><span data-stu-id="b126f-152">The parameter will be false if being invoked from inside a finalizer.</span></span> <span data-ttu-id="b126f-153">これを使用して終了処理中に実行されるコードは、ファイナライズ可能なその他のオブジェクトにアクセスしていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b126f-153">It should be used to ensure any code running during finalization is not accessing other finalizable objects.</span></span> <span data-ttu-id="b126f-154">ファイナライザーの実装の詳細については、次のセクションで説明します。</span><span class="sxs-lookup"><span data-stu-id="b126f-154">Details of implementing finalizers are described in the next section.</span></span>  
  
```csharp
protected virtual void Dispose(bool disposing) {  
    if (disposing) {  
        if (resource!= null) resource.Dispose();  
    }  
}  
```  
  
 <span data-ttu-id="b126f-155">**✓ DO** 実装、`IDisposable`だけ呼び出すことによってインターフェイス`Dispose(true)`続く`GC.SuppressFinalize(this)`です。</span><span class="sxs-lookup"><span data-stu-id="b126f-155">**✓ DO** implement the `IDisposable` interface by simply calling `Dispose(true)` followed by `GC.SuppressFinalize(this)`.</span></span>  
  
 <span data-ttu-id="b126f-156">呼び出し`SuppressFinalize`場合にのみ発生`Dispose(true)`正常に実行されます。</span><span class="sxs-lookup"><span data-stu-id="b126f-156">The call to `SuppressFinalize` should only occur if `Dispose(true)` executes successfully.</span></span>  
  
```csharp
public void Dispose(){  
    Dispose(true);  
    GC.SuppressFinalize(this);  
}  
```  
  
 <span data-ttu-id="b126f-157">**X DO NOT** パラメーターなしで行う`Dispose`仮想メソッドです。</span><span class="sxs-lookup"><span data-stu-id="b126f-157">**X DO NOT** make the parameterless `Dispose` method virtual.</span></span>  
  
 <span data-ttu-id="b126f-158">`Dispose(bool)`メソッドは、1 つのサブクラスによってオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b126f-158">The `Dispose(bool)` method is the one that should be overridden by subclasses.</span></span>  
  
```csharp
// bad design  
public class DisposableResourceHolder : IDisposable {  
    public virtual void Dispose() { ... }  
    protected virtual void Dispose(bool disposing) { ... }  
}  
  
// good design  
public class DisposableResourceHolder : IDisposable {  
    public void Dispose() { ... }  
    protected virtual void Dispose(bool disposing) { ... }  
}  
```  
  
 <span data-ttu-id="b126f-159">**X DO NOT** のすべてのオーバー ロードを宣言、`Dispose`以外のメソッド`Dispose()`と`Dispose(bool)`です。</span><span class="sxs-lookup"><span data-stu-id="b126f-159">**X DO NOT** declare any overloads of the `Dispose` method other than `Dispose()` and `Dispose(bool)`.</span></span>  
  
 <span data-ttu-id="b126f-160">`Dispose` このパターンを体系化し、実装者、ユーザー、およびコンパイラの間で混乱を避けるために予約語を考慮必要があります。</span><span class="sxs-lookup"><span data-stu-id="b126f-160">`Dispose` should be considered a reserved word to help codify this pattern and prevent confusion among implementers, users, and compilers.</span></span> <span data-ttu-id="b126f-161">一部の言語は、特定の種類を自動的にこのパターンを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="b126f-161">Some languages might choose to automatically implement this pattern on certain types.</span></span>  
  
 <span data-ttu-id="b126f-162">**✓ DO** を許可する、`Dispose(bool)`に複数回呼び出されるメソッド。</span><span class="sxs-lookup"><span data-stu-id="b126f-162">**✓ DO** allow the `Dispose(bool)` method to be called more than once.</span></span> <span data-ttu-id="b126f-163">メソッドは、最初に呼び出した後何もしないこともできます。</span><span class="sxs-lookup"><span data-stu-id="b126f-163">The method might choose to do nothing after the first call.</span></span>  
  
```csharp
public class DisposableResourceHolder : IDisposable {  
  
    bool disposed = false;  
  
    protected virtual void Dispose(bool disposing) {  
        if (disposed) return;  
        // cleanup  
        ...  
        disposed = true;  
    }  
}  
```  
  
 <span data-ttu-id="b126f-164">**X AVOID** 内から例外をスローして`Dispose(bool)`されている重要な状況で格納しているプロセスが破損している場合を除き (リークを一貫性のない共有状態などです。)。</span><span class="sxs-lookup"><span data-stu-id="b126f-164">**X AVOID** throwing an exception from within `Dispose(bool)` except under critical situations where the containing process has been corrupted (leaks, inconsistent shared state, etc.).</span></span>  
  
 <span data-ttu-id="b126f-165">ユーザーが期待する呼び出しを`Dispose`例外は発生しません。</span><span class="sxs-lookup"><span data-stu-id="b126f-165">Users expect that a call to `Dispose` will not raise an exception.</span></span>  
  
 <span data-ttu-id="b126f-166">場合`Dispose`例外を発生させる可能性があります、さらに finally ブロックのクリーンアップ ロジックは実行されません。</span><span class="sxs-lookup"><span data-stu-id="b126f-166">If `Dispose` could raise an exception, further finally-block cleanup logic will not execute.</span></span> <span data-ttu-id="b126f-167">この問題を回避するは、ユーザーはすべての呼び出しをラップする必要がある`Dispose`(内で、finally ブロック!)、try ブロックで非常に複雑なクリーンアップのハンドラーにつながります。</span><span class="sxs-lookup"><span data-stu-id="b126f-167">To work around this, the user would need to wrap every call to `Dispose` (within the finally block!) in a try block, which leads to very complex cleanup handlers.</span></span> <span data-ttu-id="b126f-168">実行している場合、`Dispose(bool disposing)`メソッド、破棄が false の場合は例外をスローしません。</span><span class="sxs-lookup"><span data-stu-id="b126f-168">If executing a `Dispose(bool disposing)` method, never throw an exception if disposing is false.</span></span> <span data-ttu-id="b126f-169">これにより、ファイナライザーのコンテキスト内で実行している場合、プロセスが終了します。</span><span class="sxs-lookup"><span data-stu-id="b126f-169">Doing so will terminate the process if executing inside a finalizer context.</span></span>  
  
 <span data-ttu-id="b126f-170">**✓ DO** スロー、<xref:System.ObjectDisposedException>オブジェクトが破棄された後は使用できませんのすべてのメンバーからです。</span><span class="sxs-lookup"><span data-stu-id="b126f-170">**✓ DO** throw an <xref:System.ObjectDisposedException> from any member that cannot be used after the object has been disposed of.</span></span>  
  
```csharp
public class DisposableResourceHolder : IDisposable {  
    bool disposed = false;  
    SafeHandle resource; // handle to a resource  
  
    public void DoSomething() {  
        if (disposed) throw new ObjectDisposedException(...);  
        // now call some native methods using the resource   
        ...  
    }  
    protected virtual void Dispose(bool disposing) {  
        if (disposed) return;  
        // cleanup  
        ...  
        disposed = true;  
    }  
}  
```  
  
 <span data-ttu-id="b126f-171">**✓ CONSIDER** メソッドを提供する`Close()`に加え、`Dispose()`領域での一般的な用語が閉じるかどうかは。</span><span class="sxs-lookup"><span data-stu-id="b126f-171">**✓ CONSIDER** providing method `Close()`, in addition to the `Dispose()`, if close is standard terminology in the area.</span></span>  
  
 <span data-ttu-id="b126f-172">重要ではこれを行うときに、`Close`実装と同じ`Dispose`の実装を検討し、`IDisposable.Dispose`メソッド明示的にします。</span><span class="sxs-lookup"><span data-stu-id="b126f-172">When doing so, it is important that you make the `Close` implementation identical to `Dispose` and consider implementing the `IDisposable.Dispose` method explicitly.</span></span>  
  
```csharp
public class Stream : IDisposable {  
    IDisposable.Dispose() {  
        Close();  
    }  
    public void Close() {  
        Dispose(true);  
        GC.SuppressFinalize(this);  
    }  
}  
```  
  
<a name="finalizable_types"></a>   
## <a name="finalizable-types"></a><span data-ttu-id="b126f-173">ファイナライズ可能な型</span><span class="sxs-lookup"><span data-stu-id="b126f-173">Finalizable Types</span></span>  
 <span data-ttu-id="b126f-174">ファイナライズ可能な型がファイナライザーをオーバーライドし、ファイナライズ コード パスを提供することによって、基本的な Dispose パターンを拡張する型、`Dispose(bool)`メソッド。</span><span class="sxs-lookup"><span data-stu-id="b126f-174">Finalizable types are types that extend the Basic Dispose Pattern by overriding the finalizer and providing finalization code path in the `Dispose(bool)` method.</span></span>  
  
 <span data-ttu-id="b126f-175">ファイナライザーは、主に、実行中に、システムの状態に関する (通常は有効な) 仮定することはできませんので、正しく実装するために非常に困難です。</span><span class="sxs-lookup"><span data-stu-id="b126f-175">Finalizers are notoriously difficult to implement correctly, primarily because you cannot make certain (normally valid) assumptions about the state of the system during their execution.</span></span> <span data-ttu-id="b126f-176">次のガイドラインを考慮して慎重に検討にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b126f-176">The following guidelines should be taken into careful consideration.</span></span>  
  
 <span data-ttu-id="b126f-177">いないだけに適用のガイドラインに注意してください、`Finalize`メソッド、ファイナライザーから呼び出された任意のコードには。</span><span class="sxs-lookup"><span data-stu-id="b126f-177">Note that some of the guidelines apply not just to the `Finalize` method, but to any code called from a finalizer.</span></span> <span data-ttu-id="b126f-178">内で実行されるロジックの場合は、基本的な Dispose パターン以前に定義した、つまり`Dispose(bool disposing)`ときに、`disposing`パラメーターは false。</span><span class="sxs-lookup"><span data-stu-id="b126f-178">In the case of the Basic Dispose Pattern previously defined, this means logic that executes inside `Dispose(bool disposing)` when the `disposing` parameter is false.</span></span>  
  
 <span data-ttu-id="b126f-179">オーバーライドが必要ない場合は、基本クラスは、既にファイナライズ可能なおよび基本的な Dispose パターンを実装、`Finalize`もう一度です。</span><span class="sxs-lookup"><span data-stu-id="b126f-179">If the base class already is finalizable and implements the Basic Dispose Pattern, you should not override `Finalize` again.</span></span> <span data-ttu-id="b126f-180">だけオーバーライドする代わりに、`Dispose(bool)`追加のリソースのクリーンアップ ロジックを提供するメソッド。</span><span class="sxs-lookup"><span data-stu-id="b126f-180">You should instead just override the `Dispose(bool)` method to provide additional resource cleanup logic.</span></span>  
  
 <span data-ttu-id="b126f-181">次のコードでは、ファイナライズ可能な型の例を示します。</span><span class="sxs-lookup"><span data-stu-id="b126f-181">The following code shows an example of a finalizable type:</span></span>  
  
```csharp
public class ComplexResourceHolder : IDisposable {  
  
    private IntPtr buffer; // unmanaged memory buffer  
    private SafeHandle resource; // disposable handle to a resource  
  
    public ComplexResourceHolder() {  
        this.buffer = ... // allocates memory  
        this.resource = ... // allocates the resource  
    }  
  
    protected virtual void Dispose(bool disposing) {  
            ReleaseBuffer(buffer); // release unmanaged memory  
        if (disposing) { // release other disposable objects  
            if (resource!= null) resource.Dispose();  
        }  
    }  
  
    ~ComplexResourceHolder() {
        Dispose(false);  
    }  
  
    public void Dispose() {
        Dispose(true);  
        GC.SuppressFinalize(this);  
    }  
}  
```  
  
 <span data-ttu-id="b126f-182">**X AVOID** ファイナライズ可能な型を作成します。</span><span class="sxs-lookup"><span data-stu-id="b126f-182">**X AVOID** making types finalizable.</span></span>  
  
 <span data-ttu-id="b126f-183">思わファイナライザーが必要なケースを慎重に検討します。</span><span class="sxs-lookup"><span data-stu-id="b126f-183">Carefully consider any case in which you think a finalizer is needed.</span></span> <span data-ttu-id="b126f-184">実際のパフォーマンスとコードの両方の複雑さの観点から、ファイナライザーを持つインスタンスに関連付けられているコスト。</span><span class="sxs-lookup"><span data-stu-id="b126f-184">There is a real cost associated with instances with finalizers, from both a performance and code complexity standpoint.</span></span> <span data-ttu-id="b126f-185">などのリソースのラッパーを使用して必要に応じて<xref:System.Runtime.InteropServices.SafeHandle>をアンマネージ リソースをカプセル化可能であれば、その場合、ファイナライザーが不要になるラッパーが、独自のリソースのクリーンアップを行うためです。</span><span class="sxs-lookup"><span data-stu-id="b126f-185">Prefer using resource wrappers such as <xref:System.Runtime.InteropServices.SafeHandle> to encapsulate unmanaged resources where possible, in which case a finalizer becomes unnecessary because the wrapper is responsible for its own resource cleanup.</span></span>  
  
 <span data-ttu-id="b126f-186">**X DO NOT** ファイナライズ可能な値の型を作成します。</span><span class="sxs-lookup"><span data-stu-id="b126f-186">**X DO NOT** make value types finalizable.</span></span>  
  
 <span data-ttu-id="b126f-187">実際に参照型のみが、CLR で確定取得し、つまり値型にファイナライザーを配置しようとするとは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b126f-187">Only reference types actually get finalized by the CLR, and thus any attempt to place a finalizer on a value type will be ignored.</span></span> <span data-ttu-id="b126f-188">C# および C++ コンパイラは、この規則を適用します。</span><span class="sxs-lookup"><span data-stu-id="b126f-188">The C# and C++ compilers enforce this rule.</span></span>  
  
 <span data-ttu-id="b126f-189">**✓ DO** 型は独自のファイナライザーがない、アンマネージ リソースを解放する必要がある場合の種類をファイナライズようにします。</span><span class="sxs-lookup"><span data-stu-id="b126f-189">**✓ DO** make a type finalizable if the type is responsible for releasing an unmanaged resource that does not have its own finalizer.</span></span>  
  
 <span data-ttu-id="b126f-190">ファイナライザーを実装するときにだけ呼び出す`Dispose(false)`内のすべてのリソースのクリーンアップ ロジックを配置し、`Dispose(bool disposing)`メソッド。</span><span class="sxs-lookup"><span data-stu-id="b126f-190">When implementing the finalizer, simply call `Dispose(false)` and place all resource cleanup logic inside the `Dispose(bool disposing)` method.</span></span>  
  
```csharp
public class ComplexResourceHolder : IDisposable {  
  
    ~ComplexResourceHolder() {
        Dispose(false);  
    }  
  
    protected virtual void Dispose(bool disposing) {
        ...  
    }  
}  
```  
  
 <span data-ttu-id="b126f-191">**✓ DO** ファイナライズ可能な型で、基本的な Dispose パターンを実装します。</span><span class="sxs-lookup"><span data-stu-id="b126f-191">**✓ DO** implement the Basic Dispose Pattern on every finalizable type.</span></span>  
  
 <span data-ttu-id="b126f-192">これにより、型のユーザーは、ファイナライザーが責任はそれらのリソースのクリーンアップが決定的を明示的に実行することを意味します。</span><span class="sxs-lookup"><span data-stu-id="b126f-192">This gives users of the type a means to explicitly perform deterministic cleanup of those same resources for which the finalizer is responsible.</span></span>  
  
 <span data-ttu-id="b126f-193">**X DO NOT** こと、が既に終了されている重大なリスクがあるため、ファイナライザーのコード パスに、ファイナライズ可能なオブジェクトにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="b126f-193">**X DO NOT** access any finalizable objects in the finalizer code path, because there is significant risk that they will have already been finalized.</span></span>  
  
 <span data-ttu-id="b126f-194">たとえば、別のファイナライズ可能なオブジェクト B を参照しているファイナライズ可能なオブジェクト、信頼性の高い方法では使用できません B A のファイナライザー、またはその逆です。</span><span class="sxs-lookup"><span data-stu-id="b126f-194">For example, a finalizable object A that has a reference to another finalizable object B cannot reliably use B in A’s finalizer, or vice versa.</span></span> <span data-ttu-id="b126f-195">(クリティカル ファイナライズの弱い順序保証) する場合を除きランダムな順序では、ファイナライザーが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b126f-195">Finalizers are called in a random order (short of a weak ordering guarantee for critical finalization).</span></span>  
  
 <span data-ttu-id="b126f-196">また、アプリケーション ドメインのアンロード中またはプロセスの終了中に、静的変数に格納されているオブジェクトは特定の時点で収集取得こともあります。</span><span class="sxs-lookup"><span data-stu-id="b126f-196">Also, be aware that objects stored in static variables will get collected at certain points during an application domain unload or while exiting the process.</span></span> <span data-ttu-id="b126f-197">ファイナライズ可能なオブジェクト (または静的変数に格納された値を使用する静的メソッドを呼び出す) を参照する静的変数ができない可能性がありますにアクセスする場合は安全な<xref:System.Environment.HasShutdownStarted%2A?displayProperty=nameWithType>true を返します。</span><span class="sxs-lookup"><span data-stu-id="b126f-197">Accessing a static variable that refers to a finalizable object (or calling a static method that might use values stored in static variables) might not be safe if <xref:System.Environment.HasShutdownStarted%2A?displayProperty=nameWithType> returns true.</span></span>  
  
 <span data-ttu-id="b126f-198">**✓ DO** ように、`Finalize`保護されているメソッド。</span><span class="sxs-lookup"><span data-stu-id="b126f-198">**✓ DO** make your `Finalize` method protected.</span></span>  
  
 <span data-ttu-id="b126f-199">C#、C++、および VB.NET の開発者は、コンパイラはこのガイドラインを適用する役立つため、これについて心配する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b126f-199">C#, C++, and VB.NET developers do not need to worry about this, because the compilers help to enforce this guideline.</span></span>  
  
 <span data-ttu-id="b126f-200">**X DO NOT** システムに重大な障害を除く、ファイナライザーのロジックから使用すると、例外のエスケープします。</span><span class="sxs-lookup"><span data-stu-id="b126f-200">**X DO NOT** let exceptions escape from the finalizer logic, except for system-critical failures.</span></span>  
  
 <span data-ttu-id="b126f-201">CLR がシャット ダウン (時点で、.NET Framework version 2.0)、プロセス全体をファイナライザーから例外がスローされた場合は実行されず、制御された方法でリリースされているリソースその他のファイナライザーを防止します。</span><span class="sxs-lookup"><span data-stu-id="b126f-201">If an exception is thrown from a finalizer, the CLR will shut down the entire process (as of .NET Framework version 2.0), preventing other finalizers from executing and resources from being released in a controlled manner.</span></span>  
  
 <span data-ttu-id="b126f-202">**✓ CONSIDER** を作成して、重要なファイナライズ可能なオブジェクトを使用して (を含む型階層を持つ型<xref:System.Runtime.ConstrainedExecution.CriticalFinalizerObject>) の状況でファイナライザーどうしても必要があります実行発生した場合でも強制アプリケーション ドメインのアンロード スレッド中止します。</span><span class="sxs-lookup"><span data-stu-id="b126f-202">**✓ CONSIDER** creating and using a critical finalizable object (a type with a type hierarchy that contains <xref:System.Runtime.ConstrainedExecution.CriticalFinalizerObject>) for situations in which a finalizer absolutely must execute even in the face of forced application domain unloads and thread aborts.</span></span>  
  
 <span data-ttu-id="b126f-203">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="b126f-203">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="b126f-204">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="b126f-204">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b126f-205">関連項目</span><span class="sxs-lookup"><span data-stu-id="b126f-205">See also</span></span>

- <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType>  
- <xref:System.Object.Finalize%2A?displayProperty=nameWithType>  
- [<span data-ttu-id="b126f-206">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="b126f-206">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="b126f-207">共通デザイン パターン</span><span class="sxs-lookup"><span data-stu-id="b126f-207">Common Design Patterns</span></span>](../../../docs/standard/design-guidelines/common-design-patterns.md)  
- [<span data-ttu-id="b126f-208">ガベージ コレクション</span><span class="sxs-lookup"><span data-stu-id="b126f-208">Garbage Collection</span></span>](../../../docs/standard/garbage-collection/index.md)
