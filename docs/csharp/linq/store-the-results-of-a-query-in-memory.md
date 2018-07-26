---
title: クエリ結果をメモリに格納する
description: 結果の格納方法。
ms.date: 11/30/2016
ms.assetid: 5b863961-1750-4cf9-9607-acea5054d15a
ms.openlocfilehash: 52d502a841c428bd90a26c803ba577e76c17197c
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2018
ms.locfileid: "37404302"
---
# <a name="store-the-results-of-a-query-in-memory"></a>クエリ結果をメモリに格納する

クエリは、基本的に、データの取得方法と編成方法を指示するための一連の命令です。 結果の各項目は順次要求されるため、クエリは遅延実行されます。 `foreach` を使用して結果を反復すると、項目はアクセスのたびに返されます。 クエリを評価し、`foreach` のループを実行せずに結果を格納するには、クエリ変数で次のメソッドのいずれかを呼び出します。

- <xref:System.Linq.Enumerable.ToList%2A>

- <xref:System.Linq.Enumerable.ToArray%2A>

- <xref:System.Linq.Enumerable.ToDictionary%2A>

- <xref:System.Linq.Enumerable.ToLookup%2A>

 クエリ結果を格納するときは、次の例に示すように、返されたコレクション オブジェクトを新しい変数に割り当てることをお勧めします。

## <a name="example"></a>例

[!code-csharp[csProgGuideLINQ#25](~/samples/snippets/csharp/concepts/linq/how-to-store-the-results-of-a-query-in-memory_1.cs)]

## <a name="see-also"></a>関連項目

[統合言語クエリ (LINQ)](index.md)