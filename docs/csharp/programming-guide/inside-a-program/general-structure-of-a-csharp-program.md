---
title: C# プログラムの一般構造 (C# プログラミング ガイド)
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, program structure
ms.assetid: 5ae964a5-0ef0-40fe-88fb-6d1793371d0d
ms.openlocfilehash: 3e2718d932506f261ea32e7289a3191bca7c22e8
ms.sourcegitcommit: 3b1cb8467bd73dee854b604e306c0e7e3882d91a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "45698157"
---
# <a name="general-structure-of-a-c-program-c-programming-guide"></a><span data-ttu-id="a2362-102">C# プログラムの一般構造 (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="a2362-102">General Structure of a C# Program (C# Programming Guide)</span></span>
<span data-ttu-id="a2362-103">C# プログラムは、1 つ以上のファイルで構成できます。</span><span class="sxs-lookup"><span data-stu-id="a2362-103">C# programs can consist of one or more files.</span></span> <span data-ttu-id="a2362-104">各ファイルには、0 個以上の名前空間を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a2362-104">Each file can contain zero or more namespaces.</span></span> <span data-ttu-id="a2362-105">名前空間には、その他の名前空間以外に、クラス、構造体、インターフェイス、列挙型、デリゲートなどの型を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a2362-105">A namespace can contain types such as classes, structs, interfaces, enumerations, and delegates, in addition to other namespaces.</span></span> <span data-ttu-id="a2362-106">次に示すのは、これら要素をすべて含む C# プログラムのスケルトンです。</span><span class="sxs-lookup"><span data-stu-id="a2362-106">The following is the skeleton of a C# program that contains all of these elements.</span></span>  
  
 [!code-csharp[csProgGuide#34](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/general-structure-of-a-csharp-program_1.cs)]  
  
## <a name="related-sections"></a><span data-ttu-id="a2362-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="a2362-107">Related Sections</span></span>  
 <span data-ttu-id="a2362-108">詳細情報</span><span class="sxs-lookup"><span data-stu-id="a2362-108">For more information:</span></span>  
  
-   [<span data-ttu-id="a2362-109">クラス</span><span class="sxs-lookup"><span data-stu-id="a2362-109">Classes</span></span>](../../../csharp/programming-guide/classes-and-structs/classes.md)  
  
-   [<span data-ttu-id="a2362-110">構造体</span><span class="sxs-lookup"><span data-stu-id="a2362-110">Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/structs.md)  
  
-   [<span data-ttu-id="a2362-111">名前空間</span><span class="sxs-lookup"><span data-stu-id="a2362-111">Namespaces</span></span>](../../../csharp/programming-guide/namespaces/index.md)  
  
-   [<span data-ttu-id="a2362-112">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2362-112">Interfaces</span></span>](../../../csharp/programming-guide/interfaces/index.md)  
  
-   [<span data-ttu-id="a2362-113">デリゲート</span><span class="sxs-lookup"><span data-stu-id="a2362-113">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="a2362-114">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="a2362-114">C# Language Specification</span></span>  

<span data-ttu-id="a2362-115">詳細については、「[C# 言語の仕様](../../language-reference/language-specification/index.md)」の「[基本概念](~/_csharplang/spec/basic-concepts.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2362-115">For more information, see [Basic concepts](~/_csharplang/spec/basic-concepts.md) in the [C# Language Specification](../../language-reference/language-specification/index.md).</span></span> <span data-ttu-id="a2362-116">言語仕様は、C# の構文と使用法に関する信頼性のある情報源です。</span><span class="sxs-lookup"><span data-stu-id="a2362-116">The language specification is the definitive source for C# syntax and usage.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a2362-117">参照</span><span class="sxs-lookup"><span data-stu-id="a2362-117">See Also</span></span>

- [<span data-ttu-id="a2362-118">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="a2362-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="a2362-119">インサイド C# プログラム</span><span class="sxs-lookup"><span data-stu-id="a2362-119">Inside a C# Program</span></span>](../../../csharp/programming-guide/inside-a-program/index.md)  
- [<span data-ttu-id="a2362-120">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="a2362-120">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="a2362-121">C# サンプル アプリケーション</span><span class="sxs-lookup"><span data-stu-id="a2362-121">C# Sample Applications</span></span>](https://msdn.microsoft.com/library/9a9d7aaa-51d3-4224-b564-95409b0f3e15)
