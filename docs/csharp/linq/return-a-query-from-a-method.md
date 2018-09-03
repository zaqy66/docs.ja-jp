---
title: メソッドからクエリを返す
description: クエリを返す方法。
ms.date: 11/30/2016
ms.assetid: db220f79-c35b-41f2-886c-cd068672d42d
ms.openlocfilehash: 1c5fa534f3f39f8201d93b986e687d85bb303736
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2018
ms.locfileid: "43473945"
---
# <a name="how-to-return-a-query-from-a-method-c-programming-guide"></a>方法 : メソッドからクエリを返す (C# プログラミング ガイド)
この例では、メソッドから、クエリを戻り値として返す方法と `out` パラメーターとして返す方法を示します。  
  
 クエリ オブジェクトはコンポーザブルです。つまり、メソッドからクエリを返すことができます。 クエリを表すオブジェクトには、結果のコレクションではなく、必要に応じて結果を生成する手順が格納されます。 メソッドからクエリ オブジェクトを返すメリットは、そのオブジェクトをさらに構成したり変更したりできることです。 そのため、クエリを返すメソッドの戻り値または `out` パラメーターも同じ型である必要があります。 メソッドがクエリを具象型 <xref:System.Collections.Generic.List%601> または <xref:System.Array> に実体化する場合は、そのメソッドは、クエリ自体ではなくクエリ結果を返すと見なされます。 メソッドから返されたクエリ変数は、引き続き構成または変更できます。  
  
## <a name="example"></a>例  
 次の例は、最初のメソッドはクエリを戻り値として返し、2 番目のメソッドはクエリを `out` パラメーターとして返しています。 どちらの場合も返されるのはクエリであり、クエリ結果ではないことに注意してください。  
  
 [!code-csharp[csProgGuideLINQ#80](~/samples/snippets/csharp/concepts/linq/how-to-return-a-query-from-a-method_1.cs)]  

## <a name="see-also"></a>参照

- [統合言語クエリ (LINQ)](index.md)
