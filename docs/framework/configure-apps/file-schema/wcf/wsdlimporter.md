---
title: <wsdlImporter>
ms.date: 03/30/2017
ms.assetid: 986b2165-8430-4dba-b1b8-00396841bb96
ms.openlocfilehash: bd6c8661f94610d932ffee631aee7ad060f04c6b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55269316"
---
# <a name="wsdlimporter"></a><span data-ttu-id="b1df2-101">\<wsdlImporter ></span><span class="sxs-lookup"><span data-stu-id="b1df2-101">\<wsdlImporter></span></span>
<span data-ttu-id="b1df2-102">WS-Policy が添付された Web サービス記述言語 (WSDL) 1.1 メタデータをインポートするすべての WSDL インポーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="b1df2-102">Specifies all the WSDL importers that imports Web Services Description Language (WSDL) 1.1 metadata with WS-Policy attachments.</span></span>  
  
<span data-ttu-id="b1df2-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="b1df2-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="b1df2-104">\<client></span><span class="sxs-lookup"><span data-stu-id="b1df2-104">\<client></span></span>  
<span data-ttu-id="b1df2-105">\<matadata></span><span class="sxs-lookup"><span data-stu-id="b1df2-105">\<metadata></span></span>  
<span data-ttu-id="b1df2-106">\<wsdlImporters></span><span class="sxs-lookup"><span data-stu-id="b1df2-106">\<wsdlImporters></span></span>  
<span data-ttu-id="b1df2-107">\<wsdlImporter ></span><span class="sxs-lookup"><span data-stu-id="b1df2-107">\<wsdlImporter></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1df2-108">構文</span><span class="sxs-lookup"><span data-stu-id="b1df2-108">Syntax</span></span>  
  
```xml  
<metadata>
  <wsdlImporters>
    <wsdlImporter type="string" />
  </wsdlImporters>
</metadata>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b1df2-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="b1df2-109">Attributes and Elements</span></span>  
 <span data-ttu-id="b1df2-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="b1df2-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b1df2-111">属性</span><span class="sxs-lookup"><span data-stu-id="b1df2-111">Attributes</span></span>  
  
|<span data-ttu-id="b1df2-112">属性</span><span class="sxs-lookup"><span data-stu-id="b1df2-112">Attribute</span></span>|<span data-ttu-id="b1df2-113">説明</span><span class="sxs-lookup"><span data-stu-id="b1df2-113">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="b1df2-114">この要素の型です。</span><span class="sxs-lookup"><span data-stu-id="b1df2-114">The type of this element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b1df2-115">子要素</span><span class="sxs-lookup"><span data-stu-id="b1df2-115">Child Elements</span></span>  
 <span data-ttu-id="b1df2-116">なし。</span><span class="sxs-lookup"><span data-stu-id="b1df2-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b1df2-117">親要素</span><span class="sxs-lookup"><span data-stu-id="b1df2-117">Parent Elements</span></span>  
  
|<span data-ttu-id="b1df2-118">要素</span><span class="sxs-lookup"><span data-stu-id="b1df2-118">Element</span></span>|<span data-ttu-id="b1df2-119">説明</span><span class="sxs-lookup"><span data-stu-id="b1df2-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b1df2-120">\<wsdlImporters></span><span class="sxs-lookup"><span data-stu-id="b1df2-120">\<wsdlImporters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdlimporters.md)|<span data-ttu-id="b1df2-121">WS-Policy が添付された Web サービス記述言語 (WSDL) 1.1 メタデータをインポートするすべての WSDL インポーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="b1df2-121">Specifies all the WSDL importers that imports Web Services Description Language (WSDL) 1.1 metadata with WS-Policy attachments.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b1df2-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="b1df2-122">Remarks</span></span>  
 <span data-ttu-id="b1df2-123">WSDL インポーターは、メタデータのインポートに加えて、コントラクトおよびエンドポイント情報を表すさまざまなクラスにその情報を変換するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b1df2-123">A WSDL importer is used to import metadata as well as convert that information into various classes that represent contract and endpoint information.</span></span> <span data-ttu-id="b1df2-124">コントラクトおよびエンドポイントの情報やプロパティを選択的にインポートできます。これらは、任意のインポート エラーを公開し、インポートおよび変換プロセスに関連する型情報を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="b1df2-124">It can selectively import contract and endpoint information and properties that expose any import errors and accept type information relevant to the import and conversion process.</span></span> <span data-ttu-id="b1df2-125">また、任意のポリシー ドキュメント、WSDL ドキュメント、WSDL 拡張、および XML スキーマ ドキュメントにアクセスするためのバインディング情報およびプロパティのインポートもサポートします。</span><span class="sxs-lookup"><span data-stu-id="b1df2-125">It also supports importing binding information and properties that provide access to any policy documents, WSDL documents, WSDL extensions, and XML schema documents.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1df2-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1df2-126">See also</span></span>
- <xref:System.ServiceModel.Configuration.WsdlImporterElement>
- <xref:System.ServiceModel.Configuration.MetadataElement>
- <xref:System.ServiceModel.Configuration.WsdlImporterElementCollection>
- <xref:System.ServiceModel.Description.MetadataImporter>
- <xref:System.ServiceModel.Description.WsdlImporter>
- [<span data-ttu-id="b1df2-127">WCF クライアントの構成</span><span class="sxs-lookup"><span data-stu-id="b1df2-127">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)
- [<span data-ttu-id="b1df2-128">クライアント</span><span class="sxs-lookup"><span data-stu-id="b1df2-128">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
