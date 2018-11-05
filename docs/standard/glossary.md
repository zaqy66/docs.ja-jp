---
title: .NET 用語集
description: .NET のドキュメントで使われている用語からいくつか選択してその意味を説明します。
author: tdykstra
ms.author: tdykstra
ms.date: 07/08/2017
ms.technology: dotnet-standard
ms.openlocfilehash: 4ffcf56ba171192048a736b58ddcfa591fd3af58
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2018
ms.locfileid: "48840272"
---
# <a name="net-glossary"></a><span data-ttu-id="83072-103">.NET 用語集</span><span class="sxs-lookup"><span data-stu-id="83072-103">.NET Glossary</span></span>

<span data-ttu-id="83072-104">この用語集の主な目的は、.NET のドキュメントで定義なしに頻繁に出現する用語と頭字語の意味を明確にすることです。</span><span class="sxs-lookup"><span data-stu-id="83072-104">The primary goal of this glossary is to clarify meanings of selected terms and acronyms that appear frequently in the .NET documentation without definitions.</span></span>

## <a name="aot"></a><span data-ttu-id="83072-105">AOT</span><span class="sxs-lookup"><span data-stu-id="83072-105">AOT</span></span>

<span data-ttu-id="83072-106">Ahead Of Time コンパイラ。</span><span class="sxs-lookup"><span data-stu-id="83072-106">Ahead-of-time compiler.</span></span>

<span data-ttu-id="83072-107">[JIT](#jit) と同様に、このコンパイラも [IL](#il) をマシン コードに変換します。</span><span class="sxs-lookup"><span data-stu-id="83072-107">Similar to [JIT](#jit), this compiler also translates [IL](#il) to machine code.</span></span> <span data-ttu-id="83072-108">JIT コンパイルとは異なり、AOT コンパイルはアプリケーションが実行される前に行われ、通常は、別のコンピューターで実行されます。</span><span class="sxs-lookup"><span data-stu-id="83072-108">In contrast to JIT compilation, AOT compilation happens before the application is executed and is usually performed on a different machine.</span></span> <span data-ttu-id="83072-109">AOT ツール チェーンは実行時にコンパイルしないので、コンパイルに費やされる時間を最小限に抑える必要はありません。</span><span class="sxs-lookup"><span data-stu-id="83072-109">Because AOT tool chains don't compile at runtime, they don't have to minimize time spent compiling.</span></span> <span data-ttu-id="83072-110">つまり、より多くの時間を最適化に費やすことができます。</span><span class="sxs-lookup"><span data-stu-id="83072-110">That means they can spend more time optimizing.</span></span> <span data-ttu-id="83072-111">AOT のコンテキストはアプリケーション全体であるため、AOT コンパイラはモジュール間のリンクとプログラム全体の分析も実行します。これは、すべての参照が追跡されて、1 つの実行可能ファイルが生成されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="83072-111">Since the context of AOT is the entire application, the AOT compiler also performs cross-module linking and whole-program analysis, which means that all references are followed and a single executable is produced.</span></span>

## <a name="aspnet"></a><span data-ttu-id="83072-112">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="83072-112">ASP.NET</span></span> 

<span data-ttu-id="83072-113">.NET Framework に付属している ASP.NET の元の実装。</span><span class="sxs-lookup"><span data-stu-id="83072-113">The original ASP.NET implementation that ships with the .NET Framework.</span></span>

<span data-ttu-id="83072-114">ASP.NET は、ASP.NET Core を含む ASP.NET の両方の実装を指す包括的な用語として使われることがあります。</span><span class="sxs-lookup"><span data-stu-id="83072-114">Sometimes ASP.NET is an umbrella term that refers to both ASP.NET implementations including ASP.NET Core.</span></span> <span data-ttu-id="83072-115">どちらを意味するかはコンテキストによって決まります。</span><span class="sxs-lookup"><span data-stu-id="83072-115">The meaning that the term carries in any given instance is determined by context.</span></span> <span data-ttu-id="83072-116">両方の実装を意味するために ASP.NET を使っているのではないことを明確にしたい場合は、ASP.NET 4.x を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83072-116">Refer to ASP.NET 4.x when you want to make it clear that you’re not using ASP.NET to mean both implementations.</span></span> 

<span data-ttu-id="83072-117">[ASP.NET のドキュメント](/aspnet/#pivot=aspnet)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-117">See [ASP.NET documentation](/aspnet/#pivot=aspnet).</span></span>

## <a name="aspnet-core"></a><span data-ttu-id="83072-118">ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="83072-118">ASP.NET Core</span></span>

<span data-ttu-id="83072-119">.NET Core 上に構築された ASP.NET のクロスプラットフォームで高パフォーマンスなオープン ソースの実装。</span><span class="sxs-lookup"><span data-stu-id="83072-119">A cross-platform, high-performance, open source implementation of ASP.NET built on .NET Core.</span></span>

<span data-ttu-id="83072-120">[ASP.NET Core のドキュメント](/aspnet/#pivot=core)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-120">See [ASP.NET Core documentation](/aspnet/#pivot=core).</span></span>

## <a name="assembly"></a><span data-ttu-id="83072-121">アセンブリ</span><span class="sxs-lookup"><span data-stu-id="83072-121">assembly</span></span>

<span data-ttu-id="83072-122">アプリケーションまたは他のアセンブリから呼び出すことができる API のコレクションを含む *.dll*/*.exe* ファイル。</span><span class="sxs-lookup"><span data-stu-id="83072-122">A *.dll*/*.exe* file that can contain a collection of APIs that can be called by applications or other assemblies.</span></span>

<span data-ttu-id="83072-123">アセンブリは、インターフェイス、クラス、構造体、列挙型、デリゲートなどの種類を含むことができます。</span><span class="sxs-lookup"><span data-stu-id="83072-123">An assembly may include types such as interfaces, classes, structures, enumerations, and delegates.</span></span> <span data-ttu-id="83072-124">プロジェクトの *bin* フォルダー内のアセンブリは、"*バイナリ*" と呼ばれることもあります。</span><span class="sxs-lookup"><span data-stu-id="83072-124">Assemblies in a project's *bin* folder are sometimes referred to as *binaries*.</span></span> <span data-ttu-id="83072-125">「[ライブラリ](#library)」もご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-125">See also [library](#library).</span></span>

## <a name="clr"></a><span data-ttu-id="83072-126">CLR</span><span class="sxs-lookup"><span data-stu-id="83072-126">CLR</span></span>

<span data-ttu-id="83072-127">共通言語ランタイム (Common Language Runtime)。</span><span class="sxs-lookup"><span data-stu-id="83072-127">Common Language Runtime.</span></span>

<span data-ttu-id="83072-128">厳密な意味はコンテキストによって異なりますが、通常は、.NET Framework のランタイムを指します。</span><span class="sxs-lookup"><span data-stu-id="83072-128">The exact meaning depends on the context, but this usually refers to the runtime of the .NET Framework.</span></span> <span data-ttu-id="83072-129">CLR は、メモリの割り当てと管理を行います。</span><span class="sxs-lookup"><span data-stu-id="83072-129">The CLR handles memory allocation and management.</span></span> <span data-ttu-id="83072-130">CLR は、アプリの実行だけでなく、[JIT](#jit) コンパイラを使って実行時にコードを生成してコンパイルする仮想マシンでもあります。</span><span class="sxs-lookup"><span data-stu-id="83072-130">The CLR is also a virtual machine that not only executes apps but also generates and compiles code on-the-fly using a [JIT](#jit) compiler.</span></span> <span data-ttu-id="83072-131">現在の Microsoft CLR の実装は Windows だけです。</span><span class="sxs-lookup"><span data-stu-id="83072-131">The current Microsoft CLR implementation is Windows only.</span></span>

## <a name="coreclr"></a><span data-ttu-id="83072-132">CoreCLR</span><span class="sxs-lookup"><span data-stu-id="83072-132">CoreCLR</span></span>

<span data-ttu-id="83072-133">.NET Core 共通言語ランタイム (.NET Core Common Language Runtime)。</span><span class="sxs-lookup"><span data-stu-id="83072-133">.NET Core Common Language Runtime.</span></span>

<span data-ttu-id="83072-134">この CLR は、CLR と同じコード ベースから作成されます。</span><span class="sxs-lookup"><span data-stu-id="83072-134">This CLR is built from the same code base as the CLR.</span></span> <span data-ttu-id="83072-135">もともと、CoreCLR は Silverlight のランタイムであり、複数のプラットフォーム (具体的には Windows と OS X) で実行するように設計されていました。現在の CoreCLR は .NET Core の一部であり、CLR の簡素化されたバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="83072-135">Originally, CoreCLR was the runtime of Silverlight and was designed to run on multiple platforms, specifically Windows and OS X. CoreCLR is now part of .NET Core and represents a simplified version of the CLR.</span></span> <span data-ttu-id="83072-136">まだ[クロスプラットフォーム](#cross-platform) ランタイムであり、多くの Linux ディストリビューションのサポートを含むようになっています。</span><span class="sxs-lookup"><span data-stu-id="83072-136">It's still a [cross-platform](#cross-platform) runtime, now including support for many Linux distributions.</span></span> <span data-ttu-id="83072-137">CoreCLR は、JIT とコード実行機能を備えた仮想マシンでもあります。</span><span class="sxs-lookup"><span data-stu-id="83072-137">CoreCLR is also a virtual machine with JIT and code execution capabilities.</span></span>

## <a name="corefx"></a><span data-ttu-id="83072-138">CoreFX</span><span class="sxs-lookup"><span data-stu-id="83072-138">CoreFX</span></span>

<span data-ttu-id="83072-139">.NET Core 基本クラス ライブラリ (BCL)</span><span class="sxs-lookup"><span data-stu-id="83072-139">.NET Core Base Class Library (BCL)</span></span>

<span data-ttu-id="83072-140">System.\* (および限られた範囲の Microsoft.\*) 名前空間を構成するライブラリのセット。</span><span class="sxs-lookup"><span data-stu-id="83072-140">A set of libraries that comprise the System.\* (and to a limited extent  Microsoft.\*) namespaces.</span></span> <span data-ttu-id="83072-141">BCL は汎用の下位レベル フレームワークであり、ASP.NET Core などの上位レベル アプリケーション フレームワークはそれを基にして構築されています。</span><span class="sxs-lookup"><span data-stu-id="83072-141">The BCL is a general purpose, lower-level framework that higher-level application frameworks, such as ASP.NET Core, build on.</span></span> <span data-ttu-id="83072-142">.NET Core BCL のソース コードは [CoreFX リポジトリ](https://github.com/dotnet/corefx)に含まれます。</span><span class="sxs-lookup"><span data-stu-id="83072-142">The source code of the .NET Core BCL is contained in the [CoreFX repository](https://github.com/dotnet/corefx).</span></span> <span data-ttu-id="83072-143">ただし、.NET Core API の大部分は .NET Framework でも使うことができるため、CoreFX は .NET Framework BCL が分岐したものと考えることができます。</span><span class="sxs-lookup"><span data-stu-id="83072-143">However, the majority of the .NET Core APIs are also available in the .NET Framework, so you can think of CoreFX as a fork of the .NET Framework BCL.</span></span>

## <a name="corert"></a><span data-ttu-id="83072-144">CoreRT</span><span class="sxs-lookup"><span data-stu-id="83072-144">CoreRT</span></span>

<span data-ttu-id="83072-145">.NET Core ランタイム。</span><span class="sxs-lookup"><span data-stu-id="83072-145">.NET Core runtime.</span></span>

<span data-ttu-id="83072-146">CLR/CoreCLR とは異なり、CoreRT は仮想マシンではありません。つまり、[JIT](#jit) が含まれないため、実行時にコードを生成して実行する機能はありません。</span><span class="sxs-lookup"><span data-stu-id="83072-146">In contrast to the CLR/CoreCLR, CoreRT is not a virtual machine, which means it doesn't include the facilities to generate and run code on-the-fly because it doesn't include a [JIT](#jit).</span></span> <span data-ttu-id="83072-147">ただし、[GC](#gc) およびランタイム型識別 (RTTI) とリフレクションの機能は備えています。</span><span class="sxs-lookup"><span data-stu-id="83072-147">It does, however, include the [GC](#gc) and the ability for runtime type identification (RTTI) and reflection.</span></span> <span data-ttu-id="83072-148">ただ、CoreRT の型システムはリフレクション用のメタデータが必要ないように設計されています。</span><span class="sxs-lookup"><span data-stu-id="83072-148">However, its type system is designed so that metadata for reflection isn't required.</span></span> <span data-ttu-id="83072-149">これにより、[AOT](#aot) ツール チェーンで余分なメタデータのリンクを削除し、(さらに重要なこととして) アプリが使っていないコードを特定することができます。</span><span class="sxs-lookup"><span data-stu-id="83072-149">This enables having an [AOT](#aot) tool chain that can link away superfluous metadata and (more importantly) identify code that the app doesn't use.</span></span> <span data-ttu-id="83072-150">CoreRT は開発中です。</span><span class="sxs-lookup"><span data-stu-id="83072-150">CoreRT is in development.</span></span>

<span data-ttu-id="83072-151">「[Intro to .NET Native and CoreRT](https://github.com/dotnet/corert/blob/master/Documentation/intro-to-corert.md)」(.NET Native と CoreRT の概要) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-151">See [Intro to .NET Native and CoreRT](https://github.com/dotnet/corert/blob/master/Documentation/intro-to-corert.md)</span></span>

## <a name="cross-platform"></a><span data-ttu-id="83072-152">クロスプラットフォーム</span><span class="sxs-lookup"><span data-stu-id="83072-152">cross-platform</span></span>

<span data-ttu-id="83072-153">Linux、Windows、iOS など、複数の異なるオペレーティング システム上で使用できるアプリケーションを開発し、実行することができます。OS ごとに作成し直す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="83072-153">The ability to develop and execute an application that can be used on multiple different operating systems, such as Linux, Windows and iOS, without having to re-write specifically for each one.</span></span> <span data-ttu-id="83072-154">そのため、異なるプラットフォーム上のアプリケーション間でコードを再利用し、一貫性を保つことができます。</span><span class="sxs-lookup"><span data-stu-id="83072-154">This enables code re-use and consistency between applications on different platforms.</span></span>

## <a name="ecosystem"></a><span data-ttu-id="83072-155">エコシステム</span><span class="sxs-lookup"><span data-stu-id="83072-155">ecosystem</span></span>

<span data-ttu-id="83072-156">特定のテクノロジ用のアプリケーションを構築して実行するために使われるすべての実行時ソフトウェア、開発ツール、およびコミュニティ リソース。</span><span class="sxs-lookup"><span data-stu-id="83072-156">All of the runtime software, development tools, and community resources that are used to build and run applications for a given technology.</span></span>

<span data-ttu-id="83072-157">".NET エコシステム" という用語は ".NET スタック" などの用語と似ていますが、サードパーティのアプリとライブラリを含む点が異なります。</span><span class="sxs-lookup"><span data-stu-id="83072-157">The term ".NET ecosystem" differs from similar terms such as ".NET stack" in its inclusion of third-party apps and libraries.</span></span> <span data-ttu-id="83072-158">文章での使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="83072-158">Here's an example in a sentence:</span></span>

- <span data-ttu-id="83072-159">"[.NET Standard](#net-standard) の背後にある意図は、.NET エコシステムの高度な統一性を確立することです。"</span><span class="sxs-lookup"><span data-stu-id="83072-159">"The motivation behind the [.NET Standard](#net-standard) is to establish greater uniformity in the .NET ecosystem."</span></span> 

## <a name="framework"></a><span data-ttu-id="83072-160">フレームワーク</span><span class="sxs-lookup"><span data-stu-id="83072-160">framework</span></span>

<span data-ttu-id="83072-161">一般に、特定のテクノロジに基づくアプリケーションの開発と展開を容易にする API の包括的なコレクション。</span><span class="sxs-lookup"><span data-stu-id="83072-161">In general, a comprehensive collection of APIs that facilitates development and deployment of applications that are based on a particular technology.</span></span> <span data-ttu-id="83072-162">この一般的な意味でのアプリケーション フレームワークの例としては、ASP.NET Core や Windows フォームなどがあります。</span><span class="sxs-lookup"><span data-stu-id="83072-162">In this general sense, ASP.NET Core and Windows Forms are examples of application frameworks.</span></span> <span data-ttu-id="83072-163">「[ライブラリ](#library)」もご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-163">See also [library](#library).</span></span>

<span data-ttu-id="83072-164">以下の語句で使われている "フレームワーク" という用語には、さらに具体的な技術的意味があります。</span><span class="sxs-lookup"><span data-stu-id="83072-164">The word "framework" has a more specific technical meaning in the following terms:</span></span>
* [<span data-ttu-id="83072-165">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="83072-165">.NET Framework</span></span>](#net-framework)
* [<span data-ttu-id="83072-166">ターゲット フレームワーク</span><span class="sxs-lookup"><span data-stu-id="83072-166">target framework</span></span>](#target-framework)
* [<span data-ttu-id="83072-167">TFM (ターゲット フレームワーク モニカー)</span><span class="sxs-lookup"><span data-stu-id="83072-167">TFM (target framework moniker)</span></span>](#tfm)

<span data-ttu-id="83072-168">既存のドキュメントでは、[.NET の実装](#implementation-of-net)を指して "フレームワーク" が使われていることがあります。</span><span class="sxs-lookup"><span data-stu-id="83072-168">In the existing documentation, "framework" sometimes refers to an [implementation of .NET](#implementation-of-net).</span></span> <span data-ttu-id="83072-169">たとえば、.NET Core をフレームワークと呼んでいる場合があります。</span><span class="sxs-lookup"><span data-stu-id="83072-169">For example, an article may call .NET Core a framework.</span></span> <span data-ttu-id="83072-170">このような混乱を招く使用法をドキュメントから除去することが予定されています。</span><span class="sxs-lookup"><span data-stu-id="83072-170">We plan to eliminate this confusing usage from the documentation.</span></span>

## <a name="gc"></a><span data-ttu-id="83072-171">[GC]</span><span class="sxs-lookup"><span data-stu-id="83072-171">GC</span></span>

<span data-ttu-id="83072-172">ガベージ コレクター (Garbage Collector)。</span><span class="sxs-lookup"><span data-stu-id="83072-172">Garbage collector.</span></span>

<span data-ttu-id="83072-173">ガベージ コレクターは、自動メモリ管理の実装です。</span><span class="sxs-lookup"><span data-stu-id="83072-173">The garbage collector is an implementation of automatic memory management.</span></span>  <span data-ttu-id="83072-174">GC は、使われなくなったオブジェクトによって占有されているメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="83072-174">The GC frees memory occupied by objects that are no longer in use.</span></span> 

<span data-ttu-id="83072-175">「[ガベージ コレクション](garbage-collection/index.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-175">See [Garbage Collection](garbage-collection/index.md).</span></span>

## <a name="il"></a><span data-ttu-id="83072-176">IL</span><span class="sxs-lookup"><span data-stu-id="83072-176">IL</span></span>

<span data-ttu-id="83072-177">中間言語 (Intermediate Language)。</span><span class="sxs-lookup"><span data-stu-id="83072-177">Intermediate language.</span></span>

<span data-ttu-id="83072-178">C# などの高レベル .NET 言語は、中間言語 (IL) と呼ばれるハードウェアに依存しない命令セットにコンパイルされます。</span><span class="sxs-lookup"><span data-stu-id="83072-178">Higher-level .NET languages, such as C#, compile down to a hardware-agnostic instruction set, which is called Intermediate Language (IL).</span></span> <span data-ttu-id="83072-179">IL は、MSIL (Microsoft IL) や CIL (Common IL) などと呼ばれることもあります。</span><span class="sxs-lookup"><span data-stu-id="83072-179">IL is sometimes referred to as MSIL (Microsoft IL) or CIL (Common IL).</span></span>

## <a name="jit"></a><span data-ttu-id="83072-180">JIT</span><span class="sxs-lookup"><span data-stu-id="83072-180">JIT</span></span>

<span data-ttu-id="83072-181">Just-In-Time コンパイラ。</span><span class="sxs-lookup"><span data-stu-id="83072-181">Just-in-time compiler.</span></span>

<span data-ttu-id="83072-182">[AOT](#aot) と同様に、このコンパイラは [IL](#il) をプロセッサが理解するマシン コードに変換します。</span><span class="sxs-lookup"><span data-stu-id="83072-182">Similar to [AOT](#aot), this compiler translates [IL](#il) to machine code that the processor understands.</span></span> <span data-ttu-id="83072-183">AOT とは異なり、JIT のコンパイルはオンデマンドで行われ、コードを実行する必要があるコンピューター上で実行されます。</span><span class="sxs-lookup"><span data-stu-id="83072-183">Unlike AOT, JIT compilation happens on demand and is performed on the same machine that the code needs to run on.</span></span> <span data-ttu-id="83072-184">JIT コンパイルはアプリケーションの実行中に行われるため、コンパイル時間は実行時間の一部になります。</span><span class="sxs-lookup"><span data-stu-id="83072-184">Since JIT compilation occurs during execution of the application, compile time is part of the run time.</span></span> <span data-ttu-id="83072-185">したがって、JIT コンパイラでは、コードの最適化に要する時間と、結果のコードによって得られる時間の節約のバランスを考える必要があります。</span><span class="sxs-lookup"><span data-stu-id="83072-185">Thus, JIT compilers have to balance time spent optimizing code against the savings that the resulting code can produce.</span></span> <span data-ttu-id="83072-186">ただし、JIT は実際のハードウェアを認識するので、開発者はさまざまな実装を出荷する必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="83072-186">But a JIT knows the actual hardware and can free developers from having to ship different implementations.</span></span>

## <a name="implementation-of-net"></a><span data-ttu-id="83072-187">.NET の実装</span><span class="sxs-lookup"><span data-stu-id="83072-187">implementation of .NET</span></span>

<span data-ttu-id="83072-188">.NET の実装には次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="83072-188">An implementation of .NET includes the following:</span></span>

- <span data-ttu-id="83072-189">1 つまたは複数のランタイム。</span><span class="sxs-lookup"><span data-stu-id="83072-189">One or more runtimes.</span></span> <span data-ttu-id="83072-190">たとえば、CLR、CoreCLR CoreRT などです。</span><span class="sxs-lookup"><span data-stu-id="83072-190">Examples: CLR, CoreCLR, CoreRT.</span></span>
- <span data-ttu-id="83072-191">.NET Standard の 1 つのバージョンを実装し、他の API を含むことができるクラス ライブラリ。</span><span class="sxs-lookup"><span data-stu-id="83072-191">A class library that implements a version of the .NET Standard and may include additional APIs.</span></span> <span data-ttu-id="83072-192">たとえば、.NET Framework 基本クラス ライブラリや .NET Core 基本クラス ライブラリなどです。</span><span class="sxs-lookup"><span data-stu-id="83072-192">Examples: .NET Framework Base Class Library, .NET Core Base Class Library.</span></span>
- <span data-ttu-id="83072-193">必要に応じて、1 つまたは複数のアプリケーション フレームワーク。</span><span class="sxs-lookup"><span data-stu-id="83072-193">Optionally, one or more application frameworks.</span></span> <span data-ttu-id="83072-194">たとえば、.NET Framework には ASP.NET、Windows フォーム、WPF が含まれます。</span><span class="sxs-lookup"><span data-stu-id="83072-194">Examples: ASP.NET, Windows Forms, and WPF are included in the .NET Framework.</span></span>
- <span data-ttu-id="83072-195">必要に応じて、開発ツール。</span><span class="sxs-lookup"><span data-stu-id="83072-195">Optionally, development tools.</span></span> <span data-ttu-id="83072-196">一部の開発ツールは、複数の実装間で共有されます。</span><span class="sxs-lookup"><span data-stu-id="83072-196">Some development tools are shared among multiple implementations.</span></span>

<span data-ttu-id="83072-197">.NET の実装の例:</span><span class="sxs-lookup"><span data-stu-id="83072-197">Examples of .NET implementations:</span></span>

- [<span data-ttu-id="83072-198">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="83072-198">.NET Framework</span></span>](#net-framework)
- [<span data-ttu-id="83072-199">.NET Core</span><span class="sxs-lookup"><span data-stu-id="83072-199">.NET Core</span></span>](#net-core)
- [<span data-ttu-id="83072-200">ユニバーサル Windows プラットフォーム (UWP)</span><span class="sxs-lookup"><span data-stu-id="83072-200">Universal Windows Platform (UWP)</span></span>](#uwp)

## <a name="library"></a><span data-ttu-id="83072-201">ライブラリ</span><span class="sxs-lookup"><span data-stu-id="83072-201">library</span></span>

<span data-ttu-id="83072-202">アプリまたは他のライブラリで呼び出すことができる API のコレクション。</span><span class="sxs-lookup"><span data-stu-id="83072-202">A collection of APIs that can be called by apps or other libraries.</span></span> <span data-ttu-id="83072-203">.NET ライブラリは 1 つ以上の[アセンブリ](#assembly)で構成されます。</span><span class="sxs-lookup"><span data-stu-id="83072-203">A .NET library is composed of one or more [assemblies](#assembly).</span></span>

<span data-ttu-id="83072-204">ライブラリと[フレームワーク](#framework)は同義語として使われることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="83072-204">The words library and [framework](#framework) are often used synonymously.</span></span>

## <a name="metapackage"></a><span data-ttu-id="83072-205">メタパッケージ</span><span class="sxs-lookup"><span data-stu-id="83072-205">metapackage</span></span>

<span data-ttu-id="83072-206">それ自体のライブラリを持たず、依存するもののリストのみを含む NuGet パッケージ。</span><span class="sxs-lookup"><span data-stu-id="83072-206">A NuGet package that has no library of its own but is only a list of dependencies.</span></span> <span data-ttu-id="83072-207">含まれるパッケージは、必要に応じて、ターゲット フレームワーク用の API を確立できます。</span><span class="sxs-lookup"><span data-stu-id="83072-207">The included packages can optionally establish the API for a target framework.</span></span>

<span data-ttu-id="83072-208">「[パッケージ、メタパッケージ、フレームワーク](../core/packages.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-208">See [Packages, Metapackages and Frameworks](../core/packages.md)</span></span>

## <a name="mono"></a><span data-ttu-id="83072-209">Mono</span><span class="sxs-lookup"><span data-stu-id="83072-209">Mono</span></span>

<span data-ttu-id="83072-210">Mono はオープン ソースであり、主に小規模なランタイムが必要な場合に使用される[クロスプラットフォーム](#cross-platform)の .NET 実装です。</span><span class="sxs-lookup"><span data-stu-id="83072-210">Mono is an open source, [cross-platform](#cross-platform) .NET implementation that is mainly used when a small runtime is required.</span></span> <span data-ttu-id="83072-211">Android、Mac、iOS、tvOS、および watchOS 上の Xamarin アプリケーションで利用されるランタイムで、フットプリントが小さいアプリに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="83072-211">It is the runtime that powers Xamarin applications on Android, Mac, iOS, tvOS and watchOS and is focused primarily on apps that require a small footprint.</span></span>

<span data-ttu-id="83072-212">現在公開されているすべての .NET Standard バージョンをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="83072-212">It supports all of the currently published .NET Standard versions.</span></span>

<span data-ttu-id="83072-213">これまで Mono は .NET Framework の多数の API を実装し、Unix で人気の高い機能の一部をエミュレートしていました。</span><span class="sxs-lookup"><span data-stu-id="83072-213">Historically, Mono implemented the larger API of the .NET Framework and emulated some of the most popular capabilities on Unix.</span></span> <span data-ttu-id="83072-214">また、Unix のそのような機能に依存する .NET アプリケーションを実行するために使用されることもあります。</span><span class="sxs-lookup"><span data-stu-id="83072-214">It is sometimes used to run .NET applications that rely on those capabilities on Unix.</span></span>

<span data-ttu-id="83072-215">一般的に Mono は、Just-In-Time コンパイラと共に使用されますが、iOS のようなプラットフォームに使用される完全な静的コンパイラ (Ahead Of Time コンパイル) としても機能します。</span><span class="sxs-lookup"><span data-stu-id="83072-215">Mono is typically used with a just-in-time compiler, but it also features a full static compiler (ahead-of-time compilation) that is used on platforms like iOS.</span></span>

<span data-ttu-id="83072-216">Mono について詳しくは、[Mono のドキュメント](https://www.mono-project.com/docs/)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-216">To learn more about Mono, see the [Mono documentation](https://www.mono-project.com/docs/).</span></span>

## <a name="net"></a><span data-ttu-id="83072-217">.NET</span><span class="sxs-lookup"><span data-stu-id="83072-217">.NET</span></span>

<span data-ttu-id="83072-218">[.NET Standard](#net-standard) とすべての [.NET の実装](#implementation-of-net)およびワークロードを表す包括的な用語。</span><span class="sxs-lookup"><span data-stu-id="83072-218">The umbrella term for [.NET Standard](#net-standard) and all [.NET implementations](#implementation-of-net) and workloads.</span></span> <span data-ttu-id="83072-219">常にすべて大文字で表し、".Net" とは表記されません。</span><span class="sxs-lookup"><span data-stu-id="83072-219">Always capitalized, never ".Net".</span></span>

<span data-ttu-id="83072-220">「[.NET ガイド](index.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-220">See the [.NET Guide](index.md)</span></span>

## <a name="net-core"></a><span data-ttu-id="83072-221">.NET Core</span><span class="sxs-lookup"><span data-stu-id="83072-221">.NET Core</span></span> 

<span data-ttu-id="83072-222">.NET のクロスプラットフォームで高パフォーマンスなオープン ソースの実装。</span><span class="sxs-lookup"><span data-stu-id="83072-222">A cross-platform, high-performance, open source implementation of .NET.</span></span> <span data-ttu-id="83072-223">Core 共通言語ランタイム (CoreCLR)、Core AOT ランタイム (CoreRT、開発中)、Core 基本クラス ライブラリ、Core SDK が含まれます。</span><span class="sxs-lookup"><span data-stu-id="83072-223">Includes the Core Common Language Runtime (CoreCLR), the Core AOT Runtime (CoreRT, in development), the Core Base Class Library, and the Core SDK.</span></span>

<span data-ttu-id="83072-224">「[.NET Core](../core/index.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-224">See [.NET Core](../core/index.md).</span></span>

## <a name="net-core-cli"></a><span data-ttu-id="83072-225">.NET Core CLI</span><span class="sxs-lookup"><span data-stu-id="83072-225">.NET Core CLI</span></span>

<span data-ttu-id="83072-226">.NET Core アプリケーション開発用のクロスプラットフォーム ツールチェーン。</span><span class="sxs-lookup"><span data-stu-id="83072-226">A cross-platform toolchain for developing .NET Core applications.</span></span>

<span data-ttu-id="83072-227">「[.NET Core コマンドライン インターフェイス (CLI) ツール](../core/tools/index.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-227">See [.NET Core command-line interface (CLI) tools](../core/tools/index.md).</span></span>

## <a name="net-core-sdk"></a><span data-ttu-id="83072-228">.NET Core SDK</span><span class="sxs-lookup"><span data-stu-id="83072-228">.NET Core SDK</span></span>

<span data-ttu-id="83072-229">一連のライブラリとツールであり、開発者はこれを利用して .NET Core のアプリケーションやライブラリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="83072-229">A set of libraries and tools that allow developers to create .NET Core applications and libraries.</span></span> <span data-ttu-id="83072-230">アプリ構築用の [.NET Core CLI](#net-core-cli)、アプリの構築および実行用の .NET Core ライブラリとランタイム、CLI コマンドとアプリケーションを実行する dotnet 実行可能ファイル (*dotnet.exe*) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="83072-230">Includes the [.NET Core CLI](#net-core-cli) for building apps, .NET Core libraries and runtime for building and running apps, and the dotnet executable (*dotnet.exe*) that runs CLI commands and runs applications.</span></span>

<span data-ttu-id="83072-231">「[.NET Core SDK の概要](../core/sdk.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-231">See [.NET Core SDK Overview](../core/sdk.md).</span></span>

## <a name="net-framework"></a><span data-ttu-id="83072-232">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="83072-232">.NET Framework</span></span>

<span data-ttu-id="83072-233">Windows でのみ動作する .NET の実装。</span><span class="sxs-lookup"><span data-stu-id="83072-233">An implementation of .NET that runs only on Windows.</span></span> <span data-ttu-id="83072-234">共通言語ランタイム (CLR)、基本クラス ライブラリ、および ASP.NET、Windows フォーム、WPF などのアプリケーション フレームワーク ライブラリが含まれます。</span><span class="sxs-lookup"><span data-stu-id="83072-234">Includes the Common Language Runtime (CLR), the Base Class Library, and application framework libraries such as ASP.NET, Windows Forms, and WPF.</span></span>

<span data-ttu-id="83072-235">「[.NET Framework ガイド](../framework/index.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-235">See [.NET Framework Guide](../framework/index.md).</span></span>

## <a name="net-native"></a><span data-ttu-id="83072-236">.NET Native</span><span class="sxs-lookup"><span data-stu-id="83072-236">.NET Native</span></span>

<span data-ttu-id="83072-237">Just-In-Time (JIT) ではなく Ahead Of Time (AOT) でネイティブ コードを生成するコンパイラ ツール チェーン。</span><span class="sxs-lookup"><span data-stu-id="83072-237">A compiler tool chain that produces native code ahead-of-time (AOT), as opposed to just-in-time (JIT).</span></span>

<span data-ttu-id="83072-238">コンパイルは、C++ のコンパイラやリンカーと同様に、開発者のコンピューターで行われます。</span><span class="sxs-lookup"><span data-stu-id="83072-238">Compilation happens on the developer's machine similar to the way a C++ compiler and linker works.</span></span> <span data-ttu-id="83072-239">未使用のコードが削除され、より多くの時間がコードの最適化に費やされます。</span><span class="sxs-lookup"><span data-stu-id="83072-239">It removes unused code and spends more time optimizing it.</span></span> <span data-ttu-id="83072-240">ライブラリからコードを抽出し、実行可能ファイルにそれらをマージします。</span><span class="sxs-lookup"><span data-stu-id="83072-240">It extracts code from libraries and merges them into the executable.</span></span> <span data-ttu-id="83072-241">結果は、アプリ全体を表す 1 つのモジュールです。</span><span class="sxs-lookup"><span data-stu-id="83072-241">The result is a single module that represents the entire app.</span></span>

<span data-ttu-id="83072-242">UWP は、.NET Native によってサポートされる最初のアプリケーション フレームワークでした。</span><span class="sxs-lookup"><span data-stu-id="83072-242">UWP was the first application framework supported by .NET Native.</span></span> <span data-ttu-id="83072-243">現在では、Windows、macOS、Linux 用のネイティブ コンソール アプリの構築がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="83072-243">Now, we support building native console apps for Windows, macOS, and Linux.</span></span>

<span data-ttu-id="83072-244">「[Intro to .NET Native and CoreRT](https://github.com/dotnet/corert/blob/master/Documentation/intro-to-corert.md)」(.NET Native と CoreRT の概要) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-244">See [Intro to .NET Native and CoreRT](https://github.com/dotnet/corert/blob/master/Documentation/intro-to-corert.md)</span></span>

## <a name="net-standard"></a><span data-ttu-id="83072-245">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="83072-245">.NET Standard</span></span>

<span data-ttu-id="83072-246">.NET の各実装で使用可能な .NET API の正式な仕様。</span><span class="sxs-lookup"><span data-stu-id="83072-246">A formal specification of .NET APIs that are available in each .NET implementation.</span></span>

<span data-ttu-id="83072-247">.NET Standard の仕様は、ドキュメントではライブラリとも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="83072-247">The .NET Standard specification is sometimes called a library in the documentation.</span></span> <span data-ttu-id="83072-248">ライブラリには仕様 (インターフェイス) だけでなく API の実装も含まれるため、.NET Standard を "ライブラリ" と呼ぶのは誤解を招きます。</span><span class="sxs-lookup"><span data-stu-id="83072-248">Because a library includes API implementations, not only specifications (interfaces), it's misleading to call .NET Standard a "library."</span></span> <span data-ttu-id="83072-249">.NET Standard メタパッケージ (`NETStandard.Library`) の名前を参照する場合を除き、そのような使用法をドキュメントから消去する予定です。</span><span class="sxs-lookup"><span data-stu-id="83072-249">We plan to eliminate that usage from the documentation, except in reference to the name of the .NET Standard metapackage (`NETStandard.Library`).</span></span>

<span data-ttu-id="83072-250">「[.NET Standard](net-standard.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-250">See [.NET Standard](net-standard.md).</span></span>

## <a name="ngen"></a><span data-ttu-id="83072-251">NGEN</span><span class="sxs-lookup"><span data-stu-id="83072-251">NGEN</span></span>

<span data-ttu-id="83072-252">ネイティブ (イメージ) 生成。</span><span class="sxs-lookup"><span data-stu-id="83072-252">Native (image) generation.</span></span>

<span data-ttu-id="83072-253">このテクノロジは、永続的な JIT コンパイラと考えることができます。</span><span class="sxs-lookup"><span data-stu-id="83072-253">You can think of this technology as a persistent JIT compiler.</span></span> <span data-ttu-id="83072-254">通常はコードが実行されるコンピューター上でコードをコンパイルしますが、一般にコンパイルはインストール時に行われます。</span><span class="sxs-lookup"><span data-stu-id="83072-254">It usually compiles code on the machine where the code is executed, but compilation typically occurs at install time.</span></span>

## <a name="package"></a><span data-ttu-id="83072-255">package</span><span class="sxs-lookup"><span data-stu-id="83072-255">package</span></span>

<span data-ttu-id="83072-256">NuGet パッケージ &mdash; または単にパッケージ &mdash; は、同じ名前の 1 つまたは複数のアセンブリと、作成者名などの追加メタデータを含む、*.zip* ファイルです。</span><span class="sxs-lookup"><span data-stu-id="83072-256">A NuGet package &mdash; or just a package &mdash; is a *.zip* file with one or more assemblies of the same name along with additional metadata such as the author name.</span></span>

<span data-ttu-id="83072-257">*.zip* ファイルは、拡張子が *.nupkg* であり、複数のターゲット フレームワークとバージョンで使う *.dll* ファイルや *.xml* ファイルなどのアセットを含むことができます。</span><span class="sxs-lookup"><span data-stu-id="83072-257">The *.zip* file has a *.nupkg* extension and may contain assets, such as *.dll* files and *.xml* files, for use with multiple target frameworks and versions.</span></span> <span data-ttu-id="83072-258">アプリまたはライブラリでインストールされるときに、アプリまたはライブラリで指定されているターゲット フレームワークに基づいて適切なアセットが選択されます。</span><span class="sxs-lookup"><span data-stu-id="83072-258">When installed in an app or library, the appropriate assets are selected based on the target framework specified by the app or library.</span></span> <span data-ttu-id="83072-259">インターフェイスを定義するアセットは *ref* フォルダーにあり、実装を定義するアセットは *lib* フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="83072-259">The assets that define the interface are in the *ref* folder, and the assets that define the implementation are in the *lib* folder.</span></span>

## <a name="platform"></a><span data-ttu-id="83072-260">platform</span><span class="sxs-lookup"><span data-stu-id="83072-260">platform</span></span>

<span data-ttu-id="83072-261">オペレーティング システムとそれが動作するハードウェア (Windows、macOS、Linux、iOS、Android)。</span><span class="sxs-lookup"><span data-stu-id="83072-261">An operating system and the hardware it runs on, such as Windows, macOS, Linux, iOS, and Android.</span></span>

<span data-ttu-id="83072-262">文章での使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="83072-262">Here are examples of usage in sentences:</span></span>

- <span data-ttu-id="83072-263">".NET Core は、.NET のクロスプラットフォームの実装です。"</span><span class="sxs-lookup"><span data-stu-id="83072-263">".NET Core is a cross-platform implementation of .NET."</span></span> 
- <span data-ttu-id="83072-264">"PCL プロファイルは Microsoft のプラットフォームを表し、.NET Standard はプラットフォームに依存しません。"</span><span class="sxs-lookup"><span data-stu-id="83072-264">"PCL profiles represent Microsoft platforms, while the .NET Standard is agnostic to platform."</span></span>

<span data-ttu-id="83072-265">.NET のドキュメントでは、.NET の実装またはすべての実装を含む .NET スタックの意味で ".NET プラットフォーム" が使われることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="83072-265">The .NET documentation frequently uses ".NET platform" to mean either an implementation of .NET or the .NET stack including all implementations.</span></span> <span data-ttu-id="83072-266">これらの使用法はどちらも本来の (OS/ハードウェア) の意味と紛らわしい場合があるので、ドキュメントから削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="83072-266">Both of these usages tend to get confused with the primary (OS/hardware) meaning, so we plan to eliminate these usages from the documentation.</span></span>

## <a name="runtime"></a><span data-ttu-id="83072-267">ランタイム</span><span class="sxs-lookup"><span data-stu-id="83072-267">runtime</span></span>

<span data-ttu-id="83072-268">マネージド プログラムの実行環境。</span><span class="sxs-lookup"><span data-stu-id="83072-268">The execution environment for a managed program.</span></span>

<span data-ttu-id="83072-269">OS は、ランタイム環境の一部ですが、.NET ランタイムの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="83072-269">The OS is part of the runtime environment but is not part of the .NET runtime.</span></span> <span data-ttu-id="83072-270">.NET ランタイムの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="83072-270">Here are some examples of .NET runtimes:</span></span>

- <span data-ttu-id="83072-271">共通言語ランタイム (CLR)</span><span class="sxs-lookup"><span data-stu-id="83072-271">Common Language Runtime (CLR)</span></span>
- <span data-ttu-id="83072-272">Core 共通言語ランタイム (CoreCLR)</span><span class="sxs-lookup"><span data-stu-id="83072-272">Core Common Language Runtime (CoreCLR)</span></span>
- <span data-ttu-id="83072-273">.NET Native (UWP の場合)</span><span class="sxs-lookup"><span data-stu-id="83072-273">.NET Native (for UWP)</span></span>
- <span data-ttu-id="83072-274">Mono ランタイム</span><span class="sxs-lookup"><span data-stu-id="83072-274">Mono runtime</span></span>

<span data-ttu-id="83072-275">.NET のドキュメントでは、.NET の実装の意味で "ランタイム" が使われることがあります。</span><span class="sxs-lookup"><span data-stu-id="83072-275">The .NET documentation sometimes uses "runtime" to mean an implementation of .NET.</span></span> <span data-ttu-id="83072-276">たとえば、次の文章の "ランタイム" は "実装" に置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="83072-276">For example, in the following sentences "runtime" should be replaced with "implementation":</span></span>

- <span data-ttu-id="83072-277">"さまざまな .NET ランタイムで、.NET Standard の特定のバージョンが実装されます。"</span><span class="sxs-lookup"><span data-stu-id="83072-277">"The various .NET runtimes implement specific versions of .NET Standard."</span></span>
- <span data-ttu-id="83072-278">"複数のランタイムでの実行を意図したライブラリは、このフレームワークを対象とする必要があります。"</span><span class="sxs-lookup"><span data-stu-id="83072-278">"Libraries that are intended to run on multiple runtimes should target this framework."</span></span> <span data-ttu-id="83072-279">(.NET Standard を指している場合)</span><span class="sxs-lookup"><span data-stu-id="83072-279">(referring to .NET Standard)</span></span>
- <span data-ttu-id="83072-280">"さまざまな .NET ランタイムで、.NET Standard の特定のバージョンが実装されます。</span><span class="sxs-lookup"><span data-stu-id="83072-280">"The various .NET runtimes implement specific versions of .NET Standard.</span></span> <span data-ttu-id="83072-281">…</span><span class="sxs-lookup"><span data-stu-id="83072-281">…</span></span> <span data-ttu-id="83072-282">.NET ランタイムの各バージョンは、サポートしている .NET Standard の最高のバージョンをアドバタイズします …"</span><span class="sxs-lookup"><span data-stu-id="83072-282">Each .NET runtime version advertises the highest .NET Standard version it supports …"</span></span>

<span data-ttu-id="83072-283">このような一貫性のない使用法は除去される予定です。</span><span class="sxs-lookup"><span data-stu-id="83072-283">We plan to eliminate this inconsistent usage.</span></span> 

## <a name="stack"></a><span data-ttu-id="83072-284">スタック</span><span class="sxs-lookup"><span data-stu-id="83072-284">stack</span></span>

<span data-ttu-id="83072-285">全体としてアプリケーションの構築と実行に使われるプログラミング テクノロジのセット。</span><span class="sxs-lookup"><span data-stu-id="83072-285">A set of programming technologies that are used together to build and run applications.</span></span>

<span data-ttu-id="83072-286">".NET スタック" は、.NET Standard および .NET のすべての実装を指します。</span><span class="sxs-lookup"><span data-stu-id="83072-286">"The .NET stack" refers to the .NET Standard and all .NET implementations.</span></span> <span data-ttu-id="83072-287">".NET スタック" という語句が .NET の 1 つの実装を示すこともあります。</span><span class="sxs-lookup"><span data-stu-id="83072-287">The phrase "a .NET stack" may refer to one implementation of .NET.</span></span> 

## <a name="target-framework"></a><span data-ttu-id="83072-288">対象フレーム</span><span class="sxs-lookup"><span data-stu-id="83072-288">target framework</span></span>

<span data-ttu-id="83072-289">.NET アプリまたはライブラリが依存する API のコレクション。</span><span class="sxs-lookup"><span data-stu-id="83072-289">The collection of APIs that a .NET app or library relies on.</span></span>

<span data-ttu-id="83072-290">アプリまたはライブラリは、.NET Standard の 1 つのバージョン (.NET Standard 2.0 など) をターゲットにできます。 .NET Standard は、.NET のすべての実装で標準化された API のセットの仕様です。</span><span class="sxs-lookup"><span data-stu-id="83072-290">An app or library can target a version of .NET Standard (for example, .NET Standard 2.0), which is specification for a standardized set of APIs across all .NET implementations.</span></span> <span data-ttu-id="83072-291">また、アプリまたはライブラリは、.NET の特定の実装のバージョンをターゲットにすることもでき、その場合は実装固有の API にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="83072-291">An app or library can also target a version of a specific .NET implementation, in which case it gets access to implementation-specific APIs.</span></span> <span data-ttu-id="83072-292">たとえば、Xamarin.iOS をターゲットにするアプリは、Xamarin が提供する iOS API ラッパーにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="83072-292">For example, an app that targets Xamarin.iOS gets access to Xamarin-provided iOS API wrappers.</span></span>

<span data-ttu-id="83072-293">一部のターゲット フレームワーク (.NET Framework など) では、使用可能な API は .NET の実装がシステムにインストールするアセンブリによって定義され、アプリケーション フレームワーク API (たとえば ASP.NET、WinForms) を含む場合があります。</span><span class="sxs-lookup"><span data-stu-id="83072-293">For some target frameworks (for example, the .NET Framework) the available APIs are defined by the assemblies that a .NET implementation installs on a system, which may include application framework APIs (for example, ASP.NET, WinForms).</span></span> <span data-ttu-id="83072-294">パッケージ ベースのターゲット フレームワーク (.NET Standard、.NET Core など) では、フレームワーク API はアプリまたはライブラリでインストールされるパッケージによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="83072-294">For package-based target frameworks (such as .NET Standard and .NET Core), the framework APIs are defined by the packages installed in the app or library.</span></span> <span data-ttu-id="83072-295">その場合、ターゲット フレームワークでは、全体としてフレームワークを構成するすべてのパッケージを参照するメタパッケージが暗黙的に指定されます。</span><span class="sxs-lookup"><span data-stu-id="83072-295">In that case, the target framework implicitly specifies a metapackage that references all the packages that together make up the framework.</span></span>

<span data-ttu-id="83072-296">「[ターゲット フレームワーク](frameworks.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-296">See [Target Frameworks](frameworks.md).</span></span>

## <a name="tfm"></a><span data-ttu-id="83072-297">TFM</span><span class="sxs-lookup"><span data-stu-id="83072-297">TFM</span></span>

<span data-ttu-id="83072-298">ターゲット フレームワーク モニカー (Target Framework Moniker)。</span><span class="sxs-lookup"><span data-stu-id="83072-298">Target framework moniker.</span></span>

<span data-ttu-id="83072-299">.NET アプリまたはライブラリのターゲット フレームワークを指定するための標準化されたトークン形式。</span><span class="sxs-lookup"><span data-stu-id="83072-299">A standardized token format for specifying the target framework of a .NET app or library.</span></span> <span data-ttu-id="83072-300">通常、ターゲット フレームワークは短い名前によって参照されます (`net462` など)。</span><span class="sxs-lookup"><span data-stu-id="83072-300">Target frameworks are typically referenced by a short name, such as `net462`.</span></span> <span data-ttu-id="83072-301">長い形式の TFM (.NETFramework,Version=4.6.2 など) も存在しますが、一般に、ターゲット フレームワークの指定には使われません。</span><span class="sxs-lookup"><span data-stu-id="83072-301">Long-form TFMs (such as .NETFramework,Version=4.6.2) exist but are not generally used to specify a target framework.</span></span>

<span data-ttu-id="83072-302">「[ターゲット フレームワーク](frameworks.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="83072-302">See [Target Frameworks](frameworks.md).</span></span>

## <a name="uwp"></a><span data-ttu-id="83072-303">UWP</span><span class="sxs-lookup"><span data-stu-id="83072-303">UWP</span></span>

<span data-ttu-id="83072-304">ユニバーサル Windows プラットフォーム (Universal Windows Platform)。</span><span class="sxs-lookup"><span data-stu-id="83072-304">Universal Windows Platform.</span></span>

<span data-ttu-id="83072-305">モノのインターネット (IoT) のために最新のタッチ対応の Windows アプリケーションとソフトウェアを構築するために使われる .NET の実装。</span><span class="sxs-lookup"><span data-stu-id="83072-305">An implementation of .NET that is used for building modern, touch-enabled Windows applications and software for the Internet of Things (IoT).</span></span> <span data-ttu-id="83072-306">PC、タブレット、ファブレット、携帯電話、Xbox など、ターゲットにする可能性があるさまざまな種類のデバイスを統一するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="83072-306">It's designed to unify the different types of devices that you may want to target, including PCs, tablets, phablets, phones, and even the Xbox.</span></span> <span data-ttu-id="83072-307">UWP は、一元的なアプリ ストア、実行環境 (AppContainer)、Win32 の代わりに使う Windows API のセット (WinRT) など、多くのサービスを提供します。</span><span class="sxs-lookup"><span data-stu-id="83072-307">UWP provides many services, such as a centralized app store, an execution environment (AppContainer), and a set of Windows APIs to use instead of Win32 (WinRT).</span></span> <span data-ttu-id="83072-308">アプリは、C++、C#、VB.NET、および JavaScript で記述することができます。</span><span class="sxs-lookup"><span data-stu-id="83072-308">Apps can be written in C++, C#, VB.NET, and JavaScript.</span></span> <span data-ttu-id="83072-309">C# と VB.NET を使うときは、.NET Core によって .NET API が提供されます。</span><span class="sxs-lookup"><span data-stu-id="83072-309">When using C# and VB.NET, the .NET APIs are provided by .NET Core.</span></span>

## <a name="see-also"></a><span data-ttu-id="83072-310">関連項目</span><span class="sxs-lookup"><span data-stu-id="83072-310">See also</span></span>

- [<span data-ttu-id="83072-311">.NET のガイド</span><span class="sxs-lookup"><span data-stu-id="83072-311">.NET Guide</span></span>](index.md)  
- [<span data-ttu-id="83072-312">.NET Framework ガイド</span><span class="sxs-lookup"><span data-stu-id="83072-312">.NET Framework Guide</span></span>](../framework/index.md)  
- [<span data-ttu-id="83072-313">.NET Core</span><span class="sxs-lookup"><span data-stu-id="83072-313">.NET Core</span></span>](../core/index.md)  
- [<span data-ttu-id="83072-314">ASP.NET の概要</span><span class="sxs-lookup"><span data-stu-id="83072-314">ASP.NET Overview</span></span>](/aspnet/index#pivot=aspnet)  
- [<span data-ttu-id="83072-315">ASP.NET Core の概要</span><span class="sxs-lookup"><span data-stu-id="83072-315">ASP.NET Core Overview</span></span>](/aspnet/index#pivot=core)  
