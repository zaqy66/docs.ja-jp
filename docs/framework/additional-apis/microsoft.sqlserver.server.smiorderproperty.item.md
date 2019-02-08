---
title: SmiOrderProperty.Item プロパティ (Microsoft.SqlServer.Server)
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- Microsoft.SqlServer.Server.SmiOrderProperty.Item
- Microsoft.SqlServer.Server.SmiOrderProperty.get_Item
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: cb2f6cb956f9571f9bd2ba7f86d79c5df6e72a15
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2019
ms.locfileid: "55827735"
---
# <a name="smiorderpropertyitem-property"></a>SmiOrderProperty.Item プロパティ

エンティティの列の順序を取得します。 このプロパティが含まれるアセンブリには、SQLAccess.dll で友人関係があります。 SQL Server で使用するものでは。 その他のデータベースには、そのデータベースによって提供されるホスティング メカニズムを使用します。

## <a name="syntax"></a>構文

```csharp
internal SmiColumnOrder Item { get; }
```

## <a name="property-value"></a>プロパティの値

列の順序。

## <a name="remarks"></a>Remarks

> [!WARNING]
> `SmiOrderProperty.Item`プロパティは内部であり、コード内で直接使用するものではありません。
>
> Microsoft はいかなる運用アプリケーションでこのプロパティの使用をサポートしていません。

## <a name="requirements"></a>必要条件

**名前空間:** <xref:Microsoft.SqlServer.Server>

**アセンブリ:** System.Data (system.data.dll 内)

**.NET framework のバージョン:** 2.0 以降で使用可能です。