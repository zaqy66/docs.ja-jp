---
title: '&lt;sessionSecurityTokenCache&gt;'
ms.date: 03/30/2017
ms.assetid: d43e676c-0153-485c-ab31-0257a2db7507
author: BrucePerlerMS
ms.openlocfilehash: b812673ac1c015adde357d3c0707d85643aad3e9
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47084333"
---
# <a name="ltsessionsecuritytokencachegt"></a>&lt;sessionSecurityTokenCache&gt;
サービスまたはセキュリティ トークン ハンドラー コレクションのセッション トークン キャッシュに登録します。  
  
 \<system.identityModel>  
\<identityConfiguration>  
\<キャッシュ >  
\<sessionSecurityTokenCache >  
  
## <a name="syntax"></a>構文  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
      <sessionSecurityTokenCache type=xs:string>  
      </sessionSecurityTokenCache>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|型|派生した型、<xref:System.IdentityModel.Tokens.SessionSecurityTokenCache>クラス。|  
  
### <a name="child-elements"></a>子要素  
 なし  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<キャッシュ >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|サービスまたはセキュリティ トークン ハンドラー コレクションで使用されるキャッシュを登録します。|  
  
## <a name="example"></a>例  
 次の XML はセッション セキュリティ トークンを保持するためのカスタム キャッシュの構成 (<xref:System.IdentityModel.Tokens.SessionSecurityToken>)。 構成から取得されますが、`ClaimsAwareWebFarm`サンプル。 このサンプルの詳細については、次を参照してください。 [WIF コード サンプル インデックス](../../../../../docs/framework/security/wif-code-sample-index.md)します。  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```  
  
## <a name="see-also"></a>関連項目  
 <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache>
