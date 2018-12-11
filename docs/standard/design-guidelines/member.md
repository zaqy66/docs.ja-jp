---
title: メンバーのデザインのガイドライン
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- member design guidelines [.NET Framework], about member design guidelines
- members [.NET Framework], design guidelines
- class library design guidelines [.NET Framework], members
- member design guidelines [.NET Framework]
ms.assetid: 0ce93180-1d7b-4f8c-9306-f828b2d66b8f
author: KrzysztofCwalina
ms.openlocfilehash: d7023bbe59eb3590af47952a2fe24c5f40b3ca68
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53155263"
---
# <a name="member-design-guidelines"></a><span data-ttu-id="fab19-102">メンバーのデザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="fab19-102">Member Design Guidelines</span></span>
<span data-ttu-id="fab19-103">メソッド、プロパティ、イベント、コンス トラクター、およびフィールドは、メンバーとしてまとめて呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="fab19-103">Methods, properties, events, constructors, and fields are collectively referred to as members.</span></span> <span data-ttu-id="fab19-104">メンバーが、最終的に、フレームワークのエンドユーザーに、フレームワークの機能が公開されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="fab19-104">Members are ultimately the means by which framework functionality is exposed to the end users of a framework.</span></span>  
  
 <span data-ttu-id="fab19-105">メンバーは、仮想または非仮想、具象か抽象クラスで静的メソッドまたはインスタンスにできるし、ユーザー補助機能のいくつかの異なるスコープを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="fab19-105">Members can be virtual or nonvirtual, concrete or abstract, static or instance, and can have several different scopes of accessibility.</span></span> <span data-ttu-id="fab19-106">さまざまな種類すべてでは、驚異的な表現力を提供しますが、同時に、framework デザイナー側注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="fab19-106">All this variety provides incredible expressiveness but at the same time requires care on the part of the framework designer.</span></span>  
  
 <span data-ttu-id="fab19-107">この章では、任意の型のメンバーを設計するときに従う必要がありますの基本的なガイドラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="fab19-107">This chapter offers basic guidelines that should be followed when designing members of any type.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="fab19-108">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="fab19-108">In This Section</span></span>  
 [<span data-ttu-id="fab19-109">メンバーのオーバーロード</span><span class="sxs-lookup"><span data-stu-id="fab19-109">Member Overloading</span></span>](../../../docs/standard/design-guidelines/member-overloading.md)  
 [<span data-ttu-id="fab19-110">プロパティのデザイン</span><span class="sxs-lookup"><span data-stu-id="fab19-110">Property Design</span></span>](../../../docs/standard/design-guidelines/property.md)  
 [<span data-ttu-id="fab19-111">コンストラクターのデザイン</span><span class="sxs-lookup"><span data-stu-id="fab19-111">Constructor Design</span></span>](../../../docs/standard/design-guidelines/constructor.md)  
 [<span data-ttu-id="fab19-112">イベントのデザイン</span><span class="sxs-lookup"><span data-stu-id="fab19-112">Event Design</span></span>](../../../docs/standard/design-guidelines/event.md)  
 [<span data-ttu-id="fab19-113">フィールドのデザイン</span><span class="sxs-lookup"><span data-stu-id="fab19-113">Field Design</span></span>](../../../docs/standard/design-guidelines/field.md)  
 [<span data-ttu-id="fab19-114">拡張メソッド</span><span class="sxs-lookup"><span data-stu-id="fab19-114">Extension Methods</span></span>](../../../docs/standard/design-guidelines/extension-methods.md)  
 [<span data-ttu-id="fab19-115">演算子のオーバーロード</span><span class="sxs-lookup"><span data-stu-id="fab19-115">Operator Overloads</span></span>](../../../docs/standard/design-guidelines/operator-overloads.md)  
 [<span data-ttu-id="fab19-116">パラメーターのデザイン</span><span class="sxs-lookup"><span data-stu-id="fab19-116">Parameter Design</span></span>](../../../docs/standard/design-guidelines/parameter-design.md)  
 <span data-ttu-id="fab19-117">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="fab19-117">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="fab19-118">*Pearson Education, Inc. からのアクセス許可によって了承を得て転載[Framework デザイン ガイドライン。規則、手法、および再利用可能な .NET ライブラリの第 2 版のパターン](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)Krzysztof Cwalina、Brad 内容では、Microsoft Windows の開発シリーズの一部として、Addison-wesley Professional、2008 年 10 月 22日を公開します。*</span><span class="sxs-lookup"><span data-stu-id="fab19-118">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fab19-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="fab19-119">See also</span></span>

- [<span data-ttu-id="fab19-120">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="fab19-120">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
