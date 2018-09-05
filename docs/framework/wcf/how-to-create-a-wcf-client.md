---
title: '方法 : Windows Communication Foundation クライアントを作成する'
ms.date: 03/30/2017
helpviewer_keywords:
- clients [WCF], running
- WCF clients [WCF], running
ms.assetid: a67884cc-1c4b-416b-8c96-5c954099f19f
ms.openlocfilehash: 9e6d75bf8911a3c36e63b3bc108faae823434d1d
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43397290"
---
# <a name="how-to-create-a-windows-communication-foundation-client"></a>方法 : Windows Communication Foundation クライアントを作成する

これは、4 番目の Windows Communication Foundation (WCF) アプリケーションを作成するために必要な 6 つのタスクです。 6 つのすべてのタスクの概要については、「[チュートリアル入門](../../../docs/framework/wcf/getting-started-tutorial.md)」を参照してください。

このトピックでは、WCF サービスからメタデータを取得し、使用して、サービスにアクセスできる WCF プロキシを作成する方法について説明します。 このタスクを完了するには、Visual Studio に用意されている "サービス参照の追加" 機能を使用します。 このツールでは、サービスの MEX エンドポイントからメタデータを取得し、選択した言語 (既定では C#) でクライアント プロキシのマネージド ソース コード ファイルを生成します。 このツールでは、クライアント プロキシを作成する以外に、クライアントの構成ファイルの作成または更新も行います。この構成ファイルにより、クライアント アプリケーションはエンドポイントのいずれかにあるサービスに接続できるようになります。

> [!NOTE]
> 使用することも、 [ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)プロキシ クラスと Visual Studio 内でサービス参照の追加を使用する代わりに構成を生成するツール。

> [!WARNING]
> クラス ライブラリ プロジェクトから WCF サービスを呼び出すときに[!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)]プロキシと関連付けられている構成ファイルを自動的に生成するサービス参照の追加機能を使用することができます。  この構成ファイルはクラス ライブラリ プロジェクトで使用されません。 クラス ライブラリを呼び出す実行可能ファイルの app.config ファイルに、生成された構成ファイル内の設定を追加する必要があります。

 クライアント アプリケーションは、生成されたプロキシ クラスを使用してサービスと通信します。 この手順で説明されて[方法: クライアントを使用して](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)します。

## <a name="to-create-a-windows-communication-foundation-client"></a>Windows Communication Foundation クライアントを作成するには

1.  はじめにソリューションを選択すると、右クリックして新しいコンソール アプリケーション プロジェクトを作成**追加**、**新しいプロジェクト**します。 **[新しいプロジェクトの追加]** ダイアログ ボックスの左側で、**[C#]** または **[VB]** の下にある **[Windows]** を選択します。 ダイアログ ボックスの中央のセクションで、**[コンソール アプリケーション]** を選択します。 プロジェクトに `GettingStartedClient` という名前を付けます。

2.  GettingStartedClient プロジェクトのターゲット フレームワークを .NET Framework 4.5 を右クリックして設定**GettingStartedClient**ソリューション エクスプ ローラーで選択して**プロパティ**します。 **[ターゲット フレームワーク]** ボックスの一覧で、**[.NET Framework 4.5]** を選択します。 VB プロジェクトが GettingStartedClient プロジェクトのプロパティ ダイアログ ボックスで、少し異なるは、ターゲット フレームワークを設定、をクリックして、**コンパイル**、画面の左側にあるタブをクリックして、 **詳細設定コンパイル オプション**ダイアログ ボックスの左下隅にあるボタンをクリックします。 次に、**[ターゲット フレームワーク]** ボックスの一覧の **[.NET Framework 4.5]** を選択します。

     ターゲット フレームワークを設定すると、ソリューションを再読み込みする Visual Studio 2011 キーを押して**OK**入力を求められたら。

3.  右クリックして System.ServiceModel への参照を GettingStartedClient プロジェクトに追加、**参照**ソリューション エクスプ ローラーで GettingStartedClient プロジェクトの下のフォルダー**追加**参照。 **[参照の追加]** ダイアログ ボックスの左側で、**[フレームワーク]** を選択します。 [アセンブリの検索] ボックスに「`System.ServiceModel`」と入力します。 ダイアログ ボックスの中央のセクションで、**[System.ServiceModel]** を選択し、**[追加]** をクリックして、**[閉じる]** をクリックします。 をクリックして、ソリューションを保存、**すべて保存**メイン メニューのボタンをクリックします。

4.  次に、電卓サービスにサービス参照を追加します。 これを実行する前に、GettingStartedHost コンソール アプリケーションを起動する必要があります。 ホストが実行されている場合を右クリックし、**参照**で GettingStartedClient プロジェクトの下のフォルダー**ソリューション エクスプ ローラー**選択**追加** >  **サービス参照**します。 [アドレス] ボックスで次の URL を入力、**サービス参照の追加**ダイアログ: [ http://localhost:8000/ServiceModelSamples/Service ](http://localhost:8000/ServiceModelSamples/Service) ] をクリックし、**移動**ボタンをクリックします。 CalculatorService は、サービスのリスト ボックスで、表示されます。 CalculatorService をダブルクリックし、それを展開して、サービスによって実装されるサービス コントラクトを表示します。 クリックしてであり、既定の名前空間のままに、 **OK**ボタンをクリックします。

     Visual Studio を使用してサービスへの参照を追加すると、ソリューション エクスプローラーで、新しい項目が GettingStartedClient プロジェクトの [サービス参照] フォルダーの下に表示されます。  使用する場合、 [ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)ツールのソース コード ファイルおよび app.config ファイルが生成されます。

     コマンド ライン ツールを使用することもできます。 [ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)クライアント コードを作成するスイッチを適切な使用。 次の例では、サービスのコード ファイルと構成ファイルを生成しています。 最初の例では VB でプロキシを生成する方法を示し、2 番目の例では C# でプロキシを生成する方法を示しています。

    ```
    svcutil.exe /language:vb /out:generatedProxy.vb /config:app.config http://localhost:8000/ServiceModelSamples/service
    ```

    ```csharp
    svcutil.exe /language:cs /out:generatedProxy.cs /config:app.config http://localhost:8000/ServiceModelSamples/service
    ```

 これで、クライアント アプリケーションで電卓サービスを呼び出すために使用されるプロキシが作成されました。 シリーズの次のトピックに進みます[方法: クライアントを構成する。](../../../docs/framework/wcf/how-to-configure-a-basic-wcf-client.md)

## <a name="see-also"></a>関連項目

- [ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [はじめに](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [自己ホスト](../../../docs/framework/wcf/samples/self-host.md)
- [方法 : 構成ファイルを使用してサービスのメタデータを公開する](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [方法 : Svcutil.exe を使用してメタデータ ドキュメントをダウンロードする](../../../docs/framework/wcf/feature-details/how-to-use-svcutil-exe-to-download-metadata-documents.md)
