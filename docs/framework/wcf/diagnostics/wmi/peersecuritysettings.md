---
title: PeerSecuritySettings
ms.date: 03/30/2017
ms.assetid: 24ae0d35-f3a3-419b-afd6-686e22aae27b
ms.openlocfilehash: 92aca4c790607de91314aacf6414d0dfacea9a9f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50193163"
---
# <a name="peersecuritysettings"></a><span data-ttu-id="1265a-102">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="1265a-102">PeerSecuritySettings</span></span>
<span data-ttu-id="1265a-103">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="1265a-103">PeerSecuritySettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1265a-104">構文</span><span class="sxs-lookup"><span data-stu-id="1265a-104">Syntax</span></span>  
  
```csharp
class PeerSecuritySettings  
{  
  string Mode;  
  PeerTransportSecuritySettings Transport;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="1265a-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="1265a-105">Methods</span></span>  
 <span data-ttu-id="1265a-106">PeerSecuritySettings クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="1265a-106">The PeerSecuritySettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="1265a-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="1265a-107">Properties</span></span>  
 <span data-ttu-id="1265a-108">PeerSecuritySettings クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="1265a-108">The PeerSecuritySettings class has the following properties:</span></span>  
  
### <a name="mode"></a><span data-ttu-id="1265a-109">モード</span><span class="sxs-lookup"><span data-stu-id="1265a-109">Mode</span></span>  
 <span data-ttu-id="1265a-110">データ型: string</span><span class="sxs-lookup"><span data-stu-id="1265a-110">Data type: string</span></span>  
  
 <span data-ttu-id="1265a-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1265a-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1265a-112">このバインディングで構成されたエンドポイントによって、メッセージ レベルおよびトランスポート レベルのセキュリティが使用されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="1265a-112">Whether message-level and transport-level security are used by an endpoint configured with the binding.</span></span>  
  
### <a name="transport"></a><span data-ttu-id="1265a-113">Transport</span><span class="sxs-lookup"><span data-stu-id="1265a-113">Transport</span></span>  
 <span data-ttu-id="1265a-114">データ型 : PeerTransportSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="1265a-114">Data type: PeerTransportSecuritySettings</span></span>  
  
 <span data-ttu-id="1265a-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1265a-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1265a-116">トランスポートのセキュリティ設定です。</span><span class="sxs-lookup"><span data-stu-id="1265a-116">Transport security settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1265a-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="1265a-117">Requirements</span></span>  
  
|<span data-ttu-id="1265a-118">MOF</span><span class="sxs-lookup"><span data-stu-id="1265a-118">MOF</span></span>|<span data-ttu-id="1265a-119">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="1265a-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="1265a-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="1265a-120">Namespace</span></span>|<span data-ttu-id="1265a-121">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="1265a-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1265a-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="1265a-122">See Also</span></span>  
 <xref:System.ServiceModel.PeerSecuritySettings>
