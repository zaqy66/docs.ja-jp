---
title: 参照と Imports ステートメント (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- assemblies [Visual Basic], namespaces
- references [Visual Basic], assembly
- namespaces [Visual Basic], assemblies
- referencing assemblies
- Imports statement [Visual Basic], referencing assemblies
- assemblies [Visual Basic], references
ms.assetid: 38149bd4-0a6f-4b31-b5f8-94a8c33f1600
ms.openlocfilehash: bd08940ac04d0218f3d3936514a72c12449b34ff
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505563"
---
# <a name="references-and-the-imports-statement-visual-basic"></a><span data-ttu-id="a1735-102">参照と Imports ステートメント (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a1735-102">References and the Imports Statement (Visual Basic)</span></span>
<span data-ttu-id="a1735-103">利用できる外部オブジェクト プロジェクトを選択して、**参照の追加**コマンドを**プロジェクト**メニュー。</span><span class="sxs-lookup"><span data-stu-id="a1735-103">You can make external objects available to your project by choosing the **Add Reference** command on the **Project** menu.</span></span> <span data-ttu-id="a1735-104">Visual Basic での参照は、タイプ ライブラリの詳細に説明と似ていますが、アセンブリを指定できます。</span><span class="sxs-lookup"><span data-stu-id="a1735-104">References in Visual Basic can point to assemblies, which are like type libraries but contain more information.</span></span>  
  
## <a name="the-imports-statement"></a><span data-ttu-id="a1735-105">Imports ステートメント</span><span class="sxs-lookup"><span data-stu-id="a1735-105">The Imports Statement</span></span>  
 <span data-ttu-id="a1735-106">アセンブリには、1 つまたは複数の名前空間が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a1735-106">Assemblies include one or more namespaces.</span></span> <span data-ttu-id="a1735-107">アセンブリへの参照を追加するときに追加することも、`Imports`ステートメント、モジュール内でそのアセンブリの名前空間の表示を制御するモジュールにします。</span><span class="sxs-lookup"><span data-stu-id="a1735-107">When you add a reference to an assembly, you can also add an `Imports` statement to a module that controls the visibility of that assembly's namespaces within the module.</span></span> <span data-ttu-id="a1735-108">`Imports`ステートメントでは、スコープのコンテキストの一意の参照を指定するために必要な名前空間の部分のみを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="a1735-108">The `Imports` statement provides a scoping context that lets you use only the portion of the namespace necessary to supply a unique reference.</span></span>  
  
 <span data-ttu-id="a1735-109">`Imports`ステートメントには、次の構文。</span><span class="sxs-lookup"><span data-stu-id="a1735-109">The `Imports` statement has the following syntax:</span></span>  
  
 <span data-ttu-id="a1735-110">`Imports` [`|``Aliasname` =] `Namespace`</span><span class="sxs-lookup"><span data-stu-id="a1735-110">`Imports` [`|``Aliasname` =] `Namespace`</span></span>  
  
 <span data-ttu-id="a1735-111">`Aliasname` インポートされた名前空間を参照するコード内で使用できる短い名前を参照します。</span><span class="sxs-lookup"><span data-stu-id="a1735-111">`Aliasname` refers to a short name you can use within code to refer to an imported namespace.</span></span> <span data-ttu-id="a1735-112">`Namespace` 名前空間のいずれかで使用可能なプロジェクト参照をプロジェクト内での定義、または以前を通じて`Imports`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="a1735-112">`Namespace` is a namespace available through either a project reference, through a definition within the project, or through a previous `Imports` statement.</span></span>  
  
 <span data-ttu-id="a1735-113">モジュールは、任意の数を含めることができます`Imports`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="a1735-113">A module may contain any number of `Imports` statements.</span></span> <span data-ttu-id="a1735-114">後に現れる必要があります`Option`ステートメント、存在する場合、その他のコードの前にします。</span><span class="sxs-lookup"><span data-stu-id="a1735-114">They must appear after any `Option` statements, if present, but before any other code.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a1735-115">プロジェクト参照とを混同しないでください、`Imports`ステートメントまたは`Declare`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="a1735-115">Do not confuse project references with the `Imports` statement or the `Declare` statement.</span></span> <span data-ttu-id="a1735-116">プロジェクト参照は、Visual Basic プロジェクトで使用できるアセンブリ内のオブジェクトなど、外部のオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="a1735-116">Project references make external objects, such as objects in assemblies, available to Visual Basic projects.</span></span> <span data-ttu-id="a1735-117">`Imports`ステートメントは、プロジェクト参照へのアクセスを簡略化が使用されますが、これらのオブジェクトへのアクセスを提供しません。</span><span class="sxs-lookup"><span data-stu-id="a1735-117">The `Imports` statement is used to simplify access to project references, but does not provide access to these objects.</span></span> <span data-ttu-id="a1735-118">`Declare`ダイナミック リンク ライブラリ (DLL) で外部プロシージャへの参照を宣言するステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="a1735-118">The `Declare` statement is used to declare a reference to an external procedure in a dynamic-link library (DLL).</span></span>  
  
## <a name="using-aliases-with-the-imports-statement"></a><span data-ttu-id="a1735-119">Imports ステートメントを使用してエイリアスを使用します。</span><span class="sxs-lookup"><span data-stu-id="a1735-119">Using Aliases with the Imports Statement</span></span>  
 <span data-ttu-id="a1735-120">`Imports`ステートメントやすくクラスのアクセス方法によって明示的に参照の完全修飾名を入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a1735-120">The `Imports` statement makes it easier to access methods of classes by eliminating the need to explicitly type the fully qualified names of references.</span></span> <span data-ttu-id="a1735-121">エイリアスを使用して、名前空間の 1 つの部分にわかりやすい名前を割り当てできます。</span><span class="sxs-lookup"><span data-stu-id="a1735-121">Aliases let you assign a friendlier name to just one part of a namespace.</span></span> <span data-ttu-id="a1735-122">などの一部は、複数の行に表示されるテキストの 1 つの原因となるシーケンスをフィード キャリッジ リターン/ライン、<xref:Microsoft.VisualBasic.ControlChars>でモジュール、<xref:Microsoft.VisualBasic?displayProperty=nameWithType>名前空間。</span><span class="sxs-lookup"><span data-stu-id="a1735-122">For example, the carriage return/line feed sequence that causes a single piece of text to be displayed on multiple lines is part of the <xref:Microsoft.VisualBasic.ControlChars> module in the <xref:Microsoft.VisualBasic?displayProperty=nameWithType> namespace.</span></span> <span data-ttu-id="a1735-123">エイリアスなしのプログラムでこの定数を使用するには、次のコードを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1735-123">To use this constant in a program without an alias, you would need to type the following code:</span></span>  
  
 [!code-vb[VbVbalrApplication#3](../../../visual-basic/programming-guide/program-structure/codesnippet/VisualBasic/references-and-the-imports-statement_1.vb)]  
  
 <span data-ttu-id="a1735-124">`Imports` ステートメントがすぐに次のいずれかの最初の行を必ず`Option`モジュール内のステートメント。</span><span class="sxs-lookup"><span data-stu-id="a1735-124">`Imports` statements must always be the first lines immediately following any `Option` statements in a module.</span></span> <span data-ttu-id="a1735-125">次のコード フラグメントをインポートしてエイリアスを割り当てる方法を示しています、<xref:Microsoft.VisualBasic.ControlChars?displayProperty=nameWithType>モジュール。</span><span class="sxs-lookup"><span data-stu-id="a1735-125">The following code fragment shows how to import and assign an alias to the <xref:Microsoft.VisualBasic.ControlChars?displayProperty=nameWithType> module:</span></span>  
  
 [!code-vb[VbVbalrApplication#4](../../../visual-basic/programming-guide/program-structure/codesnippet/VisualBasic/references-and-the-imports-statement_2.vb)]  
  
 <span data-ttu-id="a1735-126">この名前空間への今後の参照が大幅に短くできます。</span><span class="sxs-lookup"><span data-stu-id="a1735-126">Future references to this namespace can be considerably shorter:</span></span>  
  
 [!code-vb[VbVbalrApplication#5](../../../visual-basic/programming-guide/program-structure/codesnippet/VisualBasic/references-and-the-imports-statement_3.vb)]  
  
 <span data-ttu-id="a1735-127">場合、`Imports`ステートメントでは、エイリアス名を含まない、インポートされた名前空間内で定義されている要素を修飾なしのモジュールで使用できます。</span><span class="sxs-lookup"><span data-stu-id="a1735-127">If an `Imports` statement does not include an alias name, elements defined within the imported namespace can be used in the module without qualification.</span></span> <span data-ttu-id="a1735-128">エイリアス名が指定されている場合はでその名前空間内に含まれる名前の修飾子としてに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1735-128">If the alias name is specified, it must be used as a qualifier for names contained within that namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1735-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1735-129">See also</span></span>

- <xref:Microsoft.VisualBasic.ControlChars>
- <xref:Microsoft.VisualBasic>
- [<span data-ttu-id="a1735-130">Visual Basic における名前空間</span><span class="sxs-lookup"><span data-stu-id="a1735-130">Namespaces in Visual Basic</span></span>](../../../visual-basic/programming-guide/program-structure/namespaces.md)
- [<span data-ttu-id="a1735-131">アセンブリとグローバル アセンブリ キャッシュ</span><span class="sxs-lookup"><span data-stu-id="a1735-131">Assemblies and the Global Assembly Cache</span></span>](../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)
- [<span data-ttu-id="a1735-132">方法: コマンド ラインを使用してアセンブリを作成および使用する</span><span class="sxs-lookup"><span data-stu-id="a1735-132">How to: Create and Use Assemblies Using the Command Line</span></span>](../../../visual-basic/programming-guide/concepts/assemblies-gac/how-to-create-and-use-assemblies-using-the-command-line.md)
- [<span data-ttu-id="a1735-133">Imports ステートメント (.NET 名前空間および型)</span><span class="sxs-lookup"><span data-stu-id="a1735-133">Imports Statement (.NET Namespace and Type)</span></span>](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)
