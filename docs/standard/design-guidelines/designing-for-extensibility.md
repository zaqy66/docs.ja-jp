---
title: 機能拡張のデザイン
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- extending class libraries
- extensibility with class libraries in .NET Framework
- class library design guidelines [.NET Framework], extensibility
- class library extensibility [.NET Framework]
ms.assetid: 1cdb8740-871a-456c-9bd9-db96ca8d79b3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9c1690d0cdf1f57eaf0a794d6e71babfa4fa6425
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47216452"
---
# <a name="designing-for-extensibility"></a><span data-ttu-id="33a96-102">機能拡張のデザイン</span><span class="sxs-lookup"><span data-stu-id="33a96-102">Designing for Extensibility</span></span>
<span data-ttu-id="33a96-103">フレームワークの設計の 1 つの重要な側面は、フレームワークの拡張性を慎重に検討することを確認して行っています。</span><span class="sxs-lookup"><span data-stu-id="33a96-103">One important aspect of designing a framework is making sure the extensibility of the framework has been carefully considered.</span></span> <span data-ttu-id="33a96-104">これは、コストとメリットに関連付けられたさまざまな機能拡張メカニズムを理解することが必要です。</span><span class="sxs-lookup"><span data-stu-id="33a96-104">This requires that you understand the costs and benefits associated with various extensibility mechanisms.</span></span> <span data-ttu-id="33a96-105">この章では、拡張メカニズムを判断するのに役立ちます: サブクラス化、イベント、仮想メンバー、コールバック、および、-、framework の要件を満たす最適なことができます。</span><span class="sxs-lookup"><span data-stu-id="33a96-105">This chapter helps you decide which of the extensibility mechanisms—subclassing, events, virtual members, callbacks, and so on—can best meet the requirements of your framework.</span></span>  
  
 <span data-ttu-id="33a96-106">フレームワークで機能拡張を可能にする方法はたくさんあります。</span><span class="sxs-lookup"><span data-stu-id="33a96-106">There are many ways to allow extensibility in frameworks.</span></span> <span data-ttu-id="33a96-107">コストが非常に強力なするよりも低コストの範囲です。</span><span class="sxs-lookup"><span data-stu-id="33a96-107">They range from less powerful but less costly to very powerful but expensive.</span></span> <span data-ttu-id="33a96-108">任意の特定の機能拡張要件の要件を満たす最低コストのかかる機能拡張メカニズムを選択してください。</span><span class="sxs-lookup"><span data-stu-id="33a96-108">For any given extensibility requirement, you should choose the least costly extensibility mechanism that meets the requirements.</span></span> <span data-ttu-id="33a96-109">重大な変更を導入することがなくすぐ実行しないことができますが、通常は、後で、複数の機能拡張を追加することは覚えておいてください。</span><span class="sxs-lookup"><span data-stu-id="33a96-109">Keep in mind that it’s usually possible to add more extensibility later, but you can never take it away without introducing breaking changes.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="33a96-110">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="33a96-110">In This Section</span></span>  
 [<span data-ttu-id="33a96-111">シールされていないクラス</span><span class="sxs-lookup"><span data-stu-id="33a96-111">Unsealed Classes</span></span>](../../../docs/standard/design-guidelines/unsealed-classes.md)  
 [<span data-ttu-id="33a96-112">プロテクト メンバー</span><span class="sxs-lookup"><span data-stu-id="33a96-112">Protected Members</span></span>](../../../docs/standard/design-guidelines/protected-members.md)  
 [<span data-ttu-id="33a96-113">イベントとコールバック</span><span class="sxs-lookup"><span data-stu-id="33a96-113">Events and Callbacks</span></span>](../../../docs/standard/design-guidelines/events-and-callbacks.md)  
 [<span data-ttu-id="33a96-114">仮想メンバー</span><span class="sxs-lookup"><span data-stu-id="33a96-114">Virtual Members</span></span>](../../../docs/standard/design-guidelines/virtual-members.md)  
 [<span data-ttu-id="33a96-115">抽象化 (抽象型およびインターフェイス)</span><span class="sxs-lookup"><span data-stu-id="33a96-115">Abstractions (Abstract Types and Interfaces)</span></span>](../../../docs/standard/design-guidelines/abstractions-abstract-types-and-interfaces.md)  
 [<span data-ttu-id="33a96-116">抽象化の実装用の基本クラス</span><span class="sxs-lookup"><span data-stu-id="33a96-116">Base Classes for Implementing Abstractions</span></span>](../../../docs/standard/design-guidelines/base-classes-for-implementing-abstractions.md)  
 [<span data-ttu-id="33a96-117">シール</span><span class="sxs-lookup"><span data-stu-id="33a96-117">Sealing</span></span>](../../../docs/standard/design-guidelines/sealing.md)  
 <span data-ttu-id="33a96-118">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="33a96-118">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="33a96-119">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="33a96-119">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33a96-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="33a96-120">See also</span></span>

- [<span data-ttu-id="33a96-121">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="33a96-121">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
