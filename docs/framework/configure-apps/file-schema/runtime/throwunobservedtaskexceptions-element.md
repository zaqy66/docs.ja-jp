---
title: <ThrowUnobservedTaskExceptions> 要素
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ThrowUnobservedTaskExceptions element
- <ThrowUnobservedTaskExceptions> element
ms.assetid: cea7e588-8b8d-48d2-9ad5-8feaf3642c18
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3bc2bffa11c3205c265ca21a9d4c4caa9b31d4e9
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55281503"
---
# <a name="throwunobservedtaskexceptions-element"></a>\<ThrowUnobservedTaskExceptions > 要素
タスクがハンドルされない例外によって実行中のプロセスを終了するかどうかを指定します。  
  
 \<configuration>  
\<runtime>  
\<ThrowUnobservedTaskExceptions >  
  
## <a name="syntax"></a>構文  
  
```xml  
<ThrowUnobservedTaskExceptions  
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|`enabled`|必須の属性です。<br /><br /> タスクがハンドルされない例外が実行中のプロセスを終了するかどうかを指定します。|  
  
## <a name="enabled-attribute"></a>enabled 属性  
  
|値|説明|  
|-----------|-----------------|  
|`false`|タスクがハンドルされない例外の実行中のプロセスを終了しません。 既定値です。|  
|`true`|タスクがハンドルされない例外の実行中のプロセスを終了します。|  
  
### <a name="child-elements"></a>子要素  
 なし。  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|`configuration`|共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。|  
|`runtime`|ランタイム初期化オプションに関する情報を含んでいます。|  
|||  
  
## <a name="remarks"></a>Remarks  
 例外に関連付けられている場合、<xref:System.Threading.Tasks.Task>が監視されていません、あるありません<xref:System.Threading.Tasks.Task.Wait%2A>操作、親がアタッチされていないと、<xref:System.Threading.Tasks.Task.Exception%2A?displayProperty=nameWithType>プロパティは、タスクの例外を監視できないと見なさが読み取られていません。  
  
 [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)]により、既定では場合、<xref:System.Threading.Tasks.Task>を持つ、無視された例外は、ガベージ コレクション、ファイナライザーが例外をスローし、プロセスを終了します。 プロセスの終了は、ガベージ コレクションとファイナライズのタイミングによって決まります。  
  
 タスク ベースの非同期コードを記述する開発者向けに容易にできるように、[!INCLUDE[net_v45](../../../../../includes/net-v45-md.md)]監視されていない例外の場合は、この既定動作が変わります。 無視された例外の原因となる、<xref:System.Threading.Tasks.TaskScheduler.UnobservedTaskException>イベントを発生させるには、既定では、プロセスを終了しません。 代わりに、イベント ハンドラーが例外を監視するかどうかに関係なく、イベントが発生した後、例外は無視されます。  
  
 [!INCLUDE[net_v45](../../../../../includes/net-v45-md.md)]、使用することができます、 [ \<ThrowUnobservedTaskExceptions > 要素](../../../../../docs/framework/configure-apps/file-schema/runtime/throwunobservedtaskexceptions-element.md)を有効にするアプリケーション構成ファイルで、[!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)]動作が例外をスローします。  
  
 次の方法のいずれかで例外の動作を指定することもできます。  
  
-   環境変数を設定して`COMPlus_ThrowUnobservedTaskExceptions`(`set COMPlus_ThrowUnobservedTaskExceptions=1`)。  
  
-   DWORD のレジストリ設定値 ThrowUnobservedTaskExceptions = 1 に、hkey_local_machine \software\microsoft\\します。NETFramework キー。  
  
## <a name="example"></a>例  
 次の例では、アプリケーション構成ファイルを使用して、タスクでの例外のスローを有効にする方法を示します。  
  
```xml  
<configuration>   
    <runtime>   
        <ThrowUnobservedTaskExceptions enabled="true"/>   
    </runtime>   
</configuration>  
```  
  
## <a name="example"></a>例  
 次の例では、タスクから無視された例外をスローする方法を示します。 コードは、正常に動作するリリース プログラムとして実行する必要があります。  
  
 [!code-csharp[ThrowUnobservedTaskExceptions#1](../../../../../samples/snippets/csharp/VS_Snippets_CLR/throwunobservedtaskexceptions/cs/program.cs#1)]
 [!code-vb[ThrowUnobservedTaskExceptions#1](../../../../../samples/snippets/visualbasic/VS_Snippets_CLR/throwunobservedtaskexceptions/vb/program.vb#1)]  
  
## <a name="see-also"></a>関連項目
- [ランタイム設定スキーマ](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [構成ファイル スキーマ](../../../../../docs/framework/configure-apps/file-schema/index.md)
