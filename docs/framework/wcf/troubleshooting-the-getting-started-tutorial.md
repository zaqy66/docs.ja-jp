---
title: チュートリアル入門のトラブルシューティング
ms.date: 03/30/2017
ms.assetid: 69a21511-0871-4c41-9a53-93110e84d7fd
ms.openlocfilehash: 5b8cd04ef4d98e522e255e1b7529e848351b2e0c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54695661"
---
# <a name="troubleshooting-the-getting-started-tutorial"></a>チュートリアル入門のトラブルシューティング
このトピックでは、チュートリアル入門の作業中に遭遇する最も一般的な問題とその解決方法の一覧を示します。  
  
**ハード ドライブ上のプロジェクト ファイルを検索できません。**

 Visual Studio では、プロジェクト ファイルを保存 c:\users\\<user name>\Documents\\< Visual Studio バージョン\>\Projects です。  
  
**サービス アプリケーションを実行しようとしています。HTTP は URL を登録できませんでした`http://+:8000/ServiceModelSamples/Service/`.**
**プロセスには、この名前空間へのアクセス権はありません。** 

 WCF サービスをホストするプロセスは、管理者特権で実行する必要があります。 サービスを実行している場合から、Visual Studio 内でする必要があります Visual Studio 管理者として実行します。 行うためには**開始**、右クリック**Visual Studio \<*バージョン*>** 選択**管理者として実行**. コンソール ウィンドウでコマンド ライン プロンプトから、サービスを実行する場合は、同様の方法でを管理者として、コンソール ウィンドウを起動する必要があります。 をクリックして**開始**を右クリックして**コマンド プロンプト**選択**管理者として実行**。  
  
**Svcutil.exe ツールを使用しようとしています: 'svcutil' は内部または外部コマンド、操作可能なプログラムまたはバッチ ファイルとして認識されません。**

 Svcutil.exe がシステム パスに存在する必要があります。 最も簡単な解決方法は、コマンド プロンプトを使用する方法です。 をクリックして**開始**、**すべてのプログラム**、 **Visual Studio \<*バージョン*>**、 **Visual Studio Tools**、および**Visual Studio 用開発者コマンド プロンプト**します。 このコマンド プロンプトでは、Visual Studio の一部として出荷されるすべてのツールの正しい場所をシステム パスを設定します。  

**Svcutil.exe によって生成された App.config ファイルが見つかりません。**

 **既存項目の追加**ダイアログでは、既定では次の拡張子を持つファイルのみが表示されます: .cs、.resx、.settings、.xsd、.wsdl ファイル。 選択してすべてのファイルの種類を表示することを指定する**すべてのファイル (\*.\*)** の右下隅のドロップダウン リスト ボックスで、**既存項目の追加** ダイアログ ボックス。  


**クライアント アプリケーションをコンパイルするには。'CalculatorClient' の定義を含まない '\<メソッド名 >' 拡張メソッド'\<メソッド名 >' 型 'CalculatorClient' が見つかりませんでしたの最初の引数を受け付ける (が存在することを使用して、ディレクティブ、またはアセンブリ参照。)**  

外部に公開されるのは、`ServiceOperationAttribute` でマークされたメソッドのみです。 省略すると、`ServiceOperationAttribute`属性内のメソッドのいずれかから、`ICalculator`インターフェイス、このエラー メッセージを取得するには、属性が不足している操作を呼び出すクライアント アプリケーションをコンパイルするときにします。  

**クライアント アプリケーションをコンパイルするには。型または名前空間名 'CalculatorClient' が見つかりませんでした (が存在することを使用して、ディレクティブまたはアセンブリ参照)。**

 Proxy.cs または Proxy.vb ファイルをクライアント プロジェクトに追加しなかった場合にこのエラーが発生します。  

**クライアントを実行するには。未処理の例外:System.servicemodel.endpointnotfoundexception::接続できませんでした`http://localhost:8000/ServiceModelSamples/Service/CalculatorService`します。TCP エラー コード 10061:接続は行われません、ターゲット コンピューターによって拒否されたためです。**

サービスを実行せずにクライアント アプリケーションを実行した場合にこのエラーが発生します。  
  
**未処理の例外:System.servicemodel.security.securitynegotiationexception:SOAP セキュリティ ネゴシエーション`http://localhost:8000/ServiceModelSamples/Service/CalculatorService`ターゲット`http://localhost:8000/ServiceModelSamples/Service/CalculatorService`できませんでした**  

ドメインに参加しているコンピューターにネットワーク接続がない場合にこのエラーが発生します。 コンピューターをネットワークに接続するか、クライアントとサービスの両方のセキュリティをオフにします。 サービスの場合は、WSHttpBinding を作成するコードを次のように変更します。  
  
```csharp
// Step 3 of the hosting procedure: Add a service endpoint  
selfhost.AddServiceEndpoint(typeof(ICalculator), new WSHttpBinding(SecurityMode.None), "CalculatorService");  
```

クライアントは、変更、 **\<セキュリティ >** の下の要素、 **\<バインド >** 次の要素。  
  
```xml
<security mode="Node" />  
```  

## <a name="see-also"></a>関連項目
- [チュートリアル入門](../../../docs/framework/wcf/getting-started-tutorial.md)
- [WCF トラブルシューティング クイックスタート](../../../docs/framework/wcf/wcf-troubleshooting-quickstart.md)
- [セットアップ問題のトラブルシューティング](../../../docs/framework/wcf/troubleshooting-setup-issues.md)
