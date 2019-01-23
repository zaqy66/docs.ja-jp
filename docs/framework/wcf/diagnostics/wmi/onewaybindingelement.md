---
title: OneWayBindingElement
ms.date: 03/30/2017
ms.assetid: 5c7e17c3-39b9-4214-ae08-9e6141734305
ms.openlocfilehash: d84184febd6db3f233aae6fe558b8e0f50a9cb82
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54608837"
---
# <a name="onewaybindingelement"></a><span data-ttu-id="f1931-102">OneWayBindingElement</span><span class="sxs-lookup"><span data-stu-id="f1931-102">OneWayBindingElement</span></span>
<span data-ttu-id="f1931-103">OneWayBindingElement</span><span class="sxs-lookup"><span data-stu-id="f1931-103">OneWayBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f1931-104">構文</span><span class="sxs-lookup"><span data-stu-id="f1931-104">Syntax</span></span>  
  
```csharp
class OneWayBindingElement : BindingElement  
{  
  ChannelPoolSettings ChannelPoolSettings;  
  sint32 MaxAcceptedChannels;  
  boolean PacketRoutable;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="f1931-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="f1931-105">Methods</span></span>  
 <span data-ttu-id="f1931-106">OneWayBindingElement クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="f1931-106">The OneWayBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="f1931-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f1931-107">Properties</span></span>  
 <span data-ttu-id="f1931-108">OneWayBindingElement クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="f1931-108">The OneWayBindingElement class has the following properties:</span></span>  
  
### <a name="channelpoolsettings"></a><span data-ttu-id="f1931-109">ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="f1931-109">ChannelPoolSettings</span></span>  
 <span data-ttu-id="f1931-110">データの種類:ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="f1931-110">Data type: ChannelPoolSettings</span></span>  
  
 <span data-ttu-id="f1931-111">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="f1931-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f1931-112">チャネル プールの設定。</span><span class="sxs-lookup"><span data-stu-id="f1931-112">The channel pool settings.</span></span>  
  
### <a name="maxacceptedchannels"></a><span data-ttu-id="f1931-113">MaxAcceptedChannels</span><span class="sxs-lookup"><span data-stu-id="f1931-113">MaxAcceptedChannels</span></span>  
 <span data-ttu-id="f1931-114">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="f1931-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="f1931-115">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="f1931-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f1931-116">許可されるチャネルの最大数。</span><span class="sxs-lookup"><span data-stu-id="f1931-116">The maximum number of accepted channels.</span></span>  
  
### <a name="packetroutable"></a><span data-ttu-id="f1931-117">PacketRoutable</span><span class="sxs-lookup"><span data-stu-id="f1931-117">PacketRoutable</span></span>  
 <span data-ttu-id="f1931-118">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="f1931-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="f1931-119">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="f1931-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f1931-120">パケットがルーティング可能かどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="f1931-120">A value that indicates whether the packet is routable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f1931-121">必要条件</span><span class="sxs-lookup"><span data-stu-id="f1931-121">Requirements</span></span>  
  
|<span data-ttu-id="f1931-122">MOF</span><span class="sxs-lookup"><span data-stu-id="f1931-122">MOF</span></span>|<span data-ttu-id="f1931-123">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="f1931-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="f1931-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1931-124">Namespace</span></span>|<span data-ttu-id="f1931-125">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="f1931-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f1931-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1931-126">See also</span></span>
- <xref:System.ServiceModel.Channels.OneWayBindingElement>
