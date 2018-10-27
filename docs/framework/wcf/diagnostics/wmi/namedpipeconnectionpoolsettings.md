---
title: NamedPipeConnectionPoolSettings
ms.date: 03/30/2017
ms.assetid: 079bccb8-54b5-4436-a43d-5567763f72ce
ms.openlocfilehash: 77d8403947d341ea2efcef98bbf166f94f75f31f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188730"
---
# <a name="namedpipeconnectionpoolsettings"></a><span data-ttu-id="89174-102">NamedPipeConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="89174-102">NamedPipeConnectionPoolSettings</span></span>
<span data-ttu-id="89174-103">NamedPipeConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="89174-103">NamedPipeConnectionPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="89174-104">構文</span><span class="sxs-lookup"><span data-stu-id="89174-104">Syntax</span></span>  
  
```csharp
class NamedPipeConnectionPoolSettings  
{  
  string GroupName;  
  datetime IdleTimeout;  
  sint32 MaxOutboundConnectionsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="89174-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="89174-105">Methods</span></span>  
 <span data-ttu-id="89174-106">NamedPipeConnectionPoolSettings クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="89174-106">The NamedPipeConnectionPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="89174-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="89174-107">Properties</span></span>  
 <span data-ttu-id="89174-108">NamedPipeConnectionPoolSettings クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="89174-108">The NamedPipeConnectionPoolSettings class has the following properties:</span></span>  
  
### <a name="groupname"></a><span data-ttu-id="89174-109">GroupName</span><span class="sxs-lookup"><span data-stu-id="89174-109">GroupName</span></span>  
 <span data-ttu-id="89174-110">データ型: string</span><span class="sxs-lookup"><span data-stu-id="89174-110">Data type: string</span></span>  
  
 <span data-ttu-id="89174-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="89174-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="89174-112">バインド要素により使用される接続プールのグループ名。</span><span class="sxs-lookup"><span data-stu-id="89174-112">The group name of the connection pool used by the binding element.</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="89174-113">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="89174-113">IdleTimeout</span></span>  
 <span data-ttu-id="89174-114">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="89174-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="89174-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="89174-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="89174-116">接続が切断されるまでの最大アイドル時間。</span><span class="sxs-lookup"><span data-stu-id="89174-116">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="maxoutboundconnectionsperendpoint"></a><span data-ttu-id="89174-117">MaxOutboundConnectionsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="89174-117">MaxOutboundConnectionsPerEndpoint</span></span>  
 <span data-ttu-id="89174-118">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="89174-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="89174-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="89174-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="89174-120">クライアント上の各エンドポイントでの発信接続の最大数。</span><span class="sxs-lookup"><span data-stu-id="89174-120">The maximum number of outbound connections for each endpoint on the client.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="89174-121">必要条件</span><span class="sxs-lookup"><span data-stu-id="89174-121">Requirements</span></span>  
  
|<span data-ttu-id="89174-122">MOF</span><span class="sxs-lookup"><span data-stu-id="89174-122">MOF</span></span>|<span data-ttu-id="89174-123">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="89174-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="89174-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="89174-124">Namespace</span></span>|<span data-ttu-id="89174-125">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="89174-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="89174-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="89174-126">See Also</span></span>  
 <xref:System.ServiceModel.Channels.NamedPipeConnectionPoolSettings>
