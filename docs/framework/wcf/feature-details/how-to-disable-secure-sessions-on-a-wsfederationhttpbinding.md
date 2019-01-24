---
title: '方法: WSFederationHttpBinding のセキュリティで保護されたセッションを無効にします。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF, federation
- federation
ms.assetid: 675fa143-6a4e-4be3-8afc-673334ab55ec
ms.openlocfilehash: 8c03bb9601ecbaaf8694d1df26ba43e34434ac47
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54720029"
---
# <a name="how-to-disable-secure-sessions-on-a-wsfederationhttpbinding"></a><span data-ttu-id="ae778-102">方法: WSFederationHttpBinding のセキュリティで保護されたセッションを無効にします。</span><span class="sxs-lookup"><span data-stu-id="ae778-102">How to: Disable Secure Sessions on a WSFederationHttpBinding</span></span>
<span data-ttu-id="ae778-103">フェデレーション資格情報を必要とするサービスの中には、セキュリティで保護されたセッションをサポートしないものがあります。</span><span class="sxs-lookup"><span data-stu-id="ae778-103">Some services may require federated credentials but not support secure sessions.</span></span> <span data-ttu-id="ae778-104">その場合は、セキュリティで保護されたセッション機能を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae778-104">In that case, you must disable the secure session feature.</span></span> <span data-ttu-id="ae778-105"><xref:System.ServiceModel.WSHttpBinding> とは異なり、<xref:System.ServiceModel.WSFederationHttpBinding> クラスでは、サービスとの通信中に、セキュリティで保護されたセッションを無効にできません。</span><span class="sxs-lookup"><span data-stu-id="ae778-105">Unlike the <xref:System.ServiceModel.WSHttpBinding>, the <xref:System.ServiceModel.WSFederationHttpBinding> class does not provide a way to disable secure sessions when communicating with a service.</span></span> <span data-ttu-id="ae778-106">代わりに、セキュリティで保護されたセッションの設定をブートストラップで置き換えるカスタム バインドを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae778-106">Instead, you must create a custom binding that replaces the secure session settings with a bootstrap.</span></span>  
  
 <span data-ttu-id="ae778-107">ここでは、<xref:System.ServiceModel.WSFederationHttpBinding> に含まれるバインド要素を変更してカスタム バインドを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ae778-107">This topic demonstrates how to modify the binding elements contained within a <xref:System.ServiceModel.WSFederationHttpBinding> to create a custom binding.</span></span> <span data-ttu-id="ae778-108">結果は、セキュリティで保護されたセッションを使用しないことを除き、<xref:System.ServiceModel.WSFederationHttpBinding> と同じです。</span><span class="sxs-lookup"><span data-stu-id="ae778-108">The result is identical to the <xref:System.ServiceModel.WSFederationHttpBinding> except that it does not use secure sessions.</span></span>  
  
### <a name="to-create-a-custom-federated-binding-without-secure-session"></a><span data-ttu-id="ae778-109">セキュリティで保護されたセッションを使用しないカスタム フェデレーション バインディングを作成するには</span><span class="sxs-lookup"><span data-stu-id="ae778-109">To create a custom federated binding without secure session</span></span>  
  
1.  <span data-ttu-id="ae778-110">コードで強制的に、または構成ファイルから読み込む方法によって、<xref:System.ServiceModel.WSFederationHttpBinding> クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae778-110">Create an instance of the <xref:System.ServiceModel.WSFederationHttpBinding> class either imperatively in code or by loading one from the configuration file.</span></span>  
  
2.  <span data-ttu-id="ae778-111"><xref:System.ServiceModel.WSFederationHttpBinding> の複製を <xref:System.ServiceModel.Channels.CustomBinding> 内に作成します。</span><span class="sxs-lookup"><span data-stu-id="ae778-111">Clone the <xref:System.ServiceModel.WSFederationHttpBinding> into a <xref:System.ServiceModel.Channels.CustomBinding>.</span></span>  
  
3.  <span data-ttu-id="ae778-112"><xref:System.ServiceModel.Channels.SecurityBindingElement> 内で <xref:System.ServiceModel.Channels.CustomBinding> を見つけます。</span><span class="sxs-lookup"><span data-stu-id="ae778-112">Find the <xref:System.ServiceModel.Channels.SecurityBindingElement> in the <xref:System.ServiceModel.Channels.CustomBinding>.</span></span>  
  
4.  <span data-ttu-id="ae778-113"><xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters> 内で <xref:System.ServiceModel.Channels.SecurityBindingElement> を見つけます。</span><span class="sxs-lookup"><span data-stu-id="ae778-113">Find the <xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters> in the <xref:System.ServiceModel.Channels.SecurityBindingElement>.</span></span>  
  
5.  <span data-ttu-id="ae778-114">元の <xref:System.ServiceModel.Channels.SecurityBindingElement> を <xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters> のブートストラップ セキュリティ バインド要素で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="ae778-114">Replace the original <xref:System.ServiceModel.Channels.SecurityBindingElement> with the bootstrap security binding element from the <xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ae778-115">例</span><span class="sxs-lookup"><span data-stu-id="ae778-115">Example</span></span>  
 <span data-ttu-id="ae778-116">次の例では、セキュリティで保護されたセッションを使用しないカスタム フェデレーション バインディングを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae778-116">This following example creates a custom federated binding without secure session.</span></span>  
  
 [!code-csharp[c_CustomFederationBinding#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_customfederationbinding/cs/c_customfederationbinding.cs#0)]
 [!code-vb[c_CustomFederationBinding#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_customfederationbinding/vb/c_customfederationbinding.vb#0)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="ae778-117">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="ae778-117">Compiling the Code</span></span>  
  
-   <span data-ttu-id="ae778-118">このコード例をコンパイルするには、System.ServiceModel.dll アセンブリを参照するプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae778-118">To compile the code example, create a project that references the System.ServiceModel.dll assembly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae778-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae778-119">See also</span></span>
- [<span data-ttu-id="ae778-120">バインディングとセキュリティ</span><span class="sxs-lookup"><span data-stu-id="ae778-120">Bindings and Security</span></span>](../../../../docs/framework/wcf/feature-details/bindings-and-security.md)
