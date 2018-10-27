---
title: MsmqTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 1c89f073-9ed3-4025-a8c5-13535a0f526b
ms.openlocfilehash: 33cd9c427ed5ad04eaf9e9889f60f091f335d1e7
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2018
ms.locfileid: "50045989"
---
# <a name="msmqtransportbindingelement"></a><span data-ttu-id="9e57b-102">MsmqTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="9e57b-102">MsmqTransportBindingElement</span></span>
<span data-ttu-id="9e57b-103">MsmqTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="9e57b-103">MsmqTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9e57b-104">構文</span><span class="sxs-lookup"><span data-stu-id="9e57b-104">Syntax</span></span>  
  
```csharp
class MsmqTransportBindingElement : MsmqBindingElementBase  
{  
  sint32 MaxPoolSize;  
  string QueueTransferProtocol;  
  boolean UseActiveDirectory;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="9e57b-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="9e57b-105">Methods</span></span>  
 <span data-ttu-id="9e57b-106">MsmqTransportBindingElement クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="9e57b-106">The MsmqTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="9e57b-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="9e57b-107">Properties</span></span>  
 <span data-ttu-id="9e57b-108">MsmqTransportBindingElement クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="9e57b-108">The MsmqTransportBindingElement class has the following properties:</span></span>  
  
### <a name="maxpoolsize"></a><span data-ttu-id="9e57b-109">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="9e57b-109">MaxPoolSize</span></span>  
 <span data-ttu-id="9e57b-110">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="9e57b-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="9e57b-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9e57b-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9e57b-112">内部 MSMQ メッセージ オブジェクトを含むプールの最大サイズです。</span><span class="sxs-lookup"><span data-stu-id="9e57b-112">The maximum size of the pool that contains internal MSMQ message objects.</span></span>  
  
### <a name="queuetransferprotocol"></a><span data-ttu-id="9e57b-113">QueueTransferProtocol</span><span class="sxs-lookup"><span data-stu-id="9e57b-113">QueueTransferProtocol</span></span>  
 <span data-ttu-id="9e57b-114">データ型: string</span><span class="sxs-lookup"><span data-stu-id="9e57b-114">Data type: string</span></span>  
  
 <span data-ttu-id="9e57b-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9e57b-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9e57b-116">このバインディングが使用するキューに置かれた通信チャネルのトランスポートを示す列挙値です。</span><span class="sxs-lookup"><span data-stu-id="9e57b-116">An enumeration value that indicates the queued communication channel transport that this binding uses.</span></span>  
  
### <a name="useactivedirectory"></a><span data-ttu-id="9e57b-117">UseActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="9e57b-117">UseActiveDirectory</span></span>  
 <span data-ttu-id="9e57b-118">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="9e57b-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="9e57b-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9e57b-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9e57b-120">キューのアドレスを Active Directory を使用して変換する必要があるかどうかを示すブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="9e57b-120">Returns a Boolean value that indicates whether queue addresses should be converted using Active Directory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9e57b-121">必要条件</span><span class="sxs-lookup"><span data-stu-id="9e57b-121">Requirements</span></span>  
  
|<span data-ttu-id="9e57b-122">MOF</span><span class="sxs-lookup"><span data-stu-id="9e57b-122">MOF</span></span>|<span data-ttu-id="9e57b-123">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="9e57b-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="9e57b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e57b-124">Namespace</span></span>|<span data-ttu-id="9e57b-125">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="9e57b-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9e57b-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="9e57b-126">See Also</span></span>  
 <xref:System.ServiceModel.Channels.MsmqTransportBindingElement>
