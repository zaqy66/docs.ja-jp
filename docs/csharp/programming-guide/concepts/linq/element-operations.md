---
title: 要素操作 (C#)
ms.date: 10/03/2018
ms.assetid: 283206c9-3246-4c48-b01a-d9de409a7231
ms.openlocfilehash: dbae8c0b3d98fe9674fbbeb432c1e42763e81026
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2018
ms.locfileid: "48836778"
---
# <a name="element-operations-c"></a>要素操作 (C#)

要素操作では、シーケンスから単一の特定の要素が返されます。  
  
 次のセクションでは、要素操作を実行する標準クエリ演算子のメソッドの一覧を示します。  
  
## <a name="methods"></a>メソッド  
  
|メソッド名|説明|C# のクエリ式の構文|説明|  
|-----------------|-----------------|---------------------------------|----------------------|  
|ElementAt|コレクション内の指定されたインデックス位置にある要素を返します。|該当なし。|<xref:System.Linq.Enumerable.ElementAt%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.ElementAt%2A?displayProperty=nameWithType>|  
|ElementAtOrDefault|コレクション内の指定したインデックス位置にある要素を返します。インデックスが範囲外の場合は既定値を返します。|該当なし。|<xref:System.Linq.Enumerable.ElementAtOrDefault%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.ElementAtOrDefault%2A?displayProperty=nameWithType>|  
|First|コレクションの最初の要素、または条件を満たす最初の要素を返します。|該当なし。|<xref:System.Linq.Enumerable.First%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.First%2A?displayProperty=nameWithType>|  
|FirstOrDefault|コレクションの最初の要素、または条件を満たす最初の要素を返します。 そのような要素が存在しない場合は、既定値を返します。|該当なし。|<xref:System.Linq.Enumerable.FirstOrDefault%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.FirstOrDefault%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.FirstOrDefault%60%601%28System.Linq.IQueryable%7B%60%600%7D%29?displayProperty=nameWithType>|  
|末尾|コレクションの最後の要素、または条件を満たす最後の要素を返します。|該当なし。|<xref:System.Linq.Enumerable.Last%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Last%2A?displayProperty=nameWithType>|  
|LastOrDefault|コレクションの最後の要素、または条件を満たす最後の要素を返します。 そのような要素が存在しない場合は、既定値を返します。|該当なし。|<xref:System.Linq.Enumerable.LastOrDefault%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.LastOrDefault%2A?displayProperty=nameWithType>|  
|Single|コレクションの唯一の要素、または条件を満たす唯一の要素を返します。 要素がない場合、または複数の要素が返される場合は、<xref:System.InvalidOperationException> をスローします。 |該当なし。|<xref:System.Linq.Enumerable.Single%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Single%2A?displayProperty=nameWithType>|  
|SingleOrDefault|コレクションの唯一の要素、または条件を満たす唯一の要素を返します。 返す要素がない場合は、既定値を返します。 複数の要素が返される場合は、<xref:System.InvalidOperationException> をスローします。 |該当なし。|<xref:System.Linq.Enumerable.SingleOrDefault%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.SingleOrDefault%2A?displayProperty=nameWithType>|  
  
## <a name="see-also"></a>参照

- <xref:System.Linq>  
- [標準クエリ演算子の概要 (C#)](../../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)  
- [方法: ディレクトリ ツリー内で最もサイズの大きいファイルを照会する (LINQ) (C#)](../../../../csharp/programming-guide/concepts/linq/how-to-query-for-the-largest-file-or-files-in-a-directory-tree-linq.md)
