# <a name="using-dotnet-svcutilxmlserializer-on-net-core"></a>.NET Core で dotnet-svcutil.xmlserializer を使用する

## <a name="prerequisites"></a>必須コンポーネント

dotnet-svcutil.xmlserializer が機能するには、以下が必要です。 

* [.NET Core 2.1 SDK](https://www.microsoft.com/net/download/dotnet-core/sdk-2.1.300) 以降
* [.NET Core Runtime 2.1 以降](https://www.microsoft.com/net/download/dotnet-core/runtime-2.1.0)

コマンド `dotnet --info` を使用して、既にインストールされている .NET Core SDK およびランタイムのバージョンを確認することができます。

.NET Core コンソール アプリケーションで dotnet-svcutil.xmlserializer を使用するには:

1. .NET Framework で既定のテンプレート 'WCF Service Application' を使用して、'MyWCFService' という名前の WCF サービスを作成します。  次のようなサービス メソッドに ```[XmlSerializerFormat]``` 属性を追加します
    ```c#
    [ServiceContract]
    public interface IService1
    {
        [XmlSerializerFormat]
        [OperationContract(Action = "http://tempuri.org/IService1/GetData", ReplyAction = "http://tempuri.org/IService1/GetDataResponse")]
        string GetData(int value);
    }
    ```
2. netcoreapp 2.1 をターゲットとする WCF クライアント アプリケーションとして .NET Core コンソール アプリケーションを作成します。たとえば、コマンドで 'MyWCFClient' という名前のアプリを作成します。
    ```
    dotnet new console --name MyWCFClient
    ```
    csproj が netcoreapp 2.1 をターゲットにしていることを確認します。 これは、.csproj ファイル内の次の XML 要素を使用して行われます
    ```xml
    <TargetFramework>netcoreapp2.1</TargetFramework>
    ```
3. 次のコマンドを実行して、System.ServiceModel.Http へのパッケージ参照を追加します。
   
   ```dotnet add package System.ServiceModel.Http -v 4.5.0```

4. WCF クライアント コードを追加します。
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
5. .csproj ファイルを編集し、dotnet-svcutil.xmlserializer パッケージへの参照を追加します。 次に例を示します。

    i. コマンド `dotnet add package dotnet-svcutil.xmlserializer -v 1.0.0` を実行します。

    ii. MyWCFClient.csproj に次の行を追加します。
    ```xml
    <ItemGroup>
      <DotNetCliToolReference Include="dotnet-svcutil.xmlserializer" Version="1.0.0" />
    </ItemGroup>
    ```

6. `dotnet build` を実行してアプリケーションをビルドします。 すべて正常に終了すると、出力フォルダーに MyWCFClient.XmlSerializers.dll という名前のアセンブリが生成されます。 ツールがアセンブリの生成に失敗した場合は、ビルド出力に警告が表示されます。

7. ブラウザーで http://localhost:2561/Service1.svc を実行するなどして、WCF サービスを開始します。 次にクライアント アプリケーションを起動します。実行時に、事前に生成されたシリアライザーが自動的に読み込まれ、使用されます。
