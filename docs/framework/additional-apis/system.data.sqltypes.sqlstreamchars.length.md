---
title: SqlStreamChars.Length プロパティ (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/19/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Length
- System.Data.SqlTypes.SqlStreamChars.get_Length
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: ac6e6af9c9411ebc25039e0992133fae2b35ee23
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/11/2019
ms.locfileid: "54221182"
---
# <a name="sqlstreamcharslength-property"></a><span data-ttu-id="42005-102">SqlStreamChars.Length プロパティ</span><span class="sxs-lookup"><span data-stu-id="42005-102">SqlStreamChars.Length Property</span></span>

<span data-ttu-id="42005-103">派生クラスでオーバーライドされると、現在のストリームの長さを取得します。</span><span class="sxs-lookup"><span data-stu-id="42005-103">When overridden in a derived class, gets the length of the current stream.</span></span> <span data-ttu-id="42005-104">このプロパティが含まれるアセンブリには、SQLAccess.dll で友人関係があります。</span><span class="sxs-lookup"><span data-stu-id="42005-104">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="42005-105">SQL Server で使用するものでは。</span><span class="sxs-lookup"><span data-stu-id="42005-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="42005-106">その他のデータベースには、そのデータベースによって提供されるホスティング メカニズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="42005-106">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="42005-107">構文</span><span class="sxs-lookup"><span data-stu-id="42005-107">Syntax</span></span>

```csharp
public abstract long Length { get; }
```

## <a name="property-value"></a><span data-ttu-id="42005-108">プロパティの値</span><span class="sxs-lookup"><span data-stu-id="42005-108">Property value</span></span>

<xref:System.Int64>\
<span data-ttu-id="42005-109">ストリーム長。</span><span class="sxs-lookup"><span data-stu-id="42005-109">The length of the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="42005-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="42005-110">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="42005-111">`SqlStreamChars.Length`プロパティはプライベートであり、コード内で直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="42005-111">The `SqlStreamChars.Length` property is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="42005-112">Microsoft はいかなる運用アプリケーションでこのフィールドの使用をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="42005-112">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="42005-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="42005-113">Requirements</span></span>

<span data-ttu-id="42005-114">**名前空間:** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="42005-114">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="42005-115">**アセンブリ:** System.Data (system.data.dll 内)</span><span class="sxs-lookup"><span data-stu-id="42005-115">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="42005-116">**.NET framework のバージョン:** 2.0 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="42005-116">**.NET Framework versions:** Available since 2.0.</span></span>