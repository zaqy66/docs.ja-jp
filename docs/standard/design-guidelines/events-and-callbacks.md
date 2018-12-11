---
title: イベントとコールバック
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- events [.NET Framework], extensibility
- methods [.NET Framework], callback
- callback methods
- callbacks
ms.assetid: 48b55c60-495f-4089-9396-97f9122bba7c
author: KrzysztofCwalina
ms.openlocfilehash: c9ed52c5a313676baeba66f5cb79c7a56927babb
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53154425"
---
# <a name="events-and-callbacks"></a><span data-ttu-id="77a4e-102">イベントとコールバック</span><span class="sxs-lookup"><span data-stu-id="77a4e-102">Events and Callbacks</span></span>
<span data-ttu-id="77a4e-103">コールバックは、機能拡張ポイントがデリゲートからのユーザー コードにコールバックするためのフレームワークです。</span><span class="sxs-lookup"><span data-stu-id="77a4e-103">Callbacks are extensibility points that allow a framework to call back into user code through a delegate.</span></span> <span data-ttu-id="77a4e-104">これらのデリゲートは、メソッドのパラメーターでは、通常、フレームワークに渡されます。</span><span class="sxs-lookup"><span data-stu-id="77a4e-104">These delegates are usually passed to the framework through a parameter of a method.</span></span>  
  
 <span data-ttu-id="77a4e-105">イベントは、コールバックのデリゲート (イベント ハンドラー) を提供するための便利で一貫した構文をサポートする特殊なケースです。</span><span class="sxs-lookup"><span data-stu-id="77a4e-105">Events are a special case of callbacks that supports convenient and consistent syntax for supplying the delegate (an event handler).</span></span> <span data-ttu-id="77a4e-106">さらに、Visual Studio のステートメント入力候補およびデザイナーは、イベント ベースの Api を使用してヘルプを提供します。</span><span class="sxs-lookup"><span data-stu-id="77a4e-106">In addition, Visual Studio’s statement completion and designers provide help in using event-based APIs.</span></span> <span data-ttu-id="77a4e-107">(を参照してください[イベント デザイン](../../../docs/standard/design-guidelines/event.md))。</span><span class="sxs-lookup"><span data-stu-id="77a4e-107">(See [Event Design](../../../docs/standard/design-guidelines/event.md).)</span></span>  
  
 <span data-ttu-id="77a4e-108">**✓ CONSIDER** コールバックを使用して、フレームワークによって実行されるカスタム コードを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="77a4e-108">**✓ CONSIDER** using callbacks to allow users to provide custom code to be executed by the framework.</span></span>  
  
 <span data-ttu-id="77a4e-109">**✓ CONSIDER** イベントを使用したオブジェクト指向設計を理解することがなくてもフレームワークの動作をカスタマイズできるようにします。</span><span class="sxs-lookup"><span data-stu-id="77a4e-109">**✓ CONSIDER** using events to allow users to customize the behavior of a framework without the need for understanding object-oriented design.</span></span>  
  
 <span data-ttu-id="77a4e-110">**✓ DO** 幅広い開発者になじみのあるは、ステートメント入力候補の Visual Studio と統合されたために、イベントを単純なコールバックよりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="77a4e-110">**✓ DO** prefer events over plain callbacks, because they are more familiar to a broader range of developers and are integrated with Visual Studio statement completion.</span></span>  
  
 <span data-ttu-id="77a4e-111">**X AVOID** パフォーマンス重視の Api でのコールバックを使用します。</span><span class="sxs-lookup"><span data-stu-id="77a4e-111">**X AVOID** using callbacks in performance-sensitive APIs.</span></span>  
  
 <span data-ttu-id="77a4e-112">**✓ DO** 新しい`Func<...>`、 `Action<...>`、または`Expression<...>`コールバックで Api を定義するときに、カスタム デリゲートではなく型です。</span><span class="sxs-lookup"><span data-stu-id="77a4e-112">**✓ DO** use the new `Func<...>`, `Action<...>`, or `Expression<...>` types instead of custom delegates, when defining APIs with callbacks.</span></span>  
  
 <span data-ttu-id="77a4e-113">`Func<...>` `Action<...>`汎用デリゲートを表します。</span><span class="sxs-lookup"><span data-stu-id="77a4e-113">`Func<...>` and `Action<...>` represent generic delegates.</span></span> <span data-ttu-id="77a4e-114">`Expression<...>` コンパイルと、その後もできますが、実行時に呼び出されることができます関数定義を表すシリアル化およびリモート プロセスに渡されます。</span><span class="sxs-lookup"><span data-stu-id="77a4e-114">`Expression<...>` represents function definitions that can be compiled and subsequently invoked at runtime but can also be serialized and passed to remote processes.</span></span>  
  
 <span data-ttu-id="77a4e-115">**✓ DO** を測定しを使用するパフォーマンスの影響について理解する`Expression<...>`、使用する代わりに`Func<...>`と`Action<...>`デリゲート。</span><span class="sxs-lookup"><span data-stu-id="77a4e-115">**✓ DO** measure and understand performance implications of using `Expression<...>`, instead of using `Func<...>` and `Action<...>` delegates.</span></span>  
  
 <span data-ttu-id="77a4e-116">`Expression<...>` ほとんどの場合と論理的に等価では型が`Func<...>`と`Action<...>`デリゲート。</span><span class="sxs-lookup"><span data-stu-id="77a4e-116">`Expression<...>` types are in most cases logically equivalent to `Func<...>` and `Action<...>` delegates.</span></span> <span data-ttu-id="77a4e-117">主な違いは、デリゲートはローカル プロセスのシナリオで使用するものであります。式は、有益なリモート プロセスまたはマシンで式を評価することである場合を対象としています。</span><span class="sxs-lookup"><span data-stu-id="77a4e-117">The main difference between them is that the delegates are intended to be used in local process scenarios; expressions are intended for cases where it’s beneficial and possible to evaluate the expression in a remote process or machine.</span></span>  
  
 <span data-ttu-id="77a4e-118">**✓ DO** するデリゲートを呼び出すことによって実行している任意のコードを理解し、セキュリティ、正確性、および互換性への影響を与える可能性です。</span><span class="sxs-lookup"><span data-stu-id="77a4e-118">**✓ DO** understand that by calling a delegate, you are executing arbitrary code and that could have security, correctness, and compatibility repercussions.</span></span>  
  
 <span data-ttu-id="77a4e-119">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="77a4e-119">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="77a4e-120">*Pearson Education, Inc. からのアクセス許可によって了承を得て転載[Framework デザイン ガイドライン。規則、手法、および再利用可能な .NET ライブラリの第 2 版のパターン](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)Krzysztof Cwalina、Brad 内容では、Microsoft Windows の開発シリーズの一部として、Addison-wesley Professional、2008 年 10 月 22日を公開します。*</span><span class="sxs-lookup"><span data-stu-id="77a4e-120">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77a4e-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="77a4e-121">See also</span></span>

- [<span data-ttu-id="77a4e-122">機能拡張のデザイン</span><span class="sxs-lookup"><span data-stu-id="77a4e-122">Designing for Extensibility</span></span>](../../../docs/standard/design-guidelines/designing-for-extensibility.md)  
- [<span data-ttu-id="77a4e-123">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="77a4e-123">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
