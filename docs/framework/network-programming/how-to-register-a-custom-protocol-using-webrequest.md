---
title: '方法: WebRequest を使用してカスタム プロトコルを登録する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 98ddbdb9-66b1-4080-92ad-51f5c447fcf8
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 1f78f98f94daa51c17a1294285e13dfddd457106
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47230970"
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
