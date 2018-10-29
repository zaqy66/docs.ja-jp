---
title: ソケットのコード例
ms.date: 03/30/2017
helpviewer_keywords:
- application protocols, sockets
- sending data, sockets
- Socket class, asynchronous server sockets
- data requests, sockets
- requesting data from Internet, sockets
- server sockets
- sockets, code examples
- receiving data, sockets
- protocols, sockets
- Internet, sockets
- client sockets
ms.assetid: f3fc7533-6956-42c6-bbc3-73e5a221027d
ms.openlocfilehash: f709c2e0780b89e072c43e9acaf722e6851d4cbe
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50199956"
---
# <a name="socket-code-examples"></a><span data-ttu-id="81511-102">ソケットのコード例</span><span class="sxs-lookup"><span data-stu-id="81511-102">Socket Code Examples</span></span>
<span data-ttu-id="81511-103">次のコード例は、リモート ネットワーク サービスに接続するためのクライアントとして、また、リモート クライアントからの接続を待ち受けるためのサーバーとして <xref:System.Net.Sockets.Socket> クラスを利用する方法を示すものです。</span><span class="sxs-lookup"><span data-stu-id="81511-103">The following code examples demonstrate how to use the <xref:System.Net.Sockets.Socket> class as a client to connect to remote network services and as a server to listen for connections from remote clients.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="81511-104">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="81511-104">In This Section</span></span>  
 [<span data-ttu-id="81511-105">同期クライアント ソケットの例</span><span class="sxs-lookup"><span data-stu-id="81511-105">Synchronous Client Socket Example</span></span>](../../../docs/framework/network-programming/synchronous-client-socket-example.md)  
 <span data-ttu-id="81511-106">サーバーに接続し、サーバーから返されたデータを表示する同期 <xref:System.Net.Sockets.Socket> クライアントを実装する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="81511-106">Shows how to implement a synchronous <xref:System.Net.Sockets.Socket> client that connects to a server and displays the data returned from the server.</span></span>  
  
 [<span data-ttu-id="81511-107">同期サーバー ソケットの例</span><span class="sxs-lookup"><span data-stu-id="81511-107">Synchronous Server Socket Example</span></span>](../../../docs/framework/network-programming/synchronous-server-socket-example.md)  
 <span data-ttu-id="81511-108">クライアントからの接続を受け付け、クライアントから受け取ったデータをエコー バックする同期 <xref:System.Net.Sockets.Socket> サーバーを実装する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="81511-108">Shows how to implement a synchronous <xref:System.Net.Sockets.Socket> server that accepts connections from a client and echoes back the data received from the client.</span></span>  
  
 [<span data-ttu-id="81511-109">非同期クライアント ソケットの例</span><span class="sxs-lookup"><span data-stu-id="81511-109">Asynchronous Client Socket Example</span></span>](../../../docs/framework/network-programming/asynchronous-client-socket-example.md)  
 <span data-ttu-id="81511-110">サーバーに接続し、サーバーから返されたデータを表示する非同期 <xref:System.Net.Sockets.Socket> クライアントを実装する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="81511-110">Shows how to implement an asynchronous <xref:System.Net.Sockets.Socket> client that connects to a server and displays the data returned from the server.</span></span>  
  
 [<span data-ttu-id="81511-111">非同期サーバー ソケットの例</span><span class="sxs-lookup"><span data-stu-id="81511-111">Asynchronous Server Socket Example</span></span>](../../../docs/framework/network-programming/asynchronous-server-socket-example.md)  
 <span data-ttu-id="81511-112">クライアントからの接続を受け付け、クライアントから受け取ったデータをエコー バックする非同期 <xref:System.Net.Sockets.Socket> サーバーを実装する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="81511-112">Shows how to implement an asynchronous <xref:System.Net.Sockets.Socket> server that accepts connections from a client and echoes back the data received from the client.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="81511-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="81511-113">Related Sections</span></span>  
 [<span data-ttu-id="81511-114">ソケット</span><span class="sxs-lookup"><span data-stu-id="81511-114">Sockets</span></span>](../../../docs/framework/network-programming/sockets.md)  
 <span data-ttu-id="81511-115"><xref:System.Net.Sockets> 名前空間と <xref:System.Net.Sockets.Socket> クラスに関する基本情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="81511-115">Provides basic information about the <xref:System.Net.Sockets> namespace and the <xref:System.Net.Sockets.Socket> class.</span></span>  
  
 [<span data-ttu-id="81511-116">ネットワーク プログラミングにおけるセキュリティ</span><span class="sxs-lookup"><span data-stu-id="81511-116">Security in Network Programming</span></span>](../../../docs/framework/network-programming/security-in-network-programming.md)  
 <span data-ttu-id="81511-117">標準のインターネット セキュリティと認証の手法を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="81511-117">Describes how to use standard Internet security and authentication techniques.</span></span>
