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
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43800087"
---
# <a name="windowsruntimestreamextensionsasrandomaccessstreamsystemiostream-method"></a><span data-ttu-id="4e136-102">WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) メソッド</span><span class="sxs-lookup"><span data-stu-id="4e136-102">WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) Method</span></span>

<span data-ttu-id="4e136-103">[.NET Framework 4.5.1 以降のバージョンでサポート]</span><span class="sxs-lookup"><span data-stu-id="4e136-103">[Supported in the .NET Framework 4.5.1 and later versions]</span></span>

<span data-ttu-id="4e136-104">特定のストリームをランダム アクセス ストリームに変換します。</span><span class="sxs-lookup"><span data-stu-id="4e136-104">Converts the specified stream to a random access stream.</span></span>

<span data-ttu-id="4e136-105">**Namespace:** <xref:System.IO?displayProperty=nameWithType> 
**アセンブリ:** System.Runtime.WindowsRuntime (system.runtime.windowsruntime.dll 内)</span><span class="sxs-lookup"><span data-stu-id="4e136-105">**Namespace:** <xref:System.IO?displayProperty=nameWithType>
**Assembly:** System.Runtime.WindowsRuntime (in System.Runtime.WindowsRuntime.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4e136-106">構文</span><span class="sxs-lookup"><span data-stu-id="4e136-106">Syntax</span></span>

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

## <a name="parameters"></a><span data-ttu-id="4e136-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4e136-107">Parameters</span></span>

`stream`

<span data-ttu-id="4e136-108">型: <xref:System.IO.Stream?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="4e136-108">Type: <xref:System.IO.Stream?displayProperty=nameWithType></span></span>  
<span data-ttu-id="4e136-109">変換するストリーム。</span><span class="sxs-lookup"><span data-stu-id="4e136-109">The stream to convert.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e136-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="4e136-110">Return Value</span></span>

<span data-ttu-id="4e136-111">型: <xref:Windows.Storage.Streams.RandomAccessStream></span><span class="sxs-lookup"><span data-stu-id="4e136-111">Type: <xref:Windows.Storage.Streams.RandomAccessStream></span></span>  
<span data-ttu-id="4e136-112">A[!INCLUDE[wrt](../../../includes/wrt-md.md)]ランダム アクセス ストリームは、変換されたストリームを表します。</span><span class="sxs-lookup"><span data-stu-id="4e136-112">A [!INCLUDE[wrt](../../../includes/wrt-md.md)] random access stream, which represents the converted stream.</span></span>

## <a name="exceptions"></a><span data-ttu-id="4e136-113">例外</span><span class="sxs-lookup"><span data-stu-id="4e136-113">Exceptions</span></span>

|<span data-ttu-id="4e136-114">例外</span><span class="sxs-lookup"><span data-stu-id="4e136-114">Exception</span></span>|<span data-ttu-id="4e136-115">状態</span><span class="sxs-lookup"><span data-stu-id="4e136-115">Condition</span></span>|
|---------------|---------------|
|<xref:System.NotSupportedException>|<span data-ttu-id="4e136-116">変換するストリームがシークをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="4e136-116">The stream to convert does not support seeking.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4e136-117">解説</span><span class="sxs-lookup"><span data-stu-id="4e136-117">Remarks</span></span>

<span data-ttu-id="4e136-118">この拡張メソッドは、Windows ストア アプリを開発する場合のみに使用できます。</span><span class="sxs-lookup"><span data-stu-id="4e136-118">This extension method is available only when you develop Windows Store apps.</span></span> <span data-ttu-id="4e136-119">このメソッドは、Windows ストア アプリのストリームを使用する便利な方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="4e136-119">This method provides a convenient way of working with streams in Windows Store apps.</span></span> <span data-ttu-id="4e136-120">変換する .NET Framework ストリームはシークをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e136-120">The .NET Framework stream you want to convert must support seeking.</span></span> <span data-ttu-id="4e136-121">詳細については、<xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType> メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4e136-121">For more information, see the <xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType> method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e136-122">この API は .NET Framework 4.5.1 以上ではサポートされますが、Version 4.5 ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4e136-122">This API is supported in the .NET Framework 4.5.1 and later versions, but not in version 4.5.</span></span>

## <a name="version-information"></a><span data-ttu-id="4e136-123">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="4e136-123">Version Information</span></span>

<span data-ttu-id="4e136-124">**Windows ストア アプリ用 .NET**</span><span class="sxs-lookup"><span data-stu-id="4e136-124">**.NET for Windows Store apps**</span></span>

<span data-ttu-id="4e136-125">Windows 8.1 でサポート</span><span class="sxs-lookup"><span data-stu-id="4e136-125">Supported in: Windows 8.1</span></span>

## <a name="see-also"></a><span data-ttu-id="4e136-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="4e136-126">See Also</span></span>

<span data-ttu-id="4e136-127">[System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions(v=vs.110).aspx)</span><span class="sxs-lookup"><span data-stu-id="4e136-127">[System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions(v=vs.110).aspx)</span></span>  
[<span data-ttu-id="4e136-128">方法: .NET Framework ストリームと Windows ランタイム ストリームの間で変換を行う</span><span class="sxs-lookup"><span data-stu-id="4e136-128">How to: Convert Between .NET Framework Streams and Windows Runtime Streams</span></span>](../io/how-to-convert-between-dotnet-streams-and-winrt-streams.md)  