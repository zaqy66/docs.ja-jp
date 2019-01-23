---
title: 型&#39; &lt;typename&gt; &#39;が定義されていません
ms.date: 07/20/2015
f1_keywords:
- vbc30002
- bc30002
helpviewer_keywords:
- BC30002
ms.assetid: b0faf204-57fd-44de-8c05-9db027eea663
ms.openlocfilehash: 8e303a9ac6529fbbc818c94497a16463897fb0c5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54496128"
---
# <a name="type-39lttypenamegt39-is-not-defined"></a><span data-ttu-id="b4a4e-102">型&#39; &lt;typename&gt; &#39;が定義されていません</span><span class="sxs-lookup"><span data-stu-id="b4a4e-102">Type &#39;&lt;typename&gt;&#39; is not defined</span></span>
<span data-ttu-id="b4a4e-103">ステートメントは定義されていない型への参照をされています。</span><span class="sxs-lookup"><span data-stu-id="b4a4e-103">The statement has made reference to a type that has not been defined.</span></span> <span data-ttu-id="b4a4e-104">などの宣言ステートメントで型を定義できる`Enum`、 `Structure`、 `Class`、または`Interface`します。</span><span class="sxs-lookup"><span data-stu-id="b4a4e-104">You can define a type in a declaration statement such as `Enum`, `Structure`, `Class`, or `Interface`.</span></span>  
  
 <span data-ttu-id="b4a4e-105">**エラー ID:** BC30002</span><span class="sxs-lookup"><span data-stu-id="b4a4e-105">**Error ID:** BC30002</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b4a4e-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="b4a4e-106">To correct this error</span></span>  
  
-   <span data-ttu-id="b4a4e-107">型の定義とその参照の両方で同じスペル チェックを使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b4a4e-107">Ensure that the type definition and its reference both use the same spelling.</span></span>  
  
-   <span data-ttu-id="b4a4e-108">型定義が参照にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b4a4e-108">Ensure that the type definition is accessible to the reference.</span></span> <span data-ttu-id="b4a4e-109">たとえば、種類別のモジュールし、は宣言されています`Private`、型定義を参照しているモジュールに移動または宣言`Public`します。</span><span class="sxs-lookup"><span data-stu-id="b4a4e-109">For example, if the type is in another module and has been declared `Private`, move the type definition to the referencing module or declare it `Public`.</span></span>  
  
-   <span data-ttu-id="b4a4e-110">型の名前空間がプロジェクト内で再定義されていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b4a4e-110">Ensure that the namespace of the type is not redefined within your project.</span></span> <span data-ttu-id="b4a4e-111">場合を使用して、`Global`完全型名を修飾するキーワード。</span><span class="sxs-lookup"><span data-stu-id="b4a4e-111">If it is, use the `Global` keyword to fully qualify the type name.</span></span> <span data-ttu-id="b4a4e-112">たとえば、プロジェクトに名前空間が定義されている場合`System`、<xref:System.Object?displayProperty=nameWithType>で完全修飾である場合を除き、型にアクセスできません、`Global`キーワード:`Global.System.Object`します。</span><span class="sxs-lookup"><span data-stu-id="b4a4e-112">For example, if a project defines a namespace named `System`, the <xref:System.Object?displayProperty=nameWithType> type cannot be accessed unless it is fully qualified with the `Global` keyword: `Global.System.Object`.</span></span>  
  
-   <span data-ttu-id="b4a4e-113">型が定義されている場合、オブジェクト ライブラリまたはタイプ ライブラリが定義されているが、Visual Basic、クリックに登録されていない場合**参照の追加**上、**プロジェクト**メニューのおよび適切なオブジェクトを選択ライブラリまたはタイプ ライブラリ。</span><span class="sxs-lookup"><span data-stu-id="b4a4e-113">If the type is defined, but the object library or type library in which it is defined is not registered in Visual Basic, click **Add Reference** on the **Project** menu, and then select the appropriate object library or type library.</span></span>  
  
-   <span data-ttu-id="b4a4e-114">型が対象となる .NET Framework プロファイルの一部であるアセンブリであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b4a4e-114">Ensure that the type is in an assembly that is part of the targeted .NET Framework profile.</span></span> <span data-ttu-id="b4a4e-115">詳細については、「[.NET Framework を対象とするエラーのトラブルシューティング](/visualstudio/msbuild/troubleshooting-dotnet-framework-targeting-errors)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4a4e-115">For more information, see [Troubleshooting .NET Framework Targeting Errors](/visualstudio/msbuild/troubleshooting-dotnet-framework-targeting-errors).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b4a4e-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4a4e-116">See also</span></span>
- [<span data-ttu-id="b4a4e-117">Visual Basic における名前空間</span><span class="sxs-lookup"><span data-stu-id="b4a4e-117">Namespaces in Visual Basic</span></span>](../../../visual-basic/programming-guide/program-structure/namespaces.md)
- [<span data-ttu-id="b4a4e-118">Enum ステートメント</span><span class="sxs-lookup"><span data-stu-id="b4a4e-118">Enum Statement</span></span>](../../../visual-basic/language-reference/statements/enum-statement.md)
- [<span data-ttu-id="b4a4e-119">Structure ステートメント</span><span class="sxs-lookup"><span data-stu-id="b4a4e-119">Structure Statement</span></span>](../../../visual-basic/language-reference/statements/structure-statement.md)
- [<span data-ttu-id="b4a4e-120">Class ステートメント</span><span class="sxs-lookup"><span data-stu-id="b4a4e-120">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)
- [<span data-ttu-id="b4a4e-121">Interface ステートメント</span><span class="sxs-lookup"><span data-stu-id="b4a4e-121">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)
- [<span data-ttu-id="b4a4e-122">プロジェクト内の参照の管理</span><span class="sxs-lookup"><span data-stu-id="b4a4e-122">Managing references in a project</span></span>](/visualstudio/ide/managing-references-in-a-project)
