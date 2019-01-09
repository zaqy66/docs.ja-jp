---
title: SqlStreamChars.IsNull プロパティ (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/19/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.IsNull
- System.Data.SqlTypes.SqlStreamChars.get_IsNull
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 79ebb9ec54185a94cb95dfd0fb2929e61cf513ef
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152625"
---
# <a name="sqlstreamcharsisnull-property"></a><span data-ttu-id="69d29-102">SqlStreamChars.IsNull プロパティ</span><span class="sxs-lookup"><span data-stu-id="69d29-102">SqlStreamChars.IsNull Property</span></span>

<span data-ttu-id="69d29-103">派生クラスでオーバーライドされると、ストリームがあるかどうかを示す値を取得します。`null`します。</span><span class="sxs-lookup"><span data-stu-id="69d29-103">When overridden in a derived class, gets a value that indicates whether the stream is `null`.</span></span> <span data-ttu-id="69d29-104">このプロパティが含まれるアセンブリには、SQLAccess.dll で友人関係があります。</span><span class="sxs-lookup"><span data-stu-id="69d29-104">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="69d29-105">SQL Server で使用するものでは。</span><span class="sxs-lookup"><span data-stu-id="69d29-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="69d29-106">その他のデータベースには、そのデータベースによって提供されるホスティング メカニズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="69d29-106">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="69d29-107">構文</span><span class="sxs-lookup"><span data-stu-id="69d29-107">Syntax</span></span>

```csharp
public abstract bool IsNull { get; }
```

## <a name="property-value"></a><span data-ttu-id="69d29-108">プロパティの値</span><span class="sxs-lookup"><span data-stu-id="69d29-108">Property value</span></span>

<xref:System.Boolean>\
<span data-ttu-id="69d29-109">`true` ストリームの場合`null`、それ以外の`false`します。</span><span class="sxs-lookup"><span data-stu-id="69d29-109">`true` if the stream is `null`; otherwise, `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="69d29-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="69d29-110">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="69d29-111">`SqlStreamChars.IsNull`プロパティはプライベートであり、コード内で直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="69d29-111">The `SqlStreamChars.IsNull` property is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="69d29-112">Microsoft はいかなる運用アプリケーションでこのフィールドの使用をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="69d29-112">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d29-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="69d29-113">Requirements</span></span>

<span data-ttu-id="69d29-114">**名前空間:** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="69d29-114">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="69d29-115">**アセンブリ:** System.Data (system.data.dll 内)</span><span class="sxs-lookup"><span data-stu-id="69d29-115">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="69d29-116">**.NET framework のバージョン:** 2.0 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="69d29-116">**.NET Framework versions:** Available since 2.0.</span></span>