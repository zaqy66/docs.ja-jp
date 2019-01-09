---
title: SqlStreamChars.Read (Char、Int32, Int32) メソッド (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.Read
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 87bff6dd78743ae08a5a3db8a783b56a0b7c3f24
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152535"
---
# <a name="sqlstreamcharsreadchar-int32-int32-method"></a><span data-ttu-id="0836a-102">SqlStreamChars.Read (Char、Int32, Int32) メソッド</span><span class="sxs-lookup"><span data-stu-id="0836a-102">SqlStreamChars.Read(Char[], Int32, Int32) Method</span></span>

<span data-ttu-id="0836a-103">派生クラスでオーバーライドされると、入力ストリームから次の文字セットを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="0836a-103">When overridden in a derived class, reads the next set of characters from the input stream.</span></span> <span data-ttu-id="0836a-104">このメソッドを含むアセンブリには、SQLAccess.dll で友人関係があります。</span><span class="sxs-lookup"><span data-stu-id="0836a-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="0836a-105">SQL Server で使用するものでは。</span><span class="sxs-lookup"><span data-stu-id="0836a-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="0836a-106">その他のデータベースには、そのデータベースによって提供されるホスティング メカニズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="0836a-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract int Read (char[] buffer, int offset, int count);
```

## <a name="parameters"></a><span data-ttu-id="0836a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0836a-107">Parameters</span></span>

`buffer`\
<span data-ttu-id="0836a-108">読み取る文字の配列。</span><span class="sxs-lookup"><span data-stu-id="0836a-108">A char array to read.</span></span>

`offset`\
<span data-ttu-id="0836a-109">原点からのオフセット。</span><span class="sxs-lookup"><span data-stu-id="0836a-109">An offset relative to origin.</span></span>

`count`\
<span data-ttu-id="0836a-110">現在のストリームから読み取る文字の数。</span><span class="sxs-lookup"><span data-stu-id="0836a-110">The number of characters to be read from the current stream.</span></span>

## <a name="returns"></a><span data-ttu-id="0836a-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="0836a-111">Returns</span></span>

<xref:System.Int32>\
<span data-ttu-id="0836a-112">バッファーに読み取られた合計文字数。</span><span class="sxs-lookup"><span data-stu-id="0836a-112">The total number of characters read into the buffer.</span></span>

## <a name="remarks"></a><span data-ttu-id="0836a-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="0836a-113">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="0836a-114">`SqlStreamChars.Read`メソッドはプライベートであり、コード内で直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="0836a-114">The `SqlStreamChars.Read` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="0836a-115">Microsoft はいかなる運用アプリケーションでこのフィールドの使用をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="0836a-115">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="0836a-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="0836a-116">Requirements</span></span>

<span data-ttu-id="0836a-117">**名前空間:** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="0836a-117">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="0836a-118">**アセンブリ:** System.Data (system.data.dll 内)</span><span class="sxs-lookup"><span data-stu-id="0836a-118">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="0836a-119">**.NET framework のバージョン:** 2.0 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="0836a-119">**.NET Framework versions:** Available since 2.0.</span></span>