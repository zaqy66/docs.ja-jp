---
title: typeof (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- typeof
- typeof_CSharpKeyword
helpviewer_keywords:
- typeof keyword [C#]
ms.assetid: 0c08d880-515e-46bb-8cd2-48b8dd62c08d
ms.openlocfilehash: 4203b597d7045a13ffed9e61ddbbde57e2113c23
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/24/2018
ms.locfileid: "42908031"
---
# <a name="typeof-c-reference"></a><span data-ttu-id="d5b2a-102">typeof (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="d5b2a-102">typeof (C# Reference)</span></span>
<span data-ttu-id="d5b2a-103">型の `System.Type` オブジェクトを取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d5b2a-103">Used to obtain the `System.Type` object for a type.</span></span> <span data-ttu-id="d5b2a-104">`typeof` 式は次の形式になります。</span><span class="sxs-lookup"><span data-stu-id="d5b2a-104">A `typeof` expression takes the following form:</span></span>  
  
```csharp  
System.Type type = typeof(int);  
```  
  
## <a name="remarks"></a><span data-ttu-id="d5b2a-105">コメント</span><span class="sxs-lookup"><span data-stu-id="d5b2a-105">Remarks</span></span>  
 <span data-ttu-id="d5b2a-106">式の実行時の型を取得する場合は、次の例のように、.NET Framework のメソッド <xref:System.Object.GetType%2A> を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d5b2a-106">To obtain the run-time type of an expression, you can use the .NET Framework method <xref:System.Object.GetType%2A>, as in the following example:</span></span>  
  
```csharp  
int i = 0;  
System.Type type = i.GetType();  
```  
  
 <span data-ttu-id="d5b2a-107">`typeof` 演算子はオーバーロードできません。</span><span class="sxs-lookup"><span data-stu-id="d5b2a-107">The `typeof` operator cannot be overloaded.</span></span>  
  
 <span data-ttu-id="d5b2a-108">`typeof` 演算子は、オープン ジェネリック型に対しても使用できます。</span><span class="sxs-lookup"><span data-stu-id="d5b2a-108">The `typeof` operator can also be used on open generic types.</span></span> <span data-ttu-id="d5b2a-109">複数の型パラメーターを持つ型には、適切な数のコンマを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5b2a-109">Types with more than one type parameter must have the appropriate number of commas in the specification.</span></span> <span data-ttu-id="d5b2a-110">次の例は、メソッドの戻り値の型がジェネリック <xref:System.Collections.Generic.IEnumerable%601> であるかどうかを確認する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d5b2a-110">The following example shows how to determine whether the return type of a method is a generic <xref:System.Collections.Generic.IEnumerable%601>.</span></span> <span data-ttu-id="d5b2a-111">ここでは、メソッドが MethodInfo 型のインスタンスであると仮定します。</span><span class="sxs-lookup"><span data-stu-id="d5b2a-111">Assume that method is an instance of a MethodInfo type:</span></span>  
  
```csharp  
string s = method.ReturnType.GetInterface  
    (typeof(System.Collections.Generic.IEnumerable<>).FullName);  
```  
  
## <a name="example"></a><span data-ttu-id="d5b2a-112">例</span><span class="sxs-lookup"><span data-stu-id="d5b2a-112">Example</span></span>  
 [!code-csharp[csrefKeywordsOperator#12](../../../csharp/language-reference/keywords/codesnippet/CSharp/typeof_1.cs)]  
  
## <a name="example"></a><span data-ttu-id="d5b2a-113">例</span><span class="sxs-lookup"><span data-stu-id="d5b2a-113">Example</span></span>  
 <span data-ttu-id="d5b2a-114">このサンプルでは、<xref:System.Object.GetType%2A> メソッドを使用して、数値計算結果の格納に使用される型を確認しています。</span><span class="sxs-lookup"><span data-stu-id="d5b2a-114">This sample uses the <xref:System.Object.GetType%2A> method to determine the type that is used to contain the result of a numeric calculation.</span></span> <span data-ttu-id="d5b2a-115">これは、結果の数のストレージ要件によって変わります。</span><span class="sxs-lookup"><span data-stu-id="d5b2a-115">This depends on the storage requirements of the resulting number.</span></span>  
  
 [!code-csharp[csrefKeywordsOperator#13](../../../csharp/language-reference/keywords/codesnippet/CSharp/typeof_2.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="d5b2a-116">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="d5b2a-116">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="d5b2a-117">参照</span><span class="sxs-lookup"><span data-stu-id="d5b2a-117">See Also</span></span>  
 <xref:System.Type?displayProperty=nameWithType>  
 [<span data-ttu-id="d5b2a-118">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="d5b2a-118">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="d5b2a-119">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="d5b2a-119">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="d5b2a-120">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="d5b2a-120">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="d5b2a-121">is</span><span class="sxs-lookup"><span data-stu-id="d5b2a-121">is</span></span>](../../../csharp/language-reference/keywords/is.md)  
 [<span data-ttu-id="d5b2a-122">演算子のキーワード</span><span class="sxs-lookup"><span data-stu-id="d5b2a-122">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)
