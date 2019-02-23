---
title: ホストおよび基本的な Windows Communication Foundation サービスを実行する方法
ms.date: 09/14/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF services [WCF]
- WCF services [WCF], running
ms.assetid: 31774d36-923b-4e2d-812e-aa190127266f
ms.openlocfilehash: 73633c2c6119204f2fb608b32ae794a2e07b27d0
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/23/2019
ms.locfileid: "56747075"
---
# <a name="how-to-host-and-run-a-basic-windows-communication-foundation-service"></a><span data-ttu-id="8ad44-102">ホストおよび基本的な Windows Communication Foundation サービスを実行する方法</span><span class="sxs-lookup"><span data-stu-id="8ad44-102">How to host and run a basic Windows Communication Foundation service</span></span>

<span data-ttu-id="8ad44-103">Windows Communication Foundation (WCF) アプリケーションの作成に必要な 6 つのタスクのうちの 3 番目がこれです。</span><span class="sxs-lookup"><span data-stu-id="8ad44-103">This is the third of six tasks required to create a Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="8ad44-104">6 つのすべてのタスクの概要については、「[チュートリアル入門](getting-started-tutorial.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ad44-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](getting-started-tutorial.md) topic.</span></span>

<span data-ttu-id="8ad44-105">このトピックでは、コンソール アプリケーションで Windows Communication Foundation (WCF) サービスをホストする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-105">This topic describes how to host a Windows Communication Foundation (WCF) service in a console application.</span></span> <span data-ttu-id="8ad44-106">この操作は、次の手順から構成されます。</span><span class="sxs-lookup"><span data-stu-id="8ad44-106">This procedure consists of the following steps:</span></span>

- <span data-ttu-id="8ad44-107">コンソール アプリケーション プロジェクトを作成し、サービスをホストします。</span><span class="sxs-lookup"><span data-stu-id="8ad44-107">Create a console application project to host the service.</span></span>

- <span data-ttu-id="8ad44-108">サービスのサービス ホストを作成します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-108">Create a service host for the service.</span></span>

- <span data-ttu-id="8ad44-109">メタデータ交換を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8ad44-109">Enable metadata exchange.</span></span>

- <span data-ttu-id="8ad44-110">サービス ホストを開きます。</span><span class="sxs-lookup"><span data-stu-id="8ad44-110">Open the service host.</span></span>

<span data-ttu-id="8ad44-111">このタスクで書かれるコードの全容は手順に続いて提供されている例で見ることができます。</span><span class="sxs-lookup"><span data-stu-id="8ad44-111">A complete listing of the code written in this task is provided in the example following the procedure.</span></span>

## <a name="create-a-new-console-application-to-host-the-service"></a><span data-ttu-id="8ad44-112">サービスをホストする新しいコンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-112">Create a new console application to host the service</span></span>

1. <span data-ttu-id="8ad44-113">Visual Studio でのはじめにソリューションを右クリックして新しいコンソール アプリケーション プロジェクトを作成**追加** > **新しいプロジェクト**します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-113">Create a new Console Application project in Visual Studio by right-clicking on the Getting Started solution and selecting **Add** > **New Project**.</span></span> <span data-ttu-id="8ad44-114">**新しいプロジェクトの追加**ダイアログ ボックスで、左側にある、選択、 **Windows デスクトップ**カテゴリ  **Visual c#** または**Visual Basic**します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-114">In the **Add New Project** dialog, on the left-hand side, select the **Windows Desktop** category under **Visual C#** or **Visual Basic**.</span></span> <span data-ttu-id="8ad44-115">選択、**コンソール アプリ (.NET Framework)** テンプレート、および、プロジェクトの名前を**GettingStartedHost**します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-115">Select the **Console App (.NET Framework)** template, and then name the project **GettingStartedHost**.</span></span>

2. <span data-ttu-id="8ad44-116">GettingStartedLib プロジェクトへの参照を GettingStartedHost プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-116">Add a reference to the GettingStartedLib project to the GettingStartedHost project.</span></span> <span data-ttu-id="8ad44-117">右クリックし、**参照**で GettingStartedHost プロジェクトの下のフォルダー**ソリューション エクスプ ローラー**、し、**参照の追加**します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-117">Right-click on the **References** folder under the GettingStartedHost project in **Solution Explorer**, and then select **Add Reference**.</span></span> <span data-ttu-id="8ad44-118">**参照の追加**ダイアログ ボックスで、**ソリューション**ダイアログの左側にあるの ダイアログの中央のセクションで GettingStartedLib を選択し、**追加**します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-118">In the **Add Reference** dialog, select **Solution** on the left-hand side of the dialog, select GettingStartedLib in the center section of the dialog, and then choose **Add**.</span></span> <span data-ttu-id="8ad44-119">これにより、GettingStartedLib に定義されている型を GettingStartedHost プロジェクトで利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8ad44-119">This makes the types defined in GettingStartedLib available to the GettingStartedHost project.</span></span>

3. <span data-ttu-id="8ad44-120">System.ServiceModel への参照を GettingStartedHost プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-120">Add a reference to System.ServiceModel to the GettingStartedHost project.</span></span> <span data-ttu-id="8ad44-121">右クリックし、**参照**で GettingStartedHost プロジェクトの下のフォルダー**ソリューション エクスプ ローラー**選択**参照の追加**します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-121">Right-click the **References** folder under the GettingStartedHost project in **Solution Explorer** and select **Add Reference**.</span></span> <span data-ttu-id="8ad44-122">**参照の追加**ダイアログ ボックスで、 **Framework**ダイアログ ボックスの左側にある**アセンブリ**します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-122">In the **Add Reference** dialog, select **Framework** on the left-hand side of the dialog under **Assemblies**.</span></span> <span data-ttu-id="8ad44-123">検索して選択**System.ServiceModel**を選び、 **OK**。</span><span class="sxs-lookup"><span data-stu-id="8ad44-123">Find and select **System.ServiceModel**, and then choose **OK**.</span></span> <span data-ttu-id="8ad44-124">ソリューションを選択して保存**ファイル** > **すべて保存**します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-124">Save the solution by selecting **File** > **Save All**.</span></span>

## <a name="host-the-service"></a><span data-ttu-id="8ad44-125">サービスをホストします</span><span class="sxs-lookup"><span data-stu-id="8ad44-125">Host the service</span></span>

<span data-ttu-id="8ad44-126">Program.cs ファイルまたは Module.vb ファイルを開き、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-126">Open the Program.cs or Module.vb file and enter the following code:</span></span>

```csharp
using System;
using System.ServiceModel;
using System.ServiceModel.Description;
using GettingStartedLib;

namespace GettingStartedHost
{
    class Program
    {
        static void Main(string[] args)
        {
            // Step 1 Create a URI to serve as the base address.
            Uri baseAddress = new Uri("http://localhost:8000/GettingStarted/");

            // Step 2 Create a ServiceHost instance
            ServiceHost selfHost = new ServiceHost(typeof(CalculatorService), baseAddress);

            try
            {
                // Step 3 Add a service endpoint.
                selfHost.AddServiceEndpoint(typeof(ICalculator), new WSHttpBinding(), "CalculatorService");

                // Step 4 Enable metadata exchange.
                ServiceMetadataBehavior smb = new ServiceMetadataBehavior();
                smb.HttpGetEnabled = true;
                selfHost.Description.Behaviors.Add(smb);

                // Step 5 Start the service.
                selfHost.Open();
                Console.WriteLine("The service is ready.");
                Console.WriteLine("Press <ENTER> to terminate service.");
                Console.WriteLine();
                Console.ReadLine();

                // Close the ServiceHostBase to shutdown the service.
                selfHost.Close();
            }
            catch (CommunicationException ce)
            {
                Console.WriteLine("An exception occurred: {0}", ce.Message);
                selfHost.Abort();
            }
        }
    }
}
```

```vb
Imports System.ServiceModel
Imports System.ServiceModel.Description
Imports GettingStartedLibVB.GettingStartedLib

Module Service

    Class Program
        Shared Sub Main()
            ' Step 1 Create a URI to serve as the base address
            Dim baseAddress As New Uri("http://localhost:8000/GettingStarted")

            ' Step 2 Create a ServiceHost instance
            Dim selfHost As New ServiceHost(GetType(CalculatorService), baseAddress)
           Try

                ' Step 3 Add a service endpoint
                ' Add a service endpoint
                selfHost.AddServiceEndpoint( _
                    GetType(ICalculator), _
                    New WSHttpBinding(), _
                    "CalculatorService")

                ' Step 4 Enable metadata exchange.
                Dim smb As New ServiceMetadataBehavior()
                smb.HttpGetEnabled = True
                selfHost.Description.Behaviors.Add(smb)

                ' Step 5 Start the service
                selfHost.Open()
                Console.WriteLine("The service is ready.")
                Console.WriteLine("Press <ENTER> to terminate service.")
                Console.WriteLine()
                Console.ReadLine()

                ' Close the ServiceHostBase to shutdown the service.
                selfHost.Close()
            Catch ce As CommunicationException
                Console.WriteLine("An exception occurred: {0}", ce.Message)
                selfHost.Abort()
            End Try
        End Sub
    End Class

End Module
```

<span data-ttu-id="8ad44-127">**手順 1.** -サービスのベース アドレスを保持するために、Uri クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-127">**Step 1** - Creates an instance of the Uri class to hold the base address of the service.</span></span> <span data-ttu-id="8ad44-128">サービスは、ベース アドレスとオプションの URI を含む URL によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="8ad44-128">Services are identified by a URL which contains a base address and an optional URI.</span></span> <span data-ttu-id="8ad44-129">ベース アドレスの書式は、[トランスポート]://[コンピューター名またはドメイン][:省略可能なポート番号]/[省略可能な URI セグメント] です。電卓サービスのベース アドレスは、電卓サービスのベース アドレスを使用して HTTP トランスポート、localhost、ポート 8000、および URI セグメント "GettingStarted" を使用します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-129">The base address is formatted as follows:[transport]://[machine-name or domain][:optional port #]/[optional URI segment]The base address for the calculator service uses the HTTP transport, localhost, port 8000, and the URI segment "GettingStarted"</span></span>

<span data-ttu-id="8ad44-130">**手順 2** – のインスタンスを作成、<xref:System.ServiceModel.ServiceHost>クラス、サービスをホストします。</span><span class="sxs-lookup"><span data-stu-id="8ad44-130">**Step 2** – Creates an instance of the <xref:System.ServiceModel.ServiceHost> class to host the service.</span></span> <span data-ttu-id="8ad44-131">コンストラクターは、サービス コントラクトを実装するクラスの型と、サービスのベース アドレスの、2 つのパラメーターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="8ad44-131">The constructor takes two parameters, the type of the class that implements the service contract, and the base address of the service.</span></span>

<span data-ttu-id="8ad44-132">**手順 3** – 作成、<xref:System.ServiceModel.Description.ServiceEndpoint>インスタンス。</span><span class="sxs-lookup"><span data-stu-id="8ad44-132">**Step 3** – Creates a <xref:System.ServiceModel.Description.ServiceEndpoint> instance.</span></span> <span data-ttu-id="8ad44-133">サービス エンドポイントは、アドレス、バインディング、およびサービス コントラクトから構成されます。</span><span class="sxs-lookup"><span data-stu-id="8ad44-133">A service endpoint is composed of an address, a binding, and a service contract.</span></span> <span data-ttu-id="8ad44-134">
  <xref:System.ServiceModel.Description.ServiceEndpoint> コンストラクターは、サービス コントラクト インターフェイスの型、バインディング、およびアドレスを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="8ad44-134">The <xref:System.ServiceModel.Description.ServiceEndpoint> constructor therefore takes the service contract interface type, a binding, and an address.</span></span> <span data-ttu-id="8ad44-135">サービス コントラクトは、サービス型に定義および実装した `ICalculator` です。</span><span class="sxs-lookup"><span data-stu-id="8ad44-135">The service contract is `ICalculator`, which you defined and implement in the service type.</span></span> <span data-ttu-id="8ad44-136">このサンプルで使用するバインディングは、WS-\* 仕様に準拠するエンドポイントへの接続に使用される組み込みのバインディングである <xref:System.ServiceModel.WSHttpBinding> です。</span><span class="sxs-lookup"><span data-stu-id="8ad44-136">The binding used in this sample is <xref:System.ServiceModel.WSHttpBinding> which is a built-in binding that is used for connecting to endpoints that conform to the WS-\* specifications.</span></span> <span data-ttu-id="8ad44-137">WCF バインディングの詳細については、[WCF バインディングの概要](bindings-overview.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ad44-137">For more information about WCF bindings, see [WCF Bindings Overview](bindings-overview.md).</span></span> <span data-ttu-id="8ad44-138">エンドポイントを識別するために、ベース アドレスにアドレスが追加されます。</span><span class="sxs-lookup"><span data-stu-id="8ad44-138">The address is appended to the base address to identify the endpoint.</span></span> <span data-ttu-id="8ad44-139">このコードで指定されたアドレスは"CalculatorService"エンドポイントの完全修飾アドレスは`"http://localhost:8000/GettingStarted/CalculatorService"`します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-139">The address specified in this code is "CalculatorService" so the fully qualified address for the endpoint is `"http://localhost:8000/GettingStarted/CalculatorService"`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8ad44-140">サービス エンドポイントの追加は、.NET Framework 4 以降を使用する場合は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="8ad44-140">Adding a service endpoint is optional when using .NET Framework 4 or later.</span></span> <span data-ttu-id="8ad44-141">これらのバージョンでは、エンドポイントがコードまたは構成で指定されていない場合、WCF は、サービスで実装されたベース アドレスとコントラクトの組み合わせごとに、1 つの既定のエンドポイントを追加します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-141">In these versions, if no endpoints are added in code or configuration, WCF adds one default endpoint for each combination of base address and contract implemented by the service.</span></span> <span data-ttu-id="8ad44-142">既定のエンドポイントの詳細については、「[Specifying an Endpoint Address](specifying-an-endpoint-address.md)」 (エンドポイント アドレスの指定) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ad44-142">For more information about default endpoints see [Specifying an Endpoint Address](specifying-an-endpoint-address.md).</span></span> <span data-ttu-id="8ad44-143">既定のエンドポイントについては、「[Simplified Configuration](simplified-configuration.md)」 (簡易構成) と「[Simplified Configuration for WCF Services](./samples/simplified-configuration-for-wcf-services.md)」 (WCF サービスの簡易構成) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ad44-143">For more information about default endpoints, bindings, and behaviors, see [Simplified Configuration](simplified-configuration.md) and [Simplified Configuration for WCF Services](./samples/simplified-configuration-for-wcf-services.md).</span></span>

<span data-ttu-id="8ad44-144">**手順 4** – メタデータ交換を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8ad44-144">**Step 4** – Enable metadata exchange.</span></span> <span data-ttu-id="8ad44-145">クライアントは、サービス操作を呼び出すために使用されるプロキシの生成にメタデータ交換を使用します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-145">Clients will use metadata exchange to generate proxies that will be used to call the service operations.</span></span> <span data-ttu-id="8ad44-146">メタデータ交換を有効化するには、<xref:System.ServiceModel.Description.ServiceMetadataBehavior> インスタンスを作成し、その <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> プロパティを `true` に設定します。さらに、動作を <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A> インスタンスの <xref:System.ServiceModel.ServiceHost> コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-146">To enable metadata exchange create a <xref:System.ServiceModel.Description.ServiceMetadataBehavior> instance, set it’s <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> property to `true`, and add the behavior to the <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A> collection of the <xref:System.ServiceModel.ServiceHost> instance.</span></span>

<span data-ttu-id="8ad44-147">**手順 5** – オープン、<xref:System.ServiceModel.ServiceHost>受信メッセージをリッスンします。</span><span class="sxs-lookup"><span data-stu-id="8ad44-147">**Step 5** – Open the <xref:System.ServiceModel.ServiceHost> to listen for incoming messages.</span></span> <span data-ttu-id="8ad44-148">コードでは、ユーザーによる Enter キーの押下を待機しています。</span><span class="sxs-lookup"><span data-stu-id="8ad44-148">Notice the code waits for the user to hit enter.</span></span> <span data-ttu-id="8ad44-149">この動作を行わない場合、アプリは直ちに終了し、サービスはシャットダウンします。また、try/catch ブロックが使用されている点にも注意してください。</span><span class="sxs-lookup"><span data-stu-id="8ad44-149">If you do not do this, the app will close immediately and the service will shut down.Also notice a  try/catch block used.</span></span> <span data-ttu-id="8ad44-150">
  <xref:System.ServiceModel.ServiceHost> がインスタンス化された後、他のコードはすべて try/catch ブロックに配置されます。</span><span class="sxs-lookup"><span data-stu-id="8ad44-150">After the <xref:System.ServiceModel.ServiceHost> has been instantiated, all other code is placed in a try/catch block.</span></span> <span data-ttu-id="8ad44-151">によってスローされた例外を安全にキャッチの詳細については<xref:System.ServiceModel.ServiceHost>を参照してください[使用終了、中止 WCF クライアントのリソースを解放するには](samples/use-close-abort-release-wcf-client-resources.md)</span><span class="sxs-lookup"><span data-stu-id="8ad44-151">For more information about safely catching exceptions thrown by <xref:System.ServiceModel.ServiceHost>, see [Use Close and Abort to release WCF client resources](samples/use-close-abort-release-wcf-client-resources.md)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8ad44-152">WCF サービス ライブラリを追加するときに Visual Studio ホストできますがサービス ホストを起動してデバッグするときにします。</span><span class="sxs-lookup"><span data-stu-id="8ad44-152">When you add a WCF Service Library, Visual Studio can host it for you when you debug by starting a service host.</span></span> <span data-ttu-id="8ad44-153">競合を回避するために、これが無効にできます。</span><span class="sxs-lookup"><span data-stu-id="8ad44-153">To avoid conflicts you can disable this.</span></span> 
> 1. <span data-ttu-id="8ad44-154">GettingStartedLib のプロジェクトのプロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="8ad44-154">Open Project Properties for GettingStartedLib.</span></span>
> 2. <span data-ttu-id="8ad44-155">移動して**WCF オプション**をオフにし、**開始 WCF サービス ホストのデバッグ時に**します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-155">Go to **WCF Options** and uncheck **Start WCF Service Host when debugging**.</span></span>

## <a name="verify-the-service-is-working"></a><span data-ttu-id="8ad44-156">サービスが動作を確認します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-156">Verify the service is working</span></span>

1. <span data-ttu-id="8ad44-157">GettingStartedHost コンソールを実行する Visual Studio 内からアプリケーション。</span><span class="sxs-lookup"><span data-stu-id="8ad44-157">Run the GettingStartedHost console application from inside Visual Studio.</span></span>

   <span data-ttu-id="8ad44-158">サービスは、管理者特権で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ad44-158">The service must be run with administrator privileges.</span></span> <span data-ttu-id="8ad44-159">Visual Studio が管理者特権で開いた、GettingStartedHost も管理者特権で実行されます。</span><span class="sxs-lookup"><span data-stu-id="8ad44-159">Because Visual Studio was opened with administrator privileges, GettingStartedHost is also run with administrator privileges.</span></span> <span data-ttu-id="8ad44-160">使用して新しいコマンド プロンプトを開くことができますも**管理者として実行**内に service.exe を実行します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-160">You can also open a new command prompt using **Run as administrator** and run service.exe within it.</span></span>

2. <span data-ttu-id="8ad44-161">Web ブラウザーを開き、サービスのデバッグ ページを参照`http://localhost:8000/GettingStarted/`します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-161">Open a web browser and browse to the service's debug page at `http://localhost:8000/GettingStarted/`.</span></span> <span data-ttu-id="8ad44-162">**注意してください。スラッシュを終了することは重要です。**</span><span class="sxs-lookup"><span data-stu-id="8ad44-162">**Note! Ending slash is significant.**</span></span>

## <a name="example"></a><span data-ttu-id="8ad44-163">例</span><span class="sxs-lookup"><span data-stu-id="8ad44-163">Example</span></span>

<span data-ttu-id="8ad44-164">次の例では、チュートリアルの前の手順で作成したサービス コントラクトと実装を含め、コンソール アプリケーションでサービスをホストします。</span><span class="sxs-lookup"><span data-stu-id="8ad44-164">The following example includes the service contract and implementation from previous steps in the tutorial and hosts the service in a console application.</span></span>

<span data-ttu-id="8ad44-165">コマンド ライン コンパイラでコンパイルを参照するクラス ライブラリに IService1.cs と Service1.cs をコンパイル`System.ServiceModel.dll`します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-165">To compile this with a command-line compiler, compile IService1.cs and Service1.cs into a class library that references `System.ServiceModel.dll`.</span></span> <span data-ttu-id="8ad44-166">Program.cs をコンソール アプリケーションとしてコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="8ad44-166">Compile Program.cs as a console application.</span></span>

```csharp
using System;
using System.ServiceModel;

namespace GettingStartedLib
{
        [ServiceContract(Namespace = "http://Microsoft.ServiceModel.Samples")]
        public interface ICalculator
        {
            [OperationContract]
            double Add(double n1, double n2);
            [OperationContract]
            double Subtract(double n1, double n2);
            [OperationContract]
            double Multiply(double n1, double n2);
            [OperationContract]
            double Divide(double n1, double n2);
        }
}
```

```csharp
using System;
using System.ServiceModel;

namespace GettingStartedLib
{
    public class CalculatorService : ICalculator
    {
        public double Add(double n1, double n2)
        {
            double result = n1 + n2;
            Console.WriteLine("Received Add({0},{1})", n1, n2);
            // Code added to write output to the console window.
            Console.WriteLine("Return: {0}", result);
            return result;
        }

        public double Subtract(double n1, double n2)
        {
            double result = n1 - n2;
            Console.WriteLine("Received Subtract({0},{1})", n1, n2);
            Console.WriteLine("Return: {0}", result);
            return result;
        }

        public double Multiply(double n1, double n2)
        {
            double result = n1 * n2;
            Console.WriteLine("Received Multiply({0},{1})", n1, n2);
            Console.WriteLine("Return: {0}", result);
            return result;
        }

        public double Divide(double n1, double n2)
        {
            double result = n1 / n2;
            Console.WriteLine("Received Divide({0},{1})", n1, n2);
            Console.WriteLine("Return: {0}", result);
            return result;
        }
    }
}
```

```csharp
using System;
using System.ServiceModel;
using System.ServiceModel.Description;
using GettingStartedLib;

namespace GettingStartedHost
{
    class Program
    {
        static void Main(string[] args)
        {
            // Step 1 of the address configuration procedure: Create a URI to serve as the base address.
            Uri baseAddress = new Uri("http://localhost:8000/GettingStarted/");

            // Step 2 of the hosting procedure: Create ServiceHost
            ServiceHost selfHost = new ServiceHost(typeof(CalculatorService), baseAddress);

            try
            {
                // Step 3 of the hosting procedure: Add a service endpoint.
                selfHost.AddServiceEndpoint(typeof(ICalculator), new WSHttpBinding(), "CalculatorService");

                // Step 4 of the hosting procedure: Enable metadata exchange.
                ServiceMetadataBehavior smb = new ServiceMetadataBehavior();
                smb.HttpGetEnabled = true;
                selfHost.Description.Behaviors.Add(smb);

                // Step 5 of the hosting procedure: Start (and then stop) the service.
                selfHost.Open();
                Console.WriteLine("The service is ready.");
                Console.WriteLine("Press <ENTER> to terminate service.");
                Console.WriteLine();
                Console.ReadLine();

                // Close the ServiceHostBase to shutdown the service.
                selfHost.Close();
            }
            catch (CommunicationException ce)
            {
                Console.WriteLine("An exception occurred: {0}", ce.Message);
                selfHost.Abort();
            }
        }
    }
}
```

```vb
Imports System.ServiceModel

Namespace GettingStartedLib

    <ServiceContract(Namespace:="http://Microsoft.ServiceModel.Samples")> _
    Public Interface ICalculator

        <OperationContract()> _
        Function Add(ByVal n1 As Double, ByVal n2 As Double) As Double
        <OperationContract()> _
        Function Subtract(ByVal n1 As Double, ByVal n2 As Double) As Double
        <OperationContract()> _
        Function Multiply(ByVal n1 As Double, ByVal n2 As Double) As Double
        <OperationContract()> _
        Function Divide(ByVal n1 As Double, ByVal n2 As Double) As Double
    End Interface
End Namespace
```

```vb
Imports System.ServiceModel

Namespace GettingStartedLib

    Public Class CalculatorService
        Implements ICalculator

        Public Function Add(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Add
            Dim result As Double = n1 + n2
            ' Code added to write output to the console window.
            Console.WriteLine("Received Add({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result
        End Function

        Public Function Subtract(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Subtract
            Dim result As Double = n1 - n2
            Console.WriteLine("Received Subtract({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result

        End Function

        Public Function Multiply(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Multiply
            Dim result As Double = n1 * n2
            Console.WriteLine("Received Multiply({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result

        End Function

        Public Function Divide(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Divide
            Dim result As Double = n1 / n2
            Console.WriteLine("Received Divide({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result

        End Function
    End Class
End Namespace
```

```vb
Imports System.ServiceModel
Imports System.ServiceModel.Description
Imports GettingStartedLibVB.GettingStartedLib

Module Service

    Class Program
        Shared Sub Main()
            ' Step 1 of the address configuration procedure: Create a URI to serve as the base address.
            Dim baseAddress As New Uri("http://localhost:8000/GettingStarted/")

            ' Step 2 of the hosting procedure: Create ServiceHost
            Dim selfHost As New ServiceHost(GetType(CalculatorService), baseAddress)
            Try

                ' Step 3 of the hosting procedure: Add a service endpoint.
                ' Add a service endpoint
                selfHost.AddServiceEndpoint( _
                    GetType(ICalculator), _
                    New WSHttpBinding(), _
                    "CalculatorService")

                ' Step 4 of the hosting procedure: Enable metadata exchange.
                ' Enable metadata exchange
                Dim smb As New ServiceMetadataBehavior()
                smb.HttpGetEnabled = True
                selfHost.Description.Behaviors.Add(smb)

                ' Step 5 of the hosting procedure: Start (and then stop) the service.
                selfHost.Open()
                Console.WriteLine("The service is ready.")
                Console.WriteLine("Press <ENTER> to terminate service.")
                Console.WriteLine()
                Console.ReadLine()

                ' Close the ServiceHostBase to shutdown the service.
                selfHost.Close()
            Catch ce As CommunicationException
                Console.WriteLine("An exception occurred: {0}", ce.Message)
                selfHost.Abort()
            End Try
        End Sub
    End Class

End Module
```

> [!NOTE]
> <span data-ttu-id="8ad44-167">このようなサービスには、リッスンを行うコンピューター上で HTTP アドレスを登録するためのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="8ad44-167">Services such as this one require permission to register HTTP addresses on the machine for listening.</span></span> <span data-ttu-id="8ad44-168">管理者アカウントにはこのアクセス許可がありますが、管理者以外のアカウントの場合は、HTTP 名前空間へのアクセス許可を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ad44-168">Administrator accounts have this permission, but non-administrator accounts must be granted permission for HTTP namespaces.</span></span> <span data-ttu-id="8ad44-169">名前空間の予約を構成する方法については、「[Configuring HTTP and HTTPS](feature-details/configuring-http-and-https.md)」 (HTTP と HTTPS を構成する) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ad44-169">For more information about how to configure namespace reservations, see [Configuring HTTP and HTTPS](feature-details/configuring-http-and-https.md).</span></span> <span data-ttu-id="8ad44-170">Visual Studio で service.exe を実行するには、管理者権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="8ad44-170">When running under Visual Studio, the service.exe must be run with administrator privileges.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8ad44-171">次の手順</span><span class="sxs-lookup"><span data-stu-id="8ad44-171">Next steps</span></span>

<span data-ttu-id="8ad44-172">これでサービスが実行されていることが確認できました。</span><span class="sxs-lookup"><span data-stu-id="8ad44-172">Now the service is running.</span></span> <span data-ttu-id="8ad44-173">次のタスクでは、WCF クライアントを作成します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-173">In the next task, you create a WCF client.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="8ad44-174">方法: WCF クライアントを作成します。</span><span class="sxs-lookup"><span data-stu-id="8ad44-174">How to: Create a WCF client</span></span>](how-to-create-a-wcf-client.md)

<span data-ttu-id="8ad44-175">トラブルシューティングについては、「[Troubleshooting the Getting Started Tutorial](troubleshooting-the-getting-started-tutorial.md)」 (チュートリアル入門のトラブルシューティング) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ad44-175">For troubleshooting information, see [Troubleshooting the Getting Started Tutorial](troubleshooting-the-getting-started-tutorial.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8ad44-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="8ad44-176">See also</span></span>

- [<span data-ttu-id="8ad44-177">はじめに</span><span class="sxs-lookup"><span data-stu-id="8ad44-177">Getting Started</span></span>](samples/getting-started-sample.md)
- [<span data-ttu-id="8ad44-178">自己ホスト</span><span class="sxs-lookup"><span data-stu-id="8ad44-178">Self-Host</span></span>](samples/self-host.md)
- [<span data-ttu-id="8ad44-179">ホスティング サービス</span><span class="sxs-lookup"><span data-stu-id="8ad44-179">Hosting Services</span></span>](hosting-services.md)
