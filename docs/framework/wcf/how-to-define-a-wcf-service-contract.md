---
title: '方法 : Windows Communication Foundation サービス コントラクトを定義する'
ms.date: 09/14/2018
helpviewer_keywords:
- service contracts [WCF], defining
dev_langs:
- CSharp
- VB
ms.assetid: 67bf05b7-1d08-4911-83b7-a45d0b036fc3
ms.openlocfilehash: 4f85a51c47eb045d1d2f0111cb217199c9acf0d7
ms.sourcegitcommit: f513a91160b3fec289dd06646d0d6f81f8fcf910
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/18/2018
ms.locfileid: "46009009"
---
# <a name="how-to-define-a-windows-communication-foundation-service-contract"></a><span data-ttu-id="79f0d-102">方法 : Windows Communication Foundation サービス コントラクトを定義する</span><span class="sxs-lookup"><span data-stu-id="79f0d-102">How to: Define a Windows Communication Foundation Service Contract</span></span>

<span data-ttu-id="79f0d-103">これは、最初の基本的な Windows Communication Foundation (WCF) アプリケーションを作成するために必要な 6 つのタスクです。</span><span class="sxs-lookup"><span data-stu-id="79f0d-103">This is the first of six tasks required to create a basic Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="79f0d-104">6 つのすべてのタスクの概要については、「[チュートリアル入門](../../../docs/framework/wcf/getting-started-tutorial.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="79f0d-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) topic.</span></span>

 <span data-ttu-id="79f0d-105">WCF サービスを作成するときに、最初のタスクは、サービス コントラクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-105">When creating a WCF service, the first task is to define a service contract.</span></span> <span data-ttu-id="79f0d-106">サービス コントラクトは、サービスがサポートする操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-106">The service contract specifies what operations the service supports.</span></span> <span data-ttu-id="79f0d-107">操作は Web サービス メソッドと見なすことができます。</span><span class="sxs-lookup"><span data-stu-id="79f0d-107">An operation can be thought of as a Web service method.</span></span> <span data-ttu-id="79f0d-108">コントラクトは C++、C#、または Visual Basic (VB) インターフェイスを定義することで作成します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-108">Contracts are created by defining a C++, C#, or Visual Basic (VB) interface.</span></span> <span data-ttu-id="79f0d-109">インターフェイスの各メソッドは、特定のサービス操作に対応しています。</span><span class="sxs-lookup"><span data-stu-id="79f0d-109">Each method in the interface corresponds to a specific service operation.</span></span> <span data-ttu-id="79f0d-110">各インターフェイスには <xref:System.ServiceModel.ServiceContractAttribute> が適用されており、各操作には <xref:System.ServiceModel.OperationContractAttribute> 属性が適用されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="79f0d-110">Each interface must have the <xref:System.ServiceModel.ServiceContractAttribute> applied to it and each operation must have the <xref:System.ServiceModel.OperationContractAttribute> attribute applied to it.</span></span> <span data-ttu-id="79f0d-111"><xref:System.ServiceModel.ServiceContractAttribute> 属性を持つインターフェイス内のメソッドに <xref:System.ServiceModel.OperationContractAttribute> 属性がない場合、そのメソッドはサービスによって公開されません。</span><span class="sxs-lookup"><span data-stu-id="79f0d-111">If a method within an interface that has the <xref:System.ServiceModel.ServiceContractAttribute> attribute does not have the <xref:System.ServiceModel.OperationContractAttribute> attribute, that method is not exposed by the service.</span></span>

 <span data-ttu-id="79f0d-112">手順の後に、このタスクに使用するコード例を示します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-112">The code used for this task is provided in the example following the procedure.</span></span>

## <a name="define-a-service-contract"></a><span data-ttu-id="79f0d-113">サービス コントラクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-113">Define a service contract</span></span>

1. <span data-ttu-id="79f0d-114">プログラムを右クリックして、管理者として Visual Studio を開き、**開始**メニュー**詳細** > **管理者として実行**します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-114">Open Visual Studio as an administrator by right-clicking the program in the **Start** menu and selecting **More** > **Run as administrator**.</span></span>

2. <span data-ttu-id="79f0d-115">WCF サービス ライブラリ プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-115">Create a WCF Service Library project.</span></span>

   1. <span data-ttu-id="79f0d-116">**[ファイル]** メニューで、**[新規作成]**、 > **[プロジェクト]** の順に作成します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-116">From the **File** menu, select **New** > **Project**.</span></span>

   2. <span data-ttu-id="79f0d-117">**新しいプロジェクト**] ダイアログの左側にある [展開**Visual c#** または**Visual Basic**、クリックして、 **WCF**カテゴリ。</span><span class="sxs-lookup"><span data-stu-id="79f0d-117">In the **New Project** dialog, on the left-hand side, expand **Visual C#** or **Visual Basic**, and then select the **WCF** category.</span></span> <span data-ttu-id="79f0d-118">プロジェクト テンプレートの一覧は、ダイアログの中央のセクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="79f0d-118">A list of project templates is displayed in the center section of the dialog.</span></span> <span data-ttu-id="79f0d-119">選択**WCF サービス ライブラリ**します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-119">Select **WCF Service Library**.</span></span>

   3. <span data-ttu-id="79f0d-120">入力`GettingStartedLib`で、**名前**textbox と`GettingStarted`で、**ソリューション名**ダイアログの下部にあるテキスト ボックス。</span><span class="sxs-lookup"><span data-stu-id="79f0d-120">Enter `GettingStartedLib` in the **Name** textbox and `GettingStarted` in the **Solution name** textbox at the bottom of the dialog.</span></span>

   > [!NOTE]
   > <span data-ttu-id="79f0d-121">表示されない場合、 **WCF**プロジェクト テンプレートのカテゴリをインストールする必要があります、 **Windows Communication Foundation** Visual Studio のコンポーネント。</span><span class="sxs-lookup"><span data-stu-id="79f0d-121">If you don't see the **WCF** project template category, you may need to install the **Windows Communication Foundation** component of Visual Studio.</span></span> <span data-ttu-id="79f0d-122">**新しいプロジェクト** ダイアログ ボックスと書かれたリンクをクリックして**Visual Studio インストーラーを開く**します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-122">In the **New Project** dialog box, click the link that says **Open Visual Studio Installer**.</span></span> <span data-ttu-id="79f0d-123">選択、**個々 のコンポーネント**] タブの [、し、検索して選択します**Windows Communication Foundation**下、**開発アクティビティ**カテゴリ。</span><span class="sxs-lookup"><span data-stu-id="79f0d-123">Select the **Individual Components** tab, and then find and select **Windows Communication Foundation** under the **Development activities** category.</span></span> <span data-ttu-id="79f0d-124">選択**変更**コンポーネントのインストールを開始します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-124">Choose **Modify** to begin installing the component.</span></span>

   <span data-ttu-id="79f0d-125">Visual Studio は、3 つのファイルを含むプロジェクトを作成します: IService1.cs (または IService1.vb)、Service1.cs (または Service1.vb) と App.config です。IService1 ファイルには、既定のサービス コントラクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="79f0d-125">Visual Studio creates the project, which contains 3 files: IService1.cs (or IService1.vb), Service1.cs (or Service1.vb), and App.config. The IService1 file contains a default service contract.</span></span> <span data-ttu-id="79f0d-126">Service1 ファイルには、サービス コントラクトの既定の実装が含まれています。</span><span class="sxs-lookup"><span data-stu-id="79f0d-126">The Service1 file contains a default implementation of the service contract.</span></span> <span data-ttu-id="79f0d-127">App.config ファイルには、Visual Studio WCF サービス ホストに既定のサービスを読み込むために必要な構成が含まれています。</span><span class="sxs-lookup"><span data-stu-id="79f0d-127">The App.config file contains configuration needed to load the default service with the Visual Studio WCF Service Host.</span></span> <span data-ttu-id="79f0d-128">WCF サービス ホスト ツールの詳細については、次を参照してください[WCF サービス ホスト (WcfSvcHost.exe)。](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)</span><span class="sxs-lookup"><span data-stu-id="79f0d-128">For more information about the WCF Service Host tool, see [WCF Service Host (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)</span></span>

3. <span data-ttu-id="79f0d-129">IService1.cs または IService1.vb ファイルを開き、名前空間宣言を残して、名前空間の宣言内のコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-129">Open the IService1.cs or IService1.vb file and delete the code within the namespace declaration, leaving the namespace declaration.</span></span> <span data-ttu-id="79f0d-130">次のコードに示すように、名前空間宣言内に新しいインターフェイス `ICalculator` を定義します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-130">Inside the namespace declaration define a new interface called `ICalculator` as shown in the code below.</span></span>

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

     <span data-ttu-id="79f0d-131">このコントラクトは、オンライン電卓を定義します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-131">This contract defines an online calculator.</span></span> <span data-ttu-id="79f0d-132">`ICalculator` インターフェイスは <xref:System.ServiceModel.ServiceContractAttribute> 属性でマークされています。</span><span class="sxs-lookup"><span data-stu-id="79f0d-132">Notice the `ICalculator` interface is marked with the <xref:System.ServiceModel.ServiceContractAttribute> attribute.</span></span> <span data-ttu-id="79f0d-133">この属性は、コントラクト名を区別するために使用される名前空間を定義します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-133">This attribute defines a namespace that is used to disambiguate the contract name.</span></span> <span data-ttu-id="79f0d-134">各電卓操作は <xref:System.ServiceModel.OperationContractAttribute> 属性でマークされています。</span><span class="sxs-lookup"><span data-stu-id="79f0d-134">Each calculator operation is marked with the <xref:System.ServiceModel.OperationContractAttribute> attribute.</span></span>

## <a name="next-steps"></a><span data-ttu-id="79f0d-135">次の手順</span><span class="sxs-lookup"><span data-stu-id="79f0d-135">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="79f0d-136">方法: サービス コントラクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="79f0d-136">How to: Implement a service contract</span></span>](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)

## <a name="see-also"></a><span data-ttu-id="79f0d-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="79f0d-137">See also</span></span>

- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>
- [<span data-ttu-id="79f0d-138">方法: サービス コントラクトを実装する</span><span class="sxs-lookup"><span data-stu-id="79f0d-138">How to: Implement a Service Contract</span></span>](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)
- [<span data-ttu-id="79f0d-139">はじめに</span><span class="sxs-lookup"><span data-stu-id="79f0d-139">Getting Started</span></span>](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [<span data-ttu-id="79f0d-140">自己ホスト</span><span class="sxs-lookup"><span data-stu-id="79f0d-140">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)