---
title: インターネット インフォメーション サービスでホストされる WCF サービスの配置
ms.date: 03/30/2017
ms.assetid: 04ebd329-3fbd-44c3-b3ab-1de3517e27d7
ms.openlocfilehash: b2b58de703a0864ac0666cb4738a95726e28bcaf
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43740102"
---
# <a name="deploying-an-internet-information-services-hosted-wcf-service"></a>インターネット インフォメーション サービスでホストされる WCF サービスの配置
開発と、インターネット インフォメーション サービス (IIS) でホストされる Windows Communication Foundation (WCF) サービスのデプロイは、次のタスクで構成されます。  
  
-   ある IIS、ASP.NET、WCF、および WCF のアクティブ化コンポーネントが正しくインストールされ、登録されていることを確認します。  
  
-   新しい IIS アプリケーションを作成するか、既存の [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] アプリケーションを再利用します。  
  
-   WCF サービスの .svc ファイルを作成します。  
  
-   IIS アプリケーションにサービス実装を展開します。  
  
-   WCF サービスを構成します。  
  
 IIS でホストされる WCF サービスの作成の詳細なチュートリアルを参照してください。[方法: IIS で WCF サービスをホスト](../../../../docs/framework/wcf/feature-details/how-to-host-a-wcf-service-in-iis.md)します。  
  
## <a name="ensure-that-iis-aspnet-and-wcf-are-correctly-installed-and-registered"></a>IIS、ASP.NET、および WCF が正しくインストールおよび登録されていることの確認  
 IIS でホストされる WCF services が正しく機能するには、WCF、IIS、および ASP.NET をインストールする必要があります。 WCF をインストールする手順 (の一部として、 [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)])、ASP.NET と IIS が使用されているオペレーティング システムのバージョンによって異なります。 WCF のインストールの詳細については、[!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)]を参照してください[Microsoft .NET Framework 4 の Web インストーラー](https://go.microsoft.com/fwlink/?LinkId=201185)します。 IIS をインストールするための手順をご覧[IIS をインストールする](https://go.microsoft.com/fwlink/?LinkId=201188)します。  
  
 インストール プロセス、 [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)] IIS が既にコンピューターに存在する場合は、IIS で WCF を自動的に登録します。 後に IIS がインストールされている場合、 [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)]、IIS で WCF を登録する追加の手順が必要と[!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)]します。 使用しているオペレーティング システムに応じて、次のように実行します。  
  
-   [!INCLUDE[wxpsp2](../../../../includes/wxpsp2-md.md)]、Windows 7、および[!INCLUDE[ws2003](../../../../includes/ws2003-md.md)]: を使用して、 [ServiceModel 登録ツール (ServiceModelReg.exe)](../../../../docs/framework/wcf/servicemodelreg-exe.md) WCF を IIS に登録するためのツール: このツールを使用する次のように入力します。 **ServiceModelReg.exe/i/x** 、Visual studioコマンド プロンプト。 このコマンド プロンプトを開くには、[スタート] ボタンをクリックし、 **[すべてのプログラム]**, **[Microsoft Visual Studio 2012]**, **[Visual Studio ツール]** の順にポイントし、 **[Visual Studio コマンド プロンプト]** をクリックします。  
  
-   [!INCLUDE[wv](../../../../includes/wv-md.md)]: [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)]のサブコンポーネントの Windows Communication Foundation アクティベーション コンポーネントをインストールします。 コントロール パネルで、次のようにクリックします。**プログラム追加と削除**し**追加\/Windows コンポーネントの削除**します。 **Windows コンポーネント ウィザード**がアクティブになります。  
  
-   Windows 7:  
  
 最後に、ASP.NET が .NET Framework Version 4 を使用するように設定されていることを確認する必要があります。 これには、–i オプションを指定して ASPNET_Regiis ツールを実行します。 詳細については、次を参照してください[ASP.NET IIS 登録ツール。](https://go.microsoft.com/fwlink/?LinkId=201186)  
  
## <a name="create-a-new-iis-application-or-reuse-an-existing-aspnet-application"></a>新しい IIS アプリケーションの作成、または既存の ASP.NET アプリケーションの再利用  
 IIS でホストされる WCF サービスは、IIS アプリケーションの内部にする必要があります。 排他的に WCF サービスをホストする新しい IIS アプリケーションを作成することができます。 または、既にホストしている既存のアプリケーションに、WCF サービスをデプロイできる[!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)]コンテンツ (.aspx ページや ASP.NET Web サービス (ASMX))。 これらのオプションの詳細についてを参照してください、「ホスティング WCF - サイド ASP.NET を使用した」と「ASP.NET 互換モードでは WCF サービスをホスティング」セクション[WCF サービスと ASP.NET](../../../../docs/framework/wcf/feature-details/wcf-services-and-aspnet.md)します。  
  
 [!INCLUDE[iis601](../../../../includes/iis601-md.md)] とそれ以降のバージョンでは、隔離されているオブジェクト指向プログラミング アプリケーションは定期的に再起動されることに注意してください。 既定値は 1740 分です。 サポートされている最大値は 71,582 分です。 この再起動は、無効にできます。 このプロパティの詳細については、次を参照してください。、 [PeriodicRestartTime](https://go.microsoft.com/fwlink/?LinkId=109968)します。  
  
## <a name="create-an-svc-file-for-the-wcf-service"></a>WCF サービス用の .svc ファイルの作成  
 IIS でホストされる WCF サービスは、IIS アプリケーション内の特別なコンテンツ ファイル (.svc ファイル) として表されます。 これは、ASMX ページが、IIS アプリケーションの内部で .asmx ファイルとして表現されるのと同様です。 .Svc ファイルには、WCF 固有の処理ディレクティブが含まれています ([\@ServiceHost](../../../../docs/framework/configure-apps/file-schema/wcf-directive/servicehost.md)) インフラストラクチャをホストしている WCF 受信メッセージに応答してホストされるサービスをアクティブ化できるようにします。 .svc ファイルの最も一般的な構文を次のステートメントに示します。  
  
```  
<% @ServiceHost Service="MyNamespace.MyServiceImplementationTypeName" %>  
```  
  
 含まれています、 [ \@ServiceHost](../../../../docs/framework/configure-apps/file-schema/wcf-directive/servicehost.md)ディレクティブと単一の属性`Service`します。 `Service` 属性の値は、サービス実装の共通言語ランタイム (CLR: Common Language Runtime) 型名です。 このディレクティブを使用することは、次のコードを使用してサービス ホストを作成することと基本的に同じです。  
  
```csharp  
new ServiceHost( typeof( MyNamespace.MyServiceImplementationTypeName ) );  
```  
  
 サービスのベース アドレスの一覧を作成するなど、追加のホスト構成を実行することもできます。 カスタム <xref:System.ServiceModel.Activation.ServiceHostFactory> を使用して、このディレクティブをカスタム ホスト ソリューション用に拡張することもできます。 WCF サービスをホストする IIS アプリケーションは作成との有効期間を管理する責任を負いません<xref:System.ServiceModel.ServiceHost>インスタンス。 管理対象の WCF ホスティング インフラストラクチャの作成、必要な<xref:System.ServiceModel.ServiceHost>.svc ファイルの最初の要求が受信したときにインスタンスを動的にします。 このインスタンスは、コードによって明示的に閉じられるか、アプリケーションがリサイクルされるときまで解放されません。  
  
 .Svc ファイルの構文の詳細については、次を参照してください。 [ \@ServiceHost](../../../../docs/framework/configure-apps/file-schema/wcf-directive/servicehost.md)します。  
  
## <a name="deploy-the-service-implementation-to-the-iis-application"></a>IIS アプリケーションへのサービス実装の展開  
 IIS でホストされる WCF サービスと同様の動的なコンパイル モデルを使用して、[!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)]します。 同様[!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)]、次のように、さまざまな場所にいくつかの方法で、IIS でホストされる WCF サービスの実装コードを配置することができます。  
  
-   グローバル アセンブリ キャッシュ (GAC: Global Assembly Cache) またはアプリケーションの \bin ディレクトリに配置される、プリコンパイルされた .dll ファイルとして展開します。 プリコンパイルされたバイナリは、新しいバージョンのクラス ライブラリが展開されるまで更新されません。  
  
-   ようにコンパイルされていないソース ファイルは、アプリケーションの \App_Code ディレクトリにあります。 このディレクトリに配置されたソース ファイルは、アプリケーションの最初の要求を処理するときに動的に要求されます。 \App_Code ディレクトリ内のファイルを変更すると、次の要求を受け取ったときにアプリケーション全体がリサイクルされ、再コンパイルされます。  
  
-   コンパイルされていないコードは、.svc ファイルで直接配置します。 実装コードでは、後は、サービスの .svc ファイルに配置されているインラインことができます、 \@ServiceHost ディレクティブ。 インライン コードを変更すると、次の要求を受け取ったときにアプリケーションがリサイクルされ、再コンパイルされます。  
  
 詳細については、[!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)]コンパイル モデルを参照してください[ASP.NET コンパイルの概要](https://go.microsoft.com/fwlink/?LinkId=94773)します。  
  
## <a name="configure-the-wcf-service"></a>WCF サービスの構成  
 IIS でホストされる WCF サービスは、アプリケーションの Web.config ファイルに設定を保存します。 IIS でホストされるサービスは、IIS の外部でホストされる WCF サービスとして、同じ構成要素と構文を使用します。 ただし、次の制約は、IIS ホスト環境に固有です。  
  
-   IIS でホストされるサービスのベース アドレス。  
  
-   アプリケーションが IIS の外部でのホスティングの WCF サービスは、一連の情報を渡すことによって、ホストするサービスのベース アドレスを制御できますアドレス Uri を<xref:System.ServiceModel.ServiceHost>コンス トラクターまたは提供することで、 [\<ホスト >](../../../../docs/framework/configure-apps/file-schema/wcf/host.md)内の要素、サービスの構成。 IIS でホストされるサービスは、それぞれのベース アドレスを制御できません。IIS でホストされるサービスのベース アドレスは、その .svc ファイルのアドレスです。  
  
### <a name="endpoint-addresses-for-iis-hosted-services"></a>IIS でホストされるサービスのエンドポイント アドレス  
 IIS でホストされるときのエンドポイント アドレスは、常にサービスを表す .svc ファイルのアドレスを基準にした相対アドレスと見なされます。 たとえば、WCF サービスのベース アドレスは http://localhost/Application1/MyService.svc次のエンドポイント構成を使用します。  
  
```xml  
<endpoint address="anotherEndpoint" .../>  
```  
  
 これにより、エンドポイントに到達可能な"http://localhost/Application1/MyService.svc/anotherEndpoint"。  
  
 相対アドレスに到達できるエンドポイントを提供すると、空の文字列を使用するエンドポイント構成要素同様に、 http://localhost/Application1/MyService.svc、ベース アドレスであります。  
  
```xml  
<endpoint address="" ... />  
```  
  
 IIS でホストされるサービスのエンドポイントには、常に相対エンドポイント アドレスを使用する必要があります。 完全修飾エンドポイント アドレスを指定 (たとえば、 http://localhost/MyService.svc)エンドポイント アドレスが、エンドポイントを公開するサービスをホストする IIS アプリケーションを指していない場合、サービスの展開でエラーが発生します。 ホストされるサービスに相対エンドポイント アドレスを使用すると、このような競合が回避されます。  
  
### <a name="available-transports"></a>利用可能なトランスポート  
 IIS 5.1 でホストされる WCF サービスと[!INCLUDE[iis601](../../../../includes/iis601-md.md)]HTTP ベースの通信を使用してに制限されます。 これらの IIS プラットフォームでホストされるサービスで、非 HTTP バインドを使用するように構成すると、サービスをアクティブ化するときにエラーが発生します。 [!INCLUDE[iisver](../../../../includes/iisver-md.md)]でサポートされるトランスポートには、既存の MSMQ アプリケーションとの後方互換性を実現する HTTP、Net.TCP、Net.Pipe、Net.MSMQ、msmq.formatname があります。  
  
### <a name="http-transport-security"></a>HTTP トランスポート セキュリティ  
 IIS でホストされる WCF サービスと http を使用して、トランスポート セキュリティ (たとえば、HTTPS と HTTP 認証方式など、基本、ダイジェスト、および Windows 統合認証) のサービスを含む IIS 仮想ディレクトリでは、それらがサポートしていれば設定。 ホストされるエンドポイントのバインディングでの HTTP トランスポート セキュリティ設定は、そのエンドポイントを格納する IIS 仮想ディレクトリでのトランスポート セキュリティ設定と一致する必要があります。  
  
 たとえば、WCF エンドポイントが HTTP ダイジェスト認証を使用するように構成は、HTTP ダイジェスト認証を許可することも構成されている IIS 仮想ディレクトリ内になければなりません。 サービスのアクティブ化中にエラー発生の IIS 設定と WCF エンドポイントの設定の組み合わせが一致しません。  
  
## <a name="see-also"></a>関連項目  
 [インターネット インフォメーション サービスでのホスティング](../../../../docs/framework/wcf/feature-details/hosting-in-internet-information-services.md)  
 [インターネット インフォメーション サービス ホスティングのベスト プラクティス](../../../../docs/framework/wcf/feature-details/internet-information-services-hosting-best-practices.md)  
 [Windows Server App Fabric のホスティング機能](https://go.microsoft.com/fwlink/?LinkId=201276)
