---
title: '方法 : 基本的な Windows Communication Foundation サービスをホストおよび実行する'
ms.date: 09/14/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF services [WCF]
- WCF services [WCF], running
ms.assetid: 31774d36-923b-4e2d-812e-aa190127266f
ms.openlocfilehash: b79c3246b7c12a3a99a5c68586387fc30573dcb6
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2018
ms.locfileid: "46562295"
---
# <a name="how-to-host-and-run-a-basic-windows-communication-foundation-service"></a><span data-ttu-id="e5a01-102">方法 : 基本的な Windows Communication Foundation サービスをホストおよび実行する</span><span class="sxs-lookup"><span data-stu-id="e5a01-102">How to: Host and Run a Basic Windows Communication Foundation Service</span></span>

<span data-ttu-id="e5a01-103">Windows Communication Foundation (WCF) アプリケーションの作成に必要な 6 つのタスクのうちの 3 番目がこれです。</span><span class="sxs-lookup"><span data-stu-id="e5a01-103">This is the third of six tasks required to create a Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="e5a01-104">6 つのすべてのタスクの概要については、「[チュートリアル入門](../../../docs/framework/wcf/getting-started-tutorial.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5a01-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) topic.</span></span>

<span data-ttu-id="e5a01-105">このトピックでは、コンソール アプリケーションで Windows Communication Foundation (WCF) サービスをホストする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-105">This topic describes how to host a Windows Communication Foundation (WCF) service in a console application.</span></span> <span data-ttu-id="e5a01-106">この操作は、次の手順から構成されます。</span><span class="sxs-lookup"><span data-stu-id="e5a01-106">This procedure consists of the following steps:</span></span>

- <span data-ttu-id="e5a01-107">コンソール アプリケーション プロジェクトを作成し、サービスをホストします。</span><span class="sxs-lookup"><span data-stu-id="e5a01-107">Create a console application project to host the service.</span></span>

- <span data-ttu-id="e5a01-108">サービスのサービス ホストを作成します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-108">Create a service host for the service.</span></span>

- <span data-ttu-id="e5a01-109">メタデータ交換を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e5a01-109">Enable metadata exchange.</span></span>

- <span data-ttu-id="e5a01-110">サービス ホストを開きます。</span><span class="sxs-lookup"><span data-stu-id="e5a01-110">Open the service host.</span></span>

<span data-ttu-id="e5a01-111">このタスクで書かれるコードの全容は手順に続いて提供されている例で見ることができます。</span><span class="sxs-lookup"><span data-stu-id="e5a01-111">A complete listing of the code written in this task is provided in the example following the procedure.</span></span>

## <a name="create-a-new-console-application-to-host-the-service"></a><span data-ttu-id="e5a01-112">サービスをホストする新しいコンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-112">Create a new console application to host the service</span></span>

1. <span data-ttu-id="e5a01-113">Visual Studio でのはじめにソリューションを右クリックして新しいコンソール アプリケーション プロジェクトを作成**追加** > **新しいプロジェクト**します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-113">Create a new Console Application project in Visual Studio by right-clicking on the Getting Started solution and selecting **Add** > **New Project**.</span></span> <span data-ttu-id="e5a01-114">**新しいプロジェクトの追加**ダイアログ ボックスで、左側にある、選択、 **Windows デスクトップ**カテゴリ  **Visual c#** または**Visual Basic**します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-114">In the **Add New Project** dialog, on the left-hand side, select the **Windows Desktop** category under **Visual C#** or **Visual Basic**.</span></span> <span data-ttu-id="e5a01-115">選択、**コンソール アプリ (.NET Framework)** テンプレート、および、プロジェクトの名前を**GettingStartedHost**します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-115">Select the **Console App (.NET Framework)** template, and then name the project **GettingStartedHost**.</span></span>

2. <span data-ttu-id="e5a01-116">GettingStartedLib プロジェクトへの参照を GettingStartedHost プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-116">Add a reference to the GettingStartedLib project to the GettingStartedHost project.</span></span> <span data-ttu-id="e5a01-117">右クリックし、**参照**で GettingStartedHost プロジェクトの下のフォルダー**ソリューション エクスプ ローラー**、し、**参照の追加**します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-117">Right-click on the **References** folder under the GettingStartedHost project in **Solution Explorer**, and then select **Add Reference**.</span></span> <span data-ttu-id="e5a01-118">**参照の追加**ダイアログ ボックスで、**ソリューション**ダイアログの左側にあるの ダイアログの中央のセクションで GettingStartedLib を選択し、**追加**します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-118">In the **Add Reference** dialog, select **Solution** on the left-hand side of the dialog, select GettingStartedLib in the center section of the dialog, and then choose **Add**.</span></span> <span data-ttu-id="e5a01-119">これにより、GettingStartedLib に定義されている型を GettingStartedHost プロジェクトで利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e5a01-119">This makes the types defined in GettingStartedLib available to the GettingStartedHost project.</span></span>

3. <span data-ttu-id="e5a01-120">System.ServiceModel への参照を GettingStartedHost プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-120">Add a reference to System.ServiceModel to the GettingStartedHost project.</span></span> <span data-ttu-id="e5a01-121">右クリックし、**参照**で GettingStartedHost プロジェクトの下のフォルダー**ソリューション エクスプ ローラー**選択**参照の追加**します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-121">Right-click the **References** folder under the GettingStartedHost project in **Solution Explorer** and select **Add Reference**.</span></span> <span data-ttu-id="e5a01-122">**参照の追加**ダイアログ ボックスで、 **Framework**ダイアログ ボックスの左側にある**アセンブリ**します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-122">In the **Add Reference** dialog, select **Framework** on the left-hand side of the dialog under **Assemblies**.</span></span> <span data-ttu-id="e5a01-123">検索して選択**System.ServiceModel**を選び、 **OK**。</span><span class="sxs-lookup"><span data-stu-id="e5a01-123">Find and select **System.ServiceModel**, and then choose **OK**.</span></span> <span data-ttu-id="e5a01-124">ソリューションを選択して保存**ファイル** > **すべて保存**します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-124">Save the solution by selecting **File** > **Save All**.</span></span>

## <a name="host-the-service"></a><span data-ttu-id="e5a01-125">サービスをホストします</span><span class="sxs-lookup"><span data-stu-id="e5a01-125">Host the service</span></span>

<span data-ttu-id="e5a01-126">Program.cs ファイルまたは Module.vb ファイルを開き、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-126">Open the Program.cs or Module.vb file and enter the following code:</span></span>

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
            Dim baseAddress As New Uri("http://localhost:8000/ServiceModelSamples/Service")

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

<span data-ttu-id="e5a01-127">**手順 1.** -サービスのベース アドレスを保持するために、Uri クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-127">**Step 1** - Creates an instance of the Uri class to hold the base address of the service.</span></span> <span data-ttu-id="e5a01-128">サービスは、ベース アドレスとオプションの URI を含む URL によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="e5a01-128">Services are identified by a URL which contains a base address and an optional URI.</span></span> <span data-ttu-id="e5a01-129">ベース アドレスの書式は、[トランスポート]://[コンピューター名またはドメイン][:省略可能なポート番号]/[省略可能な URI セグメント] です。電卓サービスのベース アドレスは、電卓サービスのベース アドレスを使用して HTTP トランスポート、localhost、ポート 8000、および URI セグメント "GettingStarted" を使用します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-129">The base address is formatted as follows:[transport]://[machine-name or domain][:optional port #]/[optional URI segment]The base address for the calculator service uses the HTTP transport, localhost, port 8000, and the URI segment "GettingStarted"</span></span>

<span data-ttu-id="e5a01-130">**手順 2** – のインスタンスを作成、<xref:System.ServiceModel.ServiceHost>クラス、サービスをホストします。</span><span class="sxs-lookup"><span data-stu-id="e5a01-130">**Step 2** – Creates an instance of the <xref:System.ServiceModel.ServiceHost> class to host the service.</span></span> <span data-ttu-id="e5a01-131">コンストラクターは、サービス コントラクトを実装するクラスの型と、サービスのベース アドレスの、2 つのパラメーターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="e5a01-131">The constructor takes two parameters, the type of the class that implements the service contract, and the base address of the service.</span></span>

<span data-ttu-id="e5a01-132">**手順 3** – 作成、<xref:System.ServiceModel.Description.ServiceEndpoint>インスタンス。</span><span class="sxs-lookup"><span data-stu-id="e5a01-132">**Step 3** – Creates a <xref:System.ServiceModel.Description.ServiceEndpoint> instance.</span></span> <span data-ttu-id="e5a01-133">サービス エンドポイントは、アドレス、バインディング、およびサービス コントラクトから構成されます。</span><span class="sxs-lookup"><span data-stu-id="e5a01-133">A service endpoint is composed of an address, a binding, and a service contract.</span></span> <span data-ttu-id="e5a01-134"><xref:System.ServiceModel.Description.ServiceEndpoint> コンストラクターは、サービス コントラクト インターフェイスの型、バインディング、およびアドレスを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="e5a01-134">The <xref:System.ServiceModel.Description.ServiceEndpoint> constructor therefore takes the service contract interface type, a binding, and an address.</span></span> <span data-ttu-id="e5a01-135">サービス コントラクトは、サービス型に定義および実装した `ICalculator` です。</span><span class="sxs-lookup"><span data-stu-id="e5a01-135">The service contract is `ICalculator`, which you defined and implement in the service type.</span></span> <span data-ttu-id="e5a01-136">このサンプルで使用するバインディングは、WS-\* 仕様に準拠するエンドポイントへの接続に使用される組み込みのバインディングである <xref:System.ServiceModel.WSHttpBinding> です。</span><span class="sxs-lookup"><span data-stu-id="e5a01-136">The binding used in this sample is <xref:System.ServiceModel.WSHttpBinding> which is a built-in binding that is used for connecting to endpoints that conform to the WS-\* specifications.</span></span> <span data-ttu-id="e5a01-137">WCF バインディングの詳細については、[WCF バインディングの概要](../../../docs/framework/wcf/bindings-overview.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5a01-137">For more information about WCF bindings, see [WCF Bindings Overview](../../../docs/framework/wcf/bindings-overview.md).</span></span> <span data-ttu-id="e5a01-138">エンドポイントを識別するために、ベース アドレスにアドレスが追加されます。</span><span class="sxs-lookup"><span data-stu-id="e5a01-138">The address is appended to the base address to identify the endpoint.</span></span> <span data-ttu-id="e5a01-139">このコードで指定されたアドレスは"CalculatorService"エンドポイントの完全修飾アドレスは`"http://localhost:8000/GettingStarted/CalculatorService"`します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-139">The address specified in this code is "CalculatorService" so the fully qualified address for the endpoint is `"http://localhost:8000/GettingStarted/CalculatorService"`.</span></span>

    > [!IMPORTANT]
    > Adding a service endpoint is optional when using .NET Framework 4 or later. In these versions, if no endpoints are added in code or configuration, WCF adds one default endpoint for each combination of base address and contract implemented by the service. For more information about default endpoints see [Specifying an Endpoint Address](../../../docs/framework/wcf/specifying-an-endpoint-address.md). For more information about default endpoints, bindings, and behaviors, see [Simplified Configuration](../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).

<span data-ttu-id="e5a01-140">**手順 4** – メタデータ交換を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e5a01-140">**Step 4** – Enable metadata exchange.</span></span> <span data-ttu-id="e5a01-141">クライアントは、サービス操作を呼び出すために使用されるプロキシの生成にメタデータ交換を使用します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-141">Clients will use metadata exchange to generate proxies that will be used to call the service operations.</span></span> <span data-ttu-id="e5a01-142">メタデータ交換を有効化するには、<xref:System.ServiceModel.Description.ServiceMetadataBehavior> インスタンスを作成してその <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> プロパティを `true` に設定し、動作を <xref:System.ServiceModel.ServiceHost> インスタンスの <!--zz <xref:System.ServiceModel.ServiceHost.Behaviors%2A>  -->`System.ServiceModel.ServiceHost.Behaviors%2A` コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-142">To enable metadata exchange create a <xref:System.ServiceModel.Description.ServiceMetadataBehavior> instance, set it’s <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> property to `true`, and add the behavior to the <!--zz <xref:System.ServiceModel.ServiceHost.Behaviors%2A>  -->`System.ServiceModel.ServiceHost.Behaviors%2A` collection of the <xref:System.ServiceModel.ServiceHost> instance.</span></span>

<span data-ttu-id="e5a01-143">**手順 5** – オープン、<xref:System.ServiceModel.ServiceHost>受信メッセージをリッスンします。</span><span class="sxs-lookup"><span data-stu-id="e5a01-143">**Step 5** – Open the <xref:System.ServiceModel.ServiceHost> to listen for incoming messages.</span></span> <span data-ttu-id="e5a01-144">コードでは、ユーザーによる Enter キーの押下を待機しています。</span><span class="sxs-lookup"><span data-stu-id="e5a01-144">Notice the code waits for the user to hit enter.</span></span> <span data-ttu-id="e5a01-145">この動作を行わない場合、アプリは直ちに終了し、サービスはシャットダウンします。また、try/catch ブロックが使用されている点にも注意してください。</span><span class="sxs-lookup"><span data-stu-id="e5a01-145">If you do not do this, the app will close immediately and the service will shut down.Also notice a  try/catch block used.</span></span> <span data-ttu-id="e5a01-146"><xref:System.ServiceModel.ServiceHost> がインスタンス化された後、他のコードはすべて try/catch ブロックに配置されます。</span><span class="sxs-lookup"><span data-stu-id="e5a01-146">After the <xref:System.ServiceModel.ServiceHost> has been instantiated, all other code is placed in a try/catch block.</span></span> <span data-ttu-id="e5a01-147"><xref:System.ServiceModel.ServiceHost> によってスローされた例外を安全にキャッチする方法の詳細については、「[Avoiding Problems with the Using Statement](../../../docs/framework/wcf/samples/avoiding-problems-with-the-using-statement.md)」 (using ステートメントで問題を回避する) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5a01-147">For more information about safely catching exceptions thrown by <xref:System.ServiceModel.ServiceHost>, see [Avoiding Problems with the Using Statement](../../../docs/framework/wcf/samples/avoiding-problems-with-the-using-statement.md)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5a01-148">コードで行われた変更を反映するように GettingStartedLib で App.config を編集します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-148">Edit App.config in GettingStartedLib to reflect the changes made in code:</span></span>
> 1. <span data-ttu-id="e5a01-149">14 行を変更します。 `<service name="GettingStartedLib.CalculatorService">`</span><span class="sxs-lookup"><span data-stu-id="e5a01-149">Change line 14 to `<service name="GettingStartedLib.CalculatorService">`</span></span>
> 2. <span data-ttu-id="e5a01-150">行 17 を変更します。 `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`</span><span class="sxs-lookup"><span data-stu-id="e5a01-150">Change line 17 to `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`</span></span>
> 3. <span data-ttu-id="e5a01-151">変更するには、22 行目 `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.ICalculator">`</span><span class="sxs-lookup"><span data-stu-id="e5a01-151">Change line 22 to `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.ICalculator">`</span></span>

## <a name="verify-the-service-is-working"></a><span data-ttu-id="e5a01-152">サービスが動作を確認します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-152">Verify the service is working</span></span>

1. <span data-ttu-id="e5a01-153">GettingStartedHost コンソールを実行する Visual Studio 内からアプリケーション。</span><span class="sxs-lookup"><span data-stu-id="e5a01-153">Run the GettingStartedHost console application from inside Visual Studio.</span></span>

   <span data-ttu-id="e5a01-154">サービスは、管理者特権で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5a01-154">The service must be run with administrator privileges.</span></span> <span data-ttu-id="e5a01-155">Visual Studio が管理者特権で開いた、GettingStartedHost も管理者特権で実行されます。</span><span class="sxs-lookup"><span data-stu-id="e5a01-155">Because Visual Studio was opened with administrator privileges, GettingStartedHost is also run with administrator privileges.</span></span> <span data-ttu-id="e5a01-156">使用して新しいコマンド プロンプトを開くことができますも**管理者として実行**内に service.exe を実行します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-156">You can also open a new command prompt using **Run as administrator** and run service.exe within it.</span></span>

2. <span data-ttu-id="e5a01-157">Web ブラウザーを開き、サービスのデバッグ ページを参照`http://localhost:8000/GettingStarted/CalculatorService`します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-157">Open a web browser and browse to the service's debug page at `http://localhost:8000/GettingStarted/CalculatorService`.</span></span>

## <a name="example"></a><span data-ttu-id="e5a01-158">例</span><span class="sxs-lookup"><span data-stu-id="e5a01-158">Example</span></span>

<span data-ttu-id="e5a01-159">次の例では、チュートリアルの前の手順で作成したサービス コントラクトと実装を含め、コンソール アプリケーションでサービスをホストします。</span><span class="sxs-lookup"><span data-stu-id="e5a01-159">The following example includes the service contract and implementation from previous steps in the tutorial and hosts the service in a console application.</span></span>

<span data-ttu-id="e5a01-160">コマンド ライン コンパイラでコンパイルを参照するクラス ライブラリに IService1.cs と Service1.cs をコンパイル`System.ServiceModel.dll`します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-160">To compile this with a command-line compiler, compile IService1.cs and Service1.cs into a class library that references `System.ServiceModel.dll`.</span></span> <span data-ttu-id="e5a01-161">Program.cs をコンソール アプリケーションとしてコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="e5a01-161">Compile Program.cs as a console application.</span></span>

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
            Uri baseAddress = new Uri("http://localhost:8000/ServiceModelSamples/Service");

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
            Dim baseAddress As New Uri("http://localhost:8000/ServiceModelSamples/Service")

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
> <span data-ttu-id="e5a01-162">このようなサービスには、リッスンを行うコンピューター上で HTTP アドレスを登録するためのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="e5a01-162">Services such as this one require permission to register HTTP addresses on the machine for listening.</span></span> <span data-ttu-id="e5a01-163">管理者アカウントにはこのアクセス許可がありますが、管理者以外のアカウントの場合は、HTTP 名前空間へのアクセス許可を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5a01-163">Administrator accounts have this permission, but non-administrator accounts must be granted permission for HTTP namespaces.</span></span> <span data-ttu-id="e5a01-164">名前空間の予約を構成する方法については、「[Configuring HTTP and HTTPS](../../../docs/framework/wcf/feature-details/configuring-http-and-https.md)」 (HTTP と HTTPS を構成する) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5a01-164">For more information about how to configure namespace reservations, see [Configuring HTTP and HTTPS](../../../docs/framework/wcf/feature-details/configuring-http-and-https.md).</span></span> <span data-ttu-id="e5a01-165">Visual Studio で service.exe を実行するには、管理者権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="e5a01-165">When running under Visual Studio, the service.exe must be run with administrator privileges.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e5a01-166">次の手順</span><span class="sxs-lookup"><span data-stu-id="e5a01-166">Next steps</span></span>

<span data-ttu-id="e5a01-167">これでサービスが実行されていることが確認できました。</span><span class="sxs-lookup"><span data-stu-id="e5a01-167">Now the service is running.</span></span> <span data-ttu-id="e5a01-168">次のタスクでは、WCF クライアントを作成します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-168">In the next task, you create a WCF client.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="e5a01-169">方法: WCF クライアントを作成します。</span><span class="sxs-lookup"><span data-stu-id="e5a01-169">How to: Create a WCF client</span></span>](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)

<span data-ttu-id="e5a01-170">トラブルシューティングについては、「[Troubleshooting the Getting Started Tutorial](../../../docs/framework/wcf/troubleshooting-the-getting-started-tutorial.md)」 (チュートリアル入門のトラブルシューティング) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5a01-170">For troubleshooting information, see [Troubleshooting the Getting Started Tutorial](../../../docs/framework/wcf/troubleshooting-the-getting-started-tutorial.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e5a01-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5a01-171">See also</span></span>

- [<span data-ttu-id="e5a01-172">はじめに</span><span class="sxs-lookup"><span data-stu-id="e5a01-172">Getting Started</span></span>](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [<span data-ttu-id="e5a01-173">自己ホスト</span><span class="sxs-lookup"><span data-stu-id="e5a01-173">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)