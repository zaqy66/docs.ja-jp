---
title: TcpTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 33bbc1e5-44e4-4ee3-b7b5-801dc78956e4
ms.openlocfilehash: 04326484bbf1f07c66ad8fb401642880f9ba8c6e
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/26/2018
ms.locfileid: "50033715"
---
# <a name="tcptransportbindingelement"></a><span data-ttu-id="266de-102">TcpTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="266de-102">TcpTransportBindingElement</span></span>
<span data-ttu-id="266de-103">TcpTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="266de-103">TcpTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="266de-104">構文</span><span class="sxs-lookup"><span data-stu-id="266de-104">Syntax</span></span>  
  
```csharp
class TcpTransportBindingElement : ConnectionOrientedTransportBindingElement  
{  
  TcpConnectionPoolSettings ConnectionPoolSettings;  
  sint32 ListenBacklog;  
  boolean PortSharingEnabled;  
  boolean TeredoEnabled;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="266de-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="266de-105">Methods</span></span>  
 <span data-ttu-id="266de-106">TcpTransportBindingElement クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="266de-106">The TcpTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="266de-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="266de-107">Properties</span></span>  
 <span data-ttu-id="266de-108">TcpTransportBindingElement クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="266de-108">The TcpTransportBindingElement class has the following properties:</span></span>  
  
### <a name="connectionpoolsettings"></a><span data-ttu-id="266de-109">ConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="266de-109">ConnectionPoolSettings</span></span>  
 <span data-ttu-id="266de-110">データ型 : TcpConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="266de-110">Data type: TcpConnectionPoolSettings</span></span>  
  
 <span data-ttu-id="266de-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="266de-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="266de-112">接続プールの設定。</span><span class="sxs-lookup"><span data-stu-id="266de-112">The connection pool settings.</span></span>  
  
### <a name="listenbacklog"></a><span data-ttu-id="266de-113">ListenBacklog</span><span class="sxs-lookup"><span data-stu-id="266de-113">ListenBacklog</span></span>  
 <span data-ttu-id="266de-114">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="266de-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="266de-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="266de-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="266de-116">保留可能なキュー内の接続要求の最大数です。</span><span class="sxs-lookup"><span data-stu-id="266de-116">The maximum number of queued connection requests that can be pending.</span></span>  
  
### <a name="portsharingenabled"></a><span data-ttu-id="266de-117">PortSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="266de-117">PortSharingEnabled</span></span>  
 <span data-ttu-id="266de-118">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="266de-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="266de-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="266de-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="266de-120">TCP ポート共有をこの接続で有効にするかどうかを指定するブール値です。</span><span class="sxs-lookup"><span data-stu-id="266de-120">A boolean value that specifies whether TCP port sharing is enabled for this connection.</span></span>  
  
### <a name="teredoenabled"></a><span data-ttu-id="266de-121">TeredoEnabled</span><span class="sxs-lookup"><span data-stu-id="266de-121">TeredoEnabled</span></span>  
 <span data-ttu-id="266de-122">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="266de-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="266de-123">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="266de-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="266de-124">Teredo (ファイアウォールの内側にあるクライアントをアドレス指定するためのテクノロジ) を有効にするかどうかを指定するブール値です。</span><span class="sxs-lookup"><span data-stu-id="266de-124">A boolean value that specifies whether Teredo (a technology for addressing clients that are behind firewalls) is enabled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="266de-125">必要条件</span><span class="sxs-lookup"><span data-stu-id="266de-125">Requirements</span></span>  
  
|<span data-ttu-id="266de-126">MOF</span><span class="sxs-lookup"><span data-stu-id="266de-126">MOF</span></span>|<span data-ttu-id="266de-127">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="266de-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="266de-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="266de-128">Namespace</span></span>|<span data-ttu-id="266de-129">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="266de-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="266de-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="266de-130">See Also</span></span>  
 <xref:System.ServiceModel.Channels.TcpTransportBindingElement>
