---
title: My.Forms および My.WebServices が提供する既定のオブジェクト インスタンス (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- My.WebServices object [Visual Basic], developing applications
- My.Forms object [Visual Basic], developing applications
- rapid application development (RAD), My.Forms
- rapid application development (RAD), My.WebServices
ms.assetid: de930027-9108-4f0c-b97c-5e7db4d6ef79
ms.openlocfilehash: 9285e88e3dc9fd8b3731416b1c40811188d6a33d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54563601"
---
# <a name="default-object-instances-provided-by-myforms-and-mywebservices-visual-basic"></a><span data-ttu-id="93201-102">My.Forms および My.WebServices が提供する既定のオブジェクト インスタンス (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="93201-102">Default Object Instances Provided by My.Forms and My.WebServices (Visual Basic)</span></span>
<span data-ttu-id="93201-103">[My.Forms](../../../visual-basic/language-reference/objects/my-forms-object.md)と[My.WebServices](../../../visual-basic/language-reference/objects/my-webservices-object.md)オブジェクトは、フォーム、データ ソース、およびアプリケーションによって使用される XML Web サービスへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="93201-103">The [My.Forms](../../../visual-basic/language-reference/objects/my-forms-object.md) and [My.WebServices](../../../visual-basic/language-reference/objects/my-webservices-object.md) objects provide access to forms, data sources, and XML Web services used by your application.</span></span> <span data-ttu-id="93201-104">コレクションを提供することによってこれを実現*既定インスタンス*のこれらの各オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="93201-104">They do this by providing collections of *default instances* of each of these objects.</span></span>  
  
## <a name="default-instances"></a><span data-ttu-id="93201-105">既定のインスタンス</span><span class="sxs-lookup"><span data-stu-id="93201-105">Default Instances</span></span>  
 <span data-ttu-id="93201-106">既定のインスタンスがインスタンスには、ランタイムによって提供されする必要はありませんが、クラスの宣言およびインスタンスを使用して、`Dim`と`New`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="93201-106">A default instance is an instance of the class that is provided by the runtime and does not need to be declared and instantiated using the `Dim` and `New` statements.</span></span> <span data-ttu-id="93201-107">次の例は、どのようにする可能性がありますが宣言およびインスタンスのインスタンスを<xref:System.Windows.Forms.Form>と呼ばれるクラス`Form1`、どのようにこの既定のインスタンスを取得することができました<xref:System.Windows.Forms.Form>クラスを通じて`My.Forms`します。</span><span class="sxs-lookup"><span data-stu-id="93201-107">The following example demonstrates how you might have declared and instantiated an instance of a <xref:System.Windows.Forms.Form> class called `Form1`, and how you are now able to get a default instance of this <xref:System.Windows.Forms.Form> class through `My.Forms`.</span></span>  
  
 [!code-vb[VbVbcnMy#5](../../../visual-basic/developing-apps/development-with-my/codesnippet/VisualBasic/default-object-instances-provided-by-my-forms-and-my-webservices_1.vb)]  
  
 [!code-vb[VbVbcnMy#6](../../../visual-basic/developing-apps/development-with-my/codesnippet/VisualBasic/default-object-instances-provided-by-my-forms-and-my-webservices_2.vb)]  
  
 <span data-ttu-id="93201-108">`My.Forms`オブジェクトの既定のインスタンスのコレクションを返すすべて`Form`プロジェクト内に存在するクラス。</span><span class="sxs-lookup"><span data-stu-id="93201-108">The `My.Forms` object returns a collection of default instances for every `Form` class that exists in your project.</span></span> <span data-ttu-id="93201-109">同様に、`My.WebServices`アプリケーションへの参照を作成したすべての Web サービスのプロキシ クラスの既定のインスタンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="93201-109">Similarly, `My.WebServices` provides a default instance of the proxy class for every Web service that you have created a reference to in your application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93201-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="93201-110">See also</span></span>
- [<span data-ttu-id="93201-111">My.Forms オブジェクト</span><span class="sxs-lookup"><span data-stu-id="93201-111">My.Forms Object</span></span>](../../../visual-basic/language-reference/objects/my-forms-object.md)
- [<span data-ttu-id="93201-112">My.WebServices オブジェクト</span><span class="sxs-lookup"><span data-stu-id="93201-112">My.WebServices Object</span></span>](../../../visual-basic/language-reference/objects/my-webservices-object.md)
- [<span data-ttu-id="93201-113">プロジェクトの種類に応じた My の機能</span><span class="sxs-lookup"><span data-stu-id="93201-113">How My Depends on Project Type</span></span>](../../../visual-basic/developing-apps/development-with-my/how-my-depends-on-project-type.md)
