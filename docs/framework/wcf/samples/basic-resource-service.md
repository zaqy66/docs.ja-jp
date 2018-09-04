---
title: 基本的なリソース サービス
ms.date: 03/30/2017
ms.assetid: 4360063e-cc8c-4648-846e-c05a5af51a7a
ms.openlocfilehash: 2d55aecfdf6579b1de4c0cc324e59e23c251b12d
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43520137"
---
# <a name="basic-resource-service"></a>基本的なリソース サービス
このサンプルでは、取得をサポートしている顧客のコレクションを公開する Windows Communication Foundation (WCF) REST プログラミング モデルを使用して HTTP ベースのサービスを実装する、追加、削除、および置換操作する方法を示します。 このサンプルでは、自己ホスト型 WCF HTTP サービス (Service.cs) と、コンソール アプリケーション (program.cs) の呼び出しになり、サービスを作成する 2 つのコンポーネントで構成されます。  
  
## <a name="sample-details"></a>サンプルの詳細  
 WCF サービスは、リソース指向の REST 方式で顧客のコレクションを公開します。 つまり、顧客のコレクションには一意の URI があり、コレクションにはすべての顧客が含まれます。 このサービスは、コレクション全体を取得するための、コレクションの URI への HTTP `GET` の送信と、新しい顧客をコレクションに追加するための、コレクションの URI への HTTP `POST` の送信をサポートしています。 また、個々の顧客の URI では、顧客の詳細を取得する HTTP `GET`、顧客の詳細を置換する HTTP `PUT`、コレクションから顧客を削除する HTTP `DELETE` をサポートしています。 新しい顧客がコレクションに追加されると、サービスはその顧客に一意の URI を割り当て、顧客の詳細の一部として URI を格納します。 また、応答の Location HTTP ヘッダーを使用して、クライアントの URI と通信します。  
  
 App.config ファイルでは、<xref:System.ServiceModel.Description.WebHttpEndpoint> に設定されている <xref:System.ServiceModel.Description.WebHttpEndpoint.HelpEnabled%2A> プロパティを持つ既定の `true` を使用して、WCF サービスを構成します。 結果として、WCF はで自動 HTML ベースのヘルプ ページを作成します`http://localhost:8000/Customers/help`顧客の詳細は、方法の例、HTTP を構築する方法については、サービスとサービスの HTTP 応答 – などにアクセスする方法を要求を提供する。XML と JSON で表されます。  
  
 顧客のコレクション (一般的には、任意のリソース) をこの方法で公開すると、クライアントは、URI と HTTP の `GET`、`PUT`、`DELETE`、および `POST` を使用して一貫した方法でサービスと対話することができます。 Program.cs では、<xref:System.Net.HttpWebRequest> を使用してこのようなクライアントを作成する方法を示します。 これは WCF REST サービスにアクセスする方法の 1 つであることに注意してください。 <xref:System.ServiceModel.ChannelFactory> や <xref:System.Net.WebClient> などの他の .NET Framework クラスを使用して、サービスにアクセスすることも可能です。 SDK 内の他のサンプル (など、[基本 HTTP サービス](../../../../docs/framework/wcf/samples/basic-http-service.md)サンプルと[形式の自動選択](../../../../docs/framework/wcf/samples/automatic-format-selection.md)サンプル) WCF サービスとの通信にこれらのクラスを使用する方法について説明します。  
  
 このサンプルは、コンソール アプリケーション内で実行される自己ホスト型サービスとクライアントで構成されています。 コンソール アプリケーションが実行されると、クライアントはサービスに要求を発行し、応答からの適切な情報をコンソール ウィンドウに書き込みます。  
  
#### <a name="to-use-this-sample"></a>このサンプルを使用するには  
  
1.  基本的なリソース サービス サンプルのソリューションを開きます。 サンプルを正しく実行するには、[!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] を起動するときに、管理者として実行する必要があります。 これには、右クリックし、[!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)]アイコンを**管理者として実行**コンテキスト メニューから。  
  
2.  Ctrl キーと Shift キーを押しながら B キーを押してソリューションをビルドし、Ctrl キーを押しながら F5 キーを押してコンソール アプリケーションを実行します。 コンソール ウィンドウが表示されて、実行中のサービスの URI および実行中のサービスの HTML ヘルプ ページの URI が示されます。 ブラウザーでヘルプ ページの URI を入力することで、いつでも HTML ヘルプ ページを表示することができます。 サンプルが実行されると、クライアントは現在のアクティビティのステータスを書き込みます。  
  
3.  任意のキーを押して、サンプルを終了します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Web\BasicResourceService`  
  
## <a name="see-also"></a>関連項目  
 [基本的な HTTP サービス](../../../../docs/framework/wcf/samples/basic-http-service.md)  
 [形式の自動選択](../../../../docs/framework/wcf/samples/automatic-format-selection.md)
