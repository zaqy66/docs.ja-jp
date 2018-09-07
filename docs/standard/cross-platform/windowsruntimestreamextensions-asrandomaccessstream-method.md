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
ms.openlocfilehash: 8935a8c282bbe812ad76ac6d4228c38ab12626a4
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44059652"
---
# <a name="windowsruntimestreamextensionsasrandomaccessstreamsystemiostream-method"></a><span data-ttu-id="0e7a4-102">WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) メソッド</span><span class="sxs-lookup"><span data-stu-id="0e7a4-102">WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) Method</span></span>

<span data-ttu-id="0e7a4-103">[.NET Framework 4.5.1 以降のバージョンでサポート]</span><span class="sxs-lookup"><span data-stu-id="0e7a4-103">[Supported in the .NET Framework 4.5.1 and later versions]</span></span>

<span data-ttu-id="0e7a4-104">特定のストリームをランダム アクセス ストリームに変換します。</span><span class="sxs-lookup"><span data-stu-id="0e7a4-104">Converts the specified stream to a random access stream.</span></span>

<span data-ttu-id="0e7a4-105">**Namespace:** <xref:System.IO?displayProperty=nameWithType> 
**アセンブリ:** System.Runtime.WindowsRuntime (system.runtime.windowsruntime.dll 内)</span><span class="sxs-lookup"><span data-stu-id="0e7a4-105">**Namespace:** <xref:System.IO?displayProperty=nameWithType>
**Assembly:** System.Runtime.WindowsRuntime (in System.Runtime.WindowsRuntime.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0e7a4-106">構文</span><span class="sxs-lookup"><span data-stu-id="0e7a4-106">Syntax</span></span>

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

## <a name="parameters"></a><span data-ttu-id="0e7a4-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e7a4-107">Parameters</span></span>

`stream`

<span data-ttu-id="0e7a4-108">型: <xref:System.IO.Stream?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="0e7a4-108">Type: <xref:System.IO.Stream?displayProperty=nameWithType></span></span>  
<span data-ttu-id="0e7a4-109">変換するストリーム。</span><span class="sxs-lookup"><span data-stu-id="0e7a4-109">The stream to convert.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e7a4-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e7a4-110">Return Value</span></span>

<span data-ttu-id="0e7a4-111">型: <xref:Windows.Storage.Streams.RandomAccessStream></span><span class="sxs-lookup"><span data-stu-id="0e7a4-111">Type: <xref:Windows.Storage.Streams.RandomAccessStream></span></span>  
<span data-ttu-id="0e7a4-112">A[!INCLUDE[wrt](../../../includes/wrt-md.md)]ランダム アクセス ストリームは、変換されたストリームを表します。</span><span class="sxs-lookup"><span data-stu-id="0e7a4-112">A [!INCLUDE[wrt](../../../includes/wrt-md.md)] random access stream, which represents the converted stream.</span></span>

## <a name="exceptions"></a><span data-ttu-id="0e7a4-113">例外</span><span class="sxs-lookup"><span data-stu-id="0e7a4-113">Exceptions</span></span>

|<span data-ttu-id="0e7a4-114">例外</span><span class="sxs-lookup"><span data-stu-id="0e7a4-114">Exception</span></span>|<span data-ttu-id="0e7a4-115">状態</span><span class="sxs-lookup"><span data-stu-id="0e7a4-115">Condition</span></span>|
|---------------|---------------|
|<xref:System.NotSupportedException>|<span data-ttu-id="0e7a4-116">変換するストリームがシークをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="0e7a4-116">The stream to convert does not support seeking.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0e7a4-117">解説</span><span class="sxs-lookup"><span data-stu-id="0e7a4-117">Remarks</span></span>

<span data-ttu-id="0e7a4-118">この拡張メソッドは、Windows ストア アプリを開発する場合のみに使用できます。</span><span class="sxs-lookup"><span data-stu-id="0e7a4-118">This extension method is available only when you develop Windows Store apps.</span></span> <span data-ttu-id="0e7a4-119">このメソッドは、Windows ストア アプリのストリームを使用する便利な方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="0e7a4-119">This method provides a convenient way of working with streams in Windows Store apps.</span></span> <span data-ttu-id="0e7a4-120">変換する .NET Framework ストリームはシークをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e7a4-120">The .NET Framework stream you want to convert must support seeking.</span></span> <span data-ttu-id="0e7a4-121">詳細については、<xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType> メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e7a4-121">For more information, see the <xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType> method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e7a4-122">この API は .NET Framework 4.5.1 以上ではサポートされますが、Version 4.5 ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="0e7a4-122">This API is supported in the .NET Framework 4.5.1 and later versions, but not in version 4.5.</span></span>

## <a name="version-information"></a><span data-ttu-id="0e7a4-123">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="0e7a4-123">Version Information</span></span>

<span data-ttu-id="0e7a4-124">**Windows ストア アプリ用 .NET**</span><span class="sxs-lookup"><span data-stu-id="0e7a4-124">**.NET for Windows Store apps**</span></span>

<span data-ttu-id="0e7a4-125">Windows 8.1 でサポート</span><span class="sxs-lookup"><span data-stu-id="0e7a4-125">Supported in: Windows 8.1</span></span>

## <a name="see-also"></a><span data-ttu-id="0e7a4-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="0e7a4-126">See also</span></span>

<span data-ttu-id="0e7a4-127">-[System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions(v=vs.110).aspx)
-[方法: .NET Framework ストリームと Windows ランタイム ストリーム間の変換](../io/how-to-convert-between-dotnet-streams-and-winrt-streams.md)</span><span class="sxs-lookup"><span data-stu-id="0e7a4-127">-[System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions(v=vs.110).aspx)
-[How to: Convert Between .NET Framework Streams and Windows Runtime Streams](../io/how-to-convert-between-dotnet-streams-and-winrt-streams.md)</span></span>
