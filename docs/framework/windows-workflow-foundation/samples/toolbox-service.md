---
title: ツールボックス サービス
ms.date: 03/30/2017
ms.assetid: 742212d0-445e-41ed-9739-9ee848ce7f1b
ms.openlocfilehash: 0b21f10c763f3f82591f947eb4cc48cf90f4ac79
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43406463"
---
# <a name="toolbox-service"></a>ツールボックス サービス
このサンプルでは、ワークフローのコンテキストに基づいて [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] ツールボックス アクティビティを更新する方法を示します。 このサンプルには、カスタム アクティビティが選択されているかどうかに基づいてツールボックスの内容を変更するワークフローが含まれています。  
  
## <a name="discussion"></a>説明  
 ワークフローの作成中には、通常、状況に応じてツールボックスが変化することが求められます。 たとえば、特定のアクティビティをワークフローに追加すると、別のアクティビティがいくつかツールボックスに表示されるようにすることが必要な場合があります。 アクティビティをワークフローから削除したときは、ドメインの要件に基づいてツールボックスが適切に応答する必要があります。  
  
 ホストを変更したワークフロー デザイナーでは、ツールボックス コントロールを制御し、ワークフローのモデル変更に基づいて、ホストによってツールボックス コントロールで適切な変更がトリガーされるようにすることができます。 ただし、[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] では、ツールボックスをユーザーが制御することはないので、その内容を変更するにはインターフェイスが必要です。 `IActivityToolboxService` がそのインターフェイスに当たります。  
  
 この API には、次の 4 つのメソッドが用意されています。  
  
```  
public interface IActivityToolboxService   
{   
        void AddCategory(string categoryName);   
        void RemoveCategory(string categoryName);   
        void AddItem(string qualifiedTypeName, string categoryName);   
        void RemoveItem(string qualifiedTypeName, string categoryName);   
        IList<string> EnumCategories();   
        IList<string> EnumItems(string categoryName);   
}  
```  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>サンプルをセットアップ、ビルド、および実行するには  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] を使用して、WorkflowSimulator.sln ソリューション ファイルを開きます。  
  
2.  Ctrl キーと Shift キーを押しながら B キーを押して、ソリューションをビルドします。  
  
3.  Workflow.xaml ファイルを開きます。  
  
4.  追加、 **CustomActivity**ドラッグして、ツールボックスから削除します。 ツールボックス カテゴリが追加で呼び出すことに注意してください: **New WF Category**するその他のアクティビティを含む**割り当てる**します。  
  
5.  選択を解除、 **CustomActivity**別のアクティビティをドラッグします。  
  
6.  項目**割り当てる**カテゴリ**New WF Category**ツールボックスの下で削除したようになりました。 また、このカテゴリには項目がほかにないので、カテゴリも削除されます。  
  
7.  選択、 **CustomActivity**もう一度と、カテゴリと**割り当てる**アクティビティが再度追加されます。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Designer\IActivityToolboxService`
