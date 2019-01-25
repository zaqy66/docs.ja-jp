---
title: メッセージ レベルのプログラミングによる JSON 形式でのシリアル化
ms.date: 03/30/2017
ms.assetid: 5f940ba2-57ee-4c49-a779-957c5e7e71fa
ms.openlocfilehash: 39e6eaf138ee4f4946a876f492457831cbbbf80a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54663051"
---
# <a name="serializing-in-json-with-message-level-programming"></a>メッセージ レベルのプログラミングによる JSON 形式でのシリアル化
WCF は、JSON 形式でのデータのシリアル化をサポートします。 このトピックでは、<xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> を使用して型をシリアル化することを WCF に命令する方法について説明します。  
  
## <a name="typed-message-programming"></a>型指定されたメッセージのプログラミング  
 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> は、<xref:System.ServiceModel.Web.WebGetAttribute> または <xref:System.ServiceModel.Web.WebInvokeAttribute> がサービス操作に適用されるときに使用されます。 どちらの属性でも、`RequestFormat` と `ResponseFormat` を指定できます。 要求と応答に JSON を使用するには、両方の属性を `WebMessageFormat.Json` に設定します。  JSON を使用するには、<xref:System.ServiceModel.WebHttpBinding> を使用する必要があります。これにより、<xref:System.ServiceModel.Description.WebHttpBehavior> が自動的に構成されます。 WCF のシリアル化の詳細についてを参照してください。[シリアル化および逆シリアル化](../../../../docs/framework/wcf/feature-details/serialization-and-deserialization.md)、 [Windows Communication Foundation でのシリアル化](https://msdn.microsoft.com/magazine/cc163569.aspx)します。 JSON と WCF の詳細については、次を参照してください[An Introduction to WCF を使用した RESTfull サービス](https://msdn.microsoft.com/magazine/dd315413.aspx)、 [.NET 3.5 の WCF サービスの JSON の作成が有効な](https://www.pluralsight-training.net/community/blogs/fritz/archive/2008/01/31/50121.aspx)、および[WCFでRESTの概要](https://msdn.microsoft.com/netframework/dd547388).  
  
> [!IMPORTANT]
>  JSON を使用するには、SOAP 通信をサポートしていない <xref:System.ServiceModel.WebHttpBinding> と <xref:System.ServiceModel.Description.WebHttpBehavior> を使用する必要があります。 サービスと通信する、<xref:System.ServiceModel.WebHttpBinding>サービス メタデータの公開はサポートされないので、Visual Studio のサービス参照の追加機能または svcutil コマンド ライン ツールを使用して、クライアント側プロキシを生成することはできません。 使用するサービスのプログラムでを呼び出す方法の詳細<xref:System.ServiceModel.WebHttpBinding>を参照してください[WCF で REST サービスを使用する方法](https://blogs.msdn.com/b/pedram/archive/2008/04/21/how-to-consume-rest-services-with-wcf.aspx)します。  
  
## <a name="untyped-message-programming"></a>型指定されていないメッセージのプログラミング  
 型指定されていないメッセージ オブジェクトを直接操作する場合は、型指定されていないメッセージのプロパティを明示的に設定して JSON としてシリアル化する必要があります。 これを行う方法を次のコード スニペットに示します。  
  
```  
 Message response = Message.CreateMessage(  
                  MessageVersion.None,    // No SOAP message version  
                             "*",                     // SOAP action, ignored since this is JSON  
                             "Response string: JSON format specified", // Message body  
                             new DataContractJsonSerializer(typeof(string))); // Specify DataContractJsonSerializer  
      response.Properties.Add( WebBodyFormatMessageProperty.Name,   
                    new WebBodyFormatMessageProperty(WebContentFormat.Json)); // Use JSON format  
```  
  
## <a name="see-also"></a>関連項目
- [AJAX の統合と JSON のサポート](../../../../docs/framework/wcf/feature-details/ajax-integration-and-json-support.md)
- [スタンドアロン JSON のシリアル化](../../../../docs/framework/wcf/feature-details/stand-alone-json-serialization.md)
- [JSON シリアル化](../../../../docs/framework/wcf/samples/json-serialization.md)
