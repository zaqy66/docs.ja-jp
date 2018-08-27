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
# <a name="pinvokestackimbalance-mda"></a>PInvokeStackImbalance MDA

`PInvokeStackImbalance` 、CLR がスタックの深さ、プラットフォーム呼び出しの後に指定で指定される呼び出し規約、予想されるスタックの深さと一致しないことを検出すると、マネージ デバッグ アシスタント (MDA) がアクティブ化、<xref:System.Runtime.InteropServices.DllImportAttribute>属性およびマネージ シグネチャでは、パラメーターの宣言。

`PInvokeStackImbalance` MDA は 32 ビット x86 プラットフォームに対してのみ実装されています。

> [!NOTE]
> `PInvokeStackImbalance` MDA は既定で無効になります。 Visual Studio 2017 で、`PInvokeStackImbalance`で MDA が表示されます、**マネージ デバッグ アシスタント**の一覧で、**例外設定** ダイアログ ボックス (を選択すると表示される**のデバッグ** >  **Windows** > **例外設定**)。 ただし、オンまたはオフにして、**スローされたときに中断** チェック ボックスが有効または MDA を無効にしていない; のみ、MDA がアクティブになる、Visual Studio が例外をスローするかどうかを制御します。

## <a name="symptoms"></a>現象

プラットフォーム呼び出しの実行時または実行後に、アプリケーションでアクセス違反またはメモリ破損が発生します。

## <a name="cause"></a>原因

プラットフォーム呼び出しのマネージド シグネチャが、呼び出されているメソッドのアンマネージド シグネチャと一致しない可能性があります。  この不一致は、正しい数のパラメーターを宣言しないか、適切なサイズのパラメーターを指定しないマネージド シグネチャで発生する可能性があります。  また、<xref:System.Runtime.InteropServices.DllImportAttribute> 属性によって指定されている可能性がある呼び出し規約が、アンマネージ呼び出し規約と一致しない場合にも、MDA がアクティブ化される可能性があります。

## <a name="resolution"></a>解像度

マネージド プラットフォーム呼び出しシグネチャ、および呼び出し規則を確認して、ネイティブ ターゲットのシグネチャと呼び出し規則に一致することを確認します。  マネージド側とアンマネージド側の両方で、呼び出し規則を明示的に指定してください。 また、あまり可能性はありませんが、アンマネージ コンパイラのバグなど、何らかの理由によりアンマネージ関数でスタックの不均衡が発生している場合もあります。

## <a name="effect-on-the-runtime"></a>ランタイムへの影響

すべてのプラットフォーム呼び出しが、CLR の最適化されていないパスを取得するよう強制します。

## <a name="output"></a>出力

MDA メッセージが、スタックの不均衡の原因であるプラットフォーム呼び出しメソッド呼び出しの名前を示します。 メソッド `SampleMethod` のプラットフォーム呼び出しのサンプル メッセージは、次のとおりです。

**PInvoke 関数 'SampleMethod' への呼び出しがスタックのバランスです。これは、マネージ PInvoke シグネチャが非管理対象のターゲットのシグネチャと一致しないために、可能性があります。呼び出し規約と PInvoke シグネチャのパラメーターが、ターゲットのアンマネージ シグネチャを一致するかを確認します。**

## <a name="configuration"></a>構成

```xml
<mdaConfig>
  <assistants>
    <pInvokeStackImbalance />
  </assistants>
</mdaConfig>
```

## <a name="see-also"></a>関連項目

- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- 
  [マネージド デバッグ アシスタントによるエラーの診断](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [相互運用マーシャリング](../../../docs/framework/interop/interop-marshaling.md)
