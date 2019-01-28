---
title: プライベート コンストラクター - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, private constructors
- private constructors [C#]
ms.assetid: 29eeaa7d-8d81-453c-94b9-0e2800172621
ms.openlocfilehash: e406b72e5d2932464c407dce014dd8eceee59fb0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577296"
---
# <a name="private-constructors-c-programming-guide"></a><span data-ttu-id="1e36d-102">プライベート コンストラクター (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="1e36d-102">Private Constructors (C# Programming Guide)</span></span>
<span data-ttu-id="1e36d-103">プライベート コンストラクターは、特別なインスタンス コンストラクターです。</span><span class="sxs-lookup"><span data-stu-id="1e36d-103">A private constructor is a special instance constructor.</span></span> <span data-ttu-id="1e36d-104">通常は、静的メンバーだけを含むクラスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="1e36d-104">It is generally used in classes that contain static members only.</span></span> <span data-ttu-id="1e36d-105">クラスに 1 つ以上のプライベート コンストラクターがあり、パブリック コンストラクターがない場合、他のクラス (入れ子になったクラスを除く) は、このクラスのインスタンスを作成できません。</span><span class="sxs-lookup"><span data-stu-id="1e36d-105">If a class has one or more private constructors and no public constructors, other classes (except nested classes) cannot create instances of this class.</span></span> <span data-ttu-id="1e36d-106">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="1e36d-106">For example:</span></span>  
  
 [!code-csharp[csProgGuideObjects#11](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_1.cs)]  
  
 <span data-ttu-id="1e36d-107">空のコンストラクターを宣言すると、既定コンストラクターの自動生成は行われません。</span><span class="sxs-lookup"><span data-stu-id="1e36d-107">The declaration of the empty constructor prevents the automatic generation of a default constructor.</span></span> <span data-ttu-id="1e36d-108">コンストラクターにアクセス修飾子を指定しない場合でも、コンストラクターは既定でプライベートになります。</span><span class="sxs-lookup"><span data-stu-id="1e36d-108">Note that if you do not use an access modifier with the constructor it will still be private by default.</span></span> <span data-ttu-id="1e36d-109">しかし、通常は、[プライベート](../../../csharp/language-reference/keywords/private.md)修飾子を明示的に使用して、クラスをインスタンス化できないことを明確に示します。</span><span class="sxs-lookup"><span data-stu-id="1e36d-109">However, the [private](../../../csharp/language-reference/keywords/private.md) modifier is usually used explicitly to make it clear that the class cannot be instantiated.</span></span>  
  
 <span data-ttu-id="1e36d-110">プライベート コンストラクターは、<xref:System.Math> クラスなどのインスタンス フィールドやメソッドが存在しない場合や、クラスのインスタンスを取得するためにメソッドが呼び出される場合に、クラスのインスタンスが作成されないようにするために使用します。</span><span class="sxs-lookup"><span data-stu-id="1e36d-110">Private constructors are used to prevent creating instances of a class when there are no instance fields or methods, such as the <xref:System.Math> class, or when a method is called to obtain an instance of a class.</span></span> <span data-ttu-id="1e36d-111">クラス内のすべてのメソッドが静的な場合は、クラス全体を静的にすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="1e36d-111">If all the methods in the class are static, consider making the complete class static.</span></span> <span data-ttu-id="1e36d-112">詳細については、「[静的クラスと静的クラス メンバー](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e36d-112">For more information see [Static Classes and Static Class Members](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1e36d-113">例</span><span class="sxs-lookup"><span data-stu-id="1e36d-113">Example</span></span>  
 <span data-ttu-id="1e36d-114">次に示すのは、プライベート コンストラクターを使用するクラスの例です。</span><span class="sxs-lookup"><span data-stu-id="1e36d-114">The following is an example of a class using a private constructor.</span></span>  
  
 [!code-csharp[csProgGuideObjects#12](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_2.cs)]  
  
 <span data-ttu-id="1e36d-115">この例で、次のステートメントをコメント解除すると、保護レベルのためにコンストラクターにアクセスできなくなり、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="1e36d-115">Notice that if you uncomment the following statement from the example, it will generate an error because the constructor is inaccessible because of its protection level:</span></span>  
  
 [!code-csharp[csProgGuideObjects#13](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_3.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="1e36d-116">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="1e36d-116">C# Language Specification</span></span>  

<span data-ttu-id="1e36d-117">詳細については、「[C# 言語仕様](../../language-reference/language-specification/index.md)」の[プライベート コンストラクター](~/_csharplang/spec/classes.md#private-constructors)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e36d-117">For more information, see [Private constructors](~/_csharplang/spec/classes.md#private-constructors) in the [C# Language Specification](../../language-reference/language-specification/index.md).</span></span> <span data-ttu-id="1e36d-118">言語仕様は、C# の構文と使用法に関する信頼性のある情報源です。</span><span class="sxs-lookup"><span data-stu-id="1e36d-118">The language specification is the definitive source for C# syntax and usage.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1e36d-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="1e36d-119">See also</span></span>

- [<span data-ttu-id="1e36d-120">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="1e36d-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="1e36d-121">クラスと構造体</span><span class="sxs-lookup"><span data-stu-id="1e36d-121">Classes and Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/index.md)
- [<span data-ttu-id="1e36d-122">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="1e36d-122">Constructors</span></span>](../../../csharp/programming-guide/classes-and-structs/constructors.md)
- [<span data-ttu-id="1e36d-123">ファイナライザー</span><span class="sxs-lookup"><span data-stu-id="1e36d-123">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)
- [<span data-ttu-id="1e36d-124">private</span><span class="sxs-lookup"><span data-stu-id="1e36d-124">private</span></span>](../../../csharp/language-reference/keywords/private.md)
- [<span data-ttu-id="1e36d-125">public</span><span class="sxs-lookup"><span data-stu-id="1e36d-125">public</span></span>](../../../csharp/language-reference/keywords/public.md)
