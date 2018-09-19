---
title: 抽象クラスのデザイン
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- type design guidelines, abstract classes
- abstract classes, design guidelines
- class library design guidelines [.NET Framework], classes
- classes [.NET Framework], abstract
- classes [.NET Framework], design guidelines
- type design guidelines, classes
ms.assetid: d3646e6d-5c1f-4922-8fb0-ec5effb30d60
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c5b9dacc4995a126e1ee3f6062dca796194d4882
ms.sourcegitcommit: f513a91160b3fec289dd06646d0d6f81f8fcf910
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/18/2018
ms.locfileid: "46288015"
---
# <a name="abstract-class-design"></a><span data-ttu-id="74530-102">抽象クラスのデザイン</span><span class="sxs-lookup"><span data-stu-id="74530-102">Abstract Class Design</span></span>
<span data-ttu-id="74530-103">**X DO NOT** 抽象型の public または protected のコンス トラクター内部を定義します。</span><span class="sxs-lookup"><span data-stu-id="74530-103">**X DO NOT** define public or protected internal constructors in abstract types.</span></span>  
  
 <span data-ttu-id="74530-104">コンス トラクターは、ユーザーが、型のインスタンスを作成する必要がある場合にのみパブリックである必要があります。</span><span class="sxs-lookup"><span data-stu-id="74530-104">Constructors should be public only if users will need to create instances of the type.</span></span> <span data-ttu-id="74530-105">抽象型のインスタンスを作成することはできません、ため、パブリック コンス トラクターを持つ抽象型は正しく設計で、ユーザーに誤解を招きます。</span><span class="sxs-lookup"><span data-stu-id="74530-105">Because you cannot create instances of an abstract type, an abstract type with a public constructor is incorrectly designed and misleading to the users.</span></span>  
  
 <span data-ttu-id="74530-106">**✓ DO** 抽象クラス内で、保護されているか、内部のコンス トラクターを定義します。</span><span class="sxs-lookup"><span data-stu-id="74530-106">**✓ DO** define a protected or an internal constructor in abstract classes.</span></span>  
  
 <span data-ttu-id="74530-107">プロテクト コンス トラクターより一般的なサブタイプが作成されたときに、独自の初期化を実行する基本クラスでは。</span><span class="sxs-lookup"><span data-stu-id="74530-107">A protected constructor is more common and simply allows the base class to do its own initialization when subtypes are created.</span></span>  
  
 <span data-ttu-id="74530-108">アセンブリのクラスを定義する抽象クラスの具象実装を制限する、内部コンス トラクターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="74530-108">An internal constructor can be used to limit concrete implementations of the abstract class to the assembly defining the class.</span></span>  
  
 <span data-ttu-id="74530-109">**✓ DO** を出荷する各の抽象クラスから継承する少なくとも 1 つの具象型を提供します。</span><span class="sxs-lookup"><span data-stu-id="74530-109">**✓ DO** provide at least one concrete type that inherits from each abstract class that you ship.</span></span>  
  
 <span data-ttu-id="74530-110">これによって、抽象クラスのデザインを検証するを実行します。</span><span class="sxs-lookup"><span data-stu-id="74530-110">Doing this helps to validate the design of the abstract class.</span></span> <span data-ttu-id="74530-111">たとえば、<xref:System.IO.FileStream?displayProperty=nameWithType>の実装には、<xref:System.IO.Stream?displayProperty=nameWithType>抽象クラス。</span><span class="sxs-lookup"><span data-stu-id="74530-111">For example,  <xref:System.IO.FileStream?displayProperty=nameWithType> is an implementation of the <xref:System.IO.Stream?displayProperty=nameWithType> abstract class.</span></span>  
  
 <span data-ttu-id="74530-112">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="74530-112">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="74530-113">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="74530-113">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="74530-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="74530-114">See also</span></span>

- [<span data-ttu-id="74530-115">型デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="74530-115">Type Design Guidelines</span></span>](../../../docs/standard/design-guidelines/type.md)  
- [<span data-ttu-id="74530-116">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="74530-116">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
