---
title: SqlStreamChars.SetLength(Int64) メソッド (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.SetLength
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 7eb2b1bfe0a3d180b54c41cbca1d645dfb402be7
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152765"
---
# <a name="sqlstreamcharssetlengthint64-method"></a><span data-ttu-id="3c37b-102">SqlStreamChars.SetLength(Int64) メソッド</span><span class="sxs-lookup"><span data-stu-id="3c37b-102">SqlStreamChars.SetLength(Int64) Method</span></span>

<span data-ttu-id="3c37b-103">派生クラスでオーバーライドされると、ストリームで使用されるリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="3c37b-103">When overridden in a derived class, releases the resources used by the stream.</span></span> <span data-ttu-id="3c37b-104">このメソッドを含むアセンブリには、SQLAccess.dll で友人関係があります。</span><span class="sxs-lookup"><span data-stu-id="3c37b-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="3c37b-105">SQL Server で使用するものでは。</span><span class="sxs-lookup"><span data-stu-id="3c37b-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="3c37b-106">その他のデータベースには、そのデータベースによって提供されるホスティング メカニズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="3c37b-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract void SetLength (long value);
```

## <a name="parameters"></a><span data-ttu-id="3c37b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3c37b-107">Parameters</span></span>

`value`\
<span data-ttu-id="3c37b-108">現在のストリームの希望の長さ (バイト数)。</span><span class="sxs-lookup"><span data-stu-id="3c37b-108">The desired length of the current stream in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c37b-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="3c37b-109">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="3c37b-110">`SqlStreamChars.SetLength`メソッドはプライベートであり、コード内で直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="3c37b-110">The `SqlStreamChars.SetLength` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="3c37b-111">Microsoft はいかなる運用アプリケーションでこのフィールドの使用をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="3c37b-111">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c37b-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="3c37b-112">Requirements</span></span>

<span data-ttu-id="3c37b-113">**名前空間:** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="3c37b-113">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="3c37b-114">**アセンブリ:** System.Data (system.data.dll 内)</span><span class="sxs-lookup"><span data-stu-id="3c37b-114">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="3c37b-115">**.NET framework のバージョン:** 2.0 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="3c37b-115">**.NET Framework versions:** Available since 2.0.</span></span>