---
title: 非 CLS 準拠&lt;membername&gt; CLS 準拠インターフェイスでは許可されません
ms.date: 07/20/2015
f1_keywords:
- bc40033
- vbc40033
helpviewer_keywords:
- BC40033
ms.assetid: 060c4b08-798e-40f1-94cf-c05c524f1b8a
ms.openlocfilehash: c837065d2d448fc2523cfbd18efac962445f8bf0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54627696"
---
# <a name="non-cls-compliant-ltmembernamegt-is-not-allowed-in-a-cls-compliant-interface"></a><span data-ttu-id="4a068-102">非 CLS 準拠&lt;membername&gt; CLS 準拠インターフェイスでは許可されません</span><span class="sxs-lookup"><span data-stu-id="4a068-102">Non-CLS-compliant &lt;membername&gt; is not allowed in a CLS-compliant interface</span></span>
<span data-ttu-id="4a068-103">プロパティ、プロシージャ、またはインターフェイスでイベントがマーク`<CLSCompliant(True)>`インターフェイス自体としてマークされている場合`<CLSCompliant(False)>`またはマークされていません。</span><span class="sxs-lookup"><span data-stu-id="4a068-103">A property, procedure, or event in an interface is marked as `<CLSCompliant(True)>` when the interface itself is marked as `<CLSCompliant(False)>` or is not marked.</span></span>  
  
 <span data-ttu-id="4a068-104">準拠するためのインターフェイスの[Language Independence and Language-independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS) にすべてのメンバーは、準拠である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a068-104">For an interface to be compliant with the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS), all its members must be compliant.</span></span>  
  
 <span data-ttu-id="4a068-105">プログラミング要素に <xref:System.CLSCompliantAttribute> を適用する場合は、属性の `isCompliant` パラメーターを `True` または `False` のどちらかに設定して、準拠または非準拠を示します。</span><span class="sxs-lookup"><span data-stu-id="4a068-105">When you apply the <xref:System.CLSCompliantAttribute> to a programming element, you set the attribute's `isCompliant` parameter to either `True` or `False` to indicate compliance or noncompliance.</span></span> <span data-ttu-id="4a068-106">このパラメーターには既定値がありません。値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a068-106">There is no default for this parameter, and you must supply a value.</span></span>  
  
 <span data-ttu-id="4a068-107">要素に <xref:System.CLSCompliantAttribute> を適用しないと、その要素は非準拠と見なされます。</span><span class="sxs-lookup"><span data-stu-id="4a068-107">If you do not apply the <xref:System.CLSCompliantAttribute> to an element, it is considered to be noncompliant.</span></span>  
  
 <span data-ttu-id="4a068-108">既定では、このメッセージは警告です。</span><span class="sxs-lookup"><span data-stu-id="4a068-108">By default, this message is a warning.</span></span> <span data-ttu-id="4a068-109">警告を非表示にする方法や、警告をエラーとして扱う方法の詳細については、「 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4a068-109">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="4a068-110">**エラー ID:** BC40033</span><span class="sxs-lookup"><span data-stu-id="4a068-110">**Error ID:** BC40033</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="4a068-111">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="4a068-111">To correct this error</span></span>  
  
-   <span data-ttu-id="4a068-112">CLS 準拠をする必要があり、インターフェイスのソース コードを制御、マーク、インターフェイスとして`<CLSCompliant(True)>`すべてのメンバーが準拠している場合。</span><span class="sxs-lookup"><span data-stu-id="4a068-112">If you require CLS compliance and have control over the interface source code, mark the interface as `<CLSCompliant(True)>` if all its members are compliant.</span></span>  
  
-   <span data-ttu-id="4a068-113">インターフェイスのソース コードを制御することはできません、CLS 準拠が必要な場合、または準拠しているが明確でない場合は、このメンバーを別のインターフェイスを定義します。</span><span class="sxs-lookup"><span data-stu-id="4a068-113">If you require CLS compliance and do not have control over the interface source code, or if it does not qualify to be compliant, define this member within a different interface.</span></span>  
  
-   <span data-ttu-id="4a068-114">このメンバーが、現在のインターフェイス内に維持されることが必要な場合は、削除、<xref:System.CLSCompliantAttribute>その定義からとしてマークまたは`<CLSCompliant(False)>`します。</span><span class="sxs-lookup"><span data-stu-id="4a068-114">If you require that this member remain within its current interface, remove the <xref:System.CLSCompliantAttribute> from its definition or mark it as `<CLSCompliant(False)>`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a068-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="4a068-115">See also</span></span>
- [<span data-ttu-id="4a068-116">Interface ステートメント</span><span class="sxs-lookup"><span data-stu-id="4a068-116">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)

