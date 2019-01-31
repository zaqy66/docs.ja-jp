---
title: <developmentMode> 要素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/developmentMode
- http://schemas.microsoft.com/.NetConfiguration/v2.0#developmentMode
helpviewer_keywords:
- developmentMode element
- container tags, <developmentMode> element
- <developmentMode> element
ms.assetid: 60e79a8c-415a-497d-be29-b9d0fd9bdee3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 323bc5d18860c00609a92e33f4a2bd2c832b05a9
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55290070"
---
# <a name="developmentmode-element"></a>\<developmentMode > 要素
DEVPATH 環境変数によって指定されたディレクトリで、ランタイムがアセンブリの検索を行うかどうかを指定します。  
  
 \<configuration>  
\<runtime>  
\<developmentMode>  
  
## <a name="syntax"></a>構文  
  
```xml  
<developmentMode developerInstallation="true | false"/>  
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|**developerInstallation**|DEVPATH 環境変数によって指定されたディレクトリで、ランタイムがアセンブリの検索を行うかどうかを指定します。|  
  
## <a name="developerinstallation-attribute"></a>developerInstallation 属性  
  
|[値]|説明|  
|-----------|-----------------|  
|**true**|DEVPATH 環境変数によって指定されたディレクトリ内のアセンブリを検索します。|  
|**false**|DEVPATH 環境変数によって指定されたディレクトリ内のアセンブリを検索しません。 これは、既定値です。|  
  
### <a name="child-elements"></a>子要素  
 なし。  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|`configuration`|共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。|  
|`runtime`|アセンブリのバインディングとガベージ コレクションに関する情報が含まれています。|  
  
## <a name="remarks"></a>Remarks  
 開発時にのみ、この設定を使用します。 ランタイムは、DEVPATH に厳密な名前のアセンブリのバージョンをチェックしません。 単に最初に見つかったアセンブリを使用します。  
  
## <a name="example"></a>例  
 次の例では、ランタイムが DEVPATH 環境変数で指定されたディレクトリでアセンブリを検索する方法を示します。  
  
```xml  
<configuration>  
   <runtime>  
      <developmentMode developerInstallation="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>関連項目
- [ランタイム設定スキーマ](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [構成ファイル スキーマ](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [方法: DEVPATH を使用してアセンブリを検索します。](../../../../../docs/framework/configure-apps/how-to-locate-assemblies-by-using-devpath.md)
