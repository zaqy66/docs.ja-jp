---
title: シールされていないクラス
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- classes [.NET Framework], unsealed
- unsealed classes
- inheritance, classes
ms.assetid: 9a3bd505-90f5-4053-9f0d-3cf5fa3d3ebf
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ef0f1c4c9b2d1928d6f96d62ab12df9786756498
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43891378"
---
# <a name="unsealed-classes"></a><span data-ttu-id="ed0b3-102">シールされていないクラス</span><span class="sxs-lookup"><span data-stu-id="ed0b3-102">Unsealed Classes</span></span>
<span data-ttu-id="ed0b3-103">シール クラスから継承することはできませんし、機能拡張は、します。</span><span class="sxs-lookup"><span data-stu-id="ed0b3-103">Sealed classes cannot be inherited from, and they prevent extensibility.</span></span> <span data-ttu-id="ed0b3-104">これに対し、封印されていないクラスから継承できるクラスと呼びます。</span><span class="sxs-lookup"><span data-stu-id="ed0b3-104">In contrast, classes that can be inherited from are called unsealed classes.</span></span>  
  
 <span data-ttu-id="ed0b3-105">**✓ CONSIDER** 安価なを提供するのにまだ高く評価されたフレームワークを拡張機能として、仮想またはプロテクト メンバーを追加なしで封印されていないクラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="ed0b3-105">**✓ CONSIDER** using unsealed classes with no added virtual or protected members as a great way to provide inexpensive yet much appreciated extensibility to a framework.</span></span>  
  
 <span data-ttu-id="ed0b3-106">多くの場合、開発者はカスタム コンス トラクター、新しいメソッドは、メソッドのオーバー ロードなどの便利なメンバーを追加するための封印されていないクラスから継承したいと考えているとします。</span><span class="sxs-lookup"><span data-stu-id="ed0b3-106">Developers often want to inherit from unsealed classes so as to add convenience members such as custom constructors, new methods, or method overloads.</span></span> <span data-ttu-id="ed0b3-107">たとえば、`System.Messaging.MessageQueue`が封印されていないと、できるので、ユーザーがその既定値を特定のキューのパスにカスタムのキューを作成する特定のシナリオ用の API を簡略化するカスタム メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ed0b3-107">For example,  `System.Messaging.MessageQueue` is unsealed and thus allows users to create custom queues that default to a particular queue path or to add custom methods that simplify the API for specific scenarios.</span></span>  
  
 <span data-ttu-id="ed0b3-108">既定ではほとんどのプログラミング言語でクラスが封印されていないし、これは、推奨された既定のフレームワークのほとんどのクラスにもします。</span><span class="sxs-lookup"><span data-stu-id="ed0b3-108">Classes are unsealed by default in most programming languages, and this is also the recommended default for most classes in frameworks.</span></span> <span data-ttu-id="ed0b3-109">封印されていない型によって提供される拡張機能は、フレームワークのユーザーによって非常にありがたいと封印されていない型に関連付けられている相対的に低いテスト コストのために提供する非常に低コストです。</span><span class="sxs-lookup"><span data-stu-id="ed0b3-109">The extensibility afforded by unsealed types is much appreciated by framework users and quite inexpensive to provide because of relatively low test costs associated with unsealed types.</span></span>  
  
 <span data-ttu-id="ed0b3-110">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="ed0b3-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="ed0b3-111">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="ed0b3-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed0b3-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed0b3-112">See also</span></span>

- [<span data-ttu-id="ed0b3-113">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="ed0b3-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="ed0b3-114">機能拡張のデザイン</span><span class="sxs-lookup"><span data-stu-id="ed0b3-114">Designing for Extensibility</span></span>](../../../docs/standard/design-guidelines/designing-for-extensibility.md)  
- [<span data-ttu-id="ed0b3-115">シール</span><span class="sxs-lookup"><span data-stu-id="ed0b3-115">Sealing</span></span>](../../../docs/standard/design-guidelines/sealing.md)
