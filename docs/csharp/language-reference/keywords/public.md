---
title: public (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- public
- public_CSharpKeyword
helpviewer_keywords:
- public keyword [C#]
ms.assetid: 0ae45d16-a551-4b74-9845-57208de1328e
ms.openlocfilehash: 853f9c9ebe36345a897337d4e793d3c88059e068
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/27/2018
ms.locfileid: "42998728"
---
# <a name="public-c-reference"></a><span data-ttu-id="17450-102">public (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="17450-102">public (C# Reference)</span></span>
<span data-ttu-id="17450-103">`public` キーワードは、型と型のメンバーを示すアクセス修飾子です。</span><span class="sxs-lookup"><span data-stu-id="17450-103">The `public` keyword is an access modifier for types and type members.</span></span> <span data-ttu-id="17450-104">パブリック アクセスは、最も制限の少ないアクセス レベルです。</span><span class="sxs-lookup"><span data-stu-id="17450-104">Public access is the most permissive access level.</span></span> <span data-ttu-id="17450-105">次の例のように、パブリック メンバーへのアクセスには制限がありません。</span><span class="sxs-lookup"><span data-stu-id="17450-105">There are no restrictions on accessing public members, as in this example:</span></span>  
  
```csharp  
class SampleClass  
{  
    public int x; // No access restrictions.  
}  
```  
  
 <span data-ttu-id="17450-106">詳しくは、「[アクセス修飾子](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)」および「[アクセシビリティ レベル](../../../csharp/language-reference/keywords/accessibility-levels.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="17450-106">See [Access Modifiers](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md) and [Accessibility Levels](../../../csharp/language-reference/keywords/accessibility-levels.md) for more information.</span></span>  
  
## <a name="example"></a><span data-ttu-id="17450-107">例</span><span class="sxs-lookup"><span data-stu-id="17450-107">Example</span></span>  
 <span data-ttu-id="17450-108">次の例では、2 つのクラス (`PointTest` と `MainClass`) が宣言されています。</span><span class="sxs-lookup"><span data-stu-id="17450-108">In the following example, two classes are declared, `PointTest` and `MainClass`.</span></span> <span data-ttu-id="17450-109">`PointTest` のパブリック メンバー `x` および `y` は、`MainClass` から直接アクセスされます。</span><span class="sxs-lookup"><span data-stu-id="17450-109">The public members `x` and `y` of `PointTest` are accessed directly from `MainClass`.</span></span>  
  
 [!code-csharp[csrefKeywordsModifiers#13](../../../csharp/language-reference/keywords/codesnippet/CSharp/public_1.cs)]  
  
 <span data-ttu-id="17450-110">`public` アクセス レベルを [private](../../../csharp/language-reference/keywords/private.md) または [protected](../../../csharp/language-reference/keywords/protected.md) に変更すると、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="17450-110">If you change the `public` access level to [private](../../../csharp/language-reference/keywords/private.md) or [protected](../../../csharp/language-reference/keywords/protected.md), you will get the error message:</span></span>  
  
 <span data-ttu-id="17450-111">'PointTest.y' はアクセスできない保護レベルになっています。</span><span class="sxs-lookup"><span data-stu-id="17450-111">'PointTest.y' is inaccessible due to its protection level.</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="17450-112">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="17450-112">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="17450-113">参照</span><span class="sxs-lookup"><span data-stu-id="17450-113">See Also</span></span>

- [<span data-ttu-id="17450-114">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="17450-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="17450-115">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="17450-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="17450-116">アクセス修飾子</span><span class="sxs-lookup"><span data-stu-id="17450-116">Access Modifiers</span></span>](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)  
- [<span data-ttu-id="17450-117">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="17450-117">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="17450-118">アクセス修飾子</span><span class="sxs-lookup"><span data-stu-id="17450-118">Access Modifiers</span></span>](../../../csharp/language-reference/keywords/access-modifiers.md)  
- [<span data-ttu-id="17450-119">アクセシビリティ レベル</span><span class="sxs-lookup"><span data-stu-id="17450-119">Accessibility Levels</span></span>](../../../csharp/language-reference/keywords/accessibility-levels.md)  
- [<span data-ttu-id="17450-120">修飾子</span><span class="sxs-lookup"><span data-stu-id="17450-120">Modifiers</span></span>](../../../csharp/language-reference/keywords/modifiers.md)  
- [<span data-ttu-id="17450-121">private</span><span class="sxs-lookup"><span data-stu-id="17450-121">private</span></span>](../../../csharp/language-reference/keywords/private.md)  
- [<span data-ttu-id="17450-122">protected</span><span class="sxs-lookup"><span data-stu-id="17450-122">protected</span></span>](../../../csharp/language-reference/keywords/protected.md)  
- [<span data-ttu-id="17450-123">internal</span><span class="sxs-lookup"><span data-stu-id="17450-123">internal</span></span>](../../../csharp/language-reference/keywords/internal.md)
