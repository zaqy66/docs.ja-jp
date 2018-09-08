---
title: プロテクト メンバー
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- members [.NET Framework], protected
- protected members
- classes [.NET Framework], unsealed
- classes [.NET Framework], protected members
- unsealed classes
- customizing class behavior
ms.assetid: aa0b58ee-3956-494d-ab48-471ae5db8740
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4574dffc3f9dd1b60d655bfde33a4ddc1a81d350
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44140945"
---
# <a name="protected-members"></a><span data-ttu-id="eb3ef-102">プロテクト メンバー</span><span class="sxs-lookup"><span data-stu-id="eb3ef-102">Protected Members</span></span>
<span data-ttu-id="eb3ef-103">単独で保護されたメンバーでは任意の拡張機能は提供しませんより強力なサブクラス化による拡張性を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="eb3ef-103">Protected members by themselves do not provide any extensibility, but they can make extensibility through subclassing more powerful.</span></span> <span data-ttu-id="eb3ef-104">これらは、メインのパブリック インターフェイスを不必要に複雑にせず、高度なカスタマイズ オプションを公開する使用できます。</span><span class="sxs-lookup"><span data-stu-id="eb3ef-104">They can be used to expose advanced customization options without unnecessarily complicating the main public interface.</span></span>  
  
 <span data-ttu-id="eb3ef-105">フレームワークの設計者は、「保護」の名前は、セキュリティの誤った認識を与えることができますので、保護されたメンバーには注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb3ef-105">Framework designers need to be careful with protected members because the name "protected" can give a false sense of security.</span></span> <span data-ttu-id="eb3ef-106">すべてのユーザーは、封印されていないクラスのサブクラスとメンバーへのアクセスが保護されていることと、防御的なコーディング手法がパブリック メンバーの使用が保護されたメンバーに適用するため、同じ。</span><span class="sxs-lookup"><span data-stu-id="eb3ef-106">Anyone is able to subclass an unsealed class and access protected members, and so all the same defensive coding practices used for public members apply to protected members.</span></span>  
  
 <span data-ttu-id="eb3ef-107">**✓ CONSIDER** 高度なカスタマイズのメンバーを使用して保護されています。</span><span class="sxs-lookup"><span data-stu-id="eb3ef-107">**✓ CONSIDER** using protected members for advanced customization.</span></span>  
  
 <span data-ttu-id="eb3ef-108">**✓ DO** セキュリティ、ドキュメント、および互換性分析するためにパブリックと封印されていないクラスにプロテクト メンバーを処理します。</span><span class="sxs-lookup"><span data-stu-id="eb3ef-108">**✓ DO** treat protected members in unsealed classes as public for the purpose of security, documentation, and compatibility analysis.</span></span>  
  
 <span data-ttu-id="eb3ef-109">クラスから継承するすべてのユーザーし、プロテクト メンバーにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="eb3ef-109">Anyone can inherit from a class and access the protected members.</span></span>  
  
 <span data-ttu-id="eb3ef-110">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="eb3ef-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="eb3ef-111">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="eb3ef-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb3ef-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb3ef-112">See also</span></span>

- [<span data-ttu-id="eb3ef-113">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="eb3ef-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="eb3ef-114">機能拡張のデザイン</span><span class="sxs-lookup"><span data-stu-id="eb3ef-114">Designing for Extensibility</span></span>](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
