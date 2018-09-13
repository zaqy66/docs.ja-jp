---
title: .NET Framework 4.5 のポリシー アクティビティ
ms.date: 03/30/2017
ms.assetid: 8e375e0c-d7c1-4d69-88ab-36d52db0aa7e
ms.openlocfilehash: 9d8983f2f1d3f75beffeacfff4b673f6c23c4204
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2018
ms.locfileid: "44709413"
---
# <a name="policy-activity-in-net-framework-45"></a>.NET Framework 4.5 のポリシー アクティビティ
Policy4 アクティビティでの Windows Workflow Foundation [!INCLUDE[netfx35_long](../../../../includes/netfx35-long-md.md)] (WF 3.5)<xref:System.Workflow.Activities.Rules.RuleSet>オブジェクトでの Windows Workflow Foundation で使用される[!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)](WF 4.5) WF 3.5 に付属しているルール エンジンを使用して直接します。 このアクティビティを使用すると、WF 3.5 <xref:System.Workflow.Activities.Rules.RuleSet> を作成して実行できます。 Windows Workflow Foundation の一部として含まれている WF 3.5 ルール エンジンの詳細については、Windows Workflow Foundation ルール エンジンの概要を参照してください。 移行の詳細については WF へのルール[!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)]をお読みください[移行ガイダンス](../../../../docs/framework/windows-workflow-foundation/migration-guidance.md)します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\Rules-Policy4`  
  
## <a name="projects-in-this-sample"></a>このサンプルのプロジェクト  
  
|プロジェクト名|説明|メイン ファイル|  
|------------------|-----------------|----------------|  
|Policy4|Policy4 アクティビティとその [!INCLUDE[wf1](../../../../includes/wf1-md.md)] デザイナーが含まれます。|**Policy4.cs**: Policy4 アクティビティ定義。<br /><br /> **PolicyDesigner.xaml**: Policy4 アクティビティのカスタム デザイナー。 ルール エディターを使用して ([RuleSetDialog クラス](https://go.microsoft.com/fwlink/?LinkId=150378)) から[!INCLUDE[wf1](../../../../includes/wf1-md.md)]ルール エンジン。|  
|ImperativeCodeClientSample|命令型 C# コードで、Policy4 アプリケーションを使用してワークフローを構成および実行するサンプル クライアント アプリケーションです ([!INCLUDE[wf1](../../../../includes/wf1-md.md)] デザイナーは不使用)。|**ApplyDiscount.rules**: ファイルと[!INCLUDE[wf1](../../../../includes/wf1-md.md)]ルール定義。<br /><br /> **Order.cs**: 顧客の注文を表す型。 ルールはこの型のオブジェクトに適用されます。<br /><br /> **Program.cs**: 構成および Order オブジェクトのインスタンスに ApplyDiscount.rules で定義されたルールを適用する Policy4 アクティビティを含むワークフローを実行します。<br /><br /> **App.config**: ルール ファイルのパスの構成ファイル。|  
|DesignerClientSample|[!INCLUDE[wf1](../../../../includes/wf1-md.md)] デザイナーで、Policy4 アプリケーションを使用してワークフローを構成および実行するサンプル クライアント アプリケーションです。|**Sequence1.xaml**: Policy4 アクティビティを使用してルール評価を実行するシーケンシャル ワークフロー。<br /><br /> `Program.cs`: Sequence1.xaml で定義されているワークフローのインスタンスを実行します。|  
  
## <a name="the-policy4-activity"></a>Policy4 アクティビティ  
 Policy4 アクティビティは、ワークフローで <xref:System.Activities.NativeActivity%601> RuleSet を実行できるようにする [!INCLUDE[wf1](../../../../includes/wf1-md.md)] の派生クラスです。 次のコード例は、このアクティビティのパブリック OM の簡略化された定義です。  
  
```csharp  
public class Policy4Activity<TResult>: NativeActivity<TResult>  
{  
    public RuleSet RuleSet  
  
    [IsRequired]  
    public InArgument Input  
  
    public OutArgument<ValidationErrorCollection> ValidationErrors  
}  
```  
  
|プロパティ|説明|  
|--------------|-----------------|  
|RuleSet|WF [RuleSet クラス](https://go.microsoft.com/fwlink/?LinkId=150379)アクティビティが実行されるときに評価される .NET Framework 3.5 用です。|  
|TargetObject|対象のオブジェクト内のルール、 [RuleSet クラス](https://go.microsoft.com/fwlink/?LinkId=150379)評価されます。|  
|ValidationError|によって返される検証エラーの一覧、[!INCLUDE[wf1](../../../../includes/wf1-md.md)]を検証するときに、.NET Framework 3.5 用のルール エンジン、 [RuleSet クラス](https://go.microsoft.com/fwlink/?LinkId=150379)に対して実行する前にターゲット オブジェクト。|  
  
## <a name="policy4-activity-designer"></a>Policy4 アクティビティ デザイナー  
 Policy4 デザイナーを使用すると、コードを記述することなく Policy4 アクティビティを構成できます。 ソリューションをビルドした後にあります、ツールボックスのセクションで**Microsoft.Samples.Activities.Rules**します。  
  
 WF デザイナーでは、対象オブジェクトや RuleSet を構成できます。 ときに、 **Edit RuleSet**ボタンをクリックして、WF [RuleSetDialog クラス](https://go.microsoft.com/fwlink/?LinkId=150378)の[!INCLUDE[netfx35_short](../../../../includes/netfx35-short-md.md)]が表示されます。 このダイアログは、ホストを変更した [!INCLUDE[netfx35_short](../../../../includes/netfx35-short-md.md)] ルール エディターです。 このエディターを使用して、Policy4 アクティビティで実行するルールを作成および編集します。  
  
## <a name="using-this-sample"></a>このサンプルの使用  
 このサンプルを実行するのに特別な設定は必要ありません。 Visual Studio でソリューションを開き、F5 キーを押してアプリケーションを実行するだけです。  
  
 このサンプルには、ImperativeCodeClientSample と DesignerClientSample の 2 つのクライアント アプリケーションがあります。 ImperativeCodeClientSample クライアントは、C# 命令型コードを使用して Policy4 アクティビティを構成および実行する方法を示します。 DesignerClientSample は、デザイナーを使用して Policy4 アクティビティを構成および実行する方法を示します。  
  
#### <a name="to-run-the-imperativecodeclientsample-client-application"></a>ImperativeCodeClientSample クライアント アプリケーションを実行するには  
  
1.  [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] を使用して、Policy4Sample.sln ソリューション ファイルを開きます。  
  
2.  **ソリューション エクスプ ローラー**を右クリックし、 **ImperativeCodeClientSample**プロジェクト選び**スタートアップ プロジェクトとして設定**します。  
  
3.  プロジェクトを実行するには、Ctrl キーを押しながら F5 キーを押します。  
  
#### <a name="to-run-the-imperativecodeclientsample-client-application"></a>ImperativeCodeClientSample クライアント アプリケーションを実行するには  
  
1.  [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] を使用して、Policy4Sample.sln ソリューション ファイルを開きます。  
  
2.  **ソリューション エクスプ ローラー**を右クリックし、 **DesignerClientSample**プロジェクト。  
  
    -   選択**スタートアップ プロジェクトとして設定**します。  
  
3.  プロジェクトをコンパイルするには、Ctrl キーと Shift キーを押しながら B キーを押します。  
  
4.  プロジェクトを実行するには、Ctrl キーを押しながら F5 キーを押します。