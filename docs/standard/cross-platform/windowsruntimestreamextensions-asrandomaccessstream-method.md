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
ms.openlocfilehash: d5dd2829a9a00f869af3d7f370f99361979b8106
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2019
ms.locfileid: "55758795"
---
# <a name="windowsruntimestreamextensionsasrandomaccessstreamsystemiostream-method"></a><span data-ttu-id="b0266-102">WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) メソッド</span><span class="sxs-lookup"><span data-stu-id="b0266-102">WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) Method</span></span>

<span data-ttu-id="b0266-103">[.NET Framework 4.5.1 以降のバージョンでサポート]</span><span class="sxs-lookup"><span data-stu-id="b0266-103">[Supported in the .NET Framework 4.5.1 and later versions]</span></span>

<span data-ttu-id="b0266-104">特定のストリームをランダム アクセス ストリームに変換します。</span><span class="sxs-lookup"><span data-stu-id="b0266-104">Converts the specified stream to a random access stream.</span></span>

<span data-ttu-id="b0266-105">**名前空間:**<xref:System.IO?displayProperty=nameWithType>
**アセンブリ:** System.Runtime.WindowsRuntime (system.runtime.windowsruntime.dll 内)</span><span class="sxs-lookup"><span data-stu-id="b0266-105">**Namespace:** <xref:System.IO?displayProperty=nameWithType>
**Assembly:** System.Runtime.WindowsRuntime (in System.Runtime.WindowsRuntime.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b0266-106">構文</span><span class="sxs-lookup"><span data-stu-id="b0266-106">Syntax</span></span>

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

## <a name="parameters"></a><span data-ttu-id="b0266-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0266-107">Parameters</span></span>

`stream`

<span data-ttu-id="b0266-108">型: <xref:System.IO.Stream?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="b0266-108">Type: <xref:System.IO.Stream?displayProperty=nameWithType></span></span>  
<span data-ttu-id="b0266-109">変換するストリーム。</span><span class="sxs-lookup"><span data-stu-id="b0266-109">The stream to convert.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0266-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="b0266-110">Return Value</span></span>

<span data-ttu-id="b0266-111">型: <xref:Windows.Storage.Streams.RandomAccessStream></span><span class="sxs-lookup"><span data-stu-id="b0266-111">Type: <xref:Windows.Storage.Streams.RandomAccessStream></span></span>  
<span data-ttu-id="b0266-112">A[!INCLUDE[wrt](../../../includes/wrt-md.md)]ランダム アクセス ストリームは、変換されたストリームを表します。</span><span class="sxs-lookup"><span data-stu-id="b0266-112">A [!INCLUDE[wrt](../../../includes/wrt-md.md)] random access stream, which represents the converted stream.</span></span>

## <a name="exceptions"></a><span data-ttu-id="b0266-113">例外</span><span class="sxs-lookup"><span data-stu-id="b0266-113">Exceptions</span></span>

|<span data-ttu-id="b0266-114">例外</span><span class="sxs-lookup"><span data-stu-id="b0266-114">Exception</span></span>|<span data-ttu-id="b0266-115">状態</span><span class="sxs-lookup"><span data-stu-id="b0266-115">Condition</span></span>|
|---------------|---------------|
|<xref:System.NotSupportedException>|<span data-ttu-id="b0266-116">変換するストリームがシークをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="b0266-116">The stream to convert does not support seeking.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b0266-117">解説</span><span class="sxs-lookup"><span data-stu-id="b0266-117">Remarks</span></span>

<span data-ttu-id="b0266-118">この拡張メソッドは、Windows ストア アプリを開発する場合のみに使用できます。</span><span class="sxs-lookup"><span data-stu-id="b0266-118">This extension method is available only when you develop Windows Store apps.</span></span> <span data-ttu-id="b0266-119">このメソッドは、Windows ストア アプリのストリームを使用する便利な方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="b0266-119">This method provides a convenient way of working with streams in Windows Store apps.</span></span> <span data-ttu-id="b0266-120">変換する .NET Framework ストリームはシークをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0266-120">The .NET Framework stream you want to convert must support seeking.</span></span> <span data-ttu-id="b0266-121">詳細については、<xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType> メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0266-121">For more information, see the <xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType> method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0266-122">この API は .NET Framework 4.5.1 以上ではサポートされますが、Version 4.5 ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="b0266-122">This API is supported in the .NET Framework 4.5.1 and later versions, but not in version 4.5.</span></span>

## <a name="version-information"></a><span data-ttu-id="b0266-123">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="b0266-123">Version Information</span></span>

<span data-ttu-id="b0266-124">**Windows ストア アプリ用 .NET**</span><span class="sxs-lookup"><span data-stu-id="b0266-124">**.NET for Windows Store apps**</span></span>

<span data-ttu-id="b0266-125">サポートされています。Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b0266-125">Supported in: Windows 8.1</span></span>

## <a name="see-also"></a><span data-ttu-id="b0266-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0266-126">See also</span></span>

- [<span data-ttu-id="b0266-127">方法: .NET Framework ストリームと Windows ランタイム ストリームの間で変換を行う</span><span class="sxs-lookup"><span data-stu-id="b0266-127">How to: Convert Between .NET Framework Streams and Windows Runtime Streams</span></span>](../io/how-to-convert-between-dotnet-streams-and-winrt-streams.md)
