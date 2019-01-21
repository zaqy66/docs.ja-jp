---
title: SqlStreamChars.CanSeek プロパティ (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/19/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.CanSeek
- System.Data.SqlTypes.SqlStreamChars.get_CanSeek
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 8d7bd7fb90177932b413c379f618a6d36374de57
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/11/2019
ms.locfileid: "54223144"
---
# <a name="sqlstreamcharscanseek-property"></a>SqlStreamChars.CanSeek プロパティ

派生クラスでオーバーライドされると、現在のストリームがシーク操作をサポートしているかどうかを示す値を取得します。 このプロパティが含まれるアセンブリには、SQLAccess.dll で友人関係があります。 SQL Server で使用するものでは。 その他のデータベースには、そのデータベースによって提供されるホスティング メカニズムを使用します。

```csharp
public abstract bool CanSeek { get; }
```

## <a name="property-value"></a>プロパティの値

<xref:System.Boolean>\
`true` 現在のストリームがシーク操作をサポートしている場合それ以外の場合、`false`します。

## <a name="remarks"></a>Remarks

> [!WARNING]
> `SqlStreamChars.CanSeek`プロパティはプライベートであり、コード内で直接使用するものではありません。
>
> Microsoft はいかなる運用アプリケーションでこのフィールドの使用をサポートしていません。

## <a name="requirements"></a>必要条件

**名前空間:** <xref:System.Data.SqlTypes>

**アセンブリ:** System.Data (system.data.dll 内)

**.NET framework のバージョン:** 2.0 以降で使用可能です。