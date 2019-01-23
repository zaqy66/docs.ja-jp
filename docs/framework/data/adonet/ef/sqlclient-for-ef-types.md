---
title: Entity Framework 用 SqlClient の型
ms.date: 03/30/2017
ms.assetid: f2a95ead-c845-4e97-9fb3-04b444f7ed81
ms.openlocfilehash: b121020c8779cfb3959425b1019eaf085b97d6cf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505187"
---
# <a name="sqlclient-for-entity-frameworktypes"></a>Entity Framework 用 SqlClient の型
.NET Framework Data Provider for SQL Server (SqlClient) プロバイダー マニフェスト ファイルには、プロバイダー プリミティブ型のリスト、それぞれの型のファセット、概念モデルとストレージ モデルのプリミティブ型とのマッピング、および概念モデルとストレージ モデルのプリミティブ型間での昇格と変換の規則が含まれています。  
  
 次の表は、SQL Server 2008 では、型を示します[!INCLUDE[ssVersion2005](../../../../../includes/ssversion2005-md.md)]、および[!INCLUDE[ssVersion2000](../../../../../includes/ssversion2000-md.md)]データベースとどのようにこれらの型マップに概念モデル型。 いくつかの新しい型が SQL Server の新しいバージョンで導入されており、これらの型は SQL Server の古いバージョンではサポートされていません。 これらの型については次の表で説明します。  
  
|プロバイダー型の<br /><br /> name|プロバイダー型の<br /><br /> 属性|`EDMSimpleType`<br /><br /> name|ファセット|  
|----------------------------|----------------------------------|------------------------------|------------|  
|`bit`|適用なし|`Edm.Boolean`|該当なし|  
|`tinyint`|該当なし|`Edm.Byte`|該当なし|  
|`smallint`|該当なし|`Edm.Int16`|該当なし|  
|`int`|該当なし|`Edm.Int32`|該当なし|  
|`bigint`|該当なし|`Edm.Int64`|該当なし|  
|`float`|該当なし|`Edm.Double`|該当なし|  
|`real`|該当なし|`Edm.Double`|該当なし|  
|`decimal`|N/A|`Edm.Decimal`|有効桁数。<br /><br /> 最小値:1<br /><br /> 最大値:38<br /><br /> -既定値:18<br /><br /> -定数。False<br /><br /> スケール:<br /><br /> 最小値:0<br /><br /> 最大値:38<br /><br /> -既定値:0<br /><br /> -定数。False|  
|`numeric`|N/A|`Edm.Decimal`|有効桁数。<br /><br /> 最小値:1<br /><br /> 最大値:38<br /><br /> -既定値:18<br /><br /> -定数。False<br /><br /> スケール:<br /><br /> 最小値:0<br /><br /> 最大値:38<br /><br /> -既定値:0<br /><br /> -定数。False|  
|`smallmoney`|N/A|`Edm.Decimal`|有効桁数。<br /><br /> -既定値:10<br /><br /> -定数。True<br /><br /> スケール:<br /><br /> -既定値:4<br /><br /> -定数。True|  
|`money`|N/A|`Edm.Decimal`|有効桁数。<br /><br /> -既定値:19<br /><br /> -定数。True<br /><br /> スケール:<br /><br /> -既定値:4<br /><br /> -定数。True|  
|`binary`|N/A|`Edm.Binary`|MaxLength:<br /><br /> 最小値:1<br /><br /> 最大値:8000<br /><br /> -既定値:8000<br /><br /> -定数。False<br /><br /> FixedLength:<br /><br /> -既定値:True<br /><br /> -定数。True|  
|`varbinary`|N/A|`Edm.Binary`|MaxLength:<br /><br /> 最小値:1<br /><br /> 最大値:8000<br /><br /> -既定値:8000<br /><br /> -定数。False<br /><br /> FixedLength:<br /><br /> -既定値:False<br /><br /> -定数。True|  
|`varbinary(max)`<br /><br /> メモ:この型がでサポートされていません[!INCLUDE[ssVersion2000](../../../../../includes/ssversion2000-md.md)]します。|N/A|`Edm.Binary`|MaxLength:<br /><br /> -既定値:214748364780<br /><br /> -定数。True<br /><br /> FixedLength:<br /><br /> -既定値:False<br /><br /> -定数。True|  
|`image`|N/A|`Edm.Binary`|MaxLength:<br /><br /> -既定値:2147483647<br /><br /> -定数。True<br /><br /> FixedLength:<br /><br /> -既定値:False<br /><br /> -定数。True|  
|`timestamp`|N/A|`Edm.Binary`|MaxLength:<br /><br /> -既定値:8<br /><br /> -定数。True<br /><br /> FixedLength:<br /><br /> -既定値:True<br /><br /> -定数。True|  
|`rowversion`|N/A|`Edm.Binary`|MaxLength:<br /><br /> -既定値:8<br /><br /> -定数。True<br /><br /> FixedLength:<br /><br /> -既定値:True<br /><br /> -定数。True|  
|`smalldatetime`|N/A|`Edm.DateTime`|有効桁数。<br /><br /> -既定値:0<br /><br /> -定数。True|  
|`datetime`|N/A|`Edm.DateTime`|有効桁数。<br /><br /> -既定値:3<br /><br /> -定数。True|  
|`date`<br /><br /> メモ:SQL Server 2005 および SQL Server 2000 では、この型はサポートされていません。|N/A|`Edm.DateTime`|有効桁数。<br /><br /> -既定値:0<br /><br /> -定数。False|  
|`time`<br /><br /> メモ:SQL Server 2005 および SQL Server 2000 では、この型はサポートされていません。|N/A|`Edm.Time`|有効桁数。<br /><br /> -既定値:7<br /><br /> -定数。False|  
|`datetime2`<br /><br /> メモ:SQL Server 2005 および SQL Server 2000 では、この型はサポートされていません。|N/A|`Edm.DateTime`|有効桁数。<br /><br /> -既定値:7<br /><br /> -定数。False|  
|`datetimeoffset`<br /><br /> メモ:SQL Server 2005 および SQL Server 2000 では、この型はサポートされていません。|N/A|`Edm.DateTimeOffset`|有効桁数。<br /><br /> -既定値:7<br /><br /> -定数。False|  
|`nvarchar`<br /><br /> メモ:この型がでサポートされていません[!INCLUDE[ssVersion2000](../../../../../includes/ssversion2000-md.md)]します。|N/A|`Edm.String`|MaxLength:<br /><br /> 最小値:1<br /><br /> 最大値:4000<br /><br /> -既定値:4000<br /><br /> -定数。False<br /><br /> Unicode:<br /><br /> -既定値:True<br /><br /> -定数。True<br /><br /> FixedLength:<br /><br /> -既定値:False<br /><br /> -定数。True|  
|`varchar`<br /><br /> メモ:この型がでサポートされていません[!INCLUDE[ssVersion2000](../../../../../includes/ssversion2000-md.md)]します。|N/A|`Edm.String`|MaxLength:<br /><br /> 最小値:1<br /><br /> 最大値:8000<br /><br /> -既定値:8000<br /><br /> -定数。False<br /><br /> Unicode:<br /><br /> -既定値:False<br /><br /> -定数。True<br /><br /> FixedLength:<br /><br /> -既定値:False<br /><br /> -定数。True|  
|`char`|N/A|`Edm.String`|MaxLength:<br /><br /> 最小値:1<br /><br /> 最大値:8000<br /><br /> -既定値:8000<br /><br /> -定数。False<br /><br /> Unicode:<br /><br /> -既定値:False<br /><br /> -定数。True<br /><br /> FixedLength:<br /><br /> -既定値:True<br /><br /> -定数。True|  
|`nchar`|N/A|`Edm.String`|MaxLength:<br /><br /> 最小値:1<br /><br /> 最大値:4000<br /><br /> -既定値:4000<br /><br /> -定数。False<br /><br /> Unicode:<br /><br /> -既定値:True<br /><br /> -定数。True<br /><br /> FixedLength:<br /><br /> -既定値:True<br /><br /> -定数。True|  
|`varchar`(`max`)|N/A|`Edm.String`|MaxLength:<br /><br /> -既定値:2147483647<br /><br /> -定数。True<br /><br /> Unicode:<br /><br /> -既定値:False<br /><br /> -定数。True<br /><br /> FixedLength:<br /><br /> -既定値:False<br /><br /> -定数。True|  
|`nvarchar`(`max`)|N/A|`Edm.String`|MaxLength:<br /><br /> -既定値:1073741823<br /><br /> -定数。True<br /><br /> Unicode:<br /><br /> -既定値:True<br /><br /> -定数。True<br /><br /> FixedLength:<br /><br /> -既定値:False<br /><br /> -定数。True|  
|`ntext`|等号比較:False<br /><br /> 順序を比較できる:False|`Edm.String`|MaxLength:<br /><br /> -既定値:1073741823<br /><br /> -定数。True<br /><br /> Unicode:<br /><br /> -既定値:False<br /><br /> -定数。True<br /><br /> FixedLength:<br /><br /> -既定値:False<br /><br /> -定数。True|  
|`text`|等号比較:False<br /><br /> 順序を比較できる:False|`Edm.String`|MaxLength:<br /><br /> -既定値:2147483647<br /><br /> -定数。True<br /><br /> Unicode:<br /><br /> -既定値:False<br /><br /> -定数。True<br /><br /> FixedLength:<br /><br /> -既定値:False<br /><br /> -定数。True|  
|`Unique`<br /><br /> `identifier`|等号比較:True<br /><br /> 順序を比較できる:True|`Edm.Guid`|N/A|  
|`xml`|等号比較:False<br /><br /> 順序を比較できる:False|`Edm.String`|MaxLength:<br /><br /> -既定値:1073741823<br /><br /> -定数。True<br /><br /> Unicode:<br /><br /> -既定値:True<br /><br /> -定数。True<br /><br /> FixedLength:<br /><br /> -既定値:False<br /><br /> -定数。True|  
  
## <a name="see-also"></a>関連項目
- [CSDL、SSDL、および MSL 仕様](../../../../../docs/framework/data/adonet/ef/language-reference/csdl-ssdl-and-msl-specifications.md)
