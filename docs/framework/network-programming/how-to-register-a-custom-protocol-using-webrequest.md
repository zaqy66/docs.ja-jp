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
# <a name="how-to-register-a-custom-protocol-using-webrequest"></a><span data-ttu-id="52c10-102">方法: WebRequest を使用してカスタム プロトコルを登録する</span><span class="sxs-lookup"><span data-stu-id="52c10-102">How to: Register a Custom Protocol Using WebRequest</span></span>
<span data-ttu-id="52c10-103">この例では、他の場所で定義されているプロトコル固有のクラスを登録する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="52c10-103">This example shows how to register a protocol specific classthat is defined elsewhere.</span></span> <span data-ttu-id="52c10-104">この例では、`CustomWebRequestCreator` は、`CustomWebRequest` オブジェクトを返す **Create** メソッドを実装するユーザー実装のオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="52c10-104">In this example, `CustomWebRequestCreator` is the user-implemented object that implements the **Create** method that returns the `CustomWebRequest` object.</span></span> <span data-ttu-id="52c10-105">このコード例では、カスタム プロトコルを実装する `CustomWebRequest` コードが既に作成されているものとします。</span><span class="sxs-lookup"><span data-stu-id="52c10-105">The code example assumes that you have written the `CustomWebRequest` code that implements the custom protocol.</span></span>  
  
## <a name="example"></a><span data-ttu-id="52c10-106">例</span><span class="sxs-lookup"><span data-stu-id="52c10-106">Example</span></span>  
  
```csharp  
WebRequest.RegisterPrefix("custom", new CustomWebRequestCreator());  
WebRequest req = WebRequest.Create("custom://customHost.contoso.com/");  
```  
  
```vb  
WebRequest.RegisterPrefix("custom", New CustomWebRequestCreator())  
Dim req As WebRequest = WebRequest.Create("custom://customHost.contoso.com/")  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="52c10-107">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="52c10-107">Compiling the Code</span></span>  
 <span data-ttu-id="52c10-108">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="52c10-108">This example requires:</span></span>  
  
 <span data-ttu-id="52c10-109"><xref:System.Net> 名前空間への参照。</span><span class="sxs-lookup"><span data-stu-id="52c10-109">References to the <xref:System.Net> namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="52c10-110">参照</span><span class="sxs-lookup"><span data-stu-id="52c10-110">See Also</span></span>  
 [<span data-ttu-id="52c10-111">プラグ可能なプロトコルのプログラミング</span><span class="sxs-lookup"><span data-stu-id="52c10-111">Programming Pluggable Protocols</span></span>](../../../docs/framework/network-programming/programming-pluggable-protocols.md)
