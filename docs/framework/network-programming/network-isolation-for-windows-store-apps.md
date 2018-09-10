---
title: Windows ストア アプリのネットワーク分離
ms.date: 03/30/2017
ms.assetid: b064497c-d956-46b8-838d-7a0223c7e200
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 4d26b6df5d26a96bb8fa41dd3a8151fcb4a08b75
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43773658"
---
# <a name="network-isolation-for-windows-store-apps"></a><span data-ttu-id="51421-102">Windows ストア アプリのネットワーク分離</span><span class="sxs-lookup"><span data-stu-id="51421-102">Network Isolation for Windows Store Apps</span></span>
<span data-ttu-id="51421-103"><xref:System.Net>、<xref:System.Net.Http>、<xref:System.Net.Http.Headers> の各名前空間のクラスは、Windows ストア アプリまたはデスクトップ アプリを開発するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="51421-103">Classes in the <xref:System.Net>,  <xref:System.Net.Http>, and <xref:System.Net.Http.Headers> namespaces can be used to develop Windows Store  apps  or desktop apps.</span></span> <span data-ttu-id="51421-104">Windows ストア アプリで使用する場合、これらの名前空間のクラスは、[!INCLUDE[win8](../../../includes/win8-md.md)]で使用されるアプリケーション セキュリティ モデルの一部であるネットワーク分離の影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="51421-104">When used in a Windows Store app, classes in these namespaces are affected by network isolation, part of the application security model used by the [!INCLUDE[win8](../../../includes/win8-md.md)].</span></span> <span data-ttu-id="51421-105">システムでネットワーク アクセスが許可されるように、Windows ストア アプリのアプリ マニフェストで適切なネットワーク機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="51421-105">The appropriate network capabilities must be enabled in the app manifest for a Windows Store app for the system to allow network access.</span></span>  
  
## <a name="checklist-for-network-isolation"></a><span data-ttu-id="51421-106">ネットワーク分離のチェックリスト</span><span class="sxs-lookup"><span data-stu-id="51421-106">Checklist for Network Isolation</span></span>  
 <span data-ttu-id="51421-107">Windows ストア アプリに対してネットワークの分離が適切に構成されているかどうかを、このチェックリストを使って確認してください。</span><span class="sxs-lookup"><span data-stu-id="51421-107">Use this checklist to be sure that network isolation is configured for your Windows Store app.</span></span>  
  
1.  <span data-ttu-id="51421-108">アプリが必要とするネットワーク アクセス要求の方向を確認します。</span><span class="sxs-lookup"><span data-stu-id="51421-108">Determine the direction of network access requests needed by the app.</span></span> <span data-ttu-id="51421-109">これには、クライアント側から開始される送信要求と、受信側が送信を要求していない受信要求とがあります。両方の種類のネットワーク要求を組み合わせたものもあります。</span><span class="sxs-lookup"><span data-stu-id="51421-109">This can be either outbound client-initiated requests or inbound unsolicited requests or it could be a combination of both of these network request types.</span></span>  
  
2.  <span data-ttu-id="51421-110">アプリの通信相手となるネットワーク リソースの種類を確認します。</span><span class="sxs-lookup"><span data-stu-id="51421-110">Determine the type of network resources that that app will communicate with.</span></span> <span data-ttu-id="51421-111">アプリの通信相手は、ホーム ネットワークまたは職場ネットワーク上の信頼済みリソースである場合があります。</span><span class="sxs-lookup"><span data-stu-id="51421-111">An app may need to communicate with trusted resources on a Home or Work network.</span></span> <span data-ttu-id="51421-112">または、インターネット上のリソースと通信することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="51421-112">An app might need to communicate with resources on the Internet.</span></span> <span data-ttu-id="51421-113">その両方の種類のネットワーク リソースにアクセスする場合もあります。</span><span class="sxs-lookup"><span data-stu-id="51421-113">An app might need access to both types of network resources.</span></span>  
  
3.  <span data-ttu-id="51421-114">アプリ マニフェストで、必要最小限のネットワーク分離機能を構成します。</span><span class="sxs-lookup"><span data-stu-id="51421-114">Configure the minimum-required networking isolation capabilities in the app manifest.</span></span>  
  
4.  <span data-ttu-id="51421-115">アプリを展開して実行し、トラブルシューティングのためのネットワーク分離ツールを使用してテストします。</span><span class="sxs-lookup"><span data-stu-id="51421-115">Deploy and run your app to test it using the network isolation tools provided for troubleshooting.</span></span>  
  
 <span data-ttu-id="51421-116">ネットワーク機能の構成と、ネットワーク分離のトラブルシューティングに使用する分離ツールの詳細については、[!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] 開発者向けドキュメントで、[ネットワーク分離の機能を構成する方法](https://go.microsoft.com/fwlink/?LinkID=228265)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="51421-116">For more detailed information on how to configure network capabilities and isolation tools used for troubleshooting network isolation, see [How to configure network isolation capabilities](https://go.microsoft.com/fwlink/?LinkID=228265) in the [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] developer documentation.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51421-117">参照</span><span class="sxs-lookup"><span data-stu-id="51421-117">See Also</span></span>  
 [<span data-ttu-id="51421-118">Web サービスへの接続</span><span class="sxs-lookup"><span data-stu-id="51421-118">Connecting to a web service</span></span>](https://go.microsoft.com/fwlink/?LinkID=245696)  
 [<span data-ttu-id="51421-119">ネットワーク分離のガイドラインとチェックリスト</span><span class="sxs-lookup"><span data-stu-id="51421-119">Guidelines and checklist for network isolation</span></span>](https://go.microsoft.com/fwlink/?LinkID=228265)  
 [<span data-ttu-id="51421-120">クイック スタート: HttpClient を使って接続する</span><span class="sxs-lookup"><span data-stu-id="51421-120">Quickstart: Connecting using HttpClient</span></span>](https://go.microsoft.com/fwlink/?LinkId=245697)  
 [<span data-ttu-id="51421-121">HttpClient ハンドラーを使う方法</span><span class="sxs-lookup"><span data-stu-id="51421-121">How to use HttpClient handlers</span></span>](https://go.microsoft.com/fwlink/?LinkId=245699)  
 [<span data-ttu-id="51421-122">HttpClient の接続をセキュリティで保護する方法</span><span class="sxs-lookup"><span data-stu-id="51421-122">How to secure HttpClient connections</span></span>](https://go.microsoft.com/fwlink/?LinkId=245698)  
 [<span data-ttu-id="51421-123">HttpClient のサンプル</span><span class="sxs-lookup"><span data-stu-id="51421-123">HttpClient Sample</span></span>](https://go.microsoft.com/fwlink/?LinkId=242550)
