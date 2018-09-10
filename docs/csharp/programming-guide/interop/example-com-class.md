---
title: COM クラスの例 (C# プログラミング ガイド)
ms.date: 07/20/2015
helpviewer_keywords:
- examples [C#], COM classes
- COM, exposing Visual C# objects to
ms.assetid: 6504dea9-ad1c-4993-a794-830fec5270af
ms.openlocfilehash: a77f022b4cf7659d506a7893923ce47270cb8c1b
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44214993"
---
# <a name="example-com-class-c-programming-guide"></a><span data-ttu-id="5eb0c-102">COM クラスの例 (C# プログラミング ガイド)</span><span class="sxs-lookup"><span data-stu-id="5eb0c-102">Example COM Class (C# Programming Guide)</span></span>
<span data-ttu-id="5eb0c-103">ここでは、COM オブジェクトとして公開されるクラスの例を紹介します。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-103">The following is an example of a class that you would expose as a COM object.</span></span> <span data-ttu-id="5eb0c-104">このコードを .cs ファイルに保存して、プロジェクトに追加したあと、**[COM の相互運用機能に登録]** プロパティを **[True]** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-104">After this code has been placed in a .cs file and added to your project, set the **Register for COM Interop** property to **True**.</span></span> <span data-ttu-id="5eb0c-105">詳細については、「[方法: コンポーネントを COM 相互運用機能に登録する](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w29wacsy(v=vs.100))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-105">For more information, see [How to: Register a Component for COM Interop](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w29wacsy(v=vs.100)).</span></span>
  
 <span data-ttu-id="5eb0c-106">Visual C# オブジェクトを COM に公開するには、クラス インターフェイス、イベント インターフェイス (必要な場合)、クラス自体を宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-106">Exposing Visual C# objects to COM requires declaring a class interface, an events interface if it is required, and the class itself.</span></span> <span data-ttu-id="5eb0c-107">クラスのメンバーを COM で参照するには、次の規則に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-107">Class members must follow these rules to be visible to COM:</span></span>  
  
-   <span data-ttu-id="5eb0c-108">クラスはパブリックであること。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-108">The class must be public.</span></span>  
  
-   <span data-ttu-id="5eb0c-109">プロパティ、メソッド、およびイベントがパブリックであること。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-109">Properties, methods, and events must be public.</span></span>  
  
-   <span data-ttu-id="5eb0c-110">プロパティとメソッドがクラス インターフェイスで宣言されていること。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-110">Properties and methods must be declared on the class interface.</span></span>  
  
-   <span data-ttu-id="5eb0c-111">イベントがイベント インターフェイスで宣言されていること。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-111">Events must be declared in the event interface.</span></span>  
  
 <span data-ttu-id="5eb0c-112">これらのインターフェイスで宣言されていない、クラス内の他のパブリック メンバーは、COM から参照されませんが、他の .NET Framework オブジェクトからは参照されます。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-112">Other public members in the class that are not declared in these interfaces will not be visible to COM, but they will be visible to other .NET Framework objects.</span></span>  
  
 <span data-ttu-id="5eb0c-113">プロパティとメソッドを COM に公開するには、それらをクラス インターフェイスで宣言し、`DispId` 属性でマークを付けて、クラスに実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-113">To expose properties and methods to COM, you must declare them on the class interface and mark them with a `DispId` attribute, and implement them in the class.</span></span> <span data-ttu-id="5eb0c-114">メンバーをインターフェイスで宣言する順序は、COM vtable で使用される順序になります。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-114">The order in which the members are declared in the interface is the order used for the COM vtable.</span></span>  
  
 <span data-ttu-id="5eb0c-115">クラスのイベントを公開するには、それらをイベント インターフェイスで宣言し、`DispId` 属性でマークを付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-115">To expose events from your class, you must declare them on the events interface and mark them with a `DispId` attribute.</span></span> <span data-ttu-id="5eb0c-116">クラスでこのインターフェイスを実装しないでください。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-116">The class should not implement this interface.</span></span>  
  
 <span data-ttu-id="5eb0c-117">クラスでは、クラス インターフェイスが実装されます。複数のインターフェイスを実装できますが、最初に実装されるのは、既定のクラス インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-117">The class implements the class interface; it can implement more than one interface, but the first implementation will be the default class interface.</span></span> <span data-ttu-id="5eb0c-118">ここで、COM に対して公開するプロパティとメソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-118">Implement the methods and properties exposed to COM here.</span></span> <span data-ttu-id="5eb0c-119">プロパティとメソッドは、パブリックとしてマークされており、クラス インターフェイスの宣言と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-119">They must be marked public and must match the declarations in the class interface.</span></span> <span data-ttu-id="5eb0c-120">また、ここでクラスから発生するイベントを宣言します。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-120">Also, declare the events raised by the class here.</span></span> <span data-ttu-id="5eb0c-121">イベントは、パブリックとしてマークされており、イベント インターフェイスの宣言と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5eb0c-121">They must be marked public and must match the declarations in the events interface.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5eb0c-122">例</span><span class="sxs-lookup"><span data-stu-id="5eb0c-122">Example</span></span>  
 [!code-csharp[csProgGuideInterop#8](../../../csharp/programming-guide/interop/codesnippet/CSharp/example-com-class_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="5eb0c-123">参照</span><span class="sxs-lookup"><span data-stu-id="5eb0c-123">See Also</span></span>

- [<span data-ttu-id="5eb0c-124">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="5eb0c-124">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="5eb0c-125">相互運用性</span><span class="sxs-lookup"><span data-stu-id="5eb0c-125">Interoperability</span></span>](../../../csharp/programming-guide/interop/index.md)  
- <span data-ttu-id="5eb0c-126">[[ビルド] ページ (プロジェクト デザイナー) (C#)](/visualstudio/ide/reference/build-page-project-designer-csharp)</span><span class="sxs-lookup"><span data-stu-id="5eb0c-126">[Build Page, Project Designer (C#)](/visualstudio/ide/reference/build-page-project-designer-csharp)</span></span>
