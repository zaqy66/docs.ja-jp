---
title: .NET リモート処理アプリケーションの WCF への移行
ms.date: 03/30/2017
helpviewer_keywords:
- ',NET remoting [WCF]'
ms.assetid: 24793465-65ae-4308-8c12-dce4fd12a583
ms.openlocfilehash: 3f5556eeaf56ac48dd4f1d578ed2e66b90415677
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43503435"
---
# <a name="migrating-net-remoting-applications-to-wcf"></a><span data-ttu-id="d87e4-102">.NET リモート処理アプリケーションの WCF への移行</span><span class="sxs-lookup"><span data-stu-id="d87e4-102">Migrating .NET Remoting Applications to WCF</span></span>
<span data-ttu-id="d87e4-103">**このトピックの対象は、既存のアプリケーションとの下位互換性のために残されているレガシ テクノロジに特定されています。新規の開発には、このトピックを適用しないでください。WCF を使用して、分散アプリケーションを開発する必要がありますようになりました。**</span><span class="sxs-lookup"><span data-stu-id="d87e4-103">**This topic is specific to a legacy technology that is retained for backward compatibility with existing applications and is not recommended for new development. Distributed applications should now be developed using WCF.**</span></span>  
  
 <span data-ttu-id="d87e4-104">既存の .NET リモート処理アプリケーションと WCF を活用するために 2 つの方法があります。 統合と移行します。</span><span class="sxs-lookup"><span data-stu-id="d87e4-104">There are two ways to take advantage of WCF with existing .NET Remoting applications: integration and migration.</span></span> <span data-ttu-id="d87e4-105">統合により、.net Remoting 2.0 とを実行している WCF サイト側では、によって、既存の .Net を変更することがなく同時に両方のテクノロジを同じビジネス オブジェクトを公開することができます Remoting 2.0 コード。</span><span class="sxs-lookup"><span data-stu-id="d87e4-105">Integration allows you to have .Net Remoting 2.0 and WCF running side by side, letting you expose the same business objects over both technologies simultaneously without having to modify your existing .Net Remoting 2.0 code.</span></span> <span data-ttu-id="d87e4-106">統合では、[!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] 2.0 以降が実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d87e4-106">Integration requires that you are running on [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] 2.0 or greater.</span></span> <span data-ttu-id="d87e4-107">WCF の機能を利用して、Remoting 2.0 システムとの互換性を配線する必要はない場合、は、サービス全体を WCF に移行することができます。</span><span class="sxs-lookup"><span data-stu-id="d87e4-107">If you want to take advantage of WCF features and do not need wire compatibility with Remoting 2.0 systems, you can migrate your entire service to WCF.</span></span> <span data-ttu-id="d87e4-108">.NET Remoting 2.0 から WCF への移行では、リモート オブジェクトのインターフェイスとその構成設定の変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="d87e4-108">Migration from .NET Remoting 2.0 to WCF requires changes to the remote object's interface and its configuration settings.</span></span> <span data-ttu-id="d87e4-109">両方のトピックに掲載されて[を Windows Communication Foundation からリモート処理](https://go.microsoft.com/fwlink/?LinkId=74403)します。</span><span class="sxs-lookup"><span data-stu-id="d87e4-109">Both of these topics are covered in [From Remoting to the Windows Communication Foundation](https://go.microsoft.com/fwlink/?LinkId=74403).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d87e4-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="d87e4-110">See Also</span></span>  
 [<span data-ttu-id="d87e4-111">概念</span><span class="sxs-lookup"><span data-stu-id="d87e4-111">Conceptual Overview</span></span>](../../../../docs/framework/wcf/conceptual-overview.md)
