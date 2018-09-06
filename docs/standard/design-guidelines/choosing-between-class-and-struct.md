---
title: クラスまたは構造体の選択
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], structures
- class library design guidelines [.NET Framework], classes
- structures [.NET Framework], vs. classes
- classes [.NET Framework], design guidelines
- type design guidelines, structures
- structures [.NET Framework], design guidelines
- classes [.NET Framework], vs. structures
- type design guidelines, classes
ms.assetid: f8b8ec9b-0ba7-4dea-aadf-a93395cd804f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 06661cb2c34d1da9085fa2129cb0c3307b99097e
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43865554"
---
# <a name="choosing-between-class-and-struct"></a><span data-ttu-id="5f84f-102">クラスまたは構造体の選択</span><span class="sxs-lookup"><span data-stu-id="5f84f-102">Choosing Between Class and Struct</span></span>
<span data-ttu-id="5f84f-103">すべての framework デザイナーに直面して基本的な設計上の決定の 1 つが、クラス (参照型)、または構造体 (値型) として型を設計するかどうか。</span><span class="sxs-lookup"><span data-stu-id="5f84f-103">One of the basic design decisions every framework designer faces is whether to design a type as a class (a reference type) or as a struct (a value type).</span></span> <span data-ttu-id="5f84f-104">参照型と値の型の動作の違いの理解は、この選択を行うに不可欠です。</span><span class="sxs-lookup"><span data-stu-id="5f84f-104">Good understanding of the differences in the behavior of reference types and value types is crucial in making this choice.</span></span>  
  
 <span data-ttu-id="5f84f-105">最初の差。 参照型と値の型は、参照型とガベージ コレクションのヒープに割り当てられた値の型が割り当てられたスタックのいずれかまたはインラインで含まれている型し割り当て解除されたときに検討のスタックアンワインドまたは取得、含んでいる型の割り当てを解除する場合。</span><span class="sxs-lookup"><span data-stu-id="5f84f-105">The first difference between reference types and value types we will consider is that reference types are allocated on the heap and garbage-collected, whereas value types are allocated either on the stack or inline in containing types and deallocated when the stack unwinds or when their containing type gets deallocated.</span></span> <span data-ttu-id="5f84f-106">したがって、値型の割り当てと解放は、一般的な参照型の割り当てと解放よりも低コストになります。</span><span class="sxs-lookup"><span data-stu-id="5f84f-106">Therefore, allocations and deallocations of value types are in general cheaper than allocations and deallocations of reference types.</span></span>  
  
 <span data-ttu-id="5f84f-107">次に、参照型の配列では、行外、つまり配列要素に、ヒープ上にある参照型のインスタンスへの参照のみが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="5f84f-107">Next, arrays of reference types are allocated out-of-line, meaning the array elements are just references to instances of the reference type residing on the heap.</span></span> <span data-ttu-id="5f84f-108">値型の配列には、インライン、つまり、配列要素は、値の型の実際のインスタンスが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="5f84f-108">Value type arrays are allocated inline, meaning that the array elements are the actual instances of the value type.</span></span> <span data-ttu-id="5f84f-109">したがって、値型の配列の割り当てと解放は、参照型の配列の割り当てと解放よりもかなり安くなります。</span><span class="sxs-lookup"><span data-stu-id="5f84f-109">Therefore, allocations and deallocations of value type arrays are much cheaper than allocations and deallocations of reference type arrays.</span></span> <span data-ttu-id="5f84f-110">さらに、ほとんどの場合は、値型の配列と、参照の局所性量が高くが発生します。</span><span class="sxs-lookup"><span data-stu-id="5f84f-110">In addition, in a majority of cases value type arrays exhibit much better locality of reference.</span></span>  
  
 <span data-ttu-id="5f84f-111">次の相違点は、メモリ使用量に関連します。</span><span class="sxs-lookup"><span data-stu-id="5f84f-111">The next difference is related to memory usage.</span></span> <span data-ttu-id="5f84f-112">値型は、参照型またはいずれかを実装するインターフェイスにキャストするときをボックス化を取得します。</span><span class="sxs-lookup"><span data-stu-id="5f84f-112">Value types get boxed when cast to a reference type or one of the interfaces they implement.</span></span> <span data-ttu-id="5f84f-113">ボックス化解除された取得値の型にキャストするとき。</span><span class="sxs-lookup"><span data-stu-id="5f84f-113">They get unboxed when cast back to the value type.</span></span> <span data-ttu-id="5f84f-114">ボックス オブジェクトはヒープに割り当てられ、ガベージ コレクションが、あまりボックス化とボックス化解除するため、ヒープ、ガベージ コレクター、および最終的には、アプリケーションのパフォーマンスに悪影響を及ぼすことができます。</span><span class="sxs-lookup"><span data-stu-id="5f84f-114">Because boxes are objects that are allocated on the heap and are garbage-collected, too much boxing and unboxing can have a negative impact on the heap, the garbage collector, and ultimately the performance of the application.</span></span>  <span data-ttu-id="5f84f-115">これに対し、このようなボックス化は行われません、参照型にキャストされます。</span><span class="sxs-lookup"><span data-stu-id="5f84f-115">In contrast, no such boxing occurs as reference types are cast.</span></span>  
  
 <span data-ttu-id="5f84f-116">次に、参照型の割り当ては、値型の割り当て値全体をコピーする一方、参照をコピーします。</span><span class="sxs-lookup"><span data-stu-id="5f84f-116">Next, reference type assignments copy the reference, whereas value type assignments copy the entire value.</span></span> <span data-ttu-id="5f84f-117">そのため、大規模な参照型の割り当ては、大きな値の型の割り当てよりも低コストです。</span><span class="sxs-lookup"><span data-stu-id="5f84f-117">Therefore, assignments of large reference types are cheaper than assignments of large value types.</span></span>  
  
 <span data-ttu-id="5f84f-118">最後に、値の型が値によって渡されますが、参照型は、参照によって渡されます。</span><span class="sxs-lookup"><span data-stu-id="5f84f-118">Finally, reference types are passed by reference, whereas value types are passed by value.</span></span> <span data-ttu-id="5f84f-119">参照型のインスタンスへの変更では、インスタンスを指すすべての参照に影響します。</span><span class="sxs-lookup"><span data-stu-id="5f84f-119">Changes to an instance of a reference type affect all references pointing to the instance.</span></span> <span data-ttu-id="5f84f-120">値型のインスタンスは、値によって渡されるときにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5f84f-120">Value type instances are copied when they are passed by value.</span></span> <span data-ttu-id="5f84f-121">値型のインスタンスが変更されたときに、もちろんには影響しません、そのコピーのいずれか。</span><span class="sxs-lookup"><span data-stu-id="5f84f-121">When an instance of a value type is changed, it of course does not affect any of its copies.</span></span> <span data-ttu-id="5f84f-122">コピーは、ユーザーが明示的に作成されませんが、引数が渡される、または返される値を返すときに暗黙的に作成される、ために、変更可能な値の型は、多数のユーザーに混乱があります。</span><span class="sxs-lookup"><span data-stu-id="5f84f-122">Because the copies are not created explicitly by the user but are implicitly created when arguments are passed or return values are returned, value types that can be changed can be confusing to many users.</span></span> <span data-ttu-id="5f84f-123">そのため、値の型は変更できません。</span><span class="sxs-lookup"><span data-stu-id="5f84f-123">Therefore, value types should be immutable.</span></span>  
  
 <span data-ttu-id="5f84f-124">一般に、フレームワーク内の型の大部分は、クラスできなければなりません。</span><span class="sxs-lookup"><span data-stu-id="5f84f-124">As a rule of thumb, the majority of types in a framework should be classes.</span></span> <span data-ttu-id="5f84f-125">ただし、状況によっては、値型の特性ようにより適切に構造体を使用するがあります。</span><span class="sxs-lookup"><span data-stu-id="5f84f-125">There are, however, some situations in which the characteristics of a value type make it more appropriate to use structs.</span></span>  
  
 <span data-ttu-id="5f84f-126">**✓ CONSIDER** 型のインスタンスは小さく、一般的な有効期間が短いまたはその他のオブジェクトに埋め込まれている一般的な場合は、クラスの代わりに構造体を定義することです。</span><span class="sxs-lookup"><span data-stu-id="5f84f-126">**✓ CONSIDER** defining a struct instead of a class if instances of the type are small and commonly short-lived or are commonly embedded in other objects.</span></span>  
  
 <span data-ttu-id="5f84f-127">**X AVOID** すべて次の特徴の種類があるない限り、構造体を定義します。</span><span class="sxs-lookup"><span data-stu-id="5f84f-127">**X AVOID** defining a struct unless the type has all of the following characteristics:</span></span>  
  
-   <span data-ttu-id="5f84f-128">プリミティブ型のような 1 つの値を論理的に表す (`int`、`double`など。)。</span><span class="sxs-lookup"><span data-stu-id="5f84f-128">It logically represents a single value, similar to primitive types (`int`, `double`, etc.).</span></span>  
  
-   <span data-ttu-id="5f84f-129">16 バイト未満のサイズのインスタンスがあります。</span><span class="sxs-lookup"><span data-stu-id="5f84f-129">It has an instance size under 16 bytes.</span></span>  
  
-   <span data-ttu-id="5f84f-130">変更可能なことはできません。</span><span class="sxs-lookup"><span data-stu-id="5f84f-130">It is immutable.</span></span>  
  
-   <span data-ttu-id="5f84f-131">頻繁にボックス化することはありません。</span><span class="sxs-lookup"><span data-stu-id="5f84f-131">It will not have to be boxed frequently.</span></span>  
  
 <span data-ttu-id="5f84f-132">他のすべてのケースでは、クラスとして、型を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f84f-132">In all other cases, you should define your types as classes.</span></span>  
  
 <span data-ttu-id="5f84f-133">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="5f84f-133">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="5f84f-134">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="5f84f-134">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f84f-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f84f-135">See also</span></span>

- [<span data-ttu-id="5f84f-136">型デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="5f84f-136">Type Design Guidelines</span></span>](../../../docs/standard/design-guidelines/type.md)  
- [<span data-ttu-id="5f84f-137">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="5f84f-137">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
