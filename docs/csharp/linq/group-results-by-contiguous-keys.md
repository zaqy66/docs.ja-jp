---
title: 連続するキーで結果をグループ化する (C# での LINQ)
description: C# で LINQ を使用して、連続するキーで結果をグループ化する方法について説明します。
ms.date: 12/1/2016
ms.assetid: cbda9c08-151b-4c9e-82f7-c3d7f3dac66b
ms.openlocfilehash: 8ad08d861e2d0f5ee0f8a2eceeb8d82a9aa2a5a6
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2018
ms.locfileid: "37404763"
---
# <a name="group-results-by-contiguous-keys"></a><span data-ttu-id="dd87e-103">連続するキーで結果をグループ化する</span><span class="sxs-lookup"><span data-stu-id="dd87e-103">Group results by contiguous keys</span></span>

<span data-ttu-id="dd87e-104">要素をグループ化し、連続するキーのサブシーケンスを表すチャンクにする方法を次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="dd87e-104">The following example shows how to group elements into chunks that represent subsequences of contiguous keys.</span></span> <span data-ttu-id="dd87e-105">たとえば、次の一連のキーと値のペアがあるとします。</span><span class="sxs-lookup"><span data-stu-id="dd87e-105">For example, assume that you are given the following sequence of key-value pairs:</span></span>

|<span data-ttu-id="dd87e-106">キー</span><span class="sxs-lookup"><span data-stu-id="dd87e-106">Key</span></span>|<span data-ttu-id="dd87e-107">[値]</span><span class="sxs-lookup"><span data-stu-id="dd87e-107">Value</span></span>|
|---------|-----------|
|<span data-ttu-id="dd87e-108">A</span><span class="sxs-lookup"><span data-stu-id="dd87e-108">A</span></span>|<span data-ttu-id="dd87e-109">水</span><span class="sxs-lookup"><span data-stu-id="dd87e-109">We</span></span>|
|<span data-ttu-id="dd87e-110">A</span><span class="sxs-lookup"><span data-stu-id="dd87e-110">A</span></span>|<span data-ttu-id="dd87e-111">think</span><span class="sxs-lookup"><span data-stu-id="dd87e-111">think</span></span>|
|<span data-ttu-id="dd87e-112">A</span><span class="sxs-lookup"><span data-stu-id="dd87e-112">A</span></span>|<span data-ttu-id="dd87e-113">that</span><span class="sxs-lookup"><span data-stu-id="dd87e-113">that</span></span>|
|<span data-ttu-id="dd87e-114">B</span><span class="sxs-lookup"><span data-stu-id="dd87e-114">B</span></span>|<span data-ttu-id="dd87e-115">Linq</span><span class="sxs-lookup"><span data-stu-id="dd87e-115">Linq</span></span>|
|<span data-ttu-id="dd87e-116">C</span><span class="sxs-lookup"><span data-stu-id="dd87e-116">C</span></span>|<span data-ttu-id="dd87e-117">is</span><span class="sxs-lookup"><span data-stu-id="dd87e-117">is</span></span>|
|<span data-ttu-id="dd87e-118">A</span><span class="sxs-lookup"><span data-stu-id="dd87e-118">A</span></span>|<span data-ttu-id="dd87e-119">really</span><span class="sxs-lookup"><span data-stu-id="dd87e-119">really</span></span>|
|<span data-ttu-id="dd87e-120">B</span><span class="sxs-lookup"><span data-stu-id="dd87e-120">B</span></span>|<span data-ttu-id="dd87e-121">cool</span><span class="sxs-lookup"><span data-stu-id="dd87e-121">cool</span></span>|
|<span data-ttu-id="dd87e-122">B</span><span class="sxs-lookup"><span data-stu-id="dd87e-122">B</span></span>|<span data-ttu-id="dd87e-123">!</span><span class="sxs-lookup"><span data-stu-id="dd87e-123">!</span></span>|

<span data-ttu-id="dd87e-124">次のグループがこの順序で作成されます。</span><span class="sxs-lookup"><span data-stu-id="dd87e-124">The following groups will be created in this order:</span></span>

1. <span data-ttu-id="dd87e-125">We, think, that</span><span class="sxs-lookup"><span data-stu-id="dd87e-125">We, think, that</span></span>

2. <span data-ttu-id="dd87e-126">Linq</span><span class="sxs-lookup"><span data-stu-id="dd87e-126">Linq</span></span>

3. <span data-ttu-id="dd87e-127">is</span><span class="sxs-lookup"><span data-stu-id="dd87e-127">is</span></span>

4. <span data-ttu-id="dd87e-128">really</span><span class="sxs-lookup"><span data-stu-id="dd87e-128">really</span></span>

5. <span data-ttu-id="dd87e-129">cool, !</span><span class="sxs-lookup"><span data-stu-id="dd87e-129">cool, !</span></span>

<span data-ttu-id="dd87e-130">ソリューションは、結果をストリーミングで返すスレッド セーフな拡張メソッドとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="dd87e-130">The solution is implemented as an extension method that is thread-safe and that returns its results in a streaming manner.</span></span> <span data-ttu-id="dd87e-131">つまり、ソース シーケンス内を移動するときにグループが作成されます。</span><span class="sxs-lookup"><span data-stu-id="dd87e-131">In other words, it produces its groups as it moves through the source sequence.</span></span> <span data-ttu-id="dd87e-132">`group` 演算子や `orderby` 演算子とは異なり、すべてのシーケンスの読み取りが終わる前に、呼び出し元にグループを返し始めることができます。</span><span class="sxs-lookup"><span data-stu-id="dd87e-132">Unlike the `group` or `orderby` operators, it can begin returning groups to the caller before all of the sequence has been read.</span></span>

<span data-ttu-id="dd87e-133">ソース コードのコメントで説明されているように、ソース シーケンスが反復処理されるときに各グループまたはチャンクのコピーを作成することで、スレッド セーフが実現されます。</span><span class="sxs-lookup"><span data-stu-id="dd87e-133">Thread-safety is accomplished by making a copy of each group or chunk as the source sequence is iterated, as explained in the source code comments.</span></span> <span data-ttu-id="dd87e-134">ソース シーケンスに連続するアイテムの大きなシーケンスがある場合、共通言語ランタイムにより <xref:System.OutOfMemoryException> がスローされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dd87e-134">If the source sequence has a large sequence of contiguous items, the common language runtime may throw an <xref:System.OutOfMemoryException>.</span></span>

## <a name="example"></a><span data-ttu-id="dd87e-135">例</span><span class="sxs-lookup"><span data-stu-id="dd87e-135">Example</span></span>

<span data-ttu-id="dd87e-136">拡張メソッドと、それを使用するクライアント コードの両方を次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="dd87e-136">The following example shows both the extension method and the client code that uses it:</span></span>

[!code-csharp[cscsrefContiguousGroups#1](~/samples/snippets/csharp/concepts/linq/how-to-group-results-by-contiguous-keys_1.cs)]

<span data-ttu-id="dd87e-137">プロジェクトで拡張メソッドを使用するには、`MyExtensions` 静的クラスを新規または既存のソース コード ファイルにコピーし、必要に応じて、配置されている名前空間の `using` ディレクティブを追加します。</span><span class="sxs-lookup"><span data-stu-id="dd87e-137">To use the extension method in your project, copy the `MyExtensions` static class to a new or existing source code file and if it is required, add a `using` directive for the namespace where it is located.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd87e-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="dd87e-138">See also</span></span>

[<span data-ttu-id="dd87e-139">統合言語クエリ (LINQ)</span><span class="sxs-lookup"><span data-stu-id="dd87e-139">Language Integrated Query (LINQ)</span></span>](index.md)