---
title: アサーション (F#)
description: F# プログラミング言語で式をテストするためのデバッグ機能として 'アサート' 式を使用する方法について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: 85b1e839bfd19bada48b7f1821d15ddd8fa77754
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/19/2018
ms.locfileid: "46322983"
---
# <a name="assertions"></a><span data-ttu-id="5ff96-103">アサーション</span><span class="sxs-lookup"><span data-stu-id="5ff96-103">Assertions</span></span>

<span data-ttu-id="5ff96-104">`assert`式は、式のテストに使用できるデバッグ機能。</span><span class="sxs-lookup"><span data-stu-id="5ff96-104">The `assert` expression is a debugging feature that you can use to test an expression.</span></span> <span data-ttu-id="5ff96-105">デバッグ モードでエラーが発生すると、アサーションによってシステム エラーのダイアログ ボックスが生成されます。</span><span class="sxs-lookup"><span data-stu-id="5ff96-105">Upon failure in Debug mode, an assertion generates a system error dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ff96-106">構文</span><span class="sxs-lookup"><span data-stu-id="5ff96-106">Syntax</span></span>

```fsharp
assert condition
```

## <a name="remarks"></a><span data-ttu-id="5ff96-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="5ff96-107">Remarks</span></span>

<span data-ttu-id="5ff96-108">`assert`式の型`bool -> unit`します。</span><span class="sxs-lookup"><span data-stu-id="5ff96-108">The `assert` expression has type `bool -> unit`.</span></span>

<span data-ttu-id="5ff96-109">前の構文で*条件*をテストするブール式を表します。</span><span class="sxs-lookup"><span data-stu-id="5ff96-109">In the previous syntax, *condition* represents a Boolean expression that is to be tested.</span></span> <span data-ttu-id="5ff96-110">式が評価された場合`true`実行が影響を受けていないが続行されます。</span><span class="sxs-lookup"><span data-stu-id="5ff96-110">If the expression evaluates to `true`, execution continues unaffected.</span></span> <span data-ttu-id="5ff96-111">評価されると、`false`システムのエラー ダイアログ ボックスが生成されます。</span><span class="sxs-lookup"><span data-stu-id="5ff96-111">If it evaluates to `false`, a system error dialog box is generated.</span></span> <span data-ttu-id="5ff96-112">エラー ダイアログ ボックスには、文字列を含むキャプション**アサーションが失敗した**します。</span><span class="sxs-lookup"><span data-stu-id="5ff96-112">The error dialog box has a caption that contains the string **Assertion Failed**.</span></span> <span data-ttu-id="5ff96-113">ダイアログ ボックスには、アサーション エラーが発生したかを示すスタック トレースが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5ff96-113">The dialog box contains a stack trace that indicates where the assertion failure occurred.</span></span>

<span data-ttu-id="5ff96-114">デバッグ モードでコンパイルする場合にのみにアサーション チェックが有効にはつまり場合、定数`DEBUG`が定義されています。</span><span class="sxs-lookup"><span data-stu-id="5ff96-114">Assertion checking is enabled only when you compile in Debug mode; that is, if the constant `DEBUG` is defined.</span></span> <span data-ttu-id="5ff96-115">既定で、プロジェクト システムで、`DEBUG`リリース構成ではなく、デバッグ構成で定義される定数。</span><span class="sxs-lookup"><span data-stu-id="5ff96-115">In the project system, by default, the `DEBUG` constant is defined in the Debug configuration but not in the Release configuration.</span></span>

<span data-ttu-id="5ff96-116">F# の例外処理を使用してアサーション エラーをキャッチできません。</span><span class="sxs-lookup"><span data-stu-id="5ff96-116">The assertion failure error cannot be caught by using F# exception handling.</span></span>

>[!NOTE]
<span data-ttu-id="5ff96-117">`assert`関数に解決<xref:System.Diagnostics.Debug.Assert*?displayProperty=nameWithType>します。</span><span class="sxs-lookup"><span data-stu-id="5ff96-117">The `assert` function resolves to <xref:System.Diagnostics.Debug.Assert*?displayProperty=nameWithType>.</span></span>

## <a name="example"></a><span data-ttu-id="5ff96-118">例</span><span class="sxs-lookup"><span data-stu-id="5ff96-118">Example</span></span>

<span data-ttu-id="5ff96-119">次のコード例の使用を示しています、`assert`式。</span><span class="sxs-lookup"><span data-stu-id="5ff96-119">The following code example illustrates the use of the `assert` expression.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5401.fs)]

## <a name="see-also"></a><span data-ttu-id="5ff96-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ff96-120">See also</span></span>

- [<span data-ttu-id="5ff96-121">F# 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="5ff96-121">F# Language Reference</span></span>](index.md)
