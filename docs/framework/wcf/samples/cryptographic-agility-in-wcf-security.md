---
title: WCF セキュリティの暗号化方式の指定
ms.date: 03/30/2017
ms.assetid: c2c549e5-ac19-40c5-b686-8f67f52b6dbf
ms.openlocfilehash: a97f0b908d3c4d2e14fb55ec21371322dc740e47
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54668900"
---
# <a name="cryptographic-agility-in-wcf-security"></a><span data-ttu-id="c741b-102">WCF セキュリティの暗号化方式の指定</span><span class="sxs-lookup"><span data-stu-id="c741b-102">Cryptographic Agility in WCF Security</span></span>
<span data-ttu-id="c741b-103">このサンプルでは、Windows Communication Foundation (WCF) クライアントとサービスで迅速な暗号化の実装を提供する標準またはカスタム アルゴリズムで指定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c741b-103">This sample shows how to specify in a standard/custom algorithm to provide a cryptographic agile implementation in a Windows Communication Foundation (WCF) client and service.</span></span> <span data-ttu-id="c741b-104">サンプルは、以下のプロジェクトで構成されます。</span><span class="sxs-lookup"><span data-stu-id="c741b-104">The sample is composed of the following projects:</span></span>

 <span data-ttu-id="c741b-105">これは、自己ホスト型 WCF サービスを実装するサービス、`ICalculator`インターフェイスを使用してエンドポイントを保護し、<<!--zz xref:System.ServiceModel.WsHttpBinding --> `xref:System.ServiceModel.WsHttpBinding`> セキュリティで保護されたセッションと信頼できるセッションは無効にします。</span><span class="sxs-lookup"><span data-stu-id="c741b-105">Service This is a self-hosted WCF service that implements the `ICalculator` interface and secures the endpoint using the <<!--zz xref:System.ServiceModel.WsHttpBinding --> `xref:System.ServiceModel.WsHttpBinding`> with secure session and reliable session disabled.</span></span> <span data-ttu-id="c741b-106">このサービスは、カスタム `SecurityAlgorithmSuite` クラスを定義し、メッセージのセキュリティを確保するために使用される暗号化アルゴリズムを指定します。</span><span class="sxs-lookup"><span data-stu-id="c741b-106">The service defines a custom `SecurityAlgorithmSuite` class to specify the cryptographic algorithms to be used for message security.</span></span>

 <span data-ttu-id="c741b-107">クライアント認証が成功した後にサービスにアクセスする WCFclient になります。</span><span class="sxs-lookup"><span data-stu-id="c741b-107">Client This is a WCFclient that accesses the service after successful authentication.</span></span> <span data-ttu-id="c741b-108">このクライアントは、`ICalculator` インターフェイスによって公開され、サービスによって実装される操作を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c741b-108">It invokes the operations exposed by the `ICalculator` interface and implemented by the service.</span></span> <span data-ttu-id="c741b-109">このクライアントも、同じカスタム `SecurityAlgorithmSuite` クラスを定義し、メッセージのセキュリティを確保するために使用される暗号化アルゴリズムを指定します。</span><span class="sxs-lookup"><span data-stu-id="c741b-109">The client also defines the same custom `SecurityAlgorithmSuite` class to specify the cryptographic algorithms to be used for message security.</span></span>

### <a name="to-use-this-sample"></a><span data-ttu-id="c741b-110">このサンプルを使用するには</span><span class="sxs-lookup"><span data-stu-id="c741b-110">To use this sample</span></span>

1.  <span data-ttu-id="c741b-111">Visual Studio 2012 で CryptoAgility.sln ソリューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="c741b-111">Open the CryptoAgility.sln solution in Visual Studio 2012.</span></span>

2.  <span data-ttu-id="c741b-112">Ctrl キーと Shift キーを押しながら B キーを押して、ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="c741b-112">Press CTRL+SHIFT+B to build the solution.</span></span>

3.  <span data-ttu-id="c741b-113">開いている[!INCLUDE[fileExplorer](../../../../includes/fileexplorer-md.md)]\WCF\Basic\Security\CryptoAgility\Service\bin ディレクトリに移動し、service.exe を右クリックして、service.exe ファイルを管理者特権で実行**管理者として実行**します。</span><span class="sxs-lookup"><span data-stu-id="c741b-113">Open [!INCLUDE[fileExplorer](../../../../includes/fileexplorer-md.md)] and navigate to the \WCF\Basic\Security\CryptoAgility\Service\bin directory and run the service.exe file with administrator privileges by right-clicking service.exe and selecting **Run as administrator**.</span></span>

4.  <span data-ttu-id="c741b-114">\WCF\Basic\Security\CryptoAgility\Client\bin ディレクトリに移動して、client.exe ファイルを通常の方法で実行します。</span><span class="sxs-lookup"><span data-stu-id="c741b-114">Navigate to \WCF\Basic\Security\CryptoAgility\Client\bin directory and run the client.exe file normally.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="c741b-115">サンプルは、既にコンピューターにインストールされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="c741b-115">The samples may already be installed on your machine.</span></span> <span data-ttu-id="c741b-116">続行する前に、次の (既定の) ディレクトリを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c741b-116">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="c741b-117">このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。</span><span class="sxs-lookup"><span data-stu-id="c741b-117">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="c741b-118">このサンプルは、次のディレクトリに格納されます。</span><span class="sxs-lookup"><span data-stu-id="c741b-118">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Security\CryptoAgility`  
  
## <a name="see-also"></a><span data-ttu-id="c741b-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="c741b-119">See also</span></span>
- [<span data-ttu-id="c741b-120">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="c741b-120">Security</span></span>](../../../../docs/framework/wcf/feature-details/security.md)
