---
title: ユーザー定義関数 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 3f9e6bbd-8e5a-43e1-809f-f8a61338e522
ms.openlocfilehash: 03146d895c6ca780692228937fafcf25b24902aa
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2018
ms.locfileid: "44494188"
---
# <a name="user-defined-functions-entity-sql"></a>ユーザー定義関数 (Entity SQL)
Entity SQL では、クエリ内でのユーザー定義関数の呼び出しがサポートされます。 関数をインライン クエリでこれらを定義することができます (を参照してください[方法: ユーザー定義関数を呼び出す](https://msdn.microsoft.com/library/ad131b86-8b4e-4747-8605-d4fc64fb9d02)) または概念モデルの一部として (を参照してください[方法: 概念モデルでカスタム関数を定義](https://msdn.microsoft.com/library/0dad7b8b-58f6-4271-b238-f34810d68e5f))。 Entity SQL コマンドを概念モデルの関数が定義されている、 [DefiningExpression](https://msdn.microsoft.com/library/d3da8d8b-a048-47ee-8d81-0c2ea3acdd3e)の要素を[関数](https://msdn.microsoft.com/library/dc3beca7-55cf-4977-8db0-5064cdbab134)概念モデル内の要素。  
  
 Entity SQL を使用すると、関数をクエリ コマンド自体で定義することができます。 [関数](../../../../../../docs/framework/data/adonet/ef/language-reference/function-entity-sql.md)演算子は、インライン関数を定義します。 複数の関数を 1 つのコマンドで定義することができます。関数の署名が一意であれば、これら複数の関数に同じ名前を付けることができます。 詳細については、「 [Function Overload Resolution](../../../../../../docs/framework/data/adonet/ef/language-reference/function-overload-resolution-entity-sql.md)」を参照してください。  
  
## <a name="see-also"></a>関連項目  
 [関数](../../../../../../docs/framework/data/adonet/ef/language-reference/functions-entity-sql.md)
