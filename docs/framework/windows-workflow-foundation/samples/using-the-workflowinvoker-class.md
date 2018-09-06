---
title: WorkflowInvoker クラスの使用
ms.date: 03/30/2017
ms.assetid: 0a966164-3990-4e78-8aa2-c6797ebbee94
ms.openlocfilehash: d6525dbbd30aae95be4c4ee1de267736e557a541
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43748710"
---
# <a name="using-the-workflowinvoker-class"></a>WorkflowInvoker クラスの使用
このサンプルでは、<xref:System.Activities.WorkflowInvoker> クラスを使用して、メソッドのようにアクティビティを呼び出す方法を示します。  
  
## <a name="sample-details"></a>サンプルの詳細  
 アクティビティを実行するための最も簡単な方法は、<xref:System.Activities.WorkflowInvoker> クラスを使用する方法です。 このクラスは、メソッドを呼び出すようにアクティビティを直接実行することを目的として設計されています。 このクラスは、軽量で高性能な、使いやすい API で、アクティビティを実行する際に他のホスティングのバリエーションが提供する制御インフラストラクチャを必要としないシナリオで使用できます。  
  
 サンプルから派生したカスタム アクティビティを使用して<xref:System.Activities.CodeActivity%601>< Int32\>という名前`Add`2 つ追加する<xref:System.Activities.InArgument%601>、`X`と`Y`、しを返します、 `Result`<xref:System.Activities.OutArgument%601>します。 (<xref:System.Activities.CodeActivity%601>\<T > から派生した<xref:System.Activities.Activity%601>< T\>を持つ、 <xref:System.Activities.OutArgument%601> \<T > という名前の`Result`)。A `Dictionary` \<object > を介して呼び出されるアクティビティに引数を渡すために使用<xref:System.Activities.WorkflowInvoker>します。 ディクショナリのキーは、呼び出し先のアクティビティにおける引数名に対応します。 特定のキーに関連付けられた値は、キーによって識別される引数にバインドされます。  
  
 このサンプルは、<xref:System.Activities.WorkflowInvoker.Invoke%2A> を呼び出して、`X` および `Y` の値を含むディクショナリを渡します。 <xref:System.Activities.WorkflowInvoker> クラスは、これらの値を `Add` アクティビティの引数にバインドし、アクティビティを実行して、結果を返します。  
  
#### <a name="to-use-this-sample"></a>このサンプルを使用するには  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] を使用して、Invoker.sln ソリューション ファイルを開きます。  
  
2.  ソリューションをビルドするには、Ctrl キーと Shift キーを押しながら B キーを押します。  
  
3.  ソリューションを実行するには、F5 キーを押します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Execution\WorkflowInvoker`