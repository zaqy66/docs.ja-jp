---
title: '方法: Web ページを要求し、ストリームとして結果を取得する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d32b7f35-29d8-4fb7-ad71-d219edc5e359
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 2ceaa7cbaf2035276a0ba0105f3969f0249c6132
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2018
ms.locfileid: "47402605"
---
# <a name="how-to-request-a-web-page-and-retrieve-the-results-as-a-stream"></a><span data-ttu-id="84960-102">方法: Web ページを要求し、ストリームとして結果を取得する</span><span class="sxs-lookup"><span data-stu-id="84960-102">How to: Request a Web Page and Retrieve the Results as a Stream</span></span>
<span data-ttu-id="84960-103">この例では、Web ページを要求し、ストリームとして結果を取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="84960-103">This example shows how to request a Web page and retrieve the results in a stream.</span></span>  
  
## <a name="example"></a><span data-ttu-id="84960-104">例</span><span class="sxs-lookup"><span data-stu-id="84960-104">Example</span></span>  
  
```csharp  
WebClient myClient = new WebClient();  
Stream response = myClient.OpenRead("http://www.contoso.com/index.htm");  
// The stream data is used here.  
response.Close();  
```  
  
```vb  
Dim myClient As WebClient = New WebClient()  
Dim response As Stream = myClient.OpenRead("http://www.contoso.com/index.htm")  
' The stream data is used here.  
response.Close()  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="84960-105">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="84960-105">Compiling the Code</span></span>  
 <span data-ttu-id="84960-106">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="84960-106">This example requires:</span></span>  
  
-   <span data-ttu-id="84960-107"><xref:System.IO> 名前空間と <xref:System.Net> 名前空間への参照。</span><span class="sxs-lookup"><span data-stu-id="84960-107">References to the <xref:System.IO> and <xref:System.Net> namespaces.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84960-108">参照</span><span class="sxs-lookup"><span data-stu-id="84960-108">See Also</span></span>  
 [<span data-ttu-id="84960-109">データの要求</span><span class="sxs-lookup"><span data-stu-id="84960-109">Requesting Data</span></span>](../../../docs/framework/network-programming/requesting-data.md)
