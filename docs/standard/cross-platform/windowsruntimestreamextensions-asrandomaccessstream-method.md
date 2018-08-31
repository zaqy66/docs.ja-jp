---
title: WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) メソッド
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
api_name:
- System.IO.WindowsRuntimeStreamExtensions.AsRandomAccessStream
api_location:
- System.Runtime.WindowsRuntime.dll
ms.assetid: dcc72283-caed-49ee-b45d-ccaf94e97129
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a712414163446606cbc93154bc821d3b1166fe8f
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/30/2018
ms.locfileid: "43254258"
---
# <a name="windowsruntimestreamextensionsasrandomaccessstreamsystemiostream-method"></a>WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) メソッド

[.NET Framework 4.5.1 以降のバージョンでサポート]

特定のストリームをランダム アクセス ストリームに変換します。

**Namespace:** <xref:System.IO?displayProperty=nameWithType> 
**アセンブリ:** System.Runtime.WindowsRuntime (system.runtime.windowsruntime.dll 内)

## <a name="syntax"></a>構文

```csharp
[CLSCompliantAttribute(false)]
public static IRandomAccessStream AsRandomAccessStream(Stream stream)
```

```vb
'Declaration
<ExtensionAttribute> _
<CLSCompliantAttribute(False)> _
Public Shared Function AsRandomAccessStream ( _
        stream As Stream) As IRandomAccessStream
```

## <a name="parameters"></a>パラメーター

`stream`

型: <xref:System.IO.Stream?displayProperty=nameWithType>  
変換するストリーム。

## <a name="return-value"></a>戻り値

型: <xref:Windows.Storage.Streams.RandomAccessStream>  
A[!INCLUDE[wrt](../../../includes/wrt-md.md)]ランダム アクセス ストリームは、変換されたストリームを表します。

## <a name="exceptions"></a>例外

|例外|状態|
|---------------|---------------|
|<xref:System.NotSupportedException>|変換するストリームがシークをサポートしていません。|

## <a name="remarks"></a>解説

この拡張メソッドは、Windows ストア アプリを開発する場合のみに使用できます。 このメソッドは、Windows ストア アプリのストリームを使用する便利な方法を提供します。 変換する .NET Framework ストリームはシークをサポートする必要があります。 詳細については、<xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType> メソッドを参照してください。

> [!IMPORTANT]
> この API は .NET Framework 4.5.1 以上ではサポートされますが、Version 4.5 ではサポートされません。

## <a name="version-information"></a>バージョン情報

**Windows ストア アプリ用 .NET**

Windows 8.1 でサポート

## <a name="see-also"></a>関連項目

[System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions(v=vs.110).aspx)  
[方法: .NET Framework ストリームと Windows ランタイム ストリームの間で変換を行う](../io/how-to-convert-between-dotnet-streams-and-winrt-streams.md)  