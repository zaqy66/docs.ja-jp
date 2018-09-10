---
title: volatile (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- volatile_CSharpKeyword
- volatile
helpviewer_keywords:
- volatile keyword [C#]
ms.assetid: 78089bc7-7b38-4cfd-9e49-87ac036af009
ms.openlocfilehash: be7e081b18702710c00b5b86a9bc152800f0cf3d
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43526220"
---
# <a name="volatile-c-reference"></a><span data-ttu-id="5c11e-102">volatile (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="5c11e-102">volatile (C# Reference)</span></span>
<span data-ttu-id="5c11e-103">`volatile` キーワードは、同時に実行されている複数のスレッドによって、フィールドが変更される可能性があることを示します。</span><span class="sxs-lookup"><span data-stu-id="5c11e-103">The `volatile` keyword indicates that a field might be modified by multiple threads that are executing at the same time.</span></span> <span data-ttu-id="5c11e-104">`volatile` と宣言されているフィールドは、シングル スレッドによるアクセスを前提とする、コンパイラの最適化の対象にはなりません。</span><span class="sxs-lookup"><span data-stu-id="5c11e-104">Fields that are declared `volatile` are not subject to compiler optimizations that assume access by a single thread.</span></span> <span data-ttu-id="5c11e-105">これらの制限により、すべてのスレッドが、他のスレッドによって実行された volatile の書き込みを、実行された順序で観察することが保証されます。</span><span class="sxs-lookup"><span data-stu-id="5c11e-105">These restrictions ensure that all threads will observe volatile writes performed by any other thread in the order in which they were performed.</span></span> <span data-ttu-id="5c11e-106">volatile 書き込みの単一の全体的順序がすべての実行スレッドから認識される保証はありません。</span><span class="sxs-lookup"><span data-stu-id="5c11e-106">There is no guarantee of a single total ordering of volatile writes as seen from all threads of execution.</span></span>  
  
 <span data-ttu-id="5c11e-107">`volatile` 修飾子は、通常、アクセスをシリアル化する [lock](../../../csharp/language-reference/keywords/lock-statement.md) ステートメントが使用されない場合に、複数のスレッドからアクセスされるフィールドに対して使用します。</span><span class="sxs-lookup"><span data-stu-id="5c11e-107">The `volatile` modifier is usually used for a field that is accessed by multiple threads without using the [lock](../../../csharp/language-reference/keywords/lock-statement.md) statement to serialize access.</span></span>  
  
 <span data-ttu-id="5c11e-108">`volatile` キーワードは次の型のフィールドに使用できます。</span><span class="sxs-lookup"><span data-stu-id="5c11e-108">The `volatile` keyword can be applied to fields of these types:</span></span>  
  
-   <span data-ttu-id="5c11e-109">参照型。</span><span class="sxs-lookup"><span data-stu-id="5c11e-109">Reference types.</span></span>  
  
-   <span data-ttu-id="5c11e-110">ポインター型 (unsafe コンテキスト内)。</span><span class="sxs-lookup"><span data-stu-id="5c11e-110">Pointer types (in an unsafe context).</span></span> <span data-ttu-id="5c11e-111">ポインター自体は volatile にできますが、ポインターが指しているオブジェクトは volatile にできません。</span><span class="sxs-lookup"><span data-stu-id="5c11e-111">Note that although the pointer itself can be volatile, the object that it points to cannot.</span></span> <span data-ttu-id="5c11e-112">つまり、"volatile を指すポインター" は宣言できません。</span><span class="sxs-lookup"><span data-stu-id="5c11e-112">In other words, you cannot declare a "pointer to volatile."</span></span>  
  
-   <span data-ttu-id="5c11e-113">sbyte、byte、short、ushort、int、uint、char、float、bool などの型。</span><span class="sxs-lookup"><span data-stu-id="5c11e-113">Types such as sbyte, byte, short, ushort, int, uint, char, float, and bool.</span></span>  
  
-   <span data-ttu-id="5c11e-114">基本データ型 byte、sbyte、short、ushort、int、または uint のいずれかが含まれる列挙型。</span><span class="sxs-lookup"><span data-stu-id="5c11e-114">An enum type with one of the following base types: byte, sbyte, short, ushort, int, or uint.</span></span>  
  
-   <span data-ttu-id="5c11e-115">参照型であることが判明しているジェネリック型パラメーター。</span><span class="sxs-lookup"><span data-stu-id="5c11e-115">Generic type parameters known to be reference types.</span></span>  
  
-   <span data-ttu-id="5c11e-116"><xref:System.IntPtr> および <xref:System.UIntPtr>。</span><span class="sxs-lookup"><span data-stu-id="5c11e-116"><xref:System.IntPtr> and <xref:System.UIntPtr>.</span></span>  
  
 <span data-ttu-id="5c11e-117">volatile キーワードは、クラスまたは構造体のフィールドにのみ適用できます。</span><span class="sxs-lookup"><span data-stu-id="5c11e-117">The volatile keyword can only be applied to fields of a class or struct.</span></span> <span data-ttu-id="5c11e-118">ローカル変数を `volatile` として宣言することはできません。</span><span class="sxs-lookup"><span data-stu-id="5c11e-118">Local variables cannot be declared `volatile`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5c11e-119">例</span><span class="sxs-lookup"><span data-stu-id="5c11e-119">Example</span></span>  
 <span data-ttu-id="5c11e-120">次の例は、public のフィールド変数を `volatile` として宣言する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5c11e-120">The following example shows how to declare a public field variable as `volatile`.</span></span>  
  
 [!code-csharp[csrefKeywordsModifiers#24](../../../csharp/language-reference/keywords/codesnippet/CSharp/volatile_1.cs)]  
  
## <a name="example"></a><span data-ttu-id="5c11e-121">例</span><span class="sxs-lookup"><span data-stu-id="5c11e-121">Example</span></span>  
 <span data-ttu-id="5c11e-122">次の例は、補助スレッドつまりワーカー スレッドを作成および使用して、プライマリ スレッドとの並行処理を実行する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5c11e-122">The following example demonstrates how an auxiliary or worker thread can be created and used to perform processing in parallel with that of the primary thread.</span></span> <span data-ttu-id="5c11e-123">マルチスレッドの背景情報については、「[マネージド スレッド処理](../../../standard/threading/index.md)」および「[スレッド処理 (C#)](../../programming-guide/concepts/threading/index.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5c11e-123">For background information about multithreading, see [Managed Threading](../../../standard/threading/index.md) and [Threading (C#)](../../programming-guide/concepts/threading/index.md).</span></span>  
  
 [!code-csharp[csProgGuideThreading#1](../../../csharp/language-reference/keywords/codesnippet/CSharp/volatile_2.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="5c11e-124">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="5c11e-124">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="5c11e-125">参照</span><span class="sxs-lookup"><span data-stu-id="5c11e-125">See Also</span></span>

- [<span data-ttu-id="5c11e-126">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="5c11e-126">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="5c11e-127">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="5c11e-127">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="5c11e-128">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="5c11e-128">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="5c11e-129">修飾子</span><span class="sxs-lookup"><span data-stu-id="5c11e-129">Modifiers</span></span>](../../../csharp/language-reference/keywords/modifiers.md)
