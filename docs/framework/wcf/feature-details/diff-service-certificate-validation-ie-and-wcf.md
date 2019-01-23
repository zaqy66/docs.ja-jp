---
title: Internet Explorer と WCF で実行されるサービス証明書の検証の相違点
ms.date: 03/30/2017
helpviewer_keywords:
- service certificate validation [WCF]
- certificates [WCF], service certificate validation
ms.assetid: 9dffcab2-70a9-40f0-99fd-d3a0b296028f
ms.openlocfilehash: 08a790dbbc8bc51a1e47bbcbcf90ec7c035bf3df
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549786"
---
# <a name="differences-between-service-certificate-validation-done-by-internet-explorer-and-wcf"></a><span data-ttu-id="07bac-102">Internet Explorer と WCF で実行されるサービス証明書の検証の相違点</span><span class="sxs-lookup"><span data-stu-id="07bac-102">Differences Between Service Certificate Validation Done by Internet Explorer and WCF</span></span>
<span data-ttu-id="07bac-103">Internet Explorer と Windows Communication Foundation (WCF) HTTPS を使用するときにサービス証明書の検証方法の違いのためなっても、Internet Explorer は、ヘルプ ページまたは Web サービス記述言語にアクセスできません。(WSDL)、サービスの WCF クライアントが正常にできる場合でもメッセージ、サービス エンドポイントに送信します。</span><span class="sxs-lookup"><span data-stu-id="07bac-103">Because of difference between the way Internet Explorer and Windows Communication Foundation (WCF) validate service certificates when HTTPS is used, it is possible that Internet Explorer will not be able to access the Help page or Web Services Description Language (WSDL) of a service even though a WCF client is able to successfully send messages to the service endpoints.</span></span> <span data-ttu-id="07bac-104">これは Internet Explorer のチェックがあるため、サービス証明書があるかどうか、 `ServerAuthentication` WCF では、このような制約は強制されませんが、オブジェクト識別子 (OID) の拡張使用法フラグ。</span><span class="sxs-lookup"><span data-stu-id="07bac-104">This is because Internet Explorer checks whether the service certificate has the `ServerAuthentication` object identifiers (OID) in the enhanced usage flags, whereas WCF does not enforce such a constraint.</span></span> <span data-ttu-id="07bac-105">Internet Explorer がサービス ヘルプ ページまたはサービスの WSDL にアクセスできない場合は、使用、 [ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)サービス メタデータにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="07bac-105">If Internet Explorer is unable to access the service Help page or the WSDL for the service, use the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) to access the service metadata.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="07bac-106">関連項目</span><span class="sxs-lookup"><span data-stu-id="07bac-106">See also</span></span>
- [<span data-ttu-id="07bac-107">HTTPS、SSL Over TCP、SOAP セキュリティ間における証明書検証方法の相違点</span><span class="sxs-lookup"><span data-stu-id="07bac-107">Certificate Validation Differences Between HTTPS, SSL over TCP, and SOAP Security</span></span>](../../../../docs/framework/wcf/feature-details/cert-val-diff-https-ssl-over-tcp-and-soap.md)
- [<span data-ttu-id="07bac-108">方法: メタデータの取得および準拠サービスの実装</span><span class="sxs-lookup"><span data-stu-id="07bac-108">How to: Retrieve Metadata and Implement a Compliant Service</span></span>](../../../../docs/framework/wcf/feature-details/how-to-retrieve-metadata-and-implement-a-compliant-service.md)
