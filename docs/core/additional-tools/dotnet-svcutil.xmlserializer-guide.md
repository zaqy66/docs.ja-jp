# <a name="using-dotnet-svcutilxmlserializer-on-net-core"></a><span data-ttu-id="d9992-101">.NET Core で dotnet-svcutil.xmlserializer を使用する</span><span class="sxs-lookup"><span data-stu-id="d9992-101">Using dotnet-svcutil.xmlserializer on .NET Core</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d9992-102">必須コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d9992-102">Prerequisites</span></span>

<span data-ttu-id="d9992-103">dotnet-svcutil.xmlserializer が機能するには、以下が必要です。</span><span class="sxs-lookup"><span data-stu-id="d9992-103">The following is required for dotnet-svcutil.xmlserializer to work.</span></span> 

* <span data-ttu-id="d9992-104">[.NET Core 2.1 SDK](https://www.microsoft.com/net/download/dotnet-core/sdk-2.1.300) 以降</span><span class="sxs-lookup"><span data-stu-id="d9992-104">[.NET Core 2.1 SDK or later](https://www.microsoft.com/net/download/dotnet-core/sdk-2.1.300)</span></span>
* [<span data-ttu-id="d9992-105">.NET Core Runtime 2.1 以降</span><span class="sxs-lookup"><span data-stu-id="d9992-105">.NET Core Runtime 2.1 or later</span></span>](https://www.microsoft.com/net/download/dotnet-core/runtime-2.1.0)

<span data-ttu-id="d9992-106">コマンド `dotnet --info` を使用して、既にインストールされている .NET Core SDK およびランタイムのバージョンを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="d9992-106">You can use the command `dotnet --info` to check which versions of .NET Core SDK and runtime you already have installed.</span></span>

<span data-ttu-id="d9992-107">.NET Core コンソール アプリケーションで dotnet-svcutil.xmlserializer を使用するには:</span><span class="sxs-lookup"><span data-stu-id="d9992-107">To use dotnet-svcutil.xmlserializer in a .NET Core console application:</span></span>

1. <span data-ttu-id="d9992-108">.NET Framework で既定のテンプレート 'WCF Service Application' を使用して、'MyWCFService' という名前の WCF サービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="d9992-108">Create a WCF Service named 'MyWCFService' using the default template 'WCF Service Application' in .NET Framework.</span></span>  <span data-ttu-id="d9992-109">次のようなサービス メソッドに ```[XmlSerializerFormat]``` 属性を追加します</span><span class="sxs-lookup"><span data-stu-id="d9992-109">Add ```[XmlSerializerFormat]``` attribute on the service method like the following</span></span>
    ```c#
    [ServiceContract]
    public interface IService1
    {
        [XmlSerializerFormat]
        [OperationContract(Action = "http://tempuri.org/IService1/GetData", ReplyAction = "http://tempuri.org/IService1/GetDataResponse")]
        string GetData(int value);
    }
    ```
2. <span data-ttu-id="d9992-110">netcoreapp 2.1 をターゲットとする WCF クライアント アプリケーションとして .NET Core コンソール アプリケーションを作成します。たとえば、コマンドで 'MyWCFClient' という名前のアプリを作成します。</span><span class="sxs-lookup"><span data-stu-id="d9992-110">Create a .NET Core console application as WCF client application that targets at netcoreapp 2.1, e.g. create an app named 'MyWCFClient' with the command,</span></span>
    ```
    dotnet new console --name MyWCFClient
    ```
    <span data-ttu-id="d9992-111">csproj が netcoreapp 2.1 をターゲットにしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d9992-111">Make sure your csproj targets a netcoreapp 2.1.</span></span> <span data-ttu-id="d9992-112">これは、.csproj ファイル内の次の XML 要素を使用して行われます</span><span class="sxs-lookup"><span data-stu-id="d9992-112">This is done using the following XML element in your .csproj file</span></span>
    ```xml
    <TargetFramework>netcoreapp2.1</TargetFramework>
    ```
3. <span data-ttu-id="d9992-113">次のコマンドを実行して、System.ServiceModel.Http へのパッケージ参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="d9992-113">Add a package reference to System.ServiceModel.Http by running the following command:</span></span>
   
   ```dotnet add package System.ServiceModel.Http -v 4.5.0```

4. <span data-ttu-id="d9992-114">WCF クライアント コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d9992-114">Add the WCF Client code:</span></span>
    ```csharp
    using System.ServiceModel;
    
    class Program
    {
        static void Main(string[] args)
        {
            var myBinding = new BasicHttpBinding();
            var myEndpoint = new EndpointAddress("http://localhost:2561/Service1.svc"); //Fill your service url here
            var myChannelFactory = new ChannelFactory<IService1>(myBinding, myEndpoint);
            IService1 client = myChannelFactory.CreateChannel();
            string s = client.GetData(1);
            ((ICommunicationObject)client).Close();
        }
    }

    [ServiceContract]
    public interface IService1
    {
        [XmlSerializerFormat]
        [OperationContract(Action = "http://tempuri.org/IService1/GetData", ReplyAction = "http://tempuri.org/IService1/GetDataResponse")]
        string GetData(int value);
    }
    ```
5. <span data-ttu-id="d9992-115">.csproj ファイルを編集し、dotnet-svcutil.xmlserializer パッケージへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="d9992-115">Edit the .csproj file and add a reference to the dotnet-svcutil.xmlserializer package.</span></span> <span data-ttu-id="d9992-116">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="d9992-116">For example:</span></span>

    <span data-ttu-id="d9992-117">i.</span><span class="sxs-lookup"><span data-stu-id="d9992-117">i.</span></span> <span data-ttu-id="d9992-118">コマンド `dotnet add package dotnet-svcutil.xmlserializer -v 1.0.0` を実行します。</span><span class="sxs-lookup"><span data-stu-id="d9992-118">Run command: `dotnet add package dotnet-svcutil.xmlserializer -v 1.0.0`</span></span>

    <span data-ttu-id="d9992-119">ii.</span><span class="sxs-lookup"><span data-stu-id="d9992-119">ii.</span></span> <span data-ttu-id="d9992-120">MyWCFClient.csproj に次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d9992-120">Add the following lines in MyWCFClient.csproj,</span></span>
    ```xml
    <ItemGroup>
      <DotNetCliToolReference Include="dotnet-svcutil.xmlserializer" Version="1.0.0" />
    </ItemGroup>
    ```

6. <span data-ttu-id="d9992-121">`dotnet build` を実行してアプリケーションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="d9992-121">Build the application by running `dotnet build`.</span></span> <span data-ttu-id="d9992-122">すべて正常に終了すると、出力フォルダーに MyWCFClient.XmlSerializers.dll という名前のアセンブリが生成されます。</span><span class="sxs-lookup"><span data-stu-id="d9992-122">If everything succeeds, an assembly named MyWCFClient.XmlSerializers.dll will be generated in the output folder.</span></span> <span data-ttu-id="d9992-123">ツールがアセンブリの生成に失敗した場合は、ビルド出力に警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d9992-123">You will see warnings in the build output if the tool failed to generate the assembly.</span></span>

7. <span data-ttu-id="d9992-124">ブラウザーで http://localhost:2561/Service1.svc を実行するなどして、WCF サービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="d9992-124">Start the WCF service e.g. by running http://localhost:2561/Service1.svc in the browser.</span></span> <span data-ttu-id="d9992-125">次にクライアント アプリケーションを起動します。実行時に、事前に生成されたシリアライザーが自動的に読み込まれ、使用されます。</span><span class="sxs-lookup"><span data-stu-id="d9992-125">Then start the client application, and it will automatically load and use the pre-generated serializers at runtime.</span></span>
