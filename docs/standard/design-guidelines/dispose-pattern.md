---
title: Dispose パターン
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- Dispose method
- class library design guidelines [.NET Framework], Dispose method
- class library design guidelines [.NET Framework], Finalize method
- customizing Dispose method name
- Finalize method
ms.assetid: 31a6c13b-d6a2-492b-9a9f-e5238c983bcb
author: KrzysztofCwalina
ms.openlocfilehash: ee6e9898ae93e2e6628eadec150a3c9c05f5d9c5
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53147718"
---
# <a name="dispose-pattern"></a>Dispose パターン
すべてのプログラムは、実行の進行中に、メモリ、システムのハンドル、データベース接続など、1 つまたは複数のシステム リソースを取得します。 開発者は、取得して使用後に解放する必要があるために、このようなシステム リソースを使用するには注意する必要があります。  
  
 CLR では、自動メモリ管理のサポートを提供します。 マネージ メモリ (c# の演算子を使用して割り当てられたメモリ`new`) 明示的に解放する必要はありません。 ガベージ コレクター (GC) によって自動的に解放されます。 これにより、メモリの解放の難しい面倒な作業から開発者を解放し、これまでにない生産性を .NET Framework によって提供される主な理由の 1 でしょう。  
  
 残念ながら、マネージ メモリは、さまざまな種類のシステム リソースの 1 つです。 マネージ メモリ以外のリソースは、明示的に解放する必要がまだとアンマネージ リソースとして参照されます。 GC は、具体的には設計されていません、このようなアンマネージ リソースの管理、開発者の手でアンマネージ リソースを管理する責任があることを意味します。  
  
 CLR では、アンマネージ リソースを解放するときにいくつかのヘルプを提供します。 <xref:System.Object?displayProperty=nameWithType> 仮想メソッドを宣言<xref:System.Object.Finalize%2A>(ファイナライザーとも呼ばれます)、オブジェクトのメモリが GC によって解放され、アンマネージ リソースを解放をオーバーライドする前に、GC によって呼び出されます。 ファイナライザーをオーバーライドする型は、ファイナライズ可能な型と呼ばれます。  
  
 ファイナライザーはいくつかのクリーンアップのシナリオで有効になりますが、2 つの重要な欠点があります。  
  
-   GC で検出されるオブジェクトがコレクションの対象である、ファイナライザーが呼び出されます。 これは未確定一定時間後、リソースは必要ありません。 開発者がでしたまたはリソースとリソースが実際には、ファイナライザーによってリリースときの時刻をリリースするまでの遅延がでプログラムが不足している多くのリソース (リソースを簡単に使い果たされる可能性) を取得または許容できない可能性があります。リソースの使用 (大規模なアンマネージ メモリ バッファーなど) に保持するコストがかかる場合です。  
  
-   CLR は、ファイナライザーを呼び出す必要がある、ときに、次のラウンドのガベージ コレクション (コレクション間で実行するファイナライザー) まで、オブジェクトのメモリのコレクションを延期する必要があります。 これは、オブジェクトのメモリ (およびすべてのオブジェクトを参照) が、時間の長い期間に解放されないことを意味します。  
  
 そのため、ファイナライザーにのみ依存できない可能性がありますかを高パフォーマンスの高いシナリオで不足しているリソースを扱うとき、できるだけ迅速にアンマネージ リソースを解放する必要がある場合、多くのシナリオで適切な GC オーバーヘッドを追加しましたファイナライズは許されません。  
  
 フレームワークは、提供、<xref:System.IDisposable?displayProperty=nameWithType>不要なとすぐには、アンマネージ リソースを解放する手動の方法を開発者に提供するために実装するインターフェイス。 用意されています、<xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType>するように、GC が知ることができるメソッド オブジェクトが手動で破棄され、場合、オブジェクトのメモリを再要求できる前なくなった場合に、終了する必要はありません。 実装する型、`IDisposable`インターフェイス破棄可能な型として参照されます。  
  
 Dispose パターンは、使用状況とファイナライザーの実装を標準化するためのものと`IDisposable`インターフェイス。  
  
 実装の複雑さを軽減するパターンの主な動機は、<xref:System.Object.Finalize%2A>と<xref:System.IDisposable.Dispose%2A>メソッド。 複雑なメソッドがいくつかのコード パスが (相違点は、章の説明) を共有するという事実に由来します。 さらに、確定的なリソース管理のための言語サポートの進化に関連するパターンの一部の要素の歴史的な理由があります。  
  
 **✓ DO** 破棄可能な型のインスタンスを含む型で、基本的な Dispose パターンを実装します。 参照してください、 [Dispose パターンの基本的な](#basic_pattern)基本的なパターンの詳細セクション。  
  
 型が破棄可能なその他のオブジェクトの有効期間にわたって担当する場合は、開発者にも、それらを破棄する方法が必要があります。 コンテナーの使用`Dispose`メソッドは、これを可能にする便利な方法です。  
  
 **✓ DO** 基本の Dispose パターンを実装し、保持しているリソースを明示的に解放できる必要があると、ファイナライザーがない型でファイナライザーを用意します。  
  
 たとえば、アンマネージ メモリ バッファーに格納する型のパターンを実装する必要があります。 [ファイナライズ可能な型](#finalizable_types)に関連するファイナライザーを実装するガイドラインについて説明します。  
  
 **✓ CONSIDER** 基本の Dispose パターンを実装するクラスでのリソースとアンマネージ自体を保持しないことや、破棄可能なオブジェクトは、実行のサブタイプをされている可能性がします。  
  
 これの良い例は、<xref:System.IO.Stream?displayProperty=nameWithType>クラス。 すべてのリソースを保持しない抽象基本クラスが、そのサブクラスのほとんどの操作を行い、このため、このパターンを実装します。  
  
<a name="basic_pattern"></a>   
## <a name="basic-dispose-pattern"></a>基本的な Dispose パターン  
 基本的なパターンの実装では、実装する必要があります、`System.IDisposable`インターフェイスと宣言する、`Dispose(bool)`間で共有するすべてのリソースのクリーンアップ ロジックを実装するメソッド、`Dispose`メソッドと省略可能な終了します。  
  
 次の例は、基本的なパターンの単純な実装を示しています。  
  
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
  
 ブール型パラメーター`disposing`から呼び出されたメソッドであるかどうかを示す、`IDisposable.Dispose`実装、それともファイナライザーか。 `Dispose(bool)`実装は、その他の参照オブジェクト (上記のサンプルのリソース フィールドなど) にアクセスする前に、パラメーターを確認する必要があります。 このようなオブジェクトから、メソッドが呼び出された場合にのみアクセスする必要があります、`IDisposable.Dispose`実装 (ときに、`disposing`パラメーターが true に等しい)。 メソッドがファイナライザーから呼び出される場合 (`disposing`は false)、その他のオブジェクトへのアクセスはできません。 理由は、予期しない順序でオブジェクトがファイナライズし、そのため、またはその依存関係のいずれかが既にファイナライズされていることです。  
  
 また、このセクションでは、Dispose パターンを実装しないベース クラスに適用されます。 既にパターンを実装するクラスを継承する場合はオーバーライドするだけで、`Dispose(bool)`追加のリソースのクリーンアップ ロジックを提供するメソッド。  
  
 **✓ DO** 宣言、`protected virtual void Dispose(bool disposing)`アンマネージ リソースの解放に関連するすべてのロジックを集中管理するメソッド。  
  
 このメソッドでは、すべてのリソースのクリーンアップを実行します。 メソッドは、両方のファイナライザーから、`IDisposable.Dispose`メソッド。 パラメーターは、ファイナライザーの内部から呼び出されている場合は false になります。 これを使用して終了処理中に実行されるコードは、ファイナライズ可能なその他のオブジェクトにアクセスしていないことを確認してください。 ファイナライザーの実装の詳細については、次のセクションで説明します。  
  
```csharp
protected virtual void Dispose(bool disposing) {  
    if (disposing) {  
        if (resource!= null) resource.Dispose();  
    }  
}  
```  
  
 **✓ DO** 実装、`IDisposable`だけ呼び出すことによってインターフェイス`Dispose(true)`続く`GC.SuppressFinalize(this)`です。  
  
 呼び出し`SuppressFinalize`場合にのみ発生`Dispose(true)`正常に実行されます。  
  
```csharp
public void Dispose(){  
    Dispose(true);  
    GC.SuppressFinalize(this);  
}  
```  
  
 **X DO NOT** パラメーターなしで行う`Dispose`仮想メソッドです。  
  
 `Dispose(bool)`メソッドは、1 つのサブクラスによってオーバーライドする必要があります。  
  
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
  
 **X DO NOT** のすべてのオーバー ロードを宣言、`Dispose`以外のメソッド`Dispose()`と`Dispose(bool)`です。  
  
 `Dispose` このパターンを体系化し、実装者、ユーザー、およびコンパイラの間で混乱を避けるために予約語を考慮必要があります。 一部の言語は、特定の種類を自動的にこのパターンを実装することができます。  
  
 **✓ DO** を許可する、`Dispose(bool)`に複数回呼び出されるメソッド。 メソッドは、最初に呼び出した後何もしないこともできます。  
  
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
  
 **X AVOID** 内から例外をスローして`Dispose(bool)`されている重要な状況で格納しているプロセスが破損している場合を除き (リークを一貫性のない共有状態などです。)。  
  
 ユーザーが期待する呼び出しを`Dispose`例外は発生しません。  
  
 場合`Dispose`例外を発生させる可能性があります、さらに finally ブロックのクリーンアップ ロジックは実行されません。 この問題を回避するは、ユーザーはすべての呼び出しをラップする必要がある`Dispose`(内で、finally ブロック!)、try ブロックで非常に複雑なクリーンアップのハンドラーにつながります。 実行している場合、`Dispose(bool disposing)`メソッド、破棄が false の場合は例外をスローしません。 これにより、ファイナライザーのコンテキスト内で実行している場合、プロセスが終了します。  
  
 **✓ DO** スロー、<xref:System.ObjectDisposedException>オブジェクトが破棄された後は使用できませんのすべてのメンバーからです。  
  
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
  
 **✓ CONSIDER** メソッドを提供する`Close()`に加え、`Dispose()`領域での一般的な用語が閉じるかどうかは。  
  
 重要ではこれを行うときに、`Close`実装と同じ`Dispose`の実装を検討し、`IDisposable.Dispose`メソッド明示的にします。  
  
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
## <a name="finalizable-types"></a>ファイナライズ可能な型  
 ファイナライズ可能な型がファイナライザーをオーバーライドし、ファイナライズ コード パスを提供することによって、基本的な Dispose パターンを拡張する型、`Dispose(bool)`メソッド。  
  
 ファイナライザーは、主に、実行中に、システムの状態に関する (通常は有効な) 仮定することはできませんので、正しく実装するために非常に困難です。 次のガイドラインを考慮して慎重に検討にする必要があります。  
  
 いないだけに適用のガイドラインに注意してください、`Finalize`メソッド、ファイナライザーから呼び出された任意のコードには。 内で実行されるロジックの場合は、基本的な Dispose パターン以前に定義した、つまり`Dispose(bool disposing)`ときに、`disposing`パラメーターは false。  
  
 オーバーライドが必要ない場合は、基本クラスは、既にファイナライズ可能なおよび基本的な Dispose パターンを実装、`Finalize`もう一度です。 だけオーバーライドする代わりに、`Dispose(bool)`追加のリソースのクリーンアップ ロジックを提供するメソッド。  
  
 次のコードでは、ファイナライズ可能な型の例を示します。  
  
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
  
 **X AVOID** ファイナライズ可能な型を作成します。  
  
 思わファイナライザーが必要なケースを慎重に検討します。 実際のパフォーマンスとコードの両方の複雑さの観点から、ファイナライザーを持つインスタンスに関連付けられているコスト。 などのリソースのラッパーを使用して必要に応じて<xref:System.Runtime.InteropServices.SafeHandle>をアンマネージ リソースをカプセル化可能であれば、その場合、ファイナライザーが不要になるラッパーが、独自のリソースのクリーンアップを行うためです。  
  
 **X DO NOT** ファイナライズ可能な値の型を作成します。  
  
 実際に参照型のみが、CLR で確定取得し、つまり値型にファイナライザーを配置しようとするとは無視されます。 C# および C++ コンパイラは、この規則を適用します。  
  
 **✓ DO** 型は独自のファイナライザーがない、アンマネージ リソースを解放する必要がある場合の種類をファイナライズようにします。  
  
 ファイナライザーを実装するときにだけ呼び出す`Dispose(false)`内のすべてのリソースのクリーンアップ ロジックを配置し、`Dispose(bool disposing)`メソッド。  
  
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
  
 **✓ DO** ファイナライズ可能な型で、基本的な Dispose パターンを実装します。  
  
 これにより、型のユーザーは、ファイナライザーが責任はそれらのリソースのクリーンアップが決定的を明示的に実行することを意味します。  
  
 **X DO NOT** こと、が既に終了されている重大なリスクがあるため、ファイナライザーのコード パスに、ファイナライズ可能なオブジェクトにアクセスします。  
  
 たとえば、別のファイナライズ可能なオブジェクト B を参照しているファイナライズ可能なオブジェクト、信頼性の高い方法では使用できません B A のファイナライザー、またはその逆です。 (クリティカル ファイナライズの弱い順序保証) する場合を除きランダムな順序では、ファイナライザーが呼び出されます。  
  
 また、アプリケーション ドメインのアンロード中またはプロセスの終了中に、静的変数に格納されているオブジェクトは特定の時点で収集取得こともあります。 ファイナライズ可能なオブジェクト (または静的変数に格納された値を使用する静的メソッドを呼び出す) を参照する静的変数ができない可能性がありますにアクセスする場合は安全な<xref:System.Environment.HasShutdownStarted%2A?displayProperty=nameWithType>true を返します。  
  
 **✓ DO** ように、`Finalize`保護されているメソッド。  
  
 C#、C++、および VB.NET の開発者は、コンパイラはこのガイドラインを適用する役立つため、これについて心配する必要はありません。  
  
 **X DO NOT** システムに重大な障害を除く、ファイナライザーのロジックから使用すると、例外のエスケープします。  
  
 CLR がシャット ダウン (時点で、.NET Framework version 2.0)、プロセス全体をファイナライザーから例外がスローされた場合は実行されず、制御された方法でリリースされているリソースその他のファイナライザーを防止します。  
  
 **✓ CONSIDER** を作成して、重要なファイナライズ可能なオブジェクトを使用して (を含む型階層を持つ型<xref:System.Runtime.ConstrainedExecution.CriticalFinalizerObject>) の状況でファイナライザーどうしても必要があります実行発生した場合でも強制アプリケーション ドメインのアンロード スレッド中止します。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *Pearson Education, Inc. からのアクセス許可によって了承を得て転載[Framework デザイン ガイドライン。規則、手法、および再利用可能な .NET ライブラリの第 2 版のパターン](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)Krzysztof Cwalina、Brad 内容では、Microsoft Windows の開発シリーズの一部として、Addison-wesley Professional、2008 年 10 月 22日を公開します。*  
  
## <a name="see-also"></a>関連項目

- <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType>  
- <xref:System.Object.Finalize%2A?displayProperty=nameWithType>  
- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
- [共通デザイン パターン](../../../docs/standard/design-guidelines/common-design-patterns.md)  
- [ガベージ コレクション](../../../docs/standard/garbage-collection/index.md)
