---
title: ':: 演算子 (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- ::_CSharpKeyword
helpviewer_keywords:
- ':: operator [C#]'
- 'namespaces [C#], :: operator'
- namespace alias qualifier operator (::) [C#]
ms.assetid: 698b5a73-85cf-4e0e-9e8e-6496887f8527
ms.openlocfilehash: 077d5835b372897cbe797385271effc5d00bf6e3
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43525657"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="1e56f-102">:: 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="1e56f-102">:: Operator (C# Reference)</span></span>
<span data-ttu-id="1e56f-103">名前空間エイリアス修飾子 (`::`) を使用して識別子を検索できます。</span><span class="sxs-lookup"><span data-stu-id="1e56f-103">The namespace alias qualifier (`::`) is used to look up identifiers.</span></span> <span data-ttu-id="1e56f-104">この例に示すように、常に 2 つの識別子の間に配置します。</span><span class="sxs-lookup"><span data-stu-id="1e56f-104">It is always positioned between two identifiers, as in this example:</span></span>  
  
 [!code-csharp[csRefOperators#27](../../../csharp/language-reference/operators/codesnippet/CSharp/namespace-alias-qualifer_1.cs)]  

<span data-ttu-id="1e56f-105">`::` 演算子は、"*using 別名ディレクティブ*" と一緒に使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="1e56f-105">The `::` operator can also be used with a *using alias directive*:</span></span>

```csharp
// using Col=System.Collections.Generic;
var numbers = new Col::List<int> { 1, 2, 3 };
```

## <a name="remarks"></a><span data-ttu-id="1e56f-106">コメント</span><span class="sxs-lookup"><span data-stu-id="1e56f-106">Remarks</span></span>  
 <span data-ttu-id="1e56f-107">名前空間エイリアス修飾子として `global` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1e56f-107">The namespace alias qualifier can be `global`.</span></span> <span data-ttu-id="1e56f-108">これにより、エイリアスを使用した名前空間ではなく、グローバル名前空間で検索が実行されます。</span><span class="sxs-lookup"><span data-stu-id="1e56f-108">This invokes a lookup in the global namespace, rather than an aliased namespace.</span></span>  
  
## <a name="for-more-information"></a><span data-ttu-id="1e56f-109">参照項目</span><span class="sxs-lookup"><span data-stu-id="1e56f-109">For More Information</span></span>  
 <span data-ttu-id="1e56f-110">`::` 演算子の使用例については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e56f-110">For an example of how to use the `::` operator, see the following section:</span></span>  
  
-   [<span data-ttu-id="1e56f-111">方法: グローバル名前空間エイリアスを使用する</span><span class="sxs-lookup"><span data-stu-id="1e56f-111">How to: Use the Global Namespace Alias</span></span>](../../../csharp/programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="1e56f-112">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="1e56f-112">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="1e56f-113">参照</span><span class="sxs-lookup"><span data-stu-id="1e56f-113">See Also</span></span>

- [<span data-ttu-id="1e56f-114">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="1e56f-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="1e56f-115">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="1e56f-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="1e56f-116">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="1e56f-116">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="1e56f-117">名前空間キーワード</span><span class="sxs-lookup"><span data-stu-id="1e56f-117">Namespace Keywords</span></span>](../../../csharp/language-reference/keywords/namespace-keywords.md)  
- [<span data-ttu-id="1e56f-118">。演算子</span><span class="sxs-lookup"><span data-stu-id="1e56f-118">. Operator</span></span>](../../../csharp/language-reference/operators/member-access-operator.md)  
- [<span data-ttu-id="1e56f-119">extern エイリアス</span><span class="sxs-lookup"><span data-stu-id="1e56f-119">extern alias</span></span>](../../../csharp/language-reference/keywords/extern-alias.md)
