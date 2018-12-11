---
title: シールされていないクラス
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- classes [.NET Framework], unsealed
- unsealed classes
- inheritance, classes
ms.assetid: 9a3bd505-90f5-4053-9f0d-3cf5fa3d3ebf
author: KrzysztofCwalina
ms.openlocfilehash: 8d7b1500506ec73a0d33d5352756cb85039358e5
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53153229"
---
# <a name="unsealed-classes"></a><span data-ttu-id="a8c0d-102">シールされていないクラス</span><span class="sxs-lookup"><span data-stu-id="a8c0d-102">Unsealed Classes</span></span>
<span data-ttu-id="a8c0d-103">シール クラスから継承することはできませんし、機能拡張は、します。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-103">Sealed classes cannot be inherited from, and they prevent extensibility.</span></span> <span data-ttu-id="a8c0d-104">これに対し、封印されていないクラスから継承できるクラスと呼びます。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-104">In contrast, classes that can be inherited from are called unsealed classes.</span></span>  
  
 <span data-ttu-id="a8c0d-105">**✓ CONSIDER** 安価なを提供するのにまだ高く評価されたフレームワークを拡張機能として、仮想またはプロテクト メンバーを追加なしで封印されていないクラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-105">**✓ CONSIDER** using unsealed classes with no added virtual or protected members as a great way to provide inexpensive yet much appreciated extensibility to a framework.</span></span>  
  
 <span data-ttu-id="a8c0d-106">多くの場合、開発者はカスタム コンス トラクター、新しいメソッドは、メソッドのオーバー ロードなどの便利なメンバーを追加するための封印されていないクラスから継承したいと考えているとします。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-106">Developers often want to inherit from unsealed classes so as to add convenience members such as custom constructors, new methods, or method overloads.</span></span> <span data-ttu-id="a8c0d-107">たとえば、`System.Messaging.MessageQueue`が封印されていないと、できるので、ユーザーがその既定値を特定のキューのパスにカスタムのキューを作成する特定のシナリオ用の API を簡略化するカスタム メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-107">For example,  `System.Messaging.MessageQueue` is unsealed and thus allows users to create custom queues that default to a particular queue path or to add custom methods that simplify the API for specific scenarios.</span></span>  
  
 <span data-ttu-id="a8c0d-108">既定ではほとんどのプログラミング言語でクラスが封印されていないし、これは、推奨された既定のフレームワークのほとんどのクラスにもします。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-108">Classes are unsealed by default in most programming languages, and this is also the recommended default for most classes in frameworks.</span></span> <span data-ttu-id="a8c0d-109">封印されていない型によって提供される拡張機能は、フレームワークのユーザーによって非常にありがたいと封印されていない型に関連付けられている相対的に低いテスト コストのために提供する非常に低コストです。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-109">The extensibility afforded by unsealed types is much appreciated by framework users and quite inexpensive to provide because of relatively low test costs associated with unsealed types.</span></span>  
  
 <span data-ttu-id="a8c0d-110">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="a8c0d-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="a8c0d-111">*Pearson Education, Inc. からのアクセス許可によって了承を得て転載[Framework デザイン ガイドライン。規則、手法、および再利用可能な .NET ライブラリの第 2 版のパターン](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)Krzysztof Cwalina、Brad 内容では、Microsoft Windows の開発シリーズの一部として、Addison-wesley Professional、2008 年 10 月 22日を公開します。*</span><span class="sxs-lookup"><span data-stu-id="a8c0d-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a8c0d-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8c0d-112">See also</span></span>

- [<span data-ttu-id="a8c0d-113">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="a8c0d-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="a8c0d-114">機能拡張のデザイン</span><span class="sxs-lookup"><span data-stu-id="a8c0d-114">Designing for Extensibility</span></span>](../../../docs/standard/design-guidelines/designing-for-extensibility.md)  
- [<span data-ttu-id="a8c0d-115">シール</span><span class="sxs-lookup"><span data-stu-id="a8c0d-115">Sealing</span></span>](../../../docs/standard/design-guidelines/sealing.md)
