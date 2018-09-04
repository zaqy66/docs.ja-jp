---
title: カスタム追跡レコード
ms.date: 03/30/2017
ms.assetid: 24284565-c68b-40bf-b7f1-e148d151a6fc
ms.openlocfilehash: ef3c20890f33f3ffd07a9c88de863e1ebe24851f
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43520186"
---
# <a name="custom-tracking-records"></a>カスタム追跡レコード
このトピックではカスタム追跡レコードを作成し、出力されたデータをレコードと一緒に読み込む方法を示します。  
  
## <a name="emitting-custom-tracking-records"></a>カスタム追跡レコードの出力  
 次の例に示すように、カスタム追跡レコードはコード アクティビティから出力できます。  
  
```  
protected override void Execute(CodeActivityContext context)  
{  
…  
            CustomTrackingRecord customRecord = new CustomTrackingRecord("CustomEmailSentEvent");  
            customRecord.Data.Add("SendTime", sendTime);  
            context.Track(customRecord);  
}  
```  
  
 <xref:System.Activities.Tracking.CustomTrackingRecord> 上で <xref:System.Activities.NativeActivityContext.Track%2A> メソッドを呼び出すことで、`ActvityContext` をコード アクティビティに出力できます。  
  
## <a name="see-also"></a>関連項目  
 [Windows Server App Fabric の監視](https://go.microsoft.com/fwlink/?LinkId=201273)  
 [App Fabric でアプリケーションの監視](https://go.microsoft.com/fwlink/?LinkId=201275)
