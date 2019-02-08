---
title: SqlChars.Stream プロパティ (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/19/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlChars.Stream
- System.Data.SqlTypes.SqlChars.get_Stream
- System.Data.SqlTypes.SqlChars.set_Stream
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 36a6b3f45f0832ed651dc0a613f50e7170517497
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2019
ms.locfileid: "55827683"
---
# <a name="sqlcharsstream-property"></a>SqlChars.Stream プロパティ

取得または文字のストリームを設定します。 このプロパティが含まれるアセンブリには、SQLAccess.dll で友人関係があります。 SQL Server で使用するものでは。 その他のデータベースには、そのデータベースによって提供されるホスティング メカニズムを使用します。

```csharp
internal SqlStreamChars Stream { get; set; }
```

## <a name="property-value"></a>プロパティの値

`System.Data.SqlTypes.SqlStreamChars`\
文字のストリーム。

## <a name="remarks"></a>Remarks

> [!WARNING]
> `SqlChars.Stream`プロパティは内部であり、コード内で直接使用するものではありません。
>
> Microsoft はいかなる運用アプリケーションでこのプロパティの使用をサポートしていません。

## <a name="requirements"></a>必要条件

**名前空間:** <xref:System.Data.SqlTypes>

**アセンブリ:** System.Data (system.data.dll 内)

**.NET framework のバージョン:** 2.0 以降で使用可能です。