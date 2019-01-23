---
title: "'<interfacename>.<membername>' は、基本クラス '<baseclassname>' によって既に実装されています。&lt;&gt;&lt;&gt;&lt;&gt; <type> の再実装と見なされます。&lt;&gt;"
ms.date: 07/20/2015
f1_keywords:
- vbc42015
- bc42015
helpviewer_keywords:
- BC42015
ms.assetid: 658c070a-113e-4bd8-b294-12c243191160
ms.openlocfilehash: 9054c293ede9db4637f23579407f2f76db29f2ba
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2018
ms.locfileid: "33588971"
---
# <a name="39ltinterfacenamegtltmembernamegt39-is-already-implemented-by-the-base-class-39ltbaseclassnamegt39-re-implementation-of-lttypegt-assumed"></a><span data-ttu-id="9f8f1-103">'<interfacename>.<membername>' は、基本クラス '<baseclassname>' によって既に実装されています。&lt;&gt;&lt;&gt;&lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="9f8f1-103">&#39;&lt;interfacename&gt;.&lt;membername&gt;&#39; is already implemented by the base class &#39;&lt;baseclassname&gt;&#39;.</span></span> <span data-ttu-id="9f8f1-104"><type> の再実装と見なされます。&lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="9f8f1-104">Re-implementation of &lt;type&gt; assumed</span></span>
<span data-ttu-id="9f8f1-105">プロパティ、プロシージャ、または派生クラスでイベントを使用して、`Implements`句は、基底クラスで既に実装されているインターフェイス メンバーを指定します。</span><span class="sxs-lookup"><span data-stu-id="9f8f1-105">A property, procedure, or event in a derived class uses an `Implements` clause specifying an interface member that is already implemented in the base class.</span></span>  
  
 <span data-ttu-id="9f8f1-106">派生クラスでは、その基底クラスによって実装されているインターフェイス メンバーを再実装できます。</span><span class="sxs-lookup"><span data-stu-id="9f8f1-106">A derived class can reimplement an interface member that is implemented by its base class.</span></span> <span data-ttu-id="9f8f1-107">このことは、基底クラスの実装をオーバーライドすることとは異なります。</span><span class="sxs-lookup"><span data-stu-id="9f8f1-107">This is not the same as overriding the base class implementation.</span></span> <span data-ttu-id="9f8f1-108">詳細については、次を参照してください。 [Implements](../../../visual-basic/language-reference/statements/implements-clause.md)です。</span><span class="sxs-lookup"><span data-stu-id="9f8f1-108">For more information, see [Implements](../../../visual-basic/language-reference/statements/implements-clause.md).</span></span>  
  
 <span data-ttu-id="9f8f1-109">既定では、このメッセージは警告です。</span><span class="sxs-lookup"><span data-stu-id="9f8f1-109">By default, this message is a warning.</span></span> <span data-ttu-id="9f8f1-110">警告を非表示にする方法や、警告をエラーとして扱う方法の詳細については、「 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f8f1-110">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="9f8f1-111">**エラー ID:** BC42015</span><span class="sxs-lookup"><span data-stu-id="9f8f1-111">**Error ID:** BC42015</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="9f8f1-112">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="9f8f1-112">To correct this error</span></span>  
  
-   <span data-ttu-id="9f8f1-113">インターフェイス メンバーを再実装する場合は、操作を行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9f8f1-113">If you intend to reimplement the interface member, you do not need to take any action.</span></span> <span data-ttu-id="9f8f1-114">派生クラス内のコードを使用する場合を除き、再実装されたメンバーにアクセスする、`MyBase`キーワードを基底クラスの実装にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="9f8f1-114">Code in your derived class accesses the reimplemented member unless you use the `MyBase` keyword to access the base class implementation.</span></span>  
  
-   <span data-ttu-id="9f8f1-115">インターフェイス メンバーを再実装しない場合は、プロパティ、プロシージャ、またはイベント宣言から、 `Implements` 句を削除します。</span><span class="sxs-lookup"><span data-stu-id="9f8f1-115">If you do not intend to reimplement the interface member, remove the `Implements` clause from the property, procedure, or event declaration.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f8f1-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="9f8f1-116">See Also</span></span>  
 [<span data-ttu-id="9f8f1-117">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9f8f1-117">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
