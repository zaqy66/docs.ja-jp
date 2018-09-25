---
title: SymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: b2e182b6-c041-4d80-a926-6058068d9f79
author: BrucePerlerMS
ms.openlocfilehash: 180b64f6f37e5c765585e52b292319816618be28
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47076523"
---
# <a name="symmetricsecuritybindingelement"></a><span data-ttu-id="ba2f7-102">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="ba2f7-102">SymmetricSecurityBindingElement</span></span>
<span data-ttu-id="ba2f7-103">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="ba2f7-103">SymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ba2f7-104">構文</span><span class="sxs-lookup"><span data-stu-id="ba2f7-104">Syntax</span></span>  
  
```  
class SymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="ba2f7-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="ba2f7-105">Methods</span></span>  
 <span data-ttu-id="ba2f7-106">SymmetricSecurityBindingElement クラスで定義されるメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="ba2f7-106">The SymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="ba2f7-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="ba2f7-107">Properties</span></span>  
 <span data-ttu-id="ba2f7-108">SymmetricSecurityBindingElement クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="ba2f7-108">The SymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="ba2f7-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="ba2f7-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="ba2f7-110">データ型: string</span><span class="sxs-lookup"><span data-stu-id="ba2f7-110">Data type: string</span></span>  
  
 <span data-ttu-id="ba2f7-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ba2f7-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="ba2f7-112">このバインディングのメッセージの暗号化と署名の命令。</span><span class="sxs-lookup"><span data-stu-id="ba2f7-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="ba2f7-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="ba2f7-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="ba2f7-114">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="ba2f7-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="ba2f7-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ba2f7-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="ba2f7-116">バインディングで署名の確認が必要かどうか。</span><span class="sxs-lookup"><span data-stu-id="ba2f7-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ba2f7-117">要件</span><span class="sxs-lookup"><span data-stu-id="ba2f7-117">Requirements</span></span>  
  
|<span data-ttu-id="ba2f7-118">MOF</span><span class="sxs-lookup"><span data-stu-id="ba2f7-118">MOF</span></span>|<span data-ttu-id="ba2f7-119">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="ba2f7-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="ba2f7-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba2f7-120">Namespace</span></span>|<span data-ttu-id="ba2f7-121">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="ba2f7-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ba2f7-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="ba2f7-122">See Also</span></span>  
 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
