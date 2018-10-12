---
title: サポートされている配置シナリオ
ms.date: 03/30/2017
ms.assetid: 3399f208-3504-4c70-a22e-a7c02a8b94a6
ms.openlocfilehash: a86fd9d50b2bdfa2daafa3bec98802d10a1efef5
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44183380"
---
# <a name="supported-deployment-scenarios"></a>サポートされている配置シナリオ
部分的に信頼されたアプリケーションで使用するためにサポートされる Windows Communication Foundation (WCF) 機能のサブセットは、WCF を使用するが、一部のシナリオの要件を満たすために設計されています。 WCF がインターネット規模の要件を満たしているサード パーティ製のアプリケーションを実行しているホスティング プロバイダーの共有、サーバー上で、[!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)]中程度の信頼アクセス許可がセキュリティ上の理由を設定します。 クライアントでは、WCF の部分信頼サポートはなどの展開テクノロジの要件を満たすために設計[ClickOnce 配置](https://go.microsoft.com/fwlink/?LinkId=83712)または[!INCLUDE[avalon2](../../../../includes/avalon2-md.md)]の XAML ブラウザー アプリケーションのテクノロジは、シームレスかつ安全に許可します。信頼されていないサイトからのデスクトップ アプリケーションの展開。  
  
## <a name="minimum-permission-requirements"></a>最小のアクセス許可の要件  
 WCF には、次の標準の名前付き権限セットのいずれかで実行されるアプリケーションの機能のサブセットがサポートされています。  
  
-   中程度の信頼アクセス許可  
  
-   インターネット ゾーン アクセス許可  
  
 制限の厳しいアクセス許可が部分的に信頼されたアプリケーションで WCF を使用しようと、実行時にセキュリティ例外が発生する可能性があります。  
  
 このようなアクセス許可セットでサポートされる機能の詳細については、「 [Partial Trust Feature Compatibility](../../../../docs/framework/wcf/feature-details/partial-trust-feature-compatibility.md)」を参照してください。  
  
## <a name="partial-trust-on-the-server"></a>サーバーでの部分信頼  
 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] Web アプリケーション ホスティング サービスのプロバイダー事業者の多くは、それぞれのサーバーで動作するアプリケーションが [!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)] の中程度の信頼アクセス許可セットを使用して実行されることを義務付けています。 使用する WCF サービスがこれらの環境で実行できる、 <xref:System.ServiceModel.BasicHttpBinding>、 <xref:System.ServiceModel.WebHttpBinding>、または <<!--zz xref:System.ServiceModel.WsHttpBinding --> `xref:System.ServiceModel.WsHttpBinding`> トランスポート レベルのセキュリティ。  
  
 中程度の信頼ホスティング環境で実行されている WCF サービスは、クライアントの要求に応答の他のサーバーにメッセージを送信して中間層サービスとしても動作できます。 ホスティング環境が適切な <xref:System.Net.WebPermission> をアプリケーションに与えて、目的のサーバーに送信要求を行うようにする場合は、サーバーでの中間層のシナリオがサポートされます。  
  
 WCF がサポートしている SOAP メッセージングを使用して、サポートされている SOAP バインディングの 1 つだけでなく、<xref:System.ServiceModel.WebHttpBinding>部分的に信頼されたアプリケーションで Web スタイル サービスを構築するためです。 [WCF Web HTTP プログラミング モデル](../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md)、 [WCF 配信](../../../../docs/framework/wcf/feature-details/wcf-syndication.md)、および[AJAX の統合と JSON のサポート](../../../../docs/framework/wcf/feature-details/ajax-integration-and-json-support.md)WCF の機能がすべて部分信頼でサポートされています。  
  
 ワークフロー サービスは完全信頼のアクセス許可を必要とし、部分的に信頼されたアプリケーションでは使用できません。  
  
 詳細については、次を参照してください。[方法: ASP.NET 2.0 の使用中程度の信頼](https://go.microsoft.com/fwlink/?LinkId=84603)します。  
  
## <a name="partial-trust-on-the-client"></a>クライアントでの部分信頼  
 信頼されていないインターネット サイトからコードをダウンロードして実行する場合、ある程度のセキュリティ対策が必要です。 両方[ClickOnce 配置](https://go.microsoft.com/fwlink/?LinkId=83712)と[!INCLUDE[avalon2](../../../../includes/avalon2-md.md)]の XAML ブラウザー アプリケーション (XBAP) テクノロジの作成を使用して、部分信頼の信頼されていないコードに制限されたアクセス許可 (インターネット ゾーン) を付与します。  
  
 WCF は、いずれかで展開された部分的に信頼されたアプリケーション内からリモート サーバーとの通信に使用できます[ClickOnce 配置](https://go.microsoft.com/fwlink/?LinkId=83712)または XBAP します。 インターネット ゾーン アクセス許可のセットが含まれる<xref:System.Net.WebPermission>で説明されている、サポートされている WCF バインドのいずれかを使用して、配信元サーバーとの通信にこれらのアプリケーションの元のホスト用できる[Partial Trust Feature Compatibility](../../../../docs/framework/wcf/feature-details/partial-trust-feature-compatibility.md).  
  
## <a name="see-also"></a>関連項目  
 [コード アクセス セキュリティ](https://go.microsoft.com/fwlink/?LinkId=83717)  
 [Windows Presentation Foundation ブラウザーによってホストされるアプリケーションの概要](https://go.microsoft.com/fwlink/?LinkId=98397)  
 [部分信頼](../../../../docs/framework/wcf/feature-details/partial-trust.md)  
 [ASP.Net の中程度の信頼](https://go.microsoft.com/fwlink/?LinkId=69328)
