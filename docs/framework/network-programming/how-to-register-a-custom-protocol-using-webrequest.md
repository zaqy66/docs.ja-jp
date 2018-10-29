---
title: '方法: WebRequest を使用してカスタム プロトコルを登録する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 98ddbdb9-66b1-4080-92ad-51f5c447fcf8
ms.openlocfilehash: 5f863aa61058e87a7911bab3b02c3ba345419596
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50193605"
---
# <a name="how-to-register-a-custom-protocol-using-webrequest"></a>方法: WebRequest を使用してカスタム プロトコルを登録する
この例では、他の場所で定義されているプロトコル固有のクラスを登録する方法を示します。 この例では、`CustomWebRequestCreator` は、`CustomWebRequest` オブジェクトを返す **Create** メソッドを実装するユーザー実装のオブジェクトです。 このコード例では、カスタム プロトコルを実装する `CustomWebRequest` コードが既に作成されているものとします。  
  
## <a name="example"></a>例  
  
```csharp  
WebRequest.RegisterPrefix("custom", new CustomWebRequestCreator());  
WebRequest req = WebRequest.Create("custom://customHost.contoso.com/");  
```  
  
```vb  
WebRequest.RegisterPrefix("custom", New CustomWebRequestCreator())  
Dim req As WebRequest = WebRequest.Create("custom://customHost.contoso.com/")  
```  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 この例で必要な要素は次のとおりです。  
  
 <xref:System.Net> 名前空間への参照。  
  
## <a name="see-also"></a>参照  
 [プラグ可能なプロトコルのプログラミング](../../../docs/framework/network-programming/programming-pluggable-protocols.md)
