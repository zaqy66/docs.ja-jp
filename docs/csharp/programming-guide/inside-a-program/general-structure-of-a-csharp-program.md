---
title: C# プログラムの一般構造 - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, program structure
ms.assetid: 5ae964a5-0ef0-40fe-88fb-6d1793371d0d
ms.openlocfilehash: a9e20d0020b82973fb95e422c30f87421adedd5c
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236896"
---
# <a name="general-structure-of-a-c-program-c-programming-guide"></a><span data-ttu-id="29d72-102">C# プログラムの一般構造 (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="29d72-102">General Structure of a C# Program (C# Programming Guide)</span></span>
<span data-ttu-id="29d72-103">C# プログラムは、1 つ以上のファイルで構成できます。</span><span class="sxs-lookup"><span data-stu-id="29d72-103">C# programs can consist of one or more files.</span></span> <span data-ttu-id="29d72-104">各ファイルには、0 個以上の名前空間を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="29d72-104">Each file can contain zero or more namespaces.</span></span> <span data-ttu-id="29d72-105">名前空間には、その他の名前空間以外に、クラス、構造体、インターフェイス、列挙型、デリゲートなどの型を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="29d72-105">A namespace can contain types such as classes, structs, interfaces, enumerations, and delegates, in addition to other namespaces.</span></span> <span data-ttu-id="29d72-106">次に示すのは、これら要素をすべて含む C# プログラムのスケルトンです。</span><span class="sxs-lookup"><span data-stu-id="29d72-106">The following is the skeleton of a C# program that contains all of these elements.</span></span>  
  
 [!code-csharp[csProgGuide#34](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/general-structure-of-a-csharp-program_1.cs)]  
  
## <a name="related-sections"></a><span data-ttu-id="29d72-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="29d72-107">Related Sections</span></span>  
 <span data-ttu-id="29d72-108">詳細情報</span><span class="sxs-lookup"><span data-stu-id="29d72-108">For more information:</span></span>  
  
-   [<span data-ttu-id="29d72-109">クラス</span><span class="sxs-lookup"><span data-stu-id="29d72-109">Classes</span></span>](../../../csharp/programming-guide/classes-and-structs/classes.md)  
  
-   [<span data-ttu-id="29d72-110">構造体</span><span class="sxs-lookup"><span data-stu-id="29d72-110">Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/structs.md)  
  
-   [<span data-ttu-id="29d72-111">名前空間</span><span class="sxs-lookup"><span data-stu-id="29d72-111">Namespaces</span></span>](../../../csharp/programming-guide/namespaces/index.md)  
  
-   [<span data-ttu-id="29d72-112">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="29d72-112">Interfaces</span></span>](../../../csharp/programming-guide/interfaces/index.md)  
  
-   [<span data-ttu-id="29d72-113">デリゲート</span><span class="sxs-lookup"><span data-stu-id="29d72-113">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="29d72-114">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="29d72-114">C# Language Specification</span></span>  

<span data-ttu-id="29d72-115">詳細については、「[C# 言語の仕様](../../language-reference/language-specification/index.md)」の「[基本概念](~/_csharplang/spec/basic-concepts.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29d72-115">For more information, see [Basic concepts](~/_csharplang/spec/basic-concepts.md) in the [C# Language Specification](../../language-reference/language-specification/index.md).</span></span> <span data-ttu-id="29d72-116">言語仕様は、C# の構文と使用法に関する信頼性のある情報源です。</span><span class="sxs-lookup"><span data-stu-id="29d72-116">The language specification is the definitive source for C# syntax and usage.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29d72-117">参照</span><span class="sxs-lookup"><span data-stu-id="29d72-117">See Also</span></span>

- [<span data-ttu-id="29d72-118">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="29d72-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="29d72-119">インサイド C# プログラム</span><span class="sxs-lookup"><span data-stu-id="29d72-119">Inside a C# Program</span></span>](../../../csharp/programming-guide/inside-a-program/index.md)  
- [<span data-ttu-id="29d72-120">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="29d72-120">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="29d72-121">C# サンプル アプリケーション</span><span class="sxs-lookup"><span data-stu-id="29d72-121">C# Sample Applications</span></span>](https://msdn.microsoft.com/library/9a9d7aaa-51d3-4224-b564-95409b0f3e15)
