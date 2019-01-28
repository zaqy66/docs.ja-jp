---
title: アプリケーション ドメインからのセットアップ情報の取得
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- AppDomainSetup object
- retrieving setup information
- application domains, retrieving setup information
ms.assetid: 5cdb12ae-1e37-4a62-8ec7-93d6dcc6e8d9
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0c5b43258b3ce501d1302c31a70f51341d3a84d4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54588039"
---
# <a name="retrieving-setup-information-from-an-application-domain"></a><span data-ttu-id="ccb0b-102">アプリケーション ドメインからのセットアップ情報の取得</span><span class="sxs-lookup"><span data-stu-id="ccb0b-102">Retrieving Setup Information from an Application Domain</span></span>
<span data-ttu-id="ccb0b-103">アプリケーション ドメインの各インスタンスは、プロパティと <xref:System.AppDomainSetup> 情報の両方で構成されています。</span><span class="sxs-lookup"><span data-stu-id="ccb0b-103">Each instance of an application domain consists of both properties and <xref:System.AppDomainSetup> information.</span></span> <span data-ttu-id="ccb0b-104"><xref:System.AppDomain?displayProperty=nameWithType> クラスを使って、アプリケーション ドメインからセットアップ情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="ccb0b-104">You can retrieve setup information from an application domain using the <xref:System.AppDomain?displayProperty=nameWithType> class.</span></span> <span data-ttu-id="ccb0b-105">このクラスでは、アプリケーション ドメインに関する構成情報を取得する複数のメンバーが提供されています。</span><span class="sxs-lookup"><span data-stu-id="ccb0b-105">This class provides several members that retrieve configuration information about an application domain.</span></span>  
  
 <span data-ttu-id="ccb0b-106">また、アプリケーション ドメインの **AppDomainSetup** オブジェクトに対してクエリを実行し、作成時にドメインに渡されたセットアップ情報を取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="ccb0b-106">You can also query the **AppDomainSetup** object for the application domain to obtain setup information that was passed to the domain when it was created.</span></span>  
  
 <span data-ttu-id="ccb0b-107">次の例では、新しいアプリケーション ドメインを作成し、いくつかのメンバーの値をコンソールに出力しています。</span><span class="sxs-lookup"><span data-stu-id="ccb0b-107">The following example creates a new application domain and then prints several member values to the console.</span></span>  
  
 [!code-cpp[AppDomain_Setup#2](../../../samples/snippets/cpp/VS_Snippets_CLR/AppDomain_Setup/CPP/source2.cpp#2)]
 [!code-csharp[AppDomain_Setup#2](../../../samples/snippets/csharp/VS_Snippets_CLR/AppDomain_Setup/CS/source2.cs#2)]
 [!code-vb[AppDomain_Setup#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AppDomain_Setup/VB/source2.vb#2)]  
  
 <span data-ttu-id="ccb0b-108">次の例では、アプリケーション ドメインのセットアップ情報を設定してから取得しています。</span><span class="sxs-lookup"><span data-stu-id="ccb0b-108">The following example sets, and then retrieves, setup information for an application domain.</span></span> <span data-ttu-id="ccb0b-109">`AppDomain.SetupInformation.ApplicationBase` が構成情報を取得することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ccb0b-109">Note that `AppDomain.SetupInformation.ApplicationBase` gets the configuration information.</span></span>  
  
 [!code-cpp[AppDomain_Setup#3](../../../samples/snippets/cpp/VS_Snippets_CLR/AppDomain_Setup/CPP/source3.cpp#3)]
 [!code-csharp[AppDomain_Setup#3](../../../samples/snippets/csharp/VS_Snippets_CLR/AppDomain_Setup/CS/source3.cs#3)]
 [!code-vb[AppDomain_Setup#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AppDomain_Setup/VB/source3.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="ccb0b-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="ccb0b-110">See also</span></span>
- [<span data-ttu-id="ccb0b-111">アプリケーション ドメインを使用したプログラミング</span><span class="sxs-lookup"><span data-stu-id="ccb0b-111">Programming with Application Domains</span></span>](application-domains.md#programming-with-application-domains)
- [<span data-ttu-id="ccb0b-112">アプリケーション ドメインの使用</span><span class="sxs-lookup"><span data-stu-id="ccb0b-112">Using Application Domains</span></span>](../../../docs/framework/app-domains/use.md)
