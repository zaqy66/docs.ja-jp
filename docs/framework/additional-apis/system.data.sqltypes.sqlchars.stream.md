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
# <a name="sqlcharsstream-property"></a><span data-ttu-id="0d00a-102">SqlChars.Stream プロパティ</span><span class="sxs-lookup"><span data-stu-id="0d00a-102">SqlChars.Stream Property</span></span>

<span data-ttu-id="0d00a-103">取得または文字のストリームを設定します。</span><span class="sxs-lookup"><span data-stu-id="0d00a-103">Gets or sets the character stream.</span></span> <span data-ttu-id="0d00a-104">このプロパティが含まれるアセンブリには、SQLAccess.dll で友人関係があります。</span><span class="sxs-lookup"><span data-stu-id="0d00a-104">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="0d00a-105">SQL Server で使用するものでは。</span><span class="sxs-lookup"><span data-stu-id="0d00a-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="0d00a-106">その他のデータベースには、そのデータベースによって提供されるホスティング メカニズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="0d00a-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
internal SqlStreamChars Stream { get; set; }
```

## <a name="property-value"></a><span data-ttu-id="0d00a-107">プロパティの値</span><span class="sxs-lookup"><span data-stu-id="0d00a-107">Property value</span></span>

`System.Data.SqlTypes.SqlStreamChars`\
<span data-ttu-id="0d00a-108">文字のストリーム。</span><span class="sxs-lookup"><span data-stu-id="0d00a-108">The character stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d00a-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="0d00a-109">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="0d00a-110">`SqlChars.Stream`プロパティは内部であり、コード内で直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="0d00a-110">The `SqlChars.Stream` property is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="0d00a-111">Microsoft はいかなる運用アプリケーションでこのプロパティの使用をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="0d00a-111">Microsoft does not support the use of this property in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d00a-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="0d00a-112">Requirements</span></span>

<span data-ttu-id="0d00a-113">**名前空間:** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="0d00a-113">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="0d00a-114">**アセンブリ:** System.Data (system.data.dll 内)</span><span class="sxs-lookup"><span data-stu-id="0d00a-114">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="0d00a-115">**.NET framework のバージョン:** 2.0 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="0d00a-115">**.NET Framework versions:** Available since 2.0.</span></span>