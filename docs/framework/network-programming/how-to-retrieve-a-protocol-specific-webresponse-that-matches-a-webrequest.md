---
title: '方法: WebRequest に一致するプロトコル固有の WebResponse を取得する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d8c90785-f16b-42a5-8439-ed2f731b2ba8
ms.openlocfilehash: 3b3b523d6248b3c61a0994728b035bc6f02d5cf1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745351"
---
# <a name="how-to-retrieve-a-protocol-specific-webresponse-that-matches-a-webrequest"></a><span data-ttu-id="a19f0-102">方法: WebRequest に一致するプロトコル固有の WebResponse を取得する</span><span class="sxs-lookup"><span data-stu-id="a19f0-102">How to: Retrieve a Protocol-Specific WebResponse that Matches a WebRequest</span></span>
<span data-ttu-id="a19f0-103">この例では、WebRequest に一致するプロトコル固有の WebResponse を取得する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="a19f0-103">This example shows how to retrieve a protocol-specific WebResponse that matches a WebRequest.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a19f0-104">例</span><span class="sxs-lookup"><span data-stu-id="a19f0-104">Example</span></span>  
  
```csharp  
WebRequest req = WebRequest.Create("http://www.contoso.com/");  
WebResponse resp = req.GetResponse();  
```  
  
```vb  
Dim req As WebRequest = WebRequest.Create("http://www.contoso.com")  
Dim resp As WebResponse = req.GetResponse()  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="a19f0-105">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="a19f0-105">Compiling the Code</span></span>  
 <span data-ttu-id="a19f0-106">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a19f0-106">This example requires:</span></span>  
  
-   <span data-ttu-id="a19f0-107">**System.Net** 名前空間への参照。</span><span class="sxs-lookup"><span data-stu-id="a19f0-107">References to the **System.Net** namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a19f0-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="a19f0-108">See also</span></span>
- [<span data-ttu-id="a19f0-109">データの要求</span><span class="sxs-lookup"><span data-stu-id="a19f0-109">Requesting Data</span></span>](../../../docs/framework/network-programming/requesting-data.md)
