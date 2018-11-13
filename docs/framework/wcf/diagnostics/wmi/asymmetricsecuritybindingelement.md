---
title: AsymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: 7bd3b6be-8f77-4927-93ae-6fa371893cca
ms.openlocfilehash: 076313548828f1fbce9c68b48c0fa7db9cca095f
ms.sourcegitcommit: 296183dbe35077b5c5e5e74d5fbe7f399bc507ee
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/05/2018
ms.locfileid: "50982791"
---
# <a name="asymmetricsecuritybindingelement"></a><span data-ttu-id="30b93-102">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="30b93-102">AsymmetricSecurityBindingElement</span></span>
<span data-ttu-id="30b93-103">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="30b93-103">AsymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30b93-104">構文</span><span class="sxs-lookup"><span data-stu-id="30b93-104">Syntax</span></span>  
  
```csharp
class AsymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="30b93-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="30b93-105">Methods</span></span>  
 <span data-ttu-id="30b93-106">AsymmetricSecurityBindingElement クラスで定義されるメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="30b93-106">The AsymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="30b93-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="30b93-107">Properties</span></span>  
 <span data-ttu-id="30b93-108">AsymmetricSecurityBindingElement クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="30b93-108">The AsymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="30b93-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="30b93-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="30b93-110">データ型: string</span><span class="sxs-lookup"><span data-stu-id="30b93-110">Data type: string</span></span>  
  
 <span data-ttu-id="30b93-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="30b93-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="30b93-112">このバインディングのメッセージの暗号化と署名の命令。</span><span class="sxs-lookup"><span data-stu-id="30b93-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="30b93-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="30b93-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="30b93-114">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="30b93-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="30b93-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="30b93-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="30b93-116">バインディングで署名の確認が必要かどうか。</span><span class="sxs-lookup"><span data-stu-id="30b93-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="30b93-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="30b93-117">Requirements</span></span>  
  
|<span data-ttu-id="30b93-118">MOF</span><span class="sxs-lookup"><span data-stu-id="30b93-118">MOF</span></span>|<span data-ttu-id="30b93-119">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="30b93-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="30b93-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="30b93-120">Namespace</span></span>|<span data-ttu-id="30b93-121">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="30b93-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="30b93-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="30b93-122">See Also</span></span>  
 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
