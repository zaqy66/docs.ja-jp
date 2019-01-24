---
title: 変数&#39; &lt;variablename&gt; &#39; 、値が割り当てられる前に使用されます
ms.date: 07/20/2015
f1_keywords:
- vbc42104
- BC42104
helpviewer_keywords:
- BC42104
ms.assetid: 6909aa0b-b4a1-46f5-a18c-ba3e565c1dd8
ms.openlocfilehash: f91343e850600c9e5f4b4b4eb2126798baf3d980
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54647024"
---
# <a name="variable-39ltvariablenamegt39-is-used-before-it-has-been-assigned-a-value"></a><span data-ttu-id="df2e7-102">変数&#39; &lt;variablename&gt; &#39; 、値が割り当てられる前に使用されます</span><span class="sxs-lookup"><span data-stu-id="df2e7-102">Variable &#39;&lt;variablename&gt;&#39; is used before it has been assigned a value</span></span>
<span data-ttu-id="df2e7-103">変数 '\<variablename >' は、値が割り当てられる前に使用します。</span><span class="sxs-lookup"><span data-stu-id="df2e7-103">Variable '\<variablename>' is used before it has been assigned a value.</span></span> <span data-ttu-id="df2e7-104">結果として、実行時に null 参照の例外が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="df2e7-104">A null reference exception could result at run time.</span></span>  
  
 <span data-ttu-id="df2e7-105">アプリケーションでは、少なくとも 1 つのパスをそのコードを任意の値が割り当てられる前に変数を読み込むことがあります。</span><span class="sxs-lookup"><span data-stu-id="df2e7-105">An application has at least one possible path through its code that reads a variable before any value is assigned to it.</span></span>  
  
 <span data-ttu-id="df2e7-106">変数に値が割り当てられていない場合、変数はそのデータ型の既定値を保持します。</span><span class="sxs-lookup"><span data-stu-id="df2e7-106">If a variable has never been assigned a value, it holds the default value for its data type.</span></span> <span data-ttu-id="df2e7-107">参照データ型の場合、その既定値は [Nothing](../../../visual-basic/language-reference/nothing.md)です。</span><span class="sxs-lookup"><span data-stu-id="df2e7-107">For a reference data type, that default value is [Nothing](../../../visual-basic/language-reference/nothing.md).</span></span> <span data-ttu-id="df2e7-108">値が `Nothing` である参照変数を読み取ると、状況によって <xref:System.NullReferenceException> が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="df2e7-108">Reading a reference variable that has a value of `Nothing` can cause a <xref:System.NullReferenceException> in some circumstances.</span></span>  
  
 <span data-ttu-id="df2e7-109">既定では、このメッセージは警告です。</span><span class="sxs-lookup"><span data-stu-id="df2e7-109">By default, this message is a warning.</span></span> <span data-ttu-id="df2e7-110">警告を非表示にする方法や、警告をエラーとして扱う方法の詳細については、「 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df2e7-110">For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="df2e7-111">**エラー ID:** BC42104</span><span class="sxs-lookup"><span data-stu-id="df2e7-111">**Error ID:** BC42104</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="df2e7-112">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="df2e7-112">To correct this error</span></span>  
  
-   <span data-ttu-id="df2e7-113">制御フローのロジックを確認し、によって読み取られる任意のステートメントに制御が渡される前に、変数が有効な値を持つかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="df2e7-113">Check your control flow logic and make sure the variable has a valid value before control passes to any statement that reads it.</span></span>  
  
-   <span data-ttu-id="df2e7-114">変数が常に有効な値を持つことを保証するために 1 つの方法では、その宣言の一部として初期化します。</span><span class="sxs-lookup"><span data-stu-id="df2e7-114">One way to guarantee that the variable always has a valid value is to initialize it as part of its declaration.</span></span> <span data-ttu-id="df2e7-115">「初期化」を参照してください[Dim ステートメント](../../../visual-basic/language-reference/statements/dim-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="df2e7-115">See "Initialization" in [Dim Statement](../../../visual-basic/language-reference/statements/dim-statement.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df2e7-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="df2e7-116">See also</span></span>
- [<span data-ttu-id="df2e7-117">Dim ステートメント</span><span class="sxs-lookup"><span data-stu-id="df2e7-117">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)
- [<span data-ttu-id="df2e7-118">変数宣言</span><span class="sxs-lookup"><span data-stu-id="df2e7-118">Variable Declaration</span></span>](../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [<span data-ttu-id="df2e7-119">変数のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="df2e7-119">Troubleshooting Variables</span></span>](../../../visual-basic/programming-guide/language-features/variables/troubleshooting-variables.md)
