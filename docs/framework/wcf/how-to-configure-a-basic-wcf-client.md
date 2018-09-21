---
title: '方法 : 基本的な Windows Communication Foundation クライアントを構成する'
ms.date: 09/14/2018
helpviewer_keywords:
- WCF clients [WCF], configuring
ms.assetid: d067b86d-afb0-47bf-94f6-45180a3d8d78
ms.openlocfilehash: 3f267edf87711de8a5969e3e0b577648008c5a75
ms.sourcegitcommit: dfb2a100cfb4d3902c042f17b3204f49bc7635e7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2018
ms.locfileid: "46524864"
---
# <a name="how-to-configure-a-basic-windows-communication-foundation-client"></a>方法 : 基本的な Windows Communication Foundation クライアントを構成する

これは、5 番目の基本的な Windows Communication Foundation (WCF) アプリケーションを作成するために必要な 6 つのタスクです。 6 つのすべてのタスクの概要については、「[チュートリアル入門](../../../docs/framework/wcf/getting-started-tutorial.md)」を参照してください。

このトピックで説明を使用して生成されたクライアント構成ファイル、**サービス参照の追加**Visual Studio の機能または[ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)します。 クライアントを構成するには、クライアントがサービスにアクセスするために使用するエンドポイントを指定します。 エンドポイントが、アドレス、バインディング、およびコントラクト、およびこれらの各クライアントを構成する過程で指定する必要があります。

## <a name="configure-a-windows-communication-foundation-client"></a>Windows Communication Foundation クライアントを構成します。

GettingStartedClient プロジェクトから生成された構成ファイル (App.config) を開きます。 生成された構成ファイルを次の例に示します。 [\<system.serviceModel >](../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)セクションの下にある [\<endpoint >](https://msdn.microsoft.com/library/13aa23b7-2f08-4add-8dbf-a99f8127c017)要素を見つけてください。

```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
        <startup>
          <!-- specifies the version of WCF to use-->
            <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5,Profile=Client" />
        </startup>
        <system.serviceModel>
            <bindings>
                <!-- Uses wsHttpBinding-->
                <wsHttpBinding>
                    <binding name="WSHttpBinding_ICalculator" />
                </wsHttpBinding>
            </bindings>
            <client>
                <!-- specifies the endpoint to use when calling the service -->
                <endpoint address="http://localhost:8000/ServiceModelSamples/Service/CalculatorService"
                    binding="wsHttpBinding" bindingConfiguration="WSHttpBinding_ICalculator"
                    contract="ServiceReference1.ICalculator" name="WSHttpBinding_ICalculator">
                    <identity>
                        <userPrincipalName value="migree@redmond.corp.microsoft.com" />
                    </identity>
                </endpoint>
            </client>
        </system.serviceModel>
    </configuration>
```

この例では、次のアドレスにあるサービスにアクセスするクライアントが使用するエンドポイント:`http://localhost:8000/ServiceModelSamples/Service/CalculatorService`します。

endpoint 要素は、`ServiceReference1.ICalculator` サービス コントラクトが、WCF クライアントと WCF サービス間の通信に使用されるように指定します。 WCF チャネルはシステム標準の <xref:System.ServiceModel.WSHttpBinding> で構成されます。 このコントラクトを使用して生成された**サービス参照の追加**Visual Studio でします。 基本的には、GettingStartedLib プロジェクトで定義されているコントラクトのコピーです。 <xref:System.ServiceModel.WSHttpBinding> バインディングは、トランスポートとして HTTP を指定し、相互運用可能なセキュリティ、およびその他の構成詳細を指定します。

この構成で生成されたクライアントを使用する方法の詳細については、次を参照してください。[方法: クライアントを使用して](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)します。

## <a name="next-steps"></a>次の手順

> [!div class="nextstepaction"]
> [方法: WCF クライアントを使用](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)

## <a name="see-also"></a>関連項目

- [サービスとクライアントを構成するためのバインディングの使用](../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [方法: クライアントを作成する](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)
- [はじめに](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [自己ホスト](../../../docs/framework/wcf/samples/self-host.md)