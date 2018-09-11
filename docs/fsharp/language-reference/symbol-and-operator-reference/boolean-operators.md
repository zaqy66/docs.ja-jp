---
title: ブール演算子 (F#)
description: F# プログラミング言語で使用可能なブール演算子について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: faa181090efa7c4064a30b42d83afa4888e98b82
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/10/2018
ms.locfileid: "44272320"
---
# <a name="boolean-operators"></a><span data-ttu-id="18fc3-103">ブール演算子</span><span class="sxs-lookup"><span data-stu-id="18fc3-103">Boolean Operators</span></span>

<span data-ttu-id="18fc3-104">このトピックでは、f# 言語でブール演算子のサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="18fc3-104">This topic describes the support for Boolean operators in the F# language.</span></span>

## <a name="summary-of-boolean-operators"></a><span data-ttu-id="18fc3-105">ブール演算子の概要</span><span class="sxs-lookup"><span data-stu-id="18fc3-105">Summary of Boolean Operators</span></span>

<span data-ttu-id="18fc3-106">次の表では、f# 言語で使用可能なブール演算子をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="18fc3-106">The following table summarizes the Boolean operators that are available in the F# language.</span></span> <span data-ttu-id="18fc3-107">これらの演算子でサポートされている唯一の種類は、`bool`型。</span><span class="sxs-lookup"><span data-stu-id="18fc3-107">The only type supported by these operators is the `bool` type.</span></span>

|<span data-ttu-id="18fc3-108">演算子</span><span class="sxs-lookup"><span data-stu-id="18fc3-108">Operator</span></span>|<span data-ttu-id="18fc3-109">説明</span><span class="sxs-lookup"><span data-stu-id="18fc3-109">Description</span></span>|
|--------|-----------|
|`not`|<span data-ttu-id="18fc3-110">否定のブール型</span><span class="sxs-lookup"><span data-stu-id="18fc3-110">Boolean negation</span></span>|
|<code>&#124;&#124;</code>|<span data-ttu-id="18fc3-111">ブール型 OR</span><span class="sxs-lookup"><span data-stu-id="18fc3-111">Boolean OR</span></span>|
|`&&`|<span data-ttu-id="18fc3-112">ブール型 AND</span><span class="sxs-lookup"><span data-stu-id="18fc3-112">Boolean AND</span></span>|

<span data-ttu-id="18fc3-113">ブール型 AND および OR 演算子を実行*ショート サーキット評価*演算子の右辺の式を評価、式の全体的な結果を確認する必要がある場合にのみ、します。</span><span class="sxs-lookup"><span data-stu-id="18fc3-113">The Boolean AND and OR operators perform *short-circuit evaluation*, that is, they evaluate the expression on the right of the operator only when it is necessary to determine the overall result of the expression.</span></span> <span data-ttu-id="18fc3-114">2 番目の式、`&&`に最初の式が評価された場合にのみ、演算子が評価される`true`; の 2 番目の式、`||`に最初の式が評価された場合にのみ、演算子が評価される`false`します。</span><span class="sxs-lookup"><span data-stu-id="18fc3-114">The second expression of the `&&` operator is evaluated only if the first expression evaluates to `true`; the second expression of the `||` operator is evaluated only if the first expression evaluates to `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="18fc3-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="18fc3-115">See also</span></span>

- [<span data-ttu-id="18fc3-116">ビット処理演算子</span><span class="sxs-lookup"><span data-stu-id="18fc3-116">Bitwise Operators</span></span>](bitwise-operators.md)
- [<span data-ttu-id="18fc3-117">算術演算子</span><span class="sxs-lookup"><span data-stu-id="18fc3-117">Arithmetic Operators</span></span>](arithmetic-operators.md)
- [<span data-ttu-id="18fc3-118">シンボルと演算子のリファレンス</span><span class="sxs-lookup"><span data-stu-id="18fc3-118">Symbol and Operator Reference</span></span>](index.md)
