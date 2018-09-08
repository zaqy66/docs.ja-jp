---
title: 型のデザインのガイドライン
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- type design guidelines
- type design guidelines, about type design guidelines
- class library design guidelines [.NET Framework], type design guidelines
- types [.NET Framework], design guidelines
ms.assetid: 6b49314e-8bba-43ea-97ca-4e0255812f95
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a7fb9964d0e542c0937c55ae65bd88b3f7149fa8
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44187940"
---
# <a name="type-design-guidelines"></a><span data-ttu-id="7ae57-102">型のデザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="7ae57-102">Type Design Guidelines</span></span>
<span data-ttu-id="7ae57-103">CLR の観点からは、型の 2 つのカテゴリがあります: 参照型と値の型: フレームワークの設計に関する詳細については、するために、それぞれに独自の特定のデザイン規則より論理的にグループの種類を分割しますが、します。</span><span class="sxs-lookup"><span data-stu-id="7ae57-103">From the CLR perspective, there are only two categories of types—reference types and value types—but for the purpose of a discussion about framework design, we divide types into more logical groups, each with its own specific design rules.</span></span>  
  
 <span data-ttu-id="7ae57-104">クラスは、参照型の一般的なケースです。</span><span class="sxs-lookup"><span data-stu-id="7ae57-104">Classes are the general case of reference types.</span></span> <span data-ttu-id="7ae57-105">ほとんどのフレームワークの型の大部分を構成します。</span><span class="sxs-lookup"><span data-stu-id="7ae57-105">They make up the bulk of types in the majority of frameworks.</span></span> <span data-ttu-id="7ae57-106">クラスは、豊富なオブジェクト指向の機能がサポートされるを設定して、一般的な適用性を人気を助かりました。</span><span class="sxs-lookup"><span data-stu-id="7ae57-106">Classes owe their popularity to the rich set of object-oriented features they support and to their general applicability.</span></span> <span data-ttu-id="7ae57-107">基底クラスと抽象クラスは、拡張機能に関連する、特殊な論理グループです。</span><span class="sxs-lookup"><span data-stu-id="7ae57-107">Base classes and abstract classes are special logical groups related to extensibility.</span></span>  
  
 <span data-ttu-id="7ae57-108">インターフェイスは、参照型と値の型の両方で実装できる型です。</span><span class="sxs-lookup"><span data-stu-id="7ae57-108">Interfaces are types that can be implemented by both reference types and value types.</span></span> <span data-ttu-id="7ae57-109">したがって、参照型と値の型のポリモーフィックな階層のルートとして使用ができます。</span><span class="sxs-lookup"><span data-stu-id="7ae57-109">They can thus serve as roots of polymorphic hierarchies of reference types and value types.</span></span> <span data-ttu-id="7ae57-110">さらに、インターフェイスは、CLR によってネイティブでサポートされていない複数の継承をシミュレートするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="7ae57-110">In addition, interfaces can be used to simulate multiple inheritance, which is not natively supported by the CLR.</span></span>  
  
 <span data-ttu-id="7ae57-111">構造体の値型の一般的なケースは、小規模で単純な種類、言語プリミティブのように予約されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ae57-111">Structs are the general case of value types and should be reserved for small, simple types, similar to language primitives.</span></span>  
  
 <span data-ttu-id="7ae57-112">列挙型は、週、コンソールの色の日などの値の短いセットを定義するのに使用される値型の特殊なケースです。</span><span class="sxs-lookup"><span data-stu-id="7ae57-112">Enums are a special case of value types used to define short sets of values, such as days of the week, console colors, and so on.</span></span>  
  
 <span data-ttu-id="7ae57-113">静的クラスは、型の静的メンバーのコンテナーを意図したものです。</span><span class="sxs-lookup"><span data-stu-id="7ae57-113">Static classes are types intended to be containers for static members.</span></span> <span data-ttu-id="7ae57-114">その他の操作へのショートカットを提供するよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="7ae57-114">They are commonly used to provide shortcuts to other operations.</span></span>  
  
 <span data-ttu-id="7ae57-115">デリゲート、例外、属性、配列、およびコレクションは、特定の用途のためのもので、参照型のすべての特殊なケースと、この書籍での設計と使用法のガイドラインは別の場所について説明します。</span><span class="sxs-lookup"><span data-stu-id="7ae57-115">Delegates, exceptions, attributes, arrays, and collections are all special cases of reference types intended for specific uses, and guidelines for their design and usage are discussed elsewhere in this book.</span></span>  
  
 <span data-ttu-id="7ae57-116">**✓ DO** 各型が適切に定義された一連の関連するメンバーは、関連付けられていない機能のランダムなコレクションだけでなくであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7ae57-116">**✓ DO** ensure that each type is a well-defined set of related members, not just a random collection of unrelated functionality.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7ae57-117">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="7ae57-117">In This Section</span></span>  
 [<span data-ttu-id="7ae57-118">クラスまたは構造体の選択</span><span class="sxs-lookup"><span data-stu-id="7ae57-118">Choosing Between Class and Struct</span></span>](../../../docs/standard/design-guidelines/choosing-between-class-and-struct.md)  
 [<span data-ttu-id="7ae57-119">抽象クラスのデザイン</span><span class="sxs-lookup"><span data-stu-id="7ae57-119">Abstract Class Design</span></span>](../../../docs/standard/design-guidelines/abstract-class.md)  
 [<span data-ttu-id="7ae57-120">静的クラスのデザイン</span><span class="sxs-lookup"><span data-stu-id="7ae57-120">Static Class Design</span></span>](../../../docs/standard/design-guidelines/static-class.md)  
 [<span data-ttu-id="7ae57-121">インターフェイスのデザイン</span><span class="sxs-lookup"><span data-stu-id="7ae57-121">Interface Design</span></span>](../../../docs/standard/design-guidelines/interface.md)  
 [<span data-ttu-id="7ae57-122">構造体のデザイン</span><span class="sxs-lookup"><span data-stu-id="7ae57-122">Struct Design</span></span>](../../../docs/standard/design-guidelines/struct.md)  
 [<span data-ttu-id="7ae57-123">列挙型デザイン</span><span class="sxs-lookup"><span data-stu-id="7ae57-123">Enum Design</span></span>](../../../docs/standard/design-guidelines/enum.md)  
 [<span data-ttu-id="7ae57-124">入れ子にされた型</span><span class="sxs-lookup"><span data-stu-id="7ae57-124">Nested Types</span></span>](../../../docs/standard/design-guidelines/nested-types.md)  
 <span data-ttu-id="7ae57-125">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="7ae57-125">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="7ae57-126">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="7ae57-126">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7ae57-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="7ae57-127">See also</span></span>

- [<span data-ttu-id="7ae57-128">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="7ae57-128">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
