---
title: 操作方法：カスタム セキュリティ トークン プロバイダーを作成します。
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- security [WCF], providing credentials
ms.assetid: db8cb478-aa43-478b-bf97-c6489ad7c7fd
ms.openlocfilehash: 88200b41346a18732647602fb16774610014330c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53131067"
---
# <a name="how-to-create-a-custom-security-token-provider"></a>操作方法：カスタム セキュリティ トークン プロバイダーを作成します。
ここでは、カスタム セキュリティ トークン プロバイダーを持つ新しいトークンの種類を作成する方法と、そのプロバイダーをカスタム セキュリティ トークン マネージャーと統合する方法について説明します。  
  
> [!NOTE]
>  <xref:System.IdentityModel.Tokens> 名前空間にあるシステム指定のトークンがユーザーの要件に一致しない場合、カスタム トークン プロバイダーを作成します。  
  
 セキュリティ トークン プロバイダーは、クライアントまたはサービスの資格情報に基づいてセキュリティ トークンの表現を作成します。 Windows Communication Foundation (WCF) のセキュリティでカスタム セキュリティ トークン プロバイダーを使用するには、カスタム資格情報とセキュリティ トークン マネージャーの実装を作成する必要があります。  
  
 カスタム資格情報とセキュリティ トークン マネージャーの詳細については、次を参照してください。、[チュートリアル。カスタムのクライアントとサービスの資格情報を作成する](../../../../docs/framework/wcf/extending/walkthrough-creating-custom-client-and-service-credentials.md)します。  
  
 資格情報の詳細については、セキュリティ トークン マネージャー、プロバイダーおよび認証子のクラスを参照してください、[セキュリティ アーキテクチャ](https://msdn.microsoft.com/library/16593476-d36a-408d-808c-ae6fd483e28f)します。  
  
### <a name="to-create-a-custom-security-token-provider"></a>カスタム セキュリティ トークン プロバイダーを作成するには  
  
1.  <xref:System.IdentityModel.Selectors.SecurityTokenProvider> クラスから派生する新しいクラスを定義します。  
  
2.  <xref:System.IdentityModel.Selectors.SecurityTokenProvider.GetTokenCore%28System.TimeSpan%29> メソッドを実装します。 このメソッドは、セキュリティ トークンのインスタンスを作成して返す役割を担います。 `MySecurityTokenProvider` という名前のクラスを作成し、<xref:System.IdentityModel.Selectors.SecurityTokenProvider.GetTokenCore%28System.TimeSpan%29> メソッドをオーバーライドして <xref:System.IdentityModel.Tokens.X509SecurityToken> クラスのインスタンスを返す例を次に示します。 クラス コンストラクターには <xref:System.Security.Cryptography.X509Certificates.X509Certificate2> クラスのインスタンスが必要です。  
  
     [!code-csharp[c_CustomTokenProvider#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_customtokenprovider/cs/source.cs#1)]
     [!code-vb[c_CustomTokenProvider#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_customtokenprovider/vb/source.vb#1)]  
  
### <a name="to-integrate-a-custom-security-token-provider-with-a-custom-security-token-manager"></a>カスタム セキュリティ トークン マネージャーにカスタム セキュリティ トークン プロバイダーを統合するには  
  
1.  <xref:System.IdentityModel.Selectors.SecurityTokenManager> クラスから派生する新しいクラスを定義します。 以下の例は、<xref:System.ServiceModel.ClientCredentialsSecurityTokenManager> クラスから派生した <xref:System.IdentityModel.Selectors.SecurityTokenManager> クラスから派生したクラスです。  
  
2.  まだオーバーライドされていない場合は、<xref:System.IdentityModel.Selectors.SecurityTokenManager.CreateSecurityTokenProvider%28System.IdentityModel.Selectors.SecurityTokenRequirement%29> メソッドをオーバーライドします。  
  
     <xref:System.IdentityModel.Selectors.SecurityTokenManager.CreateSecurityTokenProvider%28System.IdentityModel.Selectors.SecurityTokenRequirement%29>メソッドのインスタンスを返す、<xref:System.IdentityModel.Selectors.SecurityTokenProvider>クラスに適した、 <xref:System.IdentityModel.Selectors.SecurityTokenRequirement> WCF セキュリティのフレームワークで、メソッドに渡されるパラメーター。 メソッドが適切なセキュリティ トークン パラメーターで呼び出された場合に、カスタム セキュリティ トークン プロバイダーの実装 (以前の手順で作成済み) を返すようにメソッドを変更します。 セキュリティ トークン マネージャーの詳細については、次を参照してください。、[チュートリアル。カスタムのクライアントとサービスの資格情報を作成する](../../../../docs/framework/wcf/extending/walkthrough-creating-custom-client-and-service-credentials.md)します。  
  
3.  <xref:System.IdentityModel.Selectors.SecurityTokenRequirement> パラメーターに基づいてカスタム セキュリティ トークン プロバイダーを返すカスタム ロジックをメソッドに追加します。 トークンの要件が満たされた場合に、カスタム セキュリティ トークン プロバイダーを返す例を次に示します。 要件には、X.509 セキュリティ トークンとメッセージの方向 (メッセージ出力にトークンが使用される) が含まれます。 他のすべての場合で、コードは基本クラスを呼び出し、他のセキュリティ トークンの要件に合わせてシステム指定の動作を維持します。  
  
 [!code-csharp[c_CustomTokenProvider#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_customtokenprovider/cs/source.cs#2)]
 [!code-vb[c_CustomTokenProvider#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_customtokenprovider/vb/source.vb#2)]  
  
## <a name="example"></a>例  
 完全な <xref:System.IdentityModel.Selectors.SecurityTokenProvider> 実装と対応する <xref:System.IdentityModel.Selectors.SecurityTokenManager> 実装を次に示します。  
  
 [!code-csharp[c_CustomTokenProvider#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_customtokenprovider/cs/source.cs#0)]
 [!code-vb[c_CustomTokenProvider#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_customtokenprovider/vb/source.vb#0)]  
  
## <a name="see-also"></a>関連項目  
 <xref:System.IdentityModel.Selectors.SecurityTokenProvider>  
 <xref:System.IdentityModel.Selectors.SecurityTokenRequirement>  
 <xref:System.IdentityModel.Selectors.SecurityTokenManager>  
 <xref:System.IdentityModel.Tokens.X509SecurityToken>  
 [チュートリアル:カスタムのクライアントとサービスの資格情報を作成します。](../../../../docs/framework/wcf/extending/walkthrough-creating-custom-client-and-service-credentials.md)  
 [操作方法：カスタム セキュリティ トークン オーセンティケーターを作成します。](../../../../docs/framework/wcf/extending/how-to-create-a-custom-security-token-authenticator.md)  
 [セキュリティ アーキテクチャ](https://msdn.microsoft.com/library/16593476-d36a-408d-808c-ae6fd483e28f)
