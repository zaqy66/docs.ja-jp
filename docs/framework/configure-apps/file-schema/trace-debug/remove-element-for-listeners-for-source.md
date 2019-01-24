---
title: '&lt;削除&gt;要素&lt;リスナー&gt;の&lt;ソース&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners/remove
helpviewer_keywords:
- remove element for <listeners> for <source>
- <remove> element for <listeners> for <source>
ms.assetid: 3ff6b578-273d-407f-b07f-8251f1f9f5d0
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 8beb3ef041b153535afcb8bd92e1c29787e1f161
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654413"
---
# <a name="ltremovegt-element-for-ltlistenersgt-for-ltsourcegt"></a>&lt;削除&gt;要素&lt;リスナー&gt;の&lt;ソース&gt;
トレース ソースの `Listeners` コレクションからリスナーを削除します。  
  
 \<configuration>  
\<system.diagnostics>  
\<ソース >  
\<ソース >  
\<listeners>  
\<remove>  
  
## <a name="syntax"></a>構文  
  
```xml  
<remove name="listenerName" />  
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|`name`|必須の属性です。<br /><br /> 削除するリスナーの名前、`Listeners`コレクション。|  
  
### <a name="child-elements"></a>子要素  
 なし。  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|`configuration`|共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。|  
|`system.diagnostics`|メッセージを収集、格納、およびルーティングするトレース リスナーとトレース スイッチを設定するレベルを指定します。|  
|`sources`|トレース メッセージを開始するトレース ソースを保持します。|  
|`source`|トレース メッセージを開始するトレース ソースを指定します。|  
|`listeners`|収集、格納、およびメッセージをルーティングするリスナーを指定します。|  
  
## <a name="remarks"></a>Remarks  
 `<remove>`要素から指定されたリスナーの削除、`Listeners`トレース ソースのコレクション。  
  
 要素を削除することができます、`Listeners`呼び出すことによってプログラムでトレース ソースのコレクション、<xref:System.Diagnostics.TraceListenerCollection.Remove%2A>メソッドを<xref:System.Diagnostics.TraceSource.Listeners%2A>のプロパティ、<xref:System.Diagnostics.TraceSource>インスタンス。  
  
 この要素は、マシン構成ファイル (Machine.config) と、アプリケーション構成ファイルで使用できます。  
  
## <a name="example"></a>例  
 次の例は、使用する方法を示します、`<remove>`要素を使用する前に、`<add>`リスナーを追加する要素`console`を`Listeners`トレース ソースのコレクション`TraceSourceApp`します。  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="TraceSourceApp" switchName="sourceSwitch"   
         switchType="System.Diagnostics.SourceSwitch" >  
         <listeners>  
           <remove name="Default"/>  
           <add name="console"   
             type="System.Diagnostics.ConsoleTraceListener" />  
         </listeners>  
      </source>  
    </sources>  
  </system.diagnostics>  
</configuration>   
```  
  
## <a name="see-also"></a>関連項目
- <xref:System.Diagnostics.TraceSource.Listeners%2A>
- <xref:System.Diagnostics.TraceSource>
- [トレースおよびデバッグ設定のスキーマ](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
- [\<clear>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/clear-element-for-listeners-for-source.md)
- [トレース リスナー](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
