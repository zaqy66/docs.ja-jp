---
title: AsymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: 7bd3b6be-8f77-4927-93ae-6fa371893cca
ms.openlocfilehash: e968f5f2d7ffdb193b30762d32a47be3778b98dc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54621358"
---
# <a name="asymmetricsecuritybindingelement"></a><span data-ttu-id="c00de-102">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="c00de-102">AsymmetricSecurityBindingElement</span></span>
<span data-ttu-id="c00de-103">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="c00de-103">AsymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c00de-104">構文</span><span class="sxs-lookup"><span data-stu-id="c00de-104">Syntax</span></span>  
  
```csharp
class AsymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="c00de-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="c00de-105">Methods</span></span>  
 <span data-ttu-id="c00de-106">AsymmetricSecurityBindingElement クラスで定義されるメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="c00de-106">The AsymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="c00de-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="c00de-107">Properties</span></span>  
 <span data-ttu-id="c00de-108">AsymmetricSecurityBindingElement クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="c00de-108">The AsymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="c00de-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="c00de-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="c00de-110">データ型: string</span><span class="sxs-lookup"><span data-stu-id="c00de-110">Data type: string</span></span>  
  
 <span data-ttu-id="c00de-111">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="c00de-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c00de-112">このバインディングのメッセージの暗号化と署名の命令。</span><span class="sxs-lookup"><span data-stu-id="c00de-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="c00de-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="c00de-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="c00de-114">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="c00de-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="c00de-115">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="c00de-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c00de-116">バインディングで署名の確認が必要かどうか。</span><span class="sxs-lookup"><span data-stu-id="c00de-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c00de-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="c00de-117">Requirements</span></span>  
  
|<span data-ttu-id="c00de-118">MOF</span><span class="sxs-lookup"><span data-stu-id="c00de-118">MOF</span></span>|<span data-ttu-id="c00de-119">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="c00de-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="c00de-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="c00de-120">Namespace</span></span>|<span data-ttu-id="c00de-121">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="c00de-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c00de-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="c00de-122">See also</span></span>
- <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
