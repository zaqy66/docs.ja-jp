---
title: SqlStreamChars.Seek (Int64、SeekOrigin) メソッド (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Seek
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: d52a1cd4dd70c29fc1af3fcf50c4f9b0c90125df
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2019
ms.locfileid: "55827384"
---
# <a name="sqlstreamcharsseekint64-seekorigin-method"></a><span data-ttu-id="2da21-102">SqlStreamChars.Seek (Int64、SeekOrigin) メソッド</span><span class="sxs-lookup"><span data-stu-id="2da21-102">SqlStreamChars.Seek(Int64, SeekOrigin) Method</span></span>

<span data-ttu-id="2da21-103">派生クラスでオーバーライドされた場合は、現在のストリーム内の位置を設定します。</span><span class="sxs-lookup"><span data-stu-id="2da21-103">When overridden in a derived class, sets the position within the current stream.</span></span> <span data-ttu-id="2da21-104">このメソッドを含むアセンブリには、SQLAccess.dll で友人関係があります。</span><span class="sxs-lookup"><span data-stu-id="2da21-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="2da21-105">SQL Server で使用するものでは。</span><span class="sxs-lookup"><span data-stu-id="2da21-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="2da21-106">その他のデータベースには、そのデータベースによって提供されるホスティング メカニズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="2da21-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract long Seek (long offset, System.IO.SeekOrigin origin);
```

## <a name="parameters"></a><span data-ttu-id="2da21-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2da21-107">Parameters</span></span>

`offset`\
<span data-ttu-id="2da21-108">相対バイト オフセット`origin`します。</span><span class="sxs-lookup"><span data-stu-id="2da21-108">A byte offset relative to `origin`.</span></span>

`origin`\
<span data-ttu-id="2da21-109">新しい位置の取得元となる参照ポイントを示す列挙値の 1 つ。</span><span class="sxs-lookup"><span data-stu-id="2da21-109">One of the enumeration values that indicates the reference point from which to obtain the new position.</span></span>

## <a name="returns"></a><span data-ttu-id="2da21-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="2da21-110">Returns</span></span>

<xref:System.Int32>\
<span data-ttu-id="2da21-111">現在のストリーム内の新しい位置。</span><span class="sxs-lookup"><span data-stu-id="2da21-111">The new position within the current stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="2da21-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="2da21-112">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="2da21-113">`SqlStreamChars.Seek`メソッドはプライベートであり、コード内で直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="2da21-113">The `SqlStreamChars.Seek` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="2da21-114">Microsoft はいかなる運用アプリケーションでこのフィールドの使用をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="2da21-114">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="2da21-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="2da21-115">Requirements</span></span>

<span data-ttu-id="2da21-116">**名前空間:** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="2da21-116">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="2da21-117">**アセンブリ:** System.Data (system.data.dll 内)</span><span class="sxs-lookup"><span data-stu-id="2da21-117">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="2da21-118">**.NET framework のバージョン:** 2.0 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="2da21-118">**.NET Framework versions:** Available since 2.0.</span></span>