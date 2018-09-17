---
title: C# プログラムの一般構造 (C# プログラミング ガイド)
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, program structure
ms.assetid: 5ae964a5-0ef0-40fe-88fb-6d1793371d0d
ms.openlocfilehash: d3920fff26eccdd509c72143ff8553fb0c501bbc
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2018
ms.locfileid: "45698157"
---
# <a name="general-structure-of-a-c-program-c-programming-guide"></a><span data-ttu-id="36a08-102">C# プログラムの一般構造 (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="36a08-102">General Structure of a C# Program (C# Programming Guide)</span></span>
<span data-ttu-id="36a08-103">C# プログラムは、1 つ以上のファイルで構成できます。</span><span class="sxs-lookup"><span data-stu-id="36a08-103">C# programs can consist of one or more files.</span></span> <span data-ttu-id="36a08-104">各ファイルには、0 個以上の名前空間を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="36a08-104">Each file can contain zero or more namespaces.</span></span> <span data-ttu-id="36a08-105">名前空間には、その他の名前空間以外に、クラス、構造体、インターフェイス、列挙型、デリゲートなどの型を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="36a08-105">A namespace can contain types such as classes, structs, interfaces, enumerations, and delegates, in addition to other namespaces.</span></span> <span data-ttu-id="36a08-106">次に示すのは、これら要素をすべて含む C# プログラムのスケルトンです。</span><span class="sxs-lookup"><span data-stu-id="36a08-106">The following is the skeleton of a C# program that contains all of these elements.</span></span>  
  
 [!code-csharp[csProgGuide#34](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/general-structure-of-a-csharp-program_1.cs)]  
  
## <a name="related-sections"></a><span data-ttu-id="36a08-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="36a08-107">Related Sections</span></span>  
 <span data-ttu-id="36a08-108">詳細情報</span><span class="sxs-lookup"><span data-stu-id="36a08-108">For more information:</span></span>  
  
-   [<span data-ttu-id="36a08-109">クラス</span><span class="sxs-lookup"><span data-stu-id="36a08-109">Classes</span></span>](../../../csharp/programming-guide/classes-and-structs/classes.md)  
  
-   [<span data-ttu-id="36a08-110">構造体</span><span class="sxs-lookup"><span data-stu-id="36a08-110">Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/structs.md)  
  
-   [<span data-ttu-id="36a08-111">名前空間</span><span class="sxs-lookup"><span data-stu-id="36a08-111">Namespaces</span></span>](../../../csharp/programming-guide/namespaces/index.md)  
  
-   [<span data-ttu-id="36a08-112">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="36a08-112">Interfaces</span></span>](../../../csharp/programming-guide/interfaces/index.md)  
  
-   [<span data-ttu-id="36a08-113">デリゲート</span><span class="sxs-lookup"><span data-stu-id="36a08-113">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="36a08-114">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="36a08-114">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="36a08-115">参照</span><span class="sxs-lookup"><span data-stu-id="36a08-115">See Also</span></span>

- [<span data-ttu-id="36a08-116">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="36a08-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="36a08-117">インサイド C# プログラム</span><span class="sxs-lookup"><span data-stu-id="36a08-117">Inside a C# Program</span></span>](../../../csharp/programming-guide/inside-a-program/index.md)  
- [<span data-ttu-id="36a08-118">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="36a08-118">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="36a08-119">\<paveover>C# サンプル アプリケーション</span><span class="sxs-lookup"><span data-stu-id="36a08-119">\<paveover>C# Sample Applications</span></span>](https://msdn.microsoft.com/library/9a9d7aaa-51d3-4224-b564-95409b0f3e15)
