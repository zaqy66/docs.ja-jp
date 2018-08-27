---
title: pInvokeStackImbalance MDA
ms.date: 03/30/2017
helpviewer_keywords:
- signatures, platform invoke
- stack depth
- platform invoke stack imbalance
- MDAs (managed debugging assistants), platform invoke
- platform invoke, run-time errors
- PInvokeStackImbalance MDA
- managed debugging assistants (MDAs), platform invoke
ms.assetid: 34ddc6bd-1675-4f35-86aa-de1645d5c631
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5594166081c36fbda1e5d1a62e017aaceb7a553d
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/24/2018
ms.locfileid: "42912115"
---
# <a name="pinvokestackimbalance-mda"></a><span data-ttu-id="a87ca-102">PInvokeStackImbalance MDA</span><span class="sxs-lookup"><span data-stu-id="a87ca-102">PInvokeStackImbalance MDA</span></span>

<span data-ttu-id="a87ca-103">`PInvokeStackImbalance` 、CLR がスタックの深さ、プラットフォーム呼び出しの後に指定で指定される呼び出し規約、予想されるスタックの深さと一致しないことを検出すると、マネージ デバッグ アシスタント (MDA) がアクティブ化、<xref:System.Runtime.InteropServices.DllImportAttribute>属性およびマネージ シグネチャでは、パラメーターの宣言。</span><span class="sxs-lookup"><span data-stu-id="a87ca-103">The `PInvokeStackImbalance` managed debugging assistant (MDA) is activated when the CLR detects that the stack depth after a platform invoke call does not match the expected stack depth, given the calling convention specified in the <xref:System.Runtime.InteropServices.DllImportAttribute> attribute and the declaration of the parameters in the managed signature.</span></span>

<span data-ttu-id="a87ca-104">`PInvokeStackImbalance` MDA は 32 ビット x86 プラットフォームに対してのみ実装されています。</span><span class="sxs-lookup"><span data-stu-id="a87ca-104">The `PInvokeStackImbalance` MDA is implemented only for 32-bit x86 platforms.</span></span>

> [!NOTE]
> <span data-ttu-id="a87ca-105">`PInvokeStackImbalance` MDA は既定で無効になります。</span><span class="sxs-lookup"><span data-stu-id="a87ca-105">The `PInvokeStackImbalance` MDA is disabled by default.</span></span> <span data-ttu-id="a87ca-106">Visual Studio 2017 で、`PInvokeStackImbalance`で MDA が表示されます、**マネージ デバッグ アシスタント**の一覧で、**例外設定** ダイアログ ボックス (を選択すると表示される**のデバッグ** >  **Windows** > **例外設定**)。</span><span class="sxs-lookup"><span data-stu-id="a87ca-106">In Visual Studio 2017, The `PInvokeStackImbalance` MDA appears in the **Managed Debugging Assistants** list in the **Exception Settings** dialog box (which is displayed when you select **Debug** > **Windows** > **Exception Settings**).</span></span> <span data-ttu-id="a87ca-107">ただし、オンまたはオフにして、**スローされたときに中断** チェック ボックスが有効または MDA を無効にしていない; のみ、MDA がアクティブになる、Visual Studio が例外をスローするかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="a87ca-107">However, selecting or clearing the **Break When Thrown** check box does not enable or disable the MDA; it only controls whether Visual Studio throws an exception when the MDA is activated.</span></span>

## <a name="symptoms"></a><span data-ttu-id="a87ca-108">現象</span><span class="sxs-lookup"><span data-stu-id="a87ca-108">Symptoms</span></span>

<span data-ttu-id="a87ca-109">プラットフォーム呼び出しの実行時または実行後に、アプリケーションでアクセス違反またはメモリ破損が発生します。</span><span class="sxs-lookup"><span data-stu-id="a87ca-109">An application encounters an access violation or memory corruption when making or following a platform invoke call.</span></span>

## <a name="cause"></a><span data-ttu-id="a87ca-110">原因</span><span class="sxs-lookup"><span data-stu-id="a87ca-110">Cause</span></span>

<span data-ttu-id="a87ca-111">プラットフォーム呼び出しのマネージド シグネチャが、呼び出されているメソッドのアンマネージド シグネチャと一致しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a87ca-111">The managed signature of the platform invoke call might not match the unmanaged signature of the method being called.</span></span>  <span data-ttu-id="a87ca-112">この不一致は、正しい数のパラメーターを宣言しないか、適切なサイズのパラメーターを指定しないマネージド シグネチャで発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a87ca-112">This mismatch can be caused by the managed signature not declaring the correct number of parameters or not specifying the appropriate size for the parameters.</span></span>  <span data-ttu-id="a87ca-113">また、<xref:System.Runtime.InteropServices.DllImportAttribute> 属性によって指定されている可能性がある呼び出し規約が、アンマネージ呼び出し規約と一致しない場合にも、MDA がアクティブ化される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a87ca-113">The MDA can also activate because the calling convention, possibly specified by the <xref:System.Runtime.InteropServices.DllImportAttribute> attribute, does not match the unmanaged calling convention.</span></span>

## <a name="resolution"></a><span data-ttu-id="a87ca-114">解像度</span><span class="sxs-lookup"><span data-stu-id="a87ca-114">Resolution</span></span>

<span data-ttu-id="a87ca-115">マネージド プラットフォーム呼び出しシグネチャ、および呼び出し規則を確認して、ネイティブ ターゲットのシグネチャと呼び出し規則に一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="a87ca-115">Review the managed platform invoke signature and calling convention to confirm it matches the signature and calling convention of the native target.</span></span>  <span data-ttu-id="a87ca-116">マネージド側とアンマネージド側の両方で、呼び出し規則を明示的に指定してください。</span><span class="sxs-lookup"><span data-stu-id="a87ca-116">Try explicitly specifying the calling convention on both the managed and unmanaged sides.</span></span> <span data-ttu-id="a87ca-117">また、あまり可能性はありませんが、アンマネージ コンパイラのバグなど、何らかの理由によりアンマネージ関数でスタックの不均衡が発生している場合もあります。</span><span class="sxs-lookup"><span data-stu-id="a87ca-117">It is also possible, although not as likely, that the unmanaged function unbalanced the stack for some other reason, such as a bug in the unmanaged compiler.</span></span>

## <a name="effect-on-the-runtime"></a><span data-ttu-id="a87ca-118">ランタイムへの影響</span><span class="sxs-lookup"><span data-stu-id="a87ca-118">Effect on the Runtime</span></span>

<span data-ttu-id="a87ca-119">すべてのプラットフォーム呼び出しが、CLR の最適化されていないパスを取得するよう強制します。</span><span class="sxs-lookup"><span data-stu-id="a87ca-119">Forces all platform invoke calls to take the nonoptimized path in the CLR.</span></span>

## <a name="output"></a><span data-ttu-id="a87ca-120">出力</span><span class="sxs-lookup"><span data-stu-id="a87ca-120">Output</span></span>

<span data-ttu-id="a87ca-121">MDA メッセージが、スタックの不均衡の原因であるプラットフォーム呼び出しメソッド呼び出しの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="a87ca-121">The MDA message gives the name of the platform invoke method call that is causing the stack imbalance.</span></span> <span data-ttu-id="a87ca-122">メソッド `SampleMethod` のプラットフォーム呼び出しのサンプル メッセージは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a87ca-122">A sample message of a platform invoke call on method `SampleMethod` is:</span></span>

<span data-ttu-id="a87ca-123">**PInvoke 関数 'SampleMethod' への呼び出しがスタックのバランスです。これは、マネージ PInvoke シグネチャが非管理対象のターゲットのシグネチャと一致しないために、可能性があります。呼び出し規約と PInvoke シグネチャのパラメーターが、ターゲットのアンマネージ シグネチャを一致するかを確認します。**</span><span class="sxs-lookup"><span data-stu-id="a87ca-123">**A call to PInvoke function 'SampleMethod' has unbalanced the stack. This is likely because the managed PInvoke signature does not match the unmanaged target signature. Check that the calling convention and parameters of the PInvoke signature match the target unmanaged signature.**</span></span>

## <a name="configuration"></a><span data-ttu-id="a87ca-124">構成</span><span class="sxs-lookup"><span data-stu-id="a87ca-124">Configuration</span></span>

```xml
<mdaConfig>
  <assistants>
    <pInvokeStackImbalance />
  </assistants>
</mdaConfig>
```

## <a name="see-also"></a><span data-ttu-id="a87ca-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a87ca-125">See Also</span></span>

- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- <span data-ttu-id="a87ca-126">
  [マネージド デバッグ アシスタントによるエラーの診断](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)</span><span class="sxs-lookup"><span data-stu-id="a87ca-126">[Diagnosing Errors with Managed Debugging Assistants](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)</span></span>
- [<span data-ttu-id="a87ca-127">相互運用マーシャリング</span><span class="sxs-lookup"><span data-stu-id="a87ca-127">Interop Marshaling</span></span>](../../../docs/framework/interop/interop-marshaling.md)
