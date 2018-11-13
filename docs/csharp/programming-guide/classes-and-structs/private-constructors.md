---
title: プライベート コンストラクター (C# プログラミング ガイド)
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, private constructors
- private constructors [C#]
ms.assetid: 29eeaa7d-8d81-453c-94b9-0e2800172621
ms.openlocfilehash: 5b387447046e4755287fc9f6a8813a19752799c2
ms.sourcegitcommit: b5cd9d5d3b75a5537fc9ad8a3f085f0bb1845ee0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "50980717"
---
# <a name="private-constructors-c-programming-guide"></a><span data-ttu-id="cfdc7-102">プライベート コンストラクター (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="cfdc7-102">Private Constructors (C# Programming Guide)</span></span>
<span data-ttu-id="cfdc7-103">プライベート コンストラクターは、特別なインスタンス コンストラクターです。</span><span class="sxs-lookup"><span data-stu-id="cfdc7-103">A private constructor is a special instance constructor.</span></span> <span data-ttu-id="cfdc7-104">通常は、静的メンバーだけを含むクラスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="cfdc7-104">It is generally used in classes that contain static members only.</span></span> <span data-ttu-id="cfdc7-105">クラスに 1 つ以上のプライベート コンストラクターがあり、パブリック コンストラクターがない場合、他のクラス (入れ子になったクラスを除く) は、このクラスのインスタンスを作成できません。</span><span class="sxs-lookup"><span data-stu-id="cfdc7-105">If a class has one or more private constructors and no public constructors, other classes (except nested classes) cannot create instances of this class.</span></span> <span data-ttu-id="cfdc7-106">例:</span><span class="sxs-lookup"><span data-stu-id="cfdc7-106">For example:</span></span>  
  
 [!code-csharp[csProgGuideObjects#11](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_1.cs)]  
  
 <span data-ttu-id="cfdc7-107">空のコンストラクターを宣言すると、既定コンストラクターの自動生成は行われません。</span><span class="sxs-lookup"><span data-stu-id="cfdc7-107">The declaration of the empty constructor prevents the automatic generation of a default constructor.</span></span> <span data-ttu-id="cfdc7-108">コンストラクターにアクセス修飾子を指定しない場合でも、コンストラクターは既定でプライベートになります。</span><span class="sxs-lookup"><span data-stu-id="cfdc7-108">Note that if you do not use an access modifier with the constructor it will still be private by default.</span></span> <span data-ttu-id="cfdc7-109">しかし、通常は、[プライベート](../../../csharp/language-reference/keywords/private.md)修飾子を明示的に使用して、クラスをインスタンス化できないことを明確に示します。</span><span class="sxs-lookup"><span data-stu-id="cfdc7-109">However, the [private](../../../csharp/language-reference/keywords/private.md) modifier is usually used explicitly to make it clear that the class cannot be instantiated.</span></span>  
  
 <span data-ttu-id="cfdc7-110">プライベート コンストラクターは、<xref:System.Math> クラスなどのインスタンス フィールドやメソッドが存在しない場合や、クラスのインスタンスを取得するためにメソッドが呼び出される場合に、クラスのインスタンスが作成されないようにするために使用します。</span><span class="sxs-lookup"><span data-stu-id="cfdc7-110">Private constructors are used to prevent creating instances of a class when there are no instance fields or methods, such as the <xref:System.Math> class, or when a method is called to obtain an instance of a class.</span></span> <span data-ttu-id="cfdc7-111">クラス内のすべてのメソッドが静的な場合は、クラス全体を静的にすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="cfdc7-111">If all the methods in the class are static, consider making the complete class static.</span></span> <span data-ttu-id="cfdc7-112">詳細については、「[静的クラスと静的クラス メンバー](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cfdc7-112">For more information see [Static Classes and Static Class Members](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="cfdc7-113">例</span><span class="sxs-lookup"><span data-stu-id="cfdc7-113">Example</span></span>  
 <span data-ttu-id="cfdc7-114">次に示すのは、プライベート コンストラクターを使用するクラスの例です。</span><span class="sxs-lookup"><span data-stu-id="cfdc7-114">The following is an example of a class using a private constructor.</span></span>  
  
 [!code-csharp[csProgGuideObjects#12](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_2.cs)]  
  
 <span data-ttu-id="cfdc7-115">この例で、次のステートメントをコメント解除すると、保護レベルのためにコンストラクターにアクセスできなくなり、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="cfdc7-115">Notice that if you uncomment the following statement from the example, it will generate an error because the constructor is inaccessible because of its protection level:</span></span>  
  
 [!code-csharp[csProgGuideObjects#13](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_3.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="cfdc7-116">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="cfdc7-116">C# Language Specification</span></span>  

<span data-ttu-id="cfdc7-117">詳細については、「[C# 言語仕様](../../language-reference/language-specification/index.md)」の[プライベート コンストラクター](~/_csharplang/spec/classes.md#private-constructors)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cfdc7-117">For more information, see [Private constructors](~/_csharplang/spec/classes.md#private-constructors) in the [C# Language Specification](../../language-reference/language-specification/index.md).</span></span> <span data-ttu-id="cfdc7-118">言語仕様は、C# の構文と使用法に関する信頼性のある情報源です。</span><span class="sxs-lookup"><span data-stu-id="cfdc7-118">The language specification is the definitive source for C# syntax and usage.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cfdc7-119">参照</span><span class="sxs-lookup"><span data-stu-id="cfdc7-119">See Also</span></span>

- [<span data-ttu-id="cfdc7-120">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="cfdc7-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="cfdc7-121">クラスと構造体</span><span class="sxs-lookup"><span data-stu-id="cfdc7-121">Classes and Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/index.md)  
- [<span data-ttu-id="cfdc7-122">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="cfdc7-122">Constructors</span></span>](../../../csharp/programming-guide/classes-and-structs/constructors.md)  
- [<span data-ttu-id="cfdc7-123">ファイナライザー</span><span class="sxs-lookup"><span data-stu-id="cfdc7-123">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)  
- [<span data-ttu-id="cfdc7-124">private</span><span class="sxs-lookup"><span data-stu-id="cfdc7-124">private</span></span>](../../../csharp/language-reference/keywords/private.md)  
- [<span data-ttu-id="cfdc7-125">public</span><span class="sxs-lookup"><span data-stu-id="cfdc7-125">public</span></span>](../../../csharp/language-reference/keywords/public.md)
