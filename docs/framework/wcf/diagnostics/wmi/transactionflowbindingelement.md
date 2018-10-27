---
title: TransactionFlowBindingElement
ms.date: 03/30/2017
ms.assetid: 0a9656fe-2400-45ca-ad79-92715c8cf190
ms.openlocfilehash: 027ace6ea9fc2a0e5ce63efa84e1a49c0ed2cd0a
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188028"
---
# <a name="transactionflowbindingelement"></a><span data-ttu-id="a91d6-102">TransactionFlowBindingElement</span><span class="sxs-lookup"><span data-stu-id="a91d6-102">TransactionFlowBindingElement</span></span>
<span data-ttu-id="a91d6-103">TransactionFlowBindingElement</span><span class="sxs-lookup"><span data-stu-id="a91d6-103">TransactionFlowBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a91d6-104">構文</span><span class="sxs-lookup"><span data-stu-id="a91d6-104">Syntax</span></span>  
  
```csharp
class TransactionFlowBindingElement : BindingElement  
{  
  string IssuedTokens;  
  string TransactionProtocol;  
  boolean Transactions;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="a91d6-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="a91d6-105">Methods</span></span>  
 <span data-ttu-id="a91d6-106">TransactionFlowBindingElement クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="a91d6-106">The TransactionFlowBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="a91d6-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="a91d6-107">Properties</span></span>  
 <span data-ttu-id="a91d6-108">TransactionFlowBindingElement クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="a91d6-108">The TransactionFlowBindingElement class has the following properties:</span></span>  
  
### <a name="issuedtokens"></a><span data-ttu-id="a91d6-109">IssuedTokens</span><span class="sxs-lookup"><span data-stu-id="a91d6-109">IssuedTokens</span></span>  
 <span data-ttu-id="a91d6-110">データ型: string</span><span class="sxs-lookup"><span data-stu-id="a91d6-110">Data type: string</span></span>  
  
 <span data-ttu-id="a91d6-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a91d6-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a91d6-112">発行されるセキュリティ トークン ヘッダー (WS-Trust からの IssuedTokens) の要件を指定します。</span><span class="sxs-lookup"><span data-stu-id="a91d6-112">Specifies the requirement for an issued security tokens header (IssuedTokens from WS-Trust).</span></span>  
  
### <a name="transactionprotocol"></a><span data-ttu-id="a91d6-113">TransactionProtocol</span><span class="sxs-lookup"><span data-stu-id="a91d6-113">TransactionProtocol</span></span>  
 <span data-ttu-id="a91d6-114">データ型: string</span><span class="sxs-lookup"><span data-stu-id="a91d6-114">Data type: string</span></span>  
  
 <span data-ttu-id="a91d6-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a91d6-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a91d6-116">トランザクションをフローさせるためにサービスによって使用されるトランザクション プロトコルです。</span><span class="sxs-lookup"><span data-stu-id="a91d6-116">The transactions protocol used by the service to flow transactions.</span></span>  
  
### <a name="transactions"></a><span data-ttu-id="a91d6-117">トランザクション</span><span class="sxs-lookup"><span data-stu-id="a91d6-117">Transactions</span></span>  
 <span data-ttu-id="a91d6-118">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="a91d6-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="a91d6-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a91d6-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a91d6-120">受信トランザクションをサポートするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a91d6-120">Indicates whether the incoming transaction is supported.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a91d6-121">必要条件</span><span class="sxs-lookup"><span data-stu-id="a91d6-121">Requirements</span></span>  
  
|<span data-ttu-id="a91d6-122">MOF</span><span class="sxs-lookup"><span data-stu-id="a91d6-122">MOF</span></span>|<span data-ttu-id="a91d6-123">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="a91d6-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="a91d6-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="a91d6-124">Namespace</span></span>|<span data-ttu-id="a91d6-125">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="a91d6-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a91d6-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="a91d6-126">See Also</span></span>  
 <xref:System.ServiceModel.Channels.TransactionFlowBindingElement>
