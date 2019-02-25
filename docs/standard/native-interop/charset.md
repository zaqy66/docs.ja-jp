---
title: 文字セットとマーシャリング - .NET
description: CharSet の値によって、.NET でデータをネイティブ コードにマーシャリングする方法がどのように変わるかについて説明します。
author: jkoritzinsky
ms.author: jekoritz
ms.date: 01/18/2019
ms.openlocfilehash: 2ff6c485906db481cb5236f83e885ba9fd46450b
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "56411408"
---
# <a name="charsets-and-marshalling"></a><span data-ttu-id="ee3c5-103">文字セットとマーシャリング</span><span class="sxs-lookup"><span data-stu-id="ee3c5-103">Charsets and marshalling</span></span>

<span data-ttu-id="ee3c5-104">`char` 値、`string` オブジェクト、および `System.Text.StringBuilder` オブジェクトのマーシャリング方法は、P/Invoke または構造体の `CharSet` フィールド値によって変わります。</span><span class="sxs-lookup"><span data-stu-id="ee3c5-104">The way `char` values, `string` objects, and `System.Text.StringBuilder` objects are marshalled depends on the value of the `CharSet` field on either the P/Invoke or structure.</span></span> <span data-ttu-id="ee3c5-105">P/Invoke の `CharSet` を設定するには、P/Invoke を宣言するときに <xref:System.Runtime.InteropServices.DllImportAttribute.CharSet?displayProperty=nameWithType> フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3c5-105">You can set the `CharSet` of a P/Invoke by setting the <xref:System.Runtime.InteropServices.DllImportAttribute.CharSet?displayProperty=nameWithType> field when declaring your P/Invoke.</span></span> <span data-ttu-id="ee3c5-106">構造体の `CharSet` を設定するには、構造体宣言の <xref:System.Runtime.InteropServices.StructLayoutAttribute.CharSet?displayProperty=nameWithType> フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3c5-106">To set the `CharSet` for a structure, set the <xref:System.Runtime.InteropServices.StructLayoutAttribute.CharSet?displayProperty=nameWithType> field on your struct declaration.</span></span> <span data-ttu-id="ee3c5-107">これらの属性フィールドが設定されていない場合、言語コンパイラによって使用する `CharSet` が決まります。</span><span class="sxs-lookup"><span data-stu-id="ee3c5-107">When these attribute fields are not set, it is up to the language compiler to determine which `CharSet` to use.</span></span> <span data-ttu-id="ee3c5-108">C# は既定で <xref:System.Runtime.InteropServices.CharSet.Ansi> 文字セットを使用します。</span><span class="sxs-lookup"><span data-stu-id="ee3c5-108">C# uses the <xref:System.Runtime.InteropServices.CharSet.Ansi> charset by default.</span></span>

<span data-ttu-id="ee3c5-109">次の表は、各文字セット間のマッピングと、その文字セットでマーシャリングしたときに文字または文字列がどのように表現されるかをまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="ee3c5-109">The following table shows a mapping between each charset and how a character or string is represented when marshalled with that charset:</span></span>

| <span data-ttu-id="ee3c5-110">CharSet</span><span class="sxs-lookup"><span data-stu-id="ee3c5-110">CharSet</span></span> | <span data-ttu-id="ee3c5-111">Windows</span><span class="sxs-lookup"><span data-stu-id="ee3c5-111">Windows</span></span> | <span data-ttu-id="ee3c5-112">Unix</span><span class="sxs-lookup"><span data-stu-id="ee3c5-112">Unix</span></span> | <span data-ttu-id="ee3c5-113">Mono on Unix</span><span class="sxs-lookup"><span data-stu-id="ee3c5-113">Mono on Unix</span></span> |
|---------|---------|-------|-------|
| <span data-ttu-id="ee3c5-114">Ansi</span><span class="sxs-lookup"><span data-stu-id="ee3c5-114">Ansi</span></span>    | <span data-ttu-id="ee3c5-115">`char` (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ee3c5-115">`char` (ANSI)</span></span>  | <span data-ttu-id="ee3c5-116">`char` (macOS 上では ANSI、Linux 上では UTF-8)</span><span class="sxs-lookup"><span data-stu-id="ee3c5-116">`char` (ANSI on macOS, UTF-8 on Linux)</span></span> | <span data-ttu-id="ee3c5-117">`char` (UTF-8)</span><span class="sxs-lookup"><span data-stu-id="ee3c5-117">`char` (UTF-8)</span></span> |
| <span data-ttu-id="ee3c5-118">Unicode</span><span class="sxs-lookup"><span data-stu-id="ee3c5-118">Unicode</span></span> | <span data-ttu-id="ee3c5-119">`wchar_t` (UTF-16)</span><span class="sxs-lookup"><span data-stu-id="ee3c5-119">`wchar_t` (UTF-16)</span></span> | <span data-ttu-id="ee3c5-120">`char16_t` (UTF-16)</span><span class="sxs-lookup"><span data-stu-id="ee3c5-120">`char16_t` (UTF-16)</span></span> | <span data-ttu-id="ee3c5-121">`char16_t` (UTF-16)</span><span class="sxs-lookup"><span data-stu-id="ee3c5-121">`char16_t` (UTF-16)</span></span> |
| <span data-ttu-id="ee3c5-122">自動</span><span class="sxs-lookup"><span data-stu-id="ee3c5-122">Auto</span></span> | <span data-ttu-id="ee3c5-123">`wchar_t` (UTF-16)</span><span class="sxs-lookup"><span data-stu-id="ee3c5-123">`wchar_t` (UTF-16)</span></span> | <span data-ttu-id="ee3c5-124">`char16_t` (UTF-16)</span><span class="sxs-lookup"><span data-stu-id="ee3c5-124">`char16_t` (UTF-16)</span></span> | <span data-ttu-id="ee3c5-125">`char` (UTF-8)</span><span class="sxs-lookup"><span data-stu-id="ee3c5-125">`char` (UTF-8)</span></span> |

<span data-ttu-id="ee3c5-126">文字セットを選択するときは、必ずネイティブ表現で期待される表現を必ず把握しておいてください。</span><span class="sxs-lookup"><span data-stu-id="ee3c5-126">Make sure you know what representation your native representation expects when picking your charset.</span></span>
