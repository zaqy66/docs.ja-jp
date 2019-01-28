---
title: インターフェイスのプロパティ - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- properties [C#], on interfaces
- interfaces [C#], properties
ms.assetid: 6503e9ed-33d7-44ec-b4c1-cc16c084b795
ms.openlocfilehash: af80f403942f59d672854c80830e175ef7ebaff5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54652186"
---
# <a name="interface-properties-c-programming-guide"></a><span data-ttu-id="1a006-102">インターフェイスのプロパティ (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="1a006-102">Interface Properties (C# Programming Guide)</span></span>
<span data-ttu-id="1a006-103">[interface](../../../csharp/language-reference/keywords/interface.md) でプロパティを宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="1a006-103">Properties can be declared on an [interface](../../../csharp/language-reference/keywords/interface.md).</span></span> <span data-ttu-id="1a006-104">インターフェイスのプロパティ アクセサーの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="1a006-104">The following is an example of an interface property accessor:</span></span>  
  
 [!code-csharp[csProgGuideProperties#14](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/interface-properties_1.cs)]  
  
 <span data-ttu-id="1a006-105">インターフェイス プロパティのアクセサーには、本文はありません。</span><span class="sxs-lookup"><span data-stu-id="1a006-105">The accessor of an interface property does not have a body.</span></span> <span data-ttu-id="1a006-106">したがって、アクセサーの目的は、プロパティが読み取り/書き込み、読み取り専用、または書き込み専用のどれかを示すことです。</span><span class="sxs-lookup"><span data-stu-id="1a006-106">Thus, the purpose of the accessors is to indicate whether the property is read-write, read-only, or write-only.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1a006-107">例</span><span class="sxs-lookup"><span data-stu-id="1a006-107">Example</span></span>  
 <span data-ttu-id="1a006-108">この例では、インターフェイス `IEmployee` に読み取り/書き込み専用のプロパティ `Name` および読み取り専用のプロパティ `Counter` があります。</span><span class="sxs-lookup"><span data-stu-id="1a006-108">In this example, the interface `IEmployee` has a read-write property, `Name`, and a read-only property, `Counter`.</span></span> <span data-ttu-id="1a006-109">クラス `Employee` は `IEmployee` インターフェイスを実装し、これら 2 つのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="1a006-109">The class `Employee` implements the `IEmployee` interface and uses these two properties.</span></span> <span data-ttu-id="1a006-110">プログラムは、新しい従業員の名前と現在の従業員の数を読み込んで、従業員の名前と計算した従業員番号を表示します。</span><span class="sxs-lookup"><span data-stu-id="1a006-110">The program reads the name of a new employee and the current number of employees and displays the employee name and the computed employee number.</span></span>  
  
 <span data-ttu-id="1a006-111">メンバーが宣言されているインターフェイスを参照するプロパティの完全修飾名を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="1a006-111">You could use the fully qualified name of the property, which references the interface in which the member is declared.</span></span> <span data-ttu-id="1a006-112">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="1a006-112">For example:</span></span>  
  
 [!code-csharp[csProgGuideProperties#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/interface-properties_2.cs)]  
  
 <span data-ttu-id="1a006-113">これは、[明示的なインターフェイスの実装](../../../csharp/programming-guide/interfaces/explicit-interface-implementation.md)で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1a006-113">This is called [Explicit Interface Implementation](../../../csharp/programming-guide/interfaces/explicit-interface-implementation.md).</span></span> <span data-ttu-id="1a006-114">たとえば、`Employee` クラスが 2 つのインターフェイス `ICitizen` と `IEmployee` を実装し、両方のインターフェイスが同じ `Name` プロパティを持っている場合、明示的なインターフェイス メンバーの実装が必要です。</span><span class="sxs-lookup"><span data-stu-id="1a006-114">For example, if the class `Employee` is implementing two interfaces `ICitizen` and `IEmployee` and both interfaces have the `Name` property, the explicit interface member implementation will be necessary.</span></span> <span data-ttu-id="1a006-115">つまり、次のプロパティの宣言があります。</span><span class="sxs-lookup"><span data-stu-id="1a006-115">That is, the following property declaration:</span></span>  
  
 [!code-csharp[csProgGuideProperties#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/interface-properties_2.cs)]  
  
 <span data-ttu-id="1a006-116">これは、`IEmployee` インターフェイスで `Name` プロパティを実装します。次の宣言があります。</span><span class="sxs-lookup"><span data-stu-id="1a006-116">implements the `Name` property on the `IEmployee` interface, while the following declaration:</span></span>  
  
 [!code-csharp[csProgGuideProperties#17](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/interface-properties_3.cs)]  
  
 <span data-ttu-id="1a006-117">これは、`ICitizen` インターフェイスで `Name` プロパティを実装します。</span><span class="sxs-lookup"><span data-stu-id="1a006-117">implements the `Name` property on the `ICitizen` interface.</span></span>  
  
 [!code-csharp[csProgGuideProperties#15](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/interface-properties_4.cs)]  
  
  **`210 Hazem Abolrous`**    
## <a name="sample-output"></a><span data-ttu-id="1a006-118">出力例</span><span class="sxs-lookup"><span data-stu-id="1a006-118">Sample Output</span></span>  
 `Enter number of employees: 210`  
  
 `Enter the name of the new employee: Hazem Abolrous`  
  
 `The employee information:`  
  
 `Employee number: 211`  
  
 `Employee name: Hazem Abolrous`  
  
## <a name="see-also"></a><span data-ttu-id="1a006-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a006-119">See also</span></span>

- [<span data-ttu-id="1a006-120">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="1a006-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="1a006-121">プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a006-121">Properties</span></span>](../../../csharp/programming-guide/classes-and-structs/properties.md)
- [<span data-ttu-id="1a006-122">プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="1a006-122">Using Properties</span></span>](../../../csharp/programming-guide/classes-and-structs/using-properties.md)
- [<span data-ttu-id="1a006-123">プロパティとインデクサーの比較</span><span class="sxs-lookup"><span data-stu-id="1a006-123">Comparison Between Properties and Indexers</span></span>](../../../csharp/programming-guide/indexers/comparison-between-properties-and-indexers.md)
- [<span data-ttu-id="1a006-124">インデクサー</span><span class="sxs-lookup"><span data-stu-id="1a006-124">Indexers</span></span>](../../../csharp/programming-guide/indexers/index.md)
- [<span data-ttu-id="1a006-125">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1a006-125">Interfaces</span></span>](../../../csharp/programming-guide/interfaces/index.md)
