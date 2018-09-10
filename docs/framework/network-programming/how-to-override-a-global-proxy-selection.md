---
title: '方法: グローバル プロキシの選択をオーバーライドする'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 0da481a9-b414-4230-beb0-e3ceba882fe5
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 244315b5df4200524685bc5b9fb75a0d7fd9b39e
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2018
ms.locfileid: "44185036"
---
# <a name="how-to-override-a-global-proxy-selection"></a>方法: グローバル プロキシの選択をオーバーライドする
この例では、`www.contoso.com` に **WebRequest** を送信し、ポート 80 の `alternateproxy` という名前のプロキシ サーバーでグローバル プロキシの選択をオーバーライドします。  
  
## <a name="example"></a>例  
  
```csharp  
WebRequest req = WebRequest.Create("http://www.contoso.com/");  
req.Proxy = new WebProxy("http://alternateproxy:80/");  
```  
  
```vb  
Dim req As WebRequest = WebRequest.Create("http://www.contoso.com/")  
req.Proxy = New WebProxy("http://alternateproxy:80/")  
```  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 この例で必要な要素は次のとおりです。  
  
-   **System.Net** 名前空間の [`using` ディレクティブ](~/docs/csharp/language-reference/keywords/using-directive.md)。  
  
## <a name="see-also"></a>参照  
 [アプリケーション プロトコルの使用](../../../docs/framework/network-programming/using-application-protocols.md)  
 [プロキシを介したインターネットへのアクセス](../../../docs/framework/network-programming/accessing-the-internet-through-a-proxy.md)
