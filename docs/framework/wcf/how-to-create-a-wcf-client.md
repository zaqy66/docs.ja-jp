---
title: '方法 : Windows Communication Foundation クライアントを作成する'
ms.date: 09/14/2018
helpviewer_keywords:
- clients [WCF], running
- WCF clients [WCF], running
ms.assetid: a67884cc-1c4b-416b-8c96-5c954099f19f
ms.openlocfilehash: 9572f3e2c0cddf75daf343f250b16e94bc2b0dbf
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50181671"
---
# <a name="how-to-create-a-windows-communication-foundation-client"></a><span data-ttu-id="bee12-102">方法 : Windows Communication Foundation クライアントを作成する</span><span class="sxs-lookup"><span data-stu-id="bee12-102">How to: Create a Windows Communication Foundation Client</span></span>

<span data-ttu-id="bee12-103">これは、4 番目の Windows Communication Foundation (WCF) アプリケーションを作成するために必要な 6 つのタスクです。</span><span class="sxs-lookup"><span data-stu-id="bee12-103">This is the fourth of six tasks required to create a Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="bee12-104">6 つのすべてのタスクの概要については、「[チュートリアル入門](../../../docs/framework/wcf/getting-started-tutorial.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bee12-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) topic.</span></span>

<span data-ttu-id="bee12-105">このトピックでは、WCF サービスからメタデータを取得し、使用して、サービスにアクセスできる WCF プロキシを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bee12-105">This topic describes how to retrieve metadata from a WCF service and use it to create a WCF proxy that can access the service.</span></span> <span data-ttu-id="bee12-106">このタスクを使用して、**サービス参照の追加**Visual Studio によって提供される機能です。</span><span class="sxs-lookup"><span data-stu-id="bee12-106">This task is completed by using the **Add Service Reference** functionality provided by Visual Studio.</span></span> <span data-ttu-id="bee12-107">このツールでは、サービスの MEX エンドポイントからメタデータを取得し、選択した言語 (既定では C#) でクライアント プロキシのマネージド ソース コード ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="bee12-107">This tool obtains the metadata from the service’s MEX endpoint and generates a managed source code file for a client proxy in the language you have chosen (C# by default).</span></span> <span data-ttu-id="bee12-108">このツールでは、クライアント プロキシを作成する以外に、クライアントの構成ファイルの作成または更新も行います。この構成ファイルにより、クライアント アプリケーションはエンドポイントのいずれかにあるサービスに接続できるようになります。</span><span class="sxs-lookup"><span data-stu-id="bee12-108">In addition to creating the client proxy, the tool also creates or updates the client configuration file which enables the client application to connect to the service at one of its endpoints.</span></span>

> [!NOTE]
> <span data-ttu-id="bee12-109">使用することも、 [ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)プロキシ クラスおよび使用する代わりに構成を生成するツール**サービス参照の追加**Visual Studio でします。</span><span class="sxs-lookup"><span data-stu-id="bee12-109">You can also use the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) tool to generate the proxy class and configuration instead of using **Add Service Reference** in Visual Studio.</span></span>

> [!NOTE]
> <span data-ttu-id="bee12-110">Visual Studio でクラス ライブラリ プロジェクトから WCF サービスを呼び出すときに使用できます、**サービス参照の追加**プロキシと関連付けられている構成ファイルを自動的に生成する機能。</span><span class="sxs-lookup"><span data-stu-id="bee12-110">When calling a WCF service from a class library project in Visual Studio, you can use the **Add Service Reference** feature to automatically generate a proxy and associated configuration file.</span></span> <span data-ttu-id="bee12-111">この構成ファイルはクラス ライブラリ プロジェクトで使用されません。</span><span class="sxs-lookup"><span data-stu-id="bee12-111">The configuration file will not be used by the class library project.</span></span> <span data-ttu-id="bee12-112">クラス ライブラリを呼び出す実行可能ファイルの app.config ファイルに生成された構成ファイルで設定を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bee12-112">You need to add the settings in the generated configuration file to the app.config file for the executable that calls the class library.</span></span>

<span data-ttu-id="bee12-113">クライアント アプリケーションは、生成されたプロキシ クラスを使用してサービスと通信します。</span><span class="sxs-lookup"><span data-stu-id="bee12-113">The client application uses the generated proxy class to communicate with the service.</span></span> <span data-ttu-id="bee12-114">この手順で説明されて[方法: クライアントを使用して](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)します。</span><span class="sxs-lookup"><span data-stu-id="bee12-114">This procedure is described in [How to: Use a Client](../../../docs/framework/wcf/how-to-use-a-wcf-client.md).</span></span>

## <a name="to-create-a-windows-communication-foundation-client"></a><span data-ttu-id="bee12-115">Windows Communication Foundation クライアントを作成するには</span><span class="sxs-lookup"><span data-stu-id="bee12-115">To create a Windows Communication Foundation client</span></span>

1. <span data-ttu-id="bee12-116">Visual Studio で新しいコンソール アプリケーション プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="bee12-116">Create a new console application project in Visual Studio.</span></span> <span data-ttu-id="bee12-117">入門ソリューションを右クリックして**ソリューション エクスプ ローラー**選択**追加** > **新しいプロジェクト**します。</span><span class="sxs-lookup"><span data-stu-id="bee12-117">Right-click on the Getting Started solution in **Solution Explorer** and select **Add** > **New Project**.</span></span> <span data-ttu-id="bee12-118">**新しいプロジェクトの追加**ダイアログ ボックスで、左側にある、選択、 **Windows デスクトップ**カテゴリ  **Visual c#** または**Visual Basic**します。</span><span class="sxs-lookup"><span data-stu-id="bee12-118">In the **Add New Project** dialog, on the left-hand side, select the **Windows Desktop** category under **Visual C#** or **Visual Basic**.</span></span> <span data-ttu-id="bee12-119">選択、**コンソール アプリ (.NET Framework)** テンプレート、および、プロジェクトの名前を**GettingStartedClient**します。</span><span class="sxs-lookup"><span data-stu-id="bee12-119">Select the **Console App (.NET Framework)** template, and then name the project **GettingStartedClient**.</span></span>

2. <span data-ttu-id="bee12-120">System.ServiceModel への参照を GettingStartedClient プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="bee12-120">Add a reference to System.ServiceModel to the GettingStartedClient project.</span></span> <span data-ttu-id="bee12-121">右クリックし、**参照**で GettingStartedClient プロジェクトの下のフォルダー**ソリューション エクスプ ローラー**、し、**参照の追加**します。</span><span class="sxs-lookup"><span data-stu-id="bee12-121">Right-click on the **References** folder under the GettingStartedClient project in **Solution Explorer**, and then select **Add Reference**.</span></span> <span data-ttu-id="bee12-122">**参照の追加**ダイアログ ボックスで、 **Framework**ダイアログ ボックスの左側にある**アセンブリ**します。</span><span class="sxs-lookup"><span data-stu-id="bee12-122">In the **Add Reference** dialog, select **Framework** on the left-hand side of the dialog under **Assemblies**.</span></span> <span data-ttu-id="bee12-123">検索して選択**System.ServiceModel**を選び、 **OK**。</span><span class="sxs-lookup"><span data-stu-id="bee12-123">Find and select **System.ServiceModel**, and then choose **OK**.</span></span> <span data-ttu-id="bee12-124">ソリューションを選択して保存**ファイル** > **すべて保存**します。</span><span class="sxs-lookup"><span data-stu-id="bee12-124">Save the solution by selecting **File** > **Save All**.</span></span>

3. <span data-ttu-id="bee12-125">電卓サービスにサービス参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="bee12-125">Add a service reference to the Calculator Service.</span></span>

   1. <span data-ttu-id="bee12-126">最初に、GettingStartedHost コンソール アプリケーションを開始します。</span><span class="sxs-lookup"><span data-stu-id="bee12-126">First, start up the GettingStartedHost console application.</span></span>

   2. <span data-ttu-id="bee12-127">ホストが実行されている場合を右クリックし、**参照**で GettingStartedClient プロジェクトの下のフォルダー**ソリューション エクスプ ローラー**選択**追加** >  **サービス参照**します。</span><span class="sxs-lookup"><span data-stu-id="bee12-127">Once the host is running, right-click the **References** folder under the GettingStartedClient project in **Solution Explorer** and select **Add** > **Service Reference**.</span></span>

   3. <span data-ttu-id="bee12-128">[アドレス] ボックスの次の URL を入力、**サービス参照の追加**ダイアログ。 [http://localhost:8000/GettingStarted/CalculatorService](http://localhost:8000/GettingStarted/CalculatorService)</span><span class="sxs-lookup"><span data-stu-id="bee12-128">Enter the following URL in the address box of the **Add Service Reference** dialog: [http://localhost:8000/GettingStarted/CalculatorService](http://localhost:8000/GettingStarted/CalculatorService)</span></span>

   4. <span data-ttu-id="bee12-129">選択**移動**します。</span><span class="sxs-lookup"><span data-stu-id="bee12-129">Choose **Go**.</span></span>

   <span data-ttu-id="bee12-130">CalculatorService に表示される、**サービス**ボックスの一覧。</span><span class="sxs-lookup"><span data-stu-id="bee12-130">The CalculatorService is displayed in the **Services** list box.</span></span> <span data-ttu-id="bee12-131">展開すると、サービスによって実装されるサービス コントラクトを表示する CalculatorService をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="bee12-131">Double-click CalculatorService to expand it and show the service contracts implemented by the service.</span></span> <span data-ttu-id="bee12-132">として既定の名前空間のままに、選択は、 **OK**。</span><span class="sxs-lookup"><span data-stu-id="bee12-132">Leave the default namespace as-is and choose **OK**.</span></span>

    <span data-ttu-id="bee12-133">Visual Studio を使用してサービスへの参照を追加するに新しい項目が表示されます。**ソリューション エクスプ ローラー**下、**サービス参照**GettingStartedClient プロジェクトの下のフォルダー。</span><span class="sxs-lookup"><span data-stu-id="bee12-133">When you add a reference to a service using Visual Studio, a new item appears in **Solution Explorer** under the **Service References** folder under the GettingStartedClient project.</span></span> <span data-ttu-id="bee12-134">使用する場合、 [ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)ツール、ソース コード ファイルと app.config ファイルが生成されます。</span><span class="sxs-lookup"><span data-stu-id="bee12-134">If you use the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) tool, a source code file and app.config file are generated.</span></span>

    <span data-ttu-id="bee12-135">コマンド ライン ツールを使用することもできます。 [ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)クライアント コードを作成するスイッチを適切な使用。</span><span class="sxs-lookup"><span data-stu-id="bee12-135">You can also use the command-line tool [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) with the appropriate switches to create the client code.</span></span> <span data-ttu-id="bee12-136">次の例では、サービスのコード ファイルと構成ファイルを生成しています。</span><span class="sxs-lookup"><span data-stu-id="bee12-136">The following example generates a code file and a configuration file for the service.</span></span> <span data-ttu-id="bee12-137">最初の例は、VB でプロキシを生成する方法と、2 つ目は、c# でプロキシを生成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bee12-137">The first example shows how to generate the proxy in VB, and the second shows how to generate the proxy in C#:</span></span>

    ```shell
    svcutil.exe /language:vb /out:generatedProxy.vb /config:app.config http://localhost:8000/GettingStarted/CalculatorService
    ```

    ```shell
    svcutil.exe /language:cs /out:generatedProxy.cs /config:app.config http://localhost:8000/GettingStarted/CalculatorService
    ```

## <a name="next-steps"></a><span data-ttu-id="bee12-138">次の手順</span><span class="sxs-lookup"><span data-stu-id="bee12-138">Next steps</span></span>

<span data-ttu-id="bee12-139">クライアント アプリケーションが、電卓サービスの呼び出しに使用するプロキシを作成しました。</span><span class="sxs-lookup"><span data-stu-id="bee12-139">You've created the proxy that the client application will use to call the calculator service.</span></span> <span data-ttu-id="bee12-140">シリーズの次のトピックに進みます。</span><span class="sxs-lookup"><span data-stu-id="bee12-140">Proceed to the next topic in the series.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="bee12-141">方法: クライアントを構成する</span><span class="sxs-lookup"><span data-stu-id="bee12-141">How to: Configure a Client</span></span>](../../../docs/framework/wcf/how-to-configure-a-basic-wcf-client.md)

## <a name="see-also"></a><span data-ttu-id="bee12-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="bee12-142">See also</span></span>

- [<span data-ttu-id="bee12-143">ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)</span><span class="sxs-lookup"><span data-stu-id="bee12-143">ServiceModel Metadata Utility Tool (Svcutil.exe)</span></span>](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [<span data-ttu-id="bee12-144">はじめに</span><span class="sxs-lookup"><span data-stu-id="bee12-144">Getting Started</span></span>](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [<span data-ttu-id="bee12-145">自己ホスト</span><span class="sxs-lookup"><span data-stu-id="bee12-145">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)
- [<span data-ttu-id="bee12-146">方法 : 構成ファイルを使用してサービスのメタデータを公開する</span><span class="sxs-lookup"><span data-stu-id="bee12-146">How to: Publish Metadata for a Service Using a Configuration File</span></span>](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [<span data-ttu-id="bee12-147">方法 : Svcutil.exe を使用してメタデータ ドキュメントをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="bee12-147">How to: Use Svcutil.exe to Download Metadata Documents</span></span>](../../../docs/framework/wcf/feature-details/how-to-use-svcutil-exe-to-download-metadata-documents.md)
