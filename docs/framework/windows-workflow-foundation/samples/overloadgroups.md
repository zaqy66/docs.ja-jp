---
title: OverloadGroups
ms.date: 03/30/2017
ms.assetid: d1d547d2-f5fb-4de3-a959-ee6139a4f1ad
ms.openlocfilehash: 0773e76d36b25ad5485cc8912c7012815412de9f
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2018
ms.locfileid: "43469870"
---
# <a name="overloadgroups"></a>OverloadGroups
このサンプルは、次の 2 つの興味深い特性を持つアクティビティ (`CreateLocation`) で構成されます。  
  
1.  いくつかの必須の引数といくつかの省略可能な引数があります。  
  
2.  ユーザーは、2 つの異なる引数セットのうちのどちらを指定するかを選択できます。  
  
 これらの動作は、次の 2 つの機能によって実現されます。  
  
-   `[isRequired]` : 特定のアクティビティのプロパティが割り当てられているかどうかを検証し、割り当てられていない場合は例外をスローします。  
  
-   `[OverloadGroup]` : 一連の引数をまとめて、アクティビティのユーザーが 2 つのセットのうちのどちらを使用するかを選択できるようにします。 ユーザーは、同じインスタンス内の異なるオーバーロード グループの引数を使用できません。  
  
 さまざまなワークフローを設定したら、<xref:System.Activities.Validation.ActivityValidationServices.Validate%2A> の <xref:System.Activities.Validation.ValidationResults> コレクションを返す <xref:System.Activities.Validation.Constraint> を呼び出します。 <xref:System.Activities.Validation.Constraint> オブジェクトをコンソールに出力します。  
  
### <a name="to-set-up-build-and-run-the-sample"></a>サンプルをセットアップ、ビルド、および実行するには  
  
1.  開く、 **OverloadGroups.sln**サンプル ソリューション[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]します。  
  
2.  ソリューションをビルドして実行します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Validation\OverloadGroups`
