---
title: サービスの配置
ms.date: 03/30/2017
ms.assetid: ac361bfb-017d-4da9-a2d7-fc0fb72d65bb
ms.openlocfilehash: 17773dc7a6bbed1b88c9324d27a937166e0d9f6b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54678981"
---
# <a name="deploying-services"></a><span data-ttu-id="adace-102">サービスの配置</span><span class="sxs-lookup"><span data-stu-id="adace-102">Deploying Services</span></span>
<span data-ttu-id="adace-103">このトピックでは、実行時環境に Windows Communication Foundation (WCF) アプリケーションをデプロイする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="adace-103">This topic describes how you can deploy a Windows Communication Foundation (WCF) application to a run-time environment.</span></span>  
  
## <a name="choosing-the-hosting-environment-for-your-application"></a><span data-ttu-id="adace-104">アプリケーションのホスト環境の選択</span><span class="sxs-lookup"><span data-stu-id="adace-104">Choosing the Hosting Environment for Your Application</span></span>  
 <span data-ttu-id="adace-105">マネージ コードをサポートする任意の Windows プロセスで実行するのには、WCF サービスが設計されています。</span><span class="sxs-lookup"><span data-stu-id="adace-105">WCF services are designed to run in any Windows process that supports managed code.</span></span> <span data-ttu-id="adace-106">アクティブにするには、サービスを作成してそのコンテキストと有効期間を制御するランタイム環境内で、サービスをホストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="adace-106">To become active, a service must be hosted within a run-time environment that creates it and controls its context and lifetime.</span></span> <span data-ttu-id="adace-107">ホスティング環境の範囲は、最も単純なコンソール アプリケーション内、Windows サービスやインターネット インフォメーション サービス (IIS) のようなサーバー環境、あるいは Windows アクティブ化サービス (WAS) で管理されるワーカー プロセス内での実行にまで及びます。</span><span class="sxs-lookup"><span data-stu-id="adace-107">Hosting options range from running inside the simplest console application to server environments like a Windows service, Internet Information Services (IIS), or within a worker process managed by the Windows Activation Service (WAS).</span></span> <span data-ttu-id="adace-108">WCF アプリケーションのさまざまなホスティング オプションを確認するを参照してください。[ホスティング サービス](../../../../docs/framework/wcf/hosting-services.md)します。</span><span class="sxs-lookup"><span data-stu-id="adace-108">To review the different hosting options for your WCF application, see [Hosting Services](../../../../docs/framework/wcf/hosting-services.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="adace-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="adace-109">See also</span></span>
- [<span data-ttu-id="adace-110">ホスティング</span><span class="sxs-lookup"><span data-stu-id="adace-110">Hosting</span></span>](../../../../docs/framework/wcf/feature-details/hosting.md)
- [<span data-ttu-id="adace-111">ホスティング サービス</span><span class="sxs-lookup"><span data-stu-id="adace-111">Hosting Services</span></span>](../../../../docs/framework/wcf/hosting-services.md)
