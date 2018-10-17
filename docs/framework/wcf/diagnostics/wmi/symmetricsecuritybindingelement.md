---
title: SymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: b2e182b6-c041-4d80-a926-6058068d9f79
author: BrucePerlerMS
ms.openlocfilehash: e633ae19cd17930fb140a93ffd0910c7ed8efea4
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374433"
---
# <a name="symmetricsecuritybindingelement"></a><span data-ttu-id="a64f0-102">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="a64f0-102">SymmetricSecurityBindingElement</span></span>
<span data-ttu-id="a64f0-103">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="a64f0-103">SymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a64f0-104">構文</span><span class="sxs-lookup"><span data-stu-id="a64f0-104">Syntax</span></span>  
  
```csharp
class SymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="a64f0-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="a64f0-105">Methods</span></span>  
 <span data-ttu-id="a64f0-106">SymmetricSecurityBindingElement クラスで定義されるメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="a64f0-106">The SymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="a64f0-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="a64f0-107">Properties</span></span>  
 <span data-ttu-id="a64f0-108">SymmetricSecurityBindingElement クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="a64f0-108">The SymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="a64f0-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="a64f0-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="a64f0-110">データ型: string</span><span class="sxs-lookup"><span data-stu-id="a64f0-110">Data type: string</span></span>  
  
 <span data-ttu-id="a64f0-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a64f0-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a64f0-112">このバインディングのメッセージの暗号化と署名の命令。</span><span class="sxs-lookup"><span data-stu-id="a64f0-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="a64f0-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="a64f0-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="a64f0-114">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="a64f0-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="a64f0-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a64f0-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a64f0-116">バインディングで署名の確認が必要かどうか。</span><span class="sxs-lookup"><span data-stu-id="a64f0-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a64f0-117">要件</span><span class="sxs-lookup"><span data-stu-id="a64f0-117">Requirements</span></span>  
  
|<span data-ttu-id="a64f0-118">MOF</span><span class="sxs-lookup"><span data-stu-id="a64f0-118">MOF</span></span>|<span data-ttu-id="a64f0-119">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="a64f0-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="a64f0-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="a64f0-120">Namespace</span></span>|<span data-ttu-id="a64f0-121">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="a64f0-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a64f0-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="a64f0-122">See Also</span></span>  
 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
