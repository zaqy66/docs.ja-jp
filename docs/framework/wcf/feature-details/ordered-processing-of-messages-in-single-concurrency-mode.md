---
title: Single コンカレンシー モードでメッセージを順番に処理する
ms.date: 03/30/2017
ms.assetid: a90f5662-a796-46cd-ae33-30a4072838af
ms.openlocfilehash: c9f2460a1def19212d3ba866b0b443830e9b69bb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745849"
---
# <a name="ordered-processing-of-messages-in-single-concurrency-mode"></a>Single コンカレンシー モードでメッセージを順番に処理する
WCF は、基になるチャネルがセッションフルでない限りには、メッセージの処理順序に関する保証しません。  たとえば、セッションフル チャネルではない MsmqInputChannel を使用する WCF サービスは順序でメッセージの処理に失敗します。 これは、状況によっては、開発者を必要とする処理動作しますが、セッションを使用しない場合があります。 このトピックでは、サービスが Single コンカレンシー モードで実行されている場合にこの動作を構成する方法について説明します。  
  
## <a name="in-order-message-processing"></a>順番に従ったメッセージの処理  
 <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> という名前の新しい属性が <xref:System.ServiceModel.ServiceBehaviorAttribute> に追加されました。 <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> を true に設定し、<xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> を <xref:System.ServiceModel.ConcurrencyMode.Single> に設定すると、サービスに送信されたメッセージは順番に処理されます。 次のコードは、これらの属性の設定方法を示しています。  
  
```  
[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single, EnsureOrderedDispatch = true )]  
    class Service : IService  
    {  
         // ...  
    }  
```  
  
 <xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> をその他の値に設定すると、<xref:System.InvalidOperationException> がスローされます。  
  
## <a name="see-also"></a>関連項目
- [セッション、インスタンス化、およびコンカレンシー](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)
- [コンカレンシー](../../../../docs/framework/wcf/samples/concurrency.md)
