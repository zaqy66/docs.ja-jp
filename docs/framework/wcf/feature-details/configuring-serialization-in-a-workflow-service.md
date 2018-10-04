---
title: ワークフロー サービス内でのシリアル化の構成
ms.date: 03/30/2017
ms.assetid: aa70b290-a2ee-4c3c-90ea-d0a7665096ae
ms.openlocfilehash: 67d8807e5ff45db2e8662586861d969e14ceaa8d
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48583711"
---
# <a name="configuring-serialization-in-a-workflow-service"></a>ワークフロー サービス内でのシリアル化の構成
ワークフロー サービスは、Windows Communication Foundation (WCF) サービスをそのため、オプションのいずれかを使用して、、 <xref:System.Runtime.Serialization.DataContractSerializer> (既定値) または<xref:System.Xml.Serialization.XmlSerializer>します。 ワークフロー以外のサービスを記述する場合、使用するシリアライザーの型はサービスまたは操作コントラクトで指定されます。 WCF ワークフロー サービスを作成するときに、コードでは、これらのコントラクトを指定しないが、コントラクト推論で実行時に生成されます。 コントラクト推論の詳細については、次を参照してください。[ワークフローを使用してコントラクト](../../../../docs/framework/wcf/feature-details/using-contracts-in-workflow.md)します。  シリアライザーは、<xref:System.ServiceModel.Activities.Receive.SerializerOption%2A> プロパティを使用して指定されます。 これは、次の図に示すようにデザイナーで設定できます。  
  
 ![シリアライザーの設定](../../../../docs/framework/wcf/feature-details/media/settingserialzier.png "SettingSerialzier")  
  
 シリアライザーは、次の例に示すようにコードで設定することもできます。  
  
```  
Receive approveExpense = new Receive  
            {  
                OperationName = "ApproveExpense",  
                CanCreateInstance = true,  
                ServiceContractName = "FinanceService",  
                SerializerOption = SerializerOption.DataContractSerializer,  
                Content = ReceiveContent.Create(new OutArgument<Expense>(expense))  
            };  
```  
  
 ワークフロー サービスにも既知の型を指定できます。 既知の型の詳細については、次を参照してください。 [Data Contract Known Types](../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)します。 既知の型は、デザイナーまたはコードで指定できます。 デザイナーで既知の型を指定するには、次の図に示すように <xref:System.ServiceModel.Activities.Receive> アクティビティのプロパティ ウィンドウで KnownTypes プロパティの横の省略記号ボタンをクリックします。  
  
 ![KnownTypes プロパティ](../../../../docs/framework/wcf/feature-details/media/knowntypes.png "KnownTypes")  
  
 これにより、既知の型を検索および指定できる型コレクション エディターが表示されます。  
  
 ![既知の型を追加する](../../../../docs/framework/wcf/feature-details/media/typecollectionseditor.gif "TypeCollectionsEditor")  
  
 をクリックして、**新しいタイプの追加**リンクし、既知の型のコレクションに追加する型の選択や検索ドロップダウンを使用します。 既知の型をコードで指定するには、次の例に示すように <xref:System.ServiceModel.Activities.Receive.KnownTypes%2A> プロパティを使用します。  
  
```csharp
Receive approveExpense = new Receive  
            {  
                OperationName = "ApproveExpense",  
                CanCreateInstance = true,  
                ServiceContractName = "FinanceService",  
                SerializerOption = SerializerOption.DataContractSerializer,  
                Content = ReceiveContent.Create(new OutArgument<Expense>(expense))  
            };  
            approveExpense.KnownTypes.Add(typeof(Travel));  
            approveExpense.KnownTypes.Add(typeof(Meal));  
```
