---
title: コレクション初期化子を使用してディクショナリを初期化する方法 - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- collection initializers [C#], with Dictionary
ms.assetid: 25283922-f8ee-40dc-a639-fac30804ec71
ms.openlocfilehash: 42deee85b3a425531ddadfa96cfaff6d342d1221
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243882"
---
# <a name="how-to-initialize-a-dictionary-with-a-collection-initializer-c-programming-guide"></a><span data-ttu-id="dbfdf-102">コレクション初期化子を使用してディクショナリを初期化する方法 (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="dbfdf-102">How to initialize a dictionary with a collection initializer (C# Programming Guide)</span></span>

<span data-ttu-id="dbfdf-103"><xref:System.Collections.Generic.Dictionary%602> にはキーと値のペアのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="dbfdf-103">A <xref:System.Collections.Generic.Dictionary%602> contains a collection of key/value pairs.</span></span> <span data-ttu-id="dbfdf-104">その <xref:System.Collections.Generic.Dictionary%602.Add*> メソッドは、それぞれキーと値に対する 2 つのパラメーターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="dbfdf-104">Its <xref:System.Collections.Generic.Dictionary%602.Add*> method takes two parameters, one for the key and one for the value.</span></span> <span data-ttu-id="dbfdf-105">`Add` メソッドが複数のパラメーターを受け取る <xref:System.Collections.Generic.Dictionary%602> またはコレクションを初期化するには、次の例に示すように、各パラメーターのセットを中かっこで囲みます。</span><span class="sxs-lookup"><span data-stu-id="dbfdf-105">To initialize a <xref:System.Collections.Generic.Dictionary%602>, or any collection whose `Add` method takes multiple parameters, enclose each set of parameters in braces as shown in the following example.</span></span>

## <a name="example"></a><span data-ttu-id="dbfdf-106">例</span><span class="sxs-lookup"><span data-stu-id="dbfdf-106">Example</span></span>

<span data-ttu-id="dbfdf-107">次のコード例では、<xref:System.Collections.Generic.Dictionary%602> が型 `StudentName` のインスタンスで初期化されています。</span><span class="sxs-lookup"><span data-stu-id="dbfdf-107">In the following code example, a <xref:System.Collections.Generic.Dictionary%602> is initialized with instances of type `StudentName`.</span></span>  
  
[!code-csharp[csProgGuideLINQ#34](../../../csharp/programming-guide/arrays/codesnippet/CSharp/how-to-initialize-a-dictionary-with-a-collection-initializer_1.cs)]

<span data-ttu-id="dbfdf-108">コレクションの各要素の中かっこの 2 つのペアに注目してください。</span><span class="sxs-lookup"><span data-stu-id="dbfdf-108">Note the two pairs of braces in each element of the collection.</span></span> <span data-ttu-id="dbfdf-109">最も内側の中かっこは `StudentName` のオブジェクト初期化子を囲み、最も外側の中かっこは、`students` <xref:System.Collections.Generic.Dictionary%602> に追加されるキーと値のペアの初期化子を囲んでいます。</span><span class="sxs-lookup"><span data-stu-id="dbfdf-109">The innermost braces enclose the object initializer for the `StudentName`, and the outermost braces enclose the initializer for the key/value pair that will be added to the `students` <xref:System.Collections.Generic.Dictionary%602>.</span></span> <span data-ttu-id="dbfdf-110">最後に、ディクショナリのコレクション初期化子全体が中かっこで囲まれています。</span><span class="sxs-lookup"><span data-stu-id="dbfdf-110">Finally, the whole collection initializer for the dictionary is enclosed in braces.</span></span>

## <a name="compiling-the-code"></a><span data-ttu-id="dbfdf-111">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="dbfdf-111">Compiling the code</span></span>

<span data-ttu-id="dbfdf-112">このコードを実行するには、クラスをコピーし、Visual Studio で作成した Visual C# コンソール アプリケーション プロジェクトに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="dbfdf-112">To run this code, copy and paste the class into a Visual C# console application project that has been created in Visual Studio.</span></span> <span data-ttu-id="dbfdf-113">既定では、このプロジェクトは、[!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] のバージョン 3.5 を対象としており、System.Core.dll への参照と System.Linq の using ディレクティブが含まれます。</span><span class="sxs-lookup"><span data-stu-id="dbfdf-113">By default, this project targets version 3.5 of the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)], and it has a reference to System.Core.dll and a using directive for System.Linq.</span></span> <span data-ttu-id="dbfdf-114">これらの要件のうち 1 つまたは複数を満たしていないプロジェクトの場合は、手動で追加することができます。</span><span class="sxs-lookup"><span data-stu-id="dbfdf-114">If one or more of these requirements are missing from the project, you can add them manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="dbfdf-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="dbfdf-115">See also</span></span>

- [<span data-ttu-id="dbfdf-116">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="dbfdf-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="dbfdf-117">オブジェクト初期化子とコレクション初期化子</span><span class="sxs-lookup"><span data-stu-id="dbfdf-117">Object and Collection Initializers</span></span>](../../../csharp/programming-guide/classes-and-structs/object-and-collection-initializers.md)
