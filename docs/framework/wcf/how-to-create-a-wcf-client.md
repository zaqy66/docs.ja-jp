---
title: '方法 : Windows Communication Foundation クライアントを作成する'
ms.date: 09/14/2018
helpviewer_keywords:
- clients [WCF], running
- WCF clients [WCF], running
ms.assetid: a67884cc-1c4b-416b-8c96-5c954099f19f
ms.openlocfilehash: 1eadb5008575a1a53d685db14d68e42d0dce1360
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2018
ms.locfileid: "46478293"
---
# <a name="how-to-create-a-windows-communication-foundation-client"></a>方法 : Windows Communication Foundation クライアントを作成する

これは、4 番目の Windows Communication Foundation (WCF) アプリケーションを作成するために必要な 6 つのタスクです。 6 つのすべてのタスクの概要については、「[チュートリアル入門](../../../docs/framework/wcf/getting-started-tutorial.md)」を参照してください。

このトピックでは、WCF サービスからメタデータを取得し、使用して、サービスにアクセスできる WCF プロキシを作成する方法について説明します。 このタスクを使用して、**サービス参照の追加**Visual Studio によって提供される機能です。 このツールでは、サービスの MEX エンドポイントからメタデータを取得し、選択した言語 (既定では C#) でクライアント プロキシのマネージド ソース コード ファイルを生成します。 このツールでは、クライアント プロキシを作成する以外に、クライアントの構成ファイルの作成または更新も行います。この構成ファイルにより、クライアント アプリケーションはエンドポイントのいずれかにあるサービスに接続できるようになります。

> [!NOTE]
> 使用することも、 [ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)プロキシ クラスおよび使用する代わりに構成を生成するツール**サービス参照の追加**Visual Studio でします。

> [!NOTE]
> Visual Studio でクラス ライブラリ プロジェクトから WCF サービスを呼び出すときに使用できます、**サービス参照の追加**プロキシと関連付けられている構成ファイルを自動的に生成する機能。 この構成ファイルはクラス ライブラリ プロジェクトで使用されません。 クラス ライブラリを呼び出す実行可能ファイルの app.config ファイルに生成された構成ファイルで設定を追加する必要があります。

クライアント アプリケーションは、生成されたプロキシ クラスを使用してサービスと通信します。 この手順で説明されて[方法: クライアントを使用して](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)します。

## <a name="to-create-a-windows-communication-foundation-client"></a>Windows Communication Foundation クライアントを作成するには

1. Visual Studio で新しいコンソール アプリケーション プロジェクトを作成します。 入門ソリューションを右クリックして**ソリューション エクスプ ローラー**選択**追加** > **新しいプロジェクト**します。 **新しいプロジェクトの追加**ダイアログ ボックスで、左側にある、選択、 **Windows デスクトップ**カテゴリ  **Visual c#** または**Visual Basic**します。 選択、**コンソール アプリ (.NET Framework)** テンプレート、および、プロジェクトの名前を**GettingStartedClient**します。

2. System.ServiceModel への参照を GettingStartedClient プロジェクトに追加します。 右クリックし、**参照**で GettingStartedClient プロジェクトの下のフォルダー**ソリューション エクスプ ローラー**、し、**参照の追加**します。 **参照の追加**ダイアログ ボックスで、 **Framework**ダイアログ ボックスの左側にある**アセンブリ**します。 検索して選択**System.ServiceModel**を選び、 **OK**。 ソリューションを選択して保存**ファイル** > **すべて保存**します。

3. 電卓サービスにサービス参照を追加します。

   1. 最初に、GettingStartedHost コンソール アプリケーションを開始します。

   2. ホストが実行されている場合を右クリックし、**参照**で GettingStartedClient プロジェクトの下のフォルダー**ソリューション エクスプ ローラー**選択**追加** >  **サービス参照**します。

   3. [アドレス] ボックスの次の URL を入力、**サービス参照の追加**ダイアログ。 [http://localhost:8000/GettingStartedClient/Service](http://localhost:8000/GettingStartedClient/Service)

   4. 選択**移動**します。

   CalculatorService に表示される、**サービス**ボックスの一覧。 展開すると、サービスによって実装されるサービス コントラクトを表示する CalculatorService をダブルクリックします。 として既定の名前空間のままに、選択は、 **OK**。

    Visual Studio を使用してサービスへの参照を追加するに新しい項目が表示されます。**ソリューション エクスプ ローラー**下、**サービス参照**GettingStartedClient プロジェクトの下のフォルダー。 使用する場合、 [ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)ツール、ソース コード ファイルと app.config ファイルが生成されます。

    コマンド ライン ツールを使用することもできます。 [ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)クライアント コードを作成するスイッチを適切な使用。 次の例では、サービスのコード ファイルと構成ファイルを生成しています。 最初の例は、VB でプロキシを生成する方法と、2 つ目は、c# でプロキシを生成する方法を示します。

    ```shell
    svcutil.exe /language:vb /out:generatedProxy.vb /config:app.config http://localhost:8000/GettingStartedClient/service
    ```

    ```shell
    svcutil.exe /language:cs /out:generatedProxy.cs /config:app.config http://localhost:8000/GettingStartedClient/service
    ```

## <a name="next-steps"></a>次の手順

クライアント アプリケーションが、電卓サービスの呼び出しに使用するプロキシを作成しました。 シリーズの次のトピックに進みます。

> [!div class="nextstepaction"]
> [方法: クライアントを構成する](../../../docs/framework/wcf/how-to-configure-a-basic-wcf-client.md)

## <a name="see-also"></a>関連項目

- [ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [はじめに](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [自己ホスト](../../../docs/framework/wcf/samples/self-host.md)
- [方法 : 構成ファイルを使用してサービスのメタデータを公開する](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [方法 : Svcutil.exe を使用してメタデータ ドキュメントをダウンロードする](../../../docs/framework/wcf/feature-details/how-to-use-svcutil-exe-to-download-metadata-documents.md)
