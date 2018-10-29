---
title: '方法: WebRequest に一致するプロトコル固有の WebResponse を取得する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d8c90785-f16b-42a5-8439-ed2f731b2ba8
ms.openlocfilehash: f1da226fb62c55f37183404765430c094f1cd63f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188275"
---
# <a name="how-to-retrieve-a-protocol-specific-webresponse-that-matches-a-webrequest"></a><span data-ttu-id="ed7a5-102">方法: WebRequest に一致するプロトコル固有の WebResponse を取得する</span><span class="sxs-lookup"><span data-stu-id="ed7a5-102">How to: Retrieve a Protocol-Specific WebResponse that Matches a WebRequest</span></span>
<span data-ttu-id="ed7a5-103">この例では、WebRequest に一致するプロトコル固有の WebResponse を取得する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="ed7a5-103">This example shows how to retrieve a protocol-specific WebResponse that matches a WebRequest.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ed7a5-104">例</span><span class="sxs-lookup"><span data-stu-id="ed7a5-104">Example</span></span>  
  
```csharp  
WebRequest req = WebRequest.Create("http://www.contoso.com/");  
WebResponse resp = req.GetResponse();  
```  
  
```vb  
Dim req As WebRequest = WebRequest.Create("http://www.contoso.com")  
Dim resp As WebResponse = req.GetResponse()  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="ed7a5-105">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="ed7a5-105">Compiling the Code</span></span>  
 <span data-ttu-id="ed7a5-106">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ed7a5-106">This example requires:</span></span>  
  
-   <span data-ttu-id="ed7a5-107">**System.Net** 名前空間への参照。</span><span class="sxs-lookup"><span data-stu-id="ed7a5-107">References to the **System.Net** namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed7a5-108">参照</span><span class="sxs-lookup"><span data-stu-id="ed7a5-108">See Also</span></span>  
 [<span data-ttu-id="ed7a5-109">データの要求</span><span class="sxs-lookup"><span data-stu-id="ed7a5-109">Requesting Data</span></span>](../../../docs/framework/network-programming/requesting-data.md)
