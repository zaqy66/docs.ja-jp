---
title: クエリ結果のグループ化 (C# での LINQ)
description: C# で LINQ を使用して、結果をグループ化する方法について説明します。
ms.date: 12/01/2016
ms.assetid: 2e4ec27f-06fb-4de7-8973-0189906d4520
ms.openlocfilehash: 577a358c31fcf5346e7aab7a2e2b6be10fd1beff
ms.sourcegitcommit: 5dcfeb59179e81071f54840d4902cbe00b184294
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/24/2019
ms.locfileid: "54857854"
---
# <a name="group-query-results"></a><span data-ttu-id="32404-103">クエリ結果のグループ化</span><span class="sxs-lookup"><span data-stu-id="32404-103">Group query results</span></span>

<span data-ttu-id="32404-104">グループ化は、LINQ の最も強力な機能の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="32404-104">Grouping is one of the most powerful capabilities of LINQ.</span></span> <span data-ttu-id="32404-105">次の例では、さまざまな方法でデータをグループ化する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="32404-105">The following examples show how to group data in various ways:</span></span>

- <span data-ttu-id="32404-106">1 つのプロパティで。</span><span class="sxs-lookup"><span data-stu-id="32404-106">By a single property.</span></span>

- <span data-ttu-id="32404-107">文字列プロパティの最初の文字で。</span><span class="sxs-lookup"><span data-stu-id="32404-107">By the first letter of a string property.</span></span>

- <span data-ttu-id="32404-108">計算された数値の範囲で。</span><span class="sxs-lookup"><span data-stu-id="32404-108">By a computed numeric range.</span></span>

- <span data-ttu-id="32404-109">ブール述語またはその他の式で。</span><span class="sxs-lookup"><span data-stu-id="32404-109">By Boolean predicate or other expression.</span></span>

- <span data-ttu-id="32404-110">複合キーで。</span><span class="sxs-lookup"><span data-stu-id="32404-110">By a compound key.</span></span>

<span data-ttu-id="32404-111">さらに、最後の 2 つのクエリは、学生の名と姓だけを含む新しい匿名型に結果を射影します。</span><span class="sxs-lookup"><span data-stu-id="32404-111">In addition, the last two queries project their results into a new anonymous type that contains only the student's first and last name.</span></span> <span data-ttu-id="32404-112">詳しくは、「[group 句](../language-reference/keywords/group-clause.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="32404-112">For more information, see the [group clause](../language-reference/keywords/group-clause.md).</span></span>

## <a name="example"></a><span data-ttu-id="32404-113">例</span><span class="sxs-lookup"><span data-stu-id="32404-113">Example</span></span>

<span data-ttu-id="32404-114">このトピックのすべての例では、次のヘルパー クラスとデータ ソースを使います。</span><span class="sxs-lookup"><span data-stu-id="32404-114">All the examples in this topic use the following helper classes and data sources.</span></span>

[!code-csharp[csProgGuideLINQ#15](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_1.cs)]

## <a name="example"></a><span data-ttu-id="32404-115">例</span><span class="sxs-lookup"><span data-stu-id="32404-115">Example</span></span>

<span data-ttu-id="32404-116">次の例では、要素の 1 つのプロパティをグループ化キーとして使って、ソース要素をグループ化する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="32404-116">The following example shows how to group source elements by using a single property of the element as the group key.</span></span> <span data-ttu-id="32404-117">この場合、キーは学生の姓である `string` です。</span><span class="sxs-lookup"><span data-stu-id="32404-117">In this case the key is a `string`, the student's last name.</span></span> <span data-ttu-id="32404-118">また、キーの部分文字列を使うこともできます。</span><span class="sxs-lookup"><span data-stu-id="32404-118">It is also possible to use a substring for the key.</span></span> <span data-ttu-id="32404-119">グループ化操作では、型の既定の等値比較子を使います。</span><span class="sxs-lookup"><span data-stu-id="32404-119">The grouping operation uses the default equality comparer for the type.</span></span>

<span data-ttu-id="32404-120">次のメソッドを `StudentClass` クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="32404-120">Paste the following method into the `StudentClass` class.</span></span> <span data-ttu-id="32404-121">`Main` メソッドの呼び出しステートメントを `sc.GroupBySingleProperty()` に変更します。</span><span class="sxs-lookup"><span data-stu-id="32404-121">Change the calling statement in the `Main` method to `sc.GroupBySingleProperty()`.</span></span>

[!code-csharp[csProgGuideLINQ#17](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_2.cs)]

## <a name="example"></a><span data-ttu-id="32404-122">例</span><span class="sxs-lookup"><span data-stu-id="32404-122">Example</span></span>

<span data-ttu-id="32404-123">次の例では、オブジェクトのプロパティ以外の何かをグループ化キーとして使って、ソース要素をグループ化する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="32404-123">The following example shows how to group source elements by using something other than a property of the object for the group key.</span></span> <span data-ttu-id="32404-124">この例では、キーは学生の姓の最初の文字です。</span><span class="sxs-lookup"><span data-stu-id="32404-124">In this example, the key is the first letter of the student's last name.</span></span>

<span data-ttu-id="32404-125">次のメソッドを `StudentClass` クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="32404-125">Paste the following method into the `StudentClass` class.</span></span> <span data-ttu-id="32404-126">`Main` メソッドの呼び出しステートメントを `sc.GroupBySubstring()` に変更します。</span><span class="sxs-lookup"><span data-stu-id="32404-126">Change the calling statement in the `Main` method to `sc.GroupBySubstring()`.</span></span>

[!code-csharp[csProgGuideLINQ#18](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_3.cs)]

## <a name="example"></a><span data-ttu-id="32404-127">例</span><span class="sxs-lookup"><span data-stu-id="32404-127">Example</span></span>

<span data-ttu-id="32404-128">次の例では、数値範囲をグループ化キーとして使って、ソース要素をグループ化する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="32404-128">The following example shows how to group source elements by using a numeric range as a group key.</span></span> <span data-ttu-id="32404-129">クエリは、名と姓および学生が属しているパーセンタイル範囲のみを含む匿名型に、結果を投影します。</span><span class="sxs-lookup"><span data-stu-id="32404-129">The query then projects the results into an anonymous type that contains only the first and last name and the percentile range to which the student belongs.</span></span> <span data-ttu-id="32404-130">匿名型を使っているのは、結果を表示するために完全な `Student` オブジェクトを使う必要がないためです。</span><span class="sxs-lookup"><span data-stu-id="32404-130">An anonymous type is used because it is not necessary to use the complete `Student` object to display the results.</span></span> <span data-ttu-id="32404-131">`GetPercentile` は、学生の平均スコアに基づいてパーセンタイルを計算するヘルパー関数です。</span><span class="sxs-lookup"><span data-stu-id="32404-131">`GetPercentile` is a helper function that calculates a percentile based on the student's average score.</span></span> <span data-ttu-id="32404-132">メソッドは、0 から 10 の間の整数を返します。</span><span class="sxs-lookup"><span data-stu-id="32404-132">The method returns an integer between 0 and 10.</span></span>

[!code-csharp[csProgGuideLINQ#50](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_4.cs)]

<span data-ttu-id="32404-133">次のメソッドを `StudentClass` クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="32404-133">Paste the following method into the `StudentClass` class.</span></span> <span data-ttu-id="32404-134">`Main` メソッドの呼び出しステートメントを `sc.GroupByRange()` に変更します。</span><span class="sxs-lookup"><span data-stu-id="32404-134">Change the calling statement in the `Main` method to `sc.GroupByRange()`.</span></span>

[!code-csharp[csProgGuideLINQ#19](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_5.cs)]

## <a name="example"></a><span data-ttu-id="32404-135">例</span><span class="sxs-lookup"><span data-stu-id="32404-135">Example</span></span>

<span data-ttu-id="32404-136">次の例では、ブール比較式を使って、ソース要素をグループ化する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="32404-136">The following example shows how to group source elements by using a Boolean comparison expression.</span></span> <span data-ttu-id="32404-137">この例のブール式は、学生の平均試験スコアが 75 より大きいかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="32404-137">In this example, the Boolean expression tests whether a student's average exam score is greater than 75.</span></span> <span data-ttu-id="32404-138">前の例と同じように、完全なソース要素が必要ないため、結果を匿名型に投影します。</span><span class="sxs-lookup"><span data-stu-id="32404-138">As in previous examples, the results are projected into an anonymous type because the complete source element is not needed.</span></span> <span data-ttu-id="32404-139">匿名型のプロパティは `Key` メンバーのプロパティになり、クエリ実行時に名前でアクセスできることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="32404-139">Note that the properties in the anonymous type become properties on the `Key` member and can be accessed by name when the query is executed.</span></span>

<span data-ttu-id="32404-140">次のメソッドを `StudentClass` クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="32404-140">Paste the following method into the `StudentClass` class.</span></span> <span data-ttu-id="32404-141">`Main` メソッドの呼び出しステートメントを `sc.GroupByBoolean()` に変更します。</span><span class="sxs-lookup"><span data-stu-id="32404-141">Change the calling statement in the `Main` method to `sc.GroupByBoolean()`.</span></span>

[!code-csharp[csProgGuideLINQ#20](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_6.cs)]

## <a name="example"></a><span data-ttu-id="32404-142">例</span><span class="sxs-lookup"><span data-stu-id="32404-142">Example</span></span>

<span data-ttu-id="32404-143">次の例では、匿名型を使って、複数の値を含むキーをカプセル化する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="32404-143">The following example shows how to use an anonymous type to encapsulate a key that contains multiple values.</span></span> <span data-ttu-id="32404-144">この例では、最初のキーの値は学生の姓の最初の文字です。</span><span class="sxs-lookup"><span data-stu-id="32404-144">In this example, the first key value is the first letter of the student's last name.</span></span> <span data-ttu-id="32404-145">2 番目のキーの値は、最初の試験での学生のスコアが 85 より高いかどうかを示すブール値です。</span><span class="sxs-lookup"><span data-stu-id="32404-145">The second key value is a Boolean that specifies whether the student scored over 85 on the first exam.</span></span> <span data-ttu-id="32404-146">キーの任意のプロパティでグループを並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="32404-146">You can order the groups by any property in the key.</span></span>

<span data-ttu-id="32404-147">次のメソッドを `StudentClass` クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="32404-147">Paste the following method into the `StudentClass` class.</span></span> <span data-ttu-id="32404-148">`Main` メソッドの呼び出しステートメントを `sc.GroupByCompositeKey()` に変更します。</span><span class="sxs-lookup"><span data-stu-id="32404-148">Change the calling statement in the `Main` method to `sc.GroupByCompositeKey()`.</span></span>

[!code-csharp[csProgGuideLINQ#21](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_7.cs)]

## <a name="see-also"></a><span data-ttu-id="32404-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="32404-149">See also</span></span>

- <xref:System.Linq.Enumerable.GroupBy%2A>
- <xref:System.Linq.IGrouping%602>
- [<span data-ttu-id="32404-150">統合言語クエリ (LINQ)</span><span class="sxs-lookup"><span data-stu-id="32404-150">Language Integrated Query (LINQ)</span></span>](index.md)
- [<span data-ttu-id="32404-151">group 句</span><span class="sxs-lookup"><span data-stu-id="32404-151">group clause</span></span>](../language-reference/keywords/group-clause.md)
- [<span data-ttu-id="32404-152">匿名型</span><span class="sxs-lookup"><span data-stu-id="32404-152">Anonymous Types</span></span>](../programming-guide/classes-and-structs/anonymous-types.md)
- [<span data-ttu-id="32404-153">グループ化操作でのサブクエリの実行</span><span class="sxs-lookup"><span data-stu-id="32404-153">Perform a Subquery on a Grouping Operation</span></span>](perform-a-subquery-on-a-grouping-operation.md)
- [<span data-ttu-id="32404-154">入れ子になったグループの作成</span><span class="sxs-lookup"><span data-stu-id="32404-154">Create a Nested Group</span></span>](create-a-nested-group.md)
- [<span data-ttu-id="32404-155">データのグループ化</span><span class="sxs-lookup"><span data-stu-id="32404-155">Grouping Data</span></span>](../programming-guide/concepts/linq/grouping-data.md)
