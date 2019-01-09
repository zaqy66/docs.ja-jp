---
title: SqlStreamChars.Dispose(Boolean) メソッド (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.Dispose
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 3f2180d9a1893e651f174fff6d0f073df651e712
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152565"
---
# <a name="sqlstreamcharsdisposeboolean-method"></a><span data-ttu-id="6260f-102">SqlStreamChars.Dispose(Boolean) メソッド</span><span class="sxs-lookup"><span data-stu-id="6260f-102">SqlStreamChars.Dispose(Boolean) Method</span></span>

<span data-ttu-id="6260f-103">派生クラスでオーバーライドされると、ストリームで使用されるリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="6260f-103">When overridden in a derived class, releases the resources used by the stream.</span></span> <span data-ttu-id="6260f-104">このメソッドを含むアセンブリには、SQLAccess.dll で友人関係があります。</span><span class="sxs-lookup"><span data-stu-id="6260f-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="6260f-105">SQL Server で使用するものでは。</span><span class="sxs-lookup"><span data-stu-id="6260f-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="6260f-106">その他のデータベースには、そのデータベースによって提供されるホスティング メカニズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="6260f-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
protected virtual void Dispose (bool disposing);
```

## <a name="parameters"></a><span data-ttu-id="6260f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6260f-107">Parameters</span></span>

`disposing`\
<span data-ttu-id="6260f-108">マネージ リソースとアンマネージ リソースの両方を解放する場合は `true`。アンマネージ リソースだけを解放する場合は `false`。</span><span class="sxs-lookup"><span data-stu-id="6260f-108">`true` to release both managed and unmanaged resources; `false` to release only unmanaged resources.</span></span>

## <a name="remarks"></a><span data-ttu-id="6260f-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="6260f-109">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="6260f-110">`SqlStreamChars.Dispose`メソッドはプライベートであり、コード内で直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="6260f-110">The `SqlStreamChars.Dispose` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="6260f-111">Microsoft はいかなる運用アプリケーションでこのフィールドの使用をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="6260f-111">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="6260f-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="6260f-112">Requirements</span></span>

<span data-ttu-id="6260f-113">**名前空間:** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="6260f-113">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="6260f-114">**アセンブリ:** System.Data (system.data.dll 内)</span><span class="sxs-lookup"><span data-stu-id="6260f-114">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="6260f-115">**.NET framework のバージョン:** 2.0 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="6260f-115">**.NET Framework versions:** Available since 2.0.</span></span>