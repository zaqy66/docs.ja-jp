---
title: ジェネリック - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, generics
- generics [C#]
ms.assetid: 75ea8509-a4ea-4e7a-a2b3-cf72482e9282
ms.openlocfilehash: 03a5a594db86f5286979dbe22a8841f0e7d4518c
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53240868"
---
# <a name="generics-c-programming-guide"></a><span data-ttu-id="93007-102">ジェネリック (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="93007-102">Generics (C# Programming Guide)</span></span>
<span data-ttu-id="93007-103">ジェネリックは、バージョン 2.0 の C# 言語と共通言語ランタイム (CLR) に追加されたものです。</span><span class="sxs-lookup"><span data-stu-id="93007-103">Generics were added to version 2.0 of the C# language and the common language runtime (CLR).</span></span> <span data-ttu-id="93007-104">ジェネリックは、.NET Framework に型パラメーターという概念を導入します。型パラメーターを使用すると、クラスやメソッドがクライアント コードで宣言され、インスタンス化されるまで、1 つ以上の型の指定を遅延させるクラスとメソッドを設計できます。</span><span class="sxs-lookup"><span data-stu-id="93007-104">Generics introduce to the .NET Framework the concept of type parameters, which make it possible to design classes and methods that defer the specification of one or more types until the class or method is declared and instantiated by client code.</span></span> <span data-ttu-id="93007-105">たとえば、ジェネリック型パラメーター T を使用すると、次に示すようにランタイムのキャストやボックス化操作のコストやリスクを負わずに他のクライアント コードで使用できる単一のクラスを記述できます。</span><span class="sxs-lookup"><span data-stu-id="93007-105">For example, by using a generic type parameter T you can write a single class that other client code can use without incurring the cost or risk of runtime casts or boxing operations, as shown here:</span></span>  
  
 [!code-csharp[csProgGuideGenerics#1](../../../csharp/programming-guide/generics/codesnippet/CSharp/index_1.cs)]  
  
## <a name="generics-overview"></a><span data-ttu-id="93007-106">ジェネリックの概要</span><span class="sxs-lookup"><span data-stu-id="93007-106">Generics Overview</span></span>  
  
-   <span data-ttu-id="93007-107">ジェネリック型は、コードの再利用、タイプ セーフ、およびパフォーマンスを最大化するために使用します。</span><span class="sxs-lookup"><span data-stu-id="93007-107">Use generic types to maximize code reuse, type safety, and performance.</span></span>  
  
-   <span data-ttu-id="93007-108">ジェネリックの最も一般的な用途は、コレクション クラスの作成です。</span><span class="sxs-lookup"><span data-stu-id="93007-108">The most common use of generics is to create collection classes.</span></span>  
  
-   <span data-ttu-id="93007-109">.NET Framework クラス ライブラリには、複数の新しいジェネリック コレクション クラスが <xref:System.Collections.Generic> 名前空間に含まれています。</span><span class="sxs-lookup"><span data-stu-id="93007-109">The .NET Framework class library contains several new generic collection classes in the <xref:System.Collections.Generic> namespace.</span></span> <span data-ttu-id="93007-110"><xref:System.Collections> 名前空間の <xref:System.Collections.ArrayList> などのクラスの代わりとして、できる限りこれらを使用してください。</span><span class="sxs-lookup"><span data-stu-id="93007-110">These should be used whenever possible instead of classes such as <xref:System.Collections.ArrayList> in the <xref:System.Collections> namespace.</span></span>  
  
-   <span data-ttu-id="93007-111">独自のジェネリック インターフェイス、クラス、メソッド、イベントおよびデリゲートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="93007-111">You can create your own generic interfaces, classes, methods, events and delegates.</span></span>  
  
-   <span data-ttu-id="93007-112">ジェネリック クラスは、特定のデータ型のメソッドへのアクセスを有効にするように制限できます。</span><span class="sxs-lookup"><span data-stu-id="93007-112">Generic classes may be constrained to enable access to methods on particular data types.</span></span>  
  
-   <span data-ttu-id="93007-113">ジェネリック データ型で使用される型に関する情報は、実行時にリフレクションを使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="93007-113">Information on the types that are used in a generic data type may be obtained at run-time by using reflection.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="93007-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="93007-114">Related Sections</span></span>  
 <span data-ttu-id="93007-115">詳細情報</span><span class="sxs-lookup"><span data-stu-id="93007-115">For more information:</span></span>  
  
-   [<span data-ttu-id="93007-116">ジェネリックの概要</span><span class="sxs-lookup"><span data-stu-id="93007-116">Introduction to Generics</span></span>](../../../csharp/programming-guide/generics/introduction-to-generics.md)  
  
-   [<span data-ttu-id="93007-117">ジェネリックの利点</span><span class="sxs-lookup"><span data-stu-id="93007-117">Benefits of Generics</span></span>](../../../csharp/programming-guide/generics/benefits-of-generics.md)  
  
-   [<span data-ttu-id="93007-118">ジェネリック型パラメーター</span><span class="sxs-lookup"><span data-stu-id="93007-118">Generic Type Parameters</span></span>](../../../csharp/programming-guide/generics/generic-type-parameters.md)  
  
-   [<span data-ttu-id="93007-119">型パラメーターの制約</span><span class="sxs-lookup"><span data-stu-id="93007-119">Constraints on Type Parameters</span></span>](../../../csharp/programming-guide/generics/constraints-on-type-parameters.md)  
  
-   [<span data-ttu-id="93007-120">ジェネリック クラス</span><span class="sxs-lookup"><span data-stu-id="93007-120">Generic Classes</span></span>](../../../csharp/programming-guide/generics/generic-classes.md)  
  
-   [<span data-ttu-id="93007-121">ジェネリック インターフェイス</span><span class="sxs-lookup"><span data-stu-id="93007-121">Generic Interfaces</span></span>](../../../csharp/programming-guide/generics/generic-interfaces.md)  
  
-   [<span data-ttu-id="93007-122">ジェネリック メソッド</span><span class="sxs-lookup"><span data-stu-id="93007-122">Generic Methods</span></span>](../../../csharp/programming-guide/generics/generic-methods.md)  
  
-   [<span data-ttu-id="93007-123">汎用デリゲート</span><span class="sxs-lookup"><span data-stu-id="93007-123">Generic Delegates</span></span>](../../../csharp/programming-guide/generics/generic-delegates.md)  
  
-   [<span data-ttu-id="93007-124">C++ テンプレートと C# ジェネリックの違い</span><span class="sxs-lookup"><span data-stu-id="93007-124">Differences Between C++ Templates and C# Generics</span></span>](../../../csharp/programming-guide/generics/differences-between-cpp-templates-and-csharp-generics.md)  
  
-   [<span data-ttu-id="93007-125">ジェネリックとリフレクション</span><span class="sxs-lookup"><span data-stu-id="93007-125">Generics and Reflection</span></span>](../../../csharp/programming-guide/generics/generics-and-reflection.md)  
  
-   [<span data-ttu-id="93007-126">ランタイムのジェネリック</span><span class="sxs-lookup"><span data-stu-id="93007-126">Generics in the Run Time</span></span>](../../../csharp/programming-guide/generics/generics-in-the-run-time.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="93007-127">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="93007-127">C# Language Specification</span></span>  
 <span data-ttu-id="93007-128">詳細については、「[C# 言語の仕様](~/_csharplang/spec/types.md#constructed-types)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93007-128">For more information, see the [C# Language Specification](~/_csharplang/spec/types.md#constructed-types).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93007-129">参照</span><span class="sxs-lookup"><span data-stu-id="93007-129">See Also</span></span>

- <xref:System.Collections.Generic>  
- [<span data-ttu-id="93007-130">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="93007-130">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="93007-131">型</span><span class="sxs-lookup"><span data-stu-id="93007-131">Types</span></span>](../../../csharp/programming-guide/types/index.md)  
- [<span data-ttu-id="93007-132">\<typeparam></span><span class="sxs-lookup"><span data-stu-id="93007-132">\<typeparam></span></span>](../../../csharp/programming-guide/xmldoc/typeparam.md)  
- [<span data-ttu-id="93007-133">\<typeparamref></span><span class="sxs-lookup"><span data-stu-id="93007-133">\<typeparamref></span></span>](../../../csharp/programming-guide/xmldoc/typeparamref.md)  
- [<span data-ttu-id="93007-134">.NET のジェネリック</span><span class="sxs-lookup"><span data-stu-id="93007-134">Generics in .NET</span></span>](../../../standard/generics/index.md)  