---
title: NamedPipeConnectionPoolSettings
ms.date: 03/30/2017
ms.assetid: 079bccb8-54b5-4436-a43d-5567763f72ce
ms.openlocfilehash: 3dddfa878e3cb5bd89fb76009d0dba530debb297
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54725078"
---
# <a name="namedpipeconnectionpoolsettings"></a><span data-ttu-id="0c0c4-102">NamedPipeConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="0c0c4-102">NamedPipeConnectionPoolSettings</span></span>
<span data-ttu-id="0c0c4-103">NamedPipeConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="0c0c4-103">NamedPipeConnectionPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c0c4-104">構文</span><span class="sxs-lookup"><span data-stu-id="0c0c4-104">Syntax</span></span>  
  
```csharp
class NamedPipeConnectionPoolSettings  
{  
  string GroupName;  
  datetime IdleTimeout;  
  sint32 MaxOutboundConnectionsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="0c0c4-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="0c0c4-105">Methods</span></span>  
 <span data-ttu-id="0c0c4-106">NamedPipeConnectionPoolSettings クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="0c0c4-106">The NamedPipeConnectionPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="0c0c4-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c0c4-107">Properties</span></span>  
 <span data-ttu-id="0c0c4-108">NamedPipeConnectionPoolSettings クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="0c0c4-108">The NamedPipeConnectionPoolSettings class has the following properties:</span></span>  
  
### <a name="groupname"></a><span data-ttu-id="0c0c4-109">GroupName</span><span class="sxs-lookup"><span data-stu-id="0c0c4-109">GroupName</span></span>  
 <span data-ttu-id="0c0c4-110">データ型: string</span><span class="sxs-lookup"><span data-stu-id="0c0c4-110">Data type: string</span></span>  
  
 <span data-ttu-id="0c0c4-111">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="0c0c4-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0c0c4-112">バインド要素により使用される接続プールのグループ名。</span><span class="sxs-lookup"><span data-stu-id="0c0c4-112">The group name of the connection pool used by the binding element.</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="0c0c4-113">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="0c0c4-113">IdleTimeout</span></span>  
 <span data-ttu-id="0c0c4-114">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="0c0c4-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="0c0c4-115">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="0c0c4-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0c0c4-116">接続が切断されるまでの最大アイドル時間。</span><span class="sxs-lookup"><span data-stu-id="0c0c4-116">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="maxoutboundconnectionsperendpoint"></a><span data-ttu-id="0c0c4-117">MaxOutboundConnectionsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c0c4-117">MaxOutboundConnectionsPerEndpoint</span></span>  
 <span data-ttu-id="0c0c4-118">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="0c0c4-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="0c0c4-119">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="0c0c4-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0c0c4-120">クライアント上の各エンドポイントでの発信接続の最大数。</span><span class="sxs-lookup"><span data-stu-id="0c0c4-120">The maximum number of outbound connections for each endpoint on the client.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c0c4-121">必要条件</span><span class="sxs-lookup"><span data-stu-id="0c0c4-121">Requirements</span></span>  
  
|<span data-ttu-id="0c0c4-122">MOF</span><span class="sxs-lookup"><span data-stu-id="0c0c4-122">MOF</span></span>|<span data-ttu-id="0c0c4-123">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="0c0c4-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="0c0c4-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c0c4-124">Namespace</span></span>|<span data-ttu-id="0c0c4-125">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="0c0c4-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0c0c4-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c0c4-126">See also</span></span>
- <xref:System.ServiceModel.Channels.NamedPipeConnectionPoolSettings>
