---
title: <wsdlImporters>
ms.date: 03/30/2017
ms.assetid: 270c7f93-eab7-47b6-8b94-ac3f5b7f17e4
ms.openlocfilehash: 81fb25f6a77456608fd3cb0d5e73f67c7f7867c3
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55274574"
---
# <a name="wsdlimporters"></a><span data-ttu-id="7738e-101">\<wsdlImporters></span><span class="sxs-lookup"><span data-stu-id="7738e-101">\<wsdlImporters></span></span>
<span data-ttu-id="7738e-102">この構成要素は、WS-Policy が添付された Web サービス記述言語 (WSDL) 1.1 メタデータをインポートするすべての WSDL インポートを指定します。</span><span class="sxs-lookup"><span data-stu-id="7738e-102">This configuration element specifies all the WSDL importers that imports Web Services Description Language (WSDL) 1.1 metadata with WS-Policy attachments.</span></span> <span data-ttu-id="7738e-103">各子要素は、メタデータをインポートし、その情報をコントラクトおよびエンドポイント情報を表すさまざまなクラスに変換する方法を指定する <`wsdlImporter`> です。</span><span class="sxs-lookup"><span data-stu-id="7738e-103">Each child element is a <`wsdlImporter`> that specifies the way to import metadata as well as convert that information into various classes that represent contract and endpoint information.</span></span> <span data-ttu-id="7738e-104">コントラクトおよびエンドポイントの情報やプロパティを選択的にインポートできます。これらは、任意のインポート エラーを公開し、インポートおよび変換プロセスに関連する型情報を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="7738e-104">It can selectively import contract and endpoint information and properties that expose any import errors and accept type information relevant to the import and conversion process.</span></span> <span data-ttu-id="7738e-105">また、任意のポリシー ドキュメント、WSDL ドキュメント、WSDL 拡張、および XML スキーマ ドキュメントにアクセスするためのバインディング情報およびプロパティのインポートもサポートします。</span><span class="sxs-lookup"><span data-stu-id="7738e-105">It also supports importing binding information and properties that provide access to any policy documents, WSDL documents, WSDL extensions, and XML schema documents.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7738e-106">関連項目</span><span class="sxs-lookup"><span data-stu-id="7738e-106">See also</span></span>
- <xref:System.ServiceModel.Configuration.MetadataElement>
- <xref:System.ServiceModel.Configuration.WsdlImporterElementCollection>
- <xref:System.ServiceModel.Description.MetadataImporter>
- <xref:System.ServiceModel.Description.WsdlImporter>
- [<span data-ttu-id="7738e-107">WCF クライアントの構成</span><span class="sxs-lookup"><span data-stu-id="7738e-107">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)
- [<span data-ttu-id="7738e-108">クライアント</span><span class="sxs-lookup"><span data-stu-id="7738e-108">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
