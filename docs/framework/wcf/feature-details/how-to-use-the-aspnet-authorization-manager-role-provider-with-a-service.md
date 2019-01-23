---
title: '方法: サービスと ASP.NET の承認マネージャー ロール プロバイダーを使用します。'
ms.date: 03/30/2017
ms.assetid: f21deb81-91ef-49ef-94d6-494785143271
ms.openlocfilehash: de6c96fd8d0ea17954463d554504cdb4180a5268
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54625563"
---
# <a name="how-to-use-the-aspnet-authorization-manager-role-provider-with-a-service"></a>方法: サービスと ASP.NET の承認マネージャー ロール プロバイダーを使用します。
[!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] が Web サービスをホストする場合は、承認マネージャーをアプリケーションに統合してサービスを承認することができます。 承認マネージャーを使用して、アプリケーション開発者は個々の操作を定義できます。また、個々の操作をグループ化してタスクを形成できます。 次に管理者は、ロールを承認して特定のタスクまたは個々の操作を実行できます。 承認マネージャーでは、ロール、タスク、操作、ユーザーを管理する管理ツールとして Microsoft 管理コンソール (MMC) スナップインが提供されます。 管理者は、承認マネージャーのポリシー ストアを XML ファイル、Active Directory、または Active Directory アプリケーション モード (ADAM) ストアに構成します。  
  
 承認マネージャーをアプリケーションに統合するには、Web サービスをホストする [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] アプリケーションの承認マネージャーの [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] ロール プロバイダーを構成します。 他の [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] ロール プロバイダーと同様、承認マネージャーの [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] ロール プロバイダーは <`providers`> 要素を使用して構成します。  
  
 承認マネージャーをアプリケーションに統合する Web サービスの構成ファイルの一部を示すコード例を次に示します。  
  
```xml  
<system.web>  
    <roleManager enabled="true" defaultProvider="AzManRoleProvider">  
      <providers>  
        <add name="AzManRoleProvider"  
             type="System.Web.Security.AuthorizationStoreRoleProvider, System.Web, Version=2.0.0.0, Culture=neutral, publicKeyToken=b03f5f7f11d50a3a"  
             connectionStringName="AzManPolicyStoreConnectionString"   
             applicationName="SecureService"/>  
      </providers>  
    </roleManager>  
</system.web>  
```  
  
 統合の詳細については、 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] WCF アプリケーションでは、ロール プロバイダーを参照してください[方法。ASP.NET ロール プロバイダーを使用して、サービスと](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md)します。 承認マネージャーの詳細については[!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)]を参照してください[方法。ASP.NET 2.0 で Authorization Manager (AzMan) 使用](https://go.microsoft.com/fwlink/?LinkId=71303)します。  
  
## <a name="see-also"></a>関連項目
- [方法: サービスで ASP.NET ロール プロバイダーを使用します。](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md)
