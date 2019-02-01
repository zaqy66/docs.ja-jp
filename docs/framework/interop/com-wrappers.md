---
title: COM ラッパー
ms.date: 03/30/2017
helpviewer_keywords:
- wrapper classes
- COM interop, COM wrappers
- COM wrappers
- COM, wrappers
- interoperation with unmanaged code, COM wrappers
- COM callable wrappers
ms.assetid: e56c485b-6b67-4345-8e66-fd21835a6092
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 38031509b999662c86657f0f5cdc7202de65c194
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54607200"
---
# <a name="com-wrappers"></a><span data-ttu-id="aabca-102">COM ラッパー</span><span class="sxs-lookup"><span data-stu-id="aabca-102">COM Wrappers</span></span>
<span data-ttu-id="aabca-103">COM は、次のいくつかの重要な点で、.NET Framework オブジェクト モデルとは異なります。</span><span class="sxs-lookup"><span data-stu-id="aabca-103">COM differs from the .NET Framework object model in several important ways:</span></span>  
  
-   <span data-ttu-id="aabca-104">COM オブジェクトのクライアントは、COM オブジェクトの有効期間を管理する必要があります。共通言語ランタイムはその環境でのオブジェクトの有効期間を管理します。</span><span class="sxs-lookup"><span data-stu-id="aabca-104">Clients of COM objects must manage the lifetime of those objects; the common language runtime manages the lifetime of objects in its environment.</span></span>  
  
-   <span data-ttu-id="aabca-105">COM オブジェクトのクライアントは、サービスを提供するインターフェイスを要求し、インターフェイス ポインターを取得して、そのサービスが利用可能かどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="aabca-105">Clients of COM objects discover whether a service is available by requesting an interface that provides that service and getting back an interface pointer, or not.</span></span> <span data-ttu-id="aabca-106">.NET オブジェクトのクライアントは、リフレクションを使用してオブジェクトの機能の説明を取得できます。</span><span class="sxs-lookup"><span data-stu-id="aabca-106">Clients of .NET objects can obtain a description of an object's functionality using reflection.</span></span>  
  
-   <span data-ttu-id="aabca-107">NET オブジェクトは、.NET Framework の実行環境によって管理されるメモリ内に存在します。</span><span class="sxs-lookup"><span data-stu-id="aabca-107">NET objects reside in memory managed by the .NET Framework execution environment.</span></span> <span data-ttu-id="aabca-108">実行環境では、パフォーマンス上の理由からオブジェクトをメモリ内で移動させることができ、移動先のオブジェクトへのすべての参照を更新できます。</span><span class="sxs-lookup"><span data-stu-id="aabca-108">The execution environment can move objects around in memory for performance reasons and update all references to the objects it moves.</span></span> <span data-ttu-id="aabca-109">オブジェクトへのポインターを取得するアンマネージ クライアントは、そのオブジェクトに依存するので同じ場所にとどまります。</span><span class="sxs-lookup"><span data-stu-id="aabca-109">Unmanaged clients, having obtained a pointer to an object, rely on the object to remain at the same location.</span></span> <span data-ttu-id="aabca-110">これらのクライアントには、場所が固定されていないオブジェクトを処理するための機構がありません。</span><span class="sxs-lookup"><span data-stu-id="aabca-110">These clients have no mechanism for dealing with an object whose location is not fixed.</span></span>  
  
 <span data-ttu-id="aabca-111">このような相違を克服するために、ランタイムはラッパー クラスを提供して、マネージド クライアントとアンマネージド クライアントの両方がそれぞれの環境内でオブジェクトを呼び出していると認識するようにします。</span><span class="sxs-lookup"><span data-stu-id="aabca-111">To overcome these differences, the runtime provides wrapper classes to make both managed and unmanaged clients think they are calling objects within their respective environment.</span></span> <span data-ttu-id="aabca-112">マネージド クライアントが COM オブジェクトでメソッドを呼び出すたびに、ランタイムは[ランタイム呼び出し可能ラッパー](runtime-callable-wrapper.md) (RCW) を作成します。</span><span class="sxs-lookup"><span data-stu-id="aabca-112">Whenever your managed client calls a method on a COM object, the runtime creates a [runtime callable wrapper](runtime-callable-wrapper.md) (RCW).</span></span> <span data-ttu-id="aabca-113">RCW は、特にマネージド参照機構とアンマネージド参照機構の相違を抽象化します。</span><span class="sxs-lookup"><span data-stu-id="aabca-113">RCWs abstract the differences between managed and unmanaged reference mechanisms, among other things.</span></span> <span data-ttu-id="aabca-114">また、ランタイムは [COM 呼び出し可能ラッパー](com-callable-wrapper.md) (CCW) を作成して、プロセスを反転させ、COM クライアントがシームレスに .NET オブジェクトでメソッドを呼び出せるようにします。</span><span class="sxs-lookup"><span data-stu-id="aabca-114">The runtime also creates a [COM callable wrapper](com-callable-wrapper.md) (CCW) to reverse the process, enabling a COM client to seamlessly call a method on a .NET object.</span></span> <span data-ttu-id="aabca-115">呼び出し元のコードと、ランタイムが作成するラッパー クラスの関係を示す図を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="aabca-115">As the following illustration shows, the perspective of the calling code determines which wrapper class the runtime creates.</span></span>  
  
 <span data-ttu-id="aabca-116">![COM ラッパーの概要](media/bidirectional.gif "bidirectional")</span><span class="sxs-lookup"><span data-stu-id="aabca-116">![COM wrapper overview](media/bidirectional.gif "bidirectional")</span></span>  
<span data-ttu-id="aabca-117">COM ラッパーの概要</span><span class="sxs-lookup"><span data-stu-id="aabca-117">COM wrapper overview</span></span>  
  
 <span data-ttu-id="aabca-118">ほとんどの場合、ランタイムによって生成される標準の RCW または CCW は、COM と .NET Framework の境界をまたがる呼び出しに対して適切なマーシャリングを提供します。</span><span class="sxs-lookup"><span data-stu-id="aabca-118">In most cases, the standard RCW or CCW generated by the runtime provides adequate marshaling for calls that cross the boundary between COM and the .NET Framework.</span></span> <span data-ttu-id="aabca-119">カスタム属性を使用することにより、必要に応じて、ランタイムがマネージド コードおよびアンマネージド コードを表わす方法を調整できます。</span><span class="sxs-lookup"><span data-stu-id="aabca-119">Using custom attributes, you can optionally adjust the way the runtime represents managed and unmanaged code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aabca-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="aabca-120">See also</span></span>
- <span data-ttu-id="aabca-121">[高度な COM 相互運用性](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bd9cdfyx(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="aabca-121">[Advanced COM Interoperability](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bd9cdfyx(v=vs.100))</span></span>
- [<span data-ttu-id="aabca-122">ランタイム呼び出し可能ラッパー</span><span class="sxs-lookup"><span data-stu-id="aabca-122">Runtime Callable Wrapper</span></span>](runtime-callable-wrapper.md)
- [<span data-ttu-id="aabca-123">COM 呼び出し可能ラッパー</span><span class="sxs-lookup"><span data-stu-id="aabca-123">COM Callable Wrapper</span></span>](com-callable-wrapper.md)
- <span data-ttu-id="aabca-124">[標準ラッパーのカスタマイズ](https://msdn.microsoft.com/library/c40d089b-6a3c-41b5-a20d-d760c215e49d(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="aabca-124">[Customizing Standard Wrappers](https://msdn.microsoft.com/library/c40d089b-6a3c-41b5-a20d-d760c215e49d(v=vs.100))</span></span>
- <span data-ttu-id="aabca-125">[方法: ランタイム呼び出し可能ラッパーをカスタマイズする](https://msdn.microsoft.com/library/4a4bb3da-4d60-4517-99f2-78d46a681732(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="aabca-125">[How to: Customize Runtime Callable Wrappers](https://msdn.microsoft.com/library/4a4bb3da-4d60-4517-99f2-78d46a681732(v=vs.100))</span></span>
