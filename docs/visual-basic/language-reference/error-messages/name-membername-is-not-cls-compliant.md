---
title: 名前&lt;membername&gt; CLS 準拠ではありません
ms.date: 07/20/2015
f1_keywords:
- bc40031
- vbc40031
helpviewer_keywords:
- BC40031
ms.assetid: e2b885dc-cbf9-49ff-bbbe-531657ea99f7
ms.openlocfilehash: b950be530eb80fd1c65b48e1625eb344c642d260
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54626369"
---
# <a name="name-ltmembernamegt-is-not-cls-compliant"></a><span data-ttu-id="f6ddd-102">名前&lt;membername&gt; CLS 準拠ではありません</span><span class="sxs-lookup"><span data-stu-id="f6ddd-102">Name &lt;membername&gt; is not CLS-compliant</span></span>
<span data-ttu-id="f6ddd-103">アセンブリをマーク`<CLSCompliant(True)>`アンダー スコアで始まる名前を持つメンバーを公開しますが、(`_`)。</span><span class="sxs-lookup"><span data-stu-id="f6ddd-103">An assembly is marked as `<CLSCompliant(True)>` but exposes a member with a name that begins with an underscore (`_`).</span></span>  
  
 <span data-ttu-id="f6ddd-104">プログラミング要素ですが準拠するため、1 つまたは複数アンダー スコアを含めることができます、 [Language Independence and Language-independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS) にする必要がありますされませんアンダー スコアで始まりです。</span><span class="sxs-lookup"><span data-stu-id="f6ddd-104">A programming element can contain one or more underscores, but to be compliant with the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS), it must not begin with an underscore.</span></span> <span data-ttu-id="f6ddd-105">「 [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6ddd-105">See [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>  
  
 <span data-ttu-id="f6ddd-106">プログラミング要素に <xref:System.CLSCompliantAttribute> を適用する場合は、属性の `isCompliant` パラメーターを `True` または `False` のどちらかに設定して、準拠または非準拠を示します。</span><span class="sxs-lookup"><span data-stu-id="f6ddd-106">When you apply the <xref:System.CLSCompliantAttribute> to a programming element, you set the attribute's `isCompliant` parameter to either `True` or `False` to indicate compliance or noncompliance.</span></span> <span data-ttu-id="f6ddd-107">このパラメーターには既定値がありません。値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6ddd-107">There is no default for this parameter, and you must supply a value.</span></span>  
  
 <span data-ttu-id="f6ddd-108">要素に <xref:System.CLSCompliantAttribute> を適用しないと、その要素は非準拠と見なされます。</span><span class="sxs-lookup"><span data-stu-id="f6ddd-108">If you do not apply the <xref:System.CLSCompliantAttribute> to an element, it is considered to be noncompliant.</span></span>  
  
 <span data-ttu-id="f6ddd-109">既定では、このメッセージは警告です。</span><span class="sxs-lookup"><span data-stu-id="f6ddd-109">By default, this message is a warning.</span></span> <span data-ttu-id="f6ddd-110">警告を非表示にする方法や、警告をエラーとして扱う方法の詳細については、「 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f6ddd-110">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="f6ddd-111">**エラー ID:** BC40031</span><span class="sxs-lookup"><span data-stu-id="f6ddd-111">**Error ID:** BC40031</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f6ddd-112">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="f6ddd-112">To correct this error</span></span>  
  
-   <span data-ttu-id="f6ddd-113">ソース コード制御を使用する場合は、メンバー名を変更してから、アンダー スコアで始まらないようにします。</span><span class="sxs-lookup"><span data-stu-id="f6ddd-113">If you have control over the source code, change the member name so that it does not begin with an underscore.</span></span>  
  
-   <span data-ttu-id="f6ddd-114">メンバー名が変わらない場合は、削除、<xref:System.CLSCompliantAttribute>その定義からとしてマークまたは`<CLSCompliant(False)>`します。</span><span class="sxs-lookup"><span data-stu-id="f6ddd-114">If you require that the member name remain unchanged, remove the <xref:System.CLSCompliantAttribute> from its definition or mark it as `<CLSCompliant(False)>`.</span></span> <span data-ttu-id="f6ddd-115">アセンブリをマークすることも`<CLSCompliant(True)>`します。</span><span class="sxs-lookup"><span data-stu-id="f6ddd-115">You can still mark the assembly as `<CLSCompliant(True)>`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6ddd-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6ddd-116">See also</span></span>
- [<span data-ttu-id="f6ddd-117">Declared Element Names</span><span class="sxs-lookup"><span data-stu-id="f6ddd-117">Declared Element Names</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [<span data-ttu-id="f6ddd-118">Visual Basic の名前付け規則</span><span class="sxs-lookup"><span data-stu-id="f6ddd-118">Visual Basic Naming Conventions</span></span>](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)

