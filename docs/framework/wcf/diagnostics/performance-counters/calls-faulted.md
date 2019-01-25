---
title: 失敗した呼び出し
ms.date: 03/30/2017
ms.assetid: bb9e8045-6aeb-4b7f-a825-8283c44252a1
ms.openlocfilehash: 456dbc924579cd792e746b422b074f19403137ee
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54712536"
---
# <a name="calls-faulted"></a><span data-ttu-id="1db13-102">失敗した呼び出し</span><span class="sxs-lookup"><span data-stu-id="1db13-102">Calls Faulted</span></span>
<span data-ttu-id="1db13-103">カウンター名:失敗した呼び出し</span><span class="sxs-lookup"><span data-stu-id="1db13-103">Counter Name: Calls Faulted</span></span>  
  
## <a name="description"></a><span data-ttu-id="1db13-104">説明</span><span class="sxs-lookup"><span data-stu-id="1db13-104">Description</span></span>  
 <span data-ttu-id="1db13-105">この操作への呼び出しに失敗した回数です。</span><span class="sxs-lookup"><span data-stu-id="1db13-105">Number of calls to this operation that returned faults.</span></span> <span data-ttu-id="1db13-106">Windows Communication Foundation (WCF) アプリケーションでは、サービス メソッドは、SOAP エラー メッセージを使用して、処理のエラー情報を通知します。</span><span class="sxs-lookup"><span data-stu-id="1db13-106">In Windows Communication Foundation (WCF) applications, service methods communicate processing error information using SOAP fault messages.</span></span> <span data-ttu-id="1db13-107">SOAP エラーは、サービス操作のメタデータに含まれるメッセージ型であり、堅牢かつインタラクティブに実行できるようにクライアントが使用するエラー コントラクトを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1db13-107">SOAP faults are message types that are included in the metadata for a service operation and therefore create a fault contract that clients can use to make their execution more robust or interactive.</span></span> <span data-ttu-id="1db13-108">SOAP エラーは XML 形式でクライアントに渡されるので、相互運用性の面でも優れています。</span><span class="sxs-lookup"><span data-stu-id="1db13-108">Since SOAP faults are expressed to clients in XML form, they are highly interoperable.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1db13-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="1db13-109">See also</span></span>
- [<span data-ttu-id="1db13-110">コントラクトおよびサービスのエラーの指定と処理</span><span class="sxs-lookup"><span data-stu-id="1db13-110">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
