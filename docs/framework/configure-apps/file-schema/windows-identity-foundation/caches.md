---
title: '&lt;キャッシュ&gt;'
ms.date: 03/30/2017
ms.assetid: 4651091b-3a20-40d8-b293-4408c0710143
author: BrucePerlerMS
ms.openlocfilehash: a91a389e53354e4f5b26e1510fc2f025300d65cc
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47192681"
---
# <a name="ltcachesgt"></a>&lt;キャッシュ&gt;
セッション トークンやトークン リプレイ検出のために使用されるキャッシュを登録します。  
  
 \<system.identityModel>  
\<identityConfiguration>  
\<キャッシュ >  
  
## <a name="syntax"></a>構文  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
 なし  
  
### <a name="child-elements"></a>子要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<sessionSecurityTokenCache >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/sessionsecuritytokencache.md)|サービスまたはセキュリティ トークン ハンドラー コレクションのセッション トークン キャッシュに登録します。|  
|[\<tokenReplayCache >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md)|トークン再生キャッシュ サービスまたはセキュリティ トークン ハンドラー コレクションに登録します。|  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|サービス レベルの id の設定を指定します。|  
|[\<securityTokenHandlerConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|トークン ハンドラー コレクションのセキュリティの構成を提供します。|  
  
## <a name="remarks"></a>Remarks  
 A`<caches>`下で、サービス レベルで要素を指定することができます、`<identityConfiguration>`要素またはセキュリティ トークン ハンドラー コレクション レベルの下で、`<securityTokenHandlerConfiguration>`要素。 トークン ハンドラー コレクションの設定は、サービスに指定されているものをオーバーライドします。  
  
 `<caches>`要素が表される、<xref:System.IdentityModel.Configuration.IdentityModelCachesElement>クラス。 構成済みのキャッシュがによって表される、<xref:System.IdentityModel.Configuration.IdentityModelCaches>クラス。  
  
## <a name="example"></a>例  
 次の XML はセッション セキュリティ トークンを保持するためのカスタム キャッシュの構成 (<xref:System.IdentityModel.Tokens.SessionSecurityToken>)。 構成から取得されますが、`ClaimsAwareWebFarm`サンプル。  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```
