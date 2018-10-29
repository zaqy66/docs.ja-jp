---
title: HttpListener
ms.date: 03/30/2017
helpviewer_keywords:
- HTTP
ms.assetid: 5b89d3fb-3c9a-49e2-af1f-c34c020c68ac
ms.openlocfilehash: 902225085ccaceb9d90d0c25d9369ef65ae2730b
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50193111"
---
# <a name="httplistener"></a><span data-ttu-id="30384-102">HttpListener</span><span class="sxs-lookup"><span data-stu-id="30384-102">HttpListener</span></span>
<span data-ttu-id="30384-103"><xref:System.Net.HttpListener> クラスは、プログラムによって制御できる HTTP プロトコル リスナーを提供します。</span><span class="sxs-lookup"><span data-stu-id="30384-103">The <xref:System.Net.HttpListener> class provides a programmatically controlled HTTP protocol listener.</span></span> <span data-ttu-id="30384-104">リスナーは、<xref:System.Net.HttpListener> オブジェクトの有効期間にわたってアクティブで、アプリケーション内で実行されます。</span><span class="sxs-lookup"><span data-stu-id="30384-104">The listener is active for the lifetime of the <xref:System.Net.HttpListener> object and runs within your application.</span></span>  
  
## <a name="httpsys"></a><span data-ttu-id="30384-105">HTTP.SYS</span><span class="sxs-lookup"><span data-stu-id="30384-105">HTTP.SYS</span></span>  
 <span data-ttu-id="30384-106"><xref:System.Net.HttpListener> クラスは、Windows のすべての HTTP トラフィックを処理するカーネル モード リスナーである HTTP.sys の上に構築されています。</span><span class="sxs-lookup"><span data-stu-id="30384-106">The <xref:System.Net.HttpListener> class is built on top of HTTP.sys, which is the kernel mode listener that handles all HTTP traffic for Windows.</span></span> <span data-ttu-id="30384-107">HTTP.sys は、接続管理、帯域幅の調整、および Web サーバーのログ記録を提供します。</span><span class="sxs-lookup"><span data-stu-id="30384-107">HTTP.sys provides connection management, bandwidth throttling, and Web server logging.</span></span> <span data-ttu-id="30384-108">SSL 証明書の追加には `HttpCfg.exe` ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="30384-108">Use the `HttpCfg.exe` tool to add SSL certificates.</span></span> <span data-ttu-id="30384-109">詳細については、[サーバー](https://go.microsoft.com/fwlink/?LinkID=178285) ドキュメントで、[HttpCfg.exe](https://go.microsoft.com/fwlink/?LinkID=178284) ツールのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="30384-109">For more information, see the documentation on the [HttpCfg.exe](https://go.microsoft.com/fwlink/?LinkID=178284) tool in the [Server](https://go.microsoft.com/fwlink/?LinkID=178285) documentation.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30384-110">参照</span><span class="sxs-lookup"><span data-stu-id="30384-110">See Also</span></span>  
 <xref:System.Net.HttpListener>  
 <xref:System.Net.HttpWebRequest>  
 <xref:System.Net.HttpWebResponse>  
 [<span data-ttu-id="30384-111">HTTP サーバー</span><span class="sxs-lookup"><span data-stu-id="30384-111">HTTP Server</span></span>](https://go.microsoft.com/fwlink/?LinkID=178285)  
 [<span data-ttu-id="30384-112">インターネット インフォメーションにおけるセキュリティ強化</span><span class="sxs-lookup"><span data-stu-id="30384-112">Security Enhancements in Internet Information</span></span>](https://go.microsoft.com/fwlink/?LinkID=178286)  
 [<span data-ttu-id="30384-113">HttpListener ASPX ホスト アプリケーションのサンプル</span><span class="sxs-lookup"><span data-stu-id="30384-113">HttpListener ASPX Host Application Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=179560)  
 [<span data-ttu-id="30384-114">HttpListener テクノロジのサンプル</span><span class="sxs-lookup"><span data-stu-id="30384-114">HttpListener Technology Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=179558)  
 [<span data-ttu-id="30384-115">ネットワーク プログラミングのサンプル</span><span class="sxs-lookup"><span data-stu-id="30384-115">Network Programming Samples</span></span>](../../../docs/framework/network-programming/network-programming-samples.md)
