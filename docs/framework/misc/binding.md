---
title: <binding>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 666183d6-4d1f-45c7-ac64-bdf93ee8f36f
ms.openlocfilehash: fb51eb1962603439b89a203eb668dfb543049170
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271474"
---
# <a name="binding"></a><span data-ttu-id="7bc9e-101">\<binding></span><span class="sxs-lookup"><span data-stu-id="7bc9e-101">\<binding></span></span>
<span data-ttu-id="7bc9e-102">`binding` 要素を使用して、Windows Communication Foundation (WCF) によって提供される異なる型の定義済みバインディングを構成できます。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-102">You can use the `binding` element to configure different types of predefined bindings provided by Windows Communication Foundation (WCF).</span></span>  
  
## <a name="system-provided-binding"></a><span data-ttu-id="7bc9e-103">システム指定のバインディング</span><span class="sxs-lookup"><span data-stu-id="7bc9e-103">System-Provided Binding</span></span>  
 <span data-ttu-id="7bc9e-104">システム指定のバインディングは、WCF メッセージ スタックの複雑さを隠蔽します。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-104">System-provided bindings hide the complexity of the WCF messaging stack.</span></span> <span data-ttu-id="7bc9e-105">システム指定のバインディングを使用しているアプリケーションは、スタックを完全に制御する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-105">Applications using system-provided bindings do not require full control over the stack.</span></span> <span data-ttu-id="7bc9e-106">システム指定の各バインディングに公開される属性は、バインディングが処理する使用シナリオに最適な属性です。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-106">The attributes exposed on each system-provided binding are the ones most appropriate for the usage scenario the binding addresses.</span></span>  
  
 <span data-ttu-id="7bc9e-107">システム指定の各バインディングの構成セクションは、バインディングの構成に使用される複数の構成を定義できます。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-107">The configuration section for each system-provided binding can define several configurations used to configure the binding.</span></span> <span data-ttu-id="7bc9e-108">各構成は、一意の名前によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-108">Each configuration is identified by a unique name.</span></span>  
  
 <span data-ttu-id="7bc9e-109">要素または属性をシステム指定のバインディングに追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-109">It is not possible to add elements or attributes to a system-provided binding.</span></span> <span data-ttu-id="7bc9e-110">追加するには、このトピックの「カスタム バインディング」セクションで説明するように、カスタム バインディングを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-110">To do so, you should implement a custom binding as described in the "Custom Binding" section of this topic.</span></span> <span data-ttu-id="7bc9e-111">システム指定のバインディングを完全に再現し、ユーザー アプリケーションで制御するいくつかの設定を追加するカスタム バインディングを定義できます。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-111">It is possible to define a custom binding that mimics a system-provided binding perfectly and adds a few settings the user application wants to have control over.</span></span>  
  
## <a name="custom-binding"></a><span data-ttu-id="7bc9e-112">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="7bc9e-112">Custom Binding</span></span>  
 <span data-ttu-id="7bc9e-113">カスタム バインディングを使用すると、WCF メッセージ スタックのフル コントロールが可能になります。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-113">Custom bindings provide full control over the WCF messaging stack.</span></span> <span data-ttu-id="7bc9e-114">個別のバインディングは、メッセージ スタックを、スタック要素の構成要素をスタックに出現する順序で指定することにより定義します。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-114">An individual binding defines the message stack by specifying the configuration elements for the stack elements in the order they appear on the stack.</span></span> <span data-ttu-id="7bc9e-115">各要素は、スタック内の 1 つの要素を定義および構成します。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-115">Each element defines and configures the one element of the stack.</span></span> <span data-ttu-id="7bc9e-116">各カスタム バインディング内の `transport` 要素は 1 つだけにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-116">There must be one and only one `transport` element in each custom binding.</span></span> <span data-ttu-id="7bc9e-117">この要素がない場合、メッセージ スタックは不完全です。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-117">Without this element, the messaging stack is incomplete.</span></span>  
  
 <span data-ttu-id="7bc9e-118">要素がスタックに出現する順序は重要です。それは、その順序で操作がメッセージに適用されるためです。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-118">The order in which elements appear in the stack matters, because it is the order in which operations are applied to the message.</span></span> <span data-ttu-id="7bc9e-119">スタック要素で推奨される順序を次に示します。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-119">The recommended order of stack elements is the following:</span></span>  
  
1.  <span data-ttu-id="7bc9e-120">トランザクション (省略可能)</span><span class="sxs-lookup"><span data-stu-id="7bc9e-120">Transactions (optional)</span></span>  
  
2.  <span data-ttu-id="7bc9e-121">リライアブル メッセージ機能 (省略可能)</span><span class="sxs-lookup"><span data-stu-id="7bc9e-121">Reliable Messaging (optional)</span></span>  
  
3.  <span data-ttu-id="7bc9e-122">セキュリティ (省略可能)</span><span class="sxs-lookup"><span data-stu-id="7bc9e-122">Security (optional)</span></span>  
  
4.  <span data-ttu-id="7bc9e-123">エンコーダー</span><span class="sxs-lookup"><span data-stu-id="7bc9e-123">Encoder</span></span>  
  
5.  <span data-ttu-id="7bc9e-124">Transport</span><span class="sxs-lookup"><span data-stu-id="7bc9e-124">Transport</span></span>  
  
 <span data-ttu-id="7bc9e-125">カスタム バインドは、`name` 属性によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="7bc9e-125">Custom bindings are identified by their `name` attribute.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7bc9e-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="7bc9e-126">See also</span></span>
- <xref:System.ServiceModel.Configuration.BindingsSection>
- <xref:System.ServiceModel.Channels.Binding>
- <xref:System.ServiceModel.Channels.BindingElement>
- [<span data-ttu-id="7bc9e-127">バインディング</span><span class="sxs-lookup"><span data-stu-id="7bc9e-127">Bindings</span></span>](../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="7bc9e-128">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="7bc9e-128">Custom Bindings</span></span>](../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="7bc9e-129">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="7bc9e-129">\<customBinding></span></span>](../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
