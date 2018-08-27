---
title: CLR ストアド プロシージャ
ms.date: 03/30/2017
ms.assetid: fd7eea9b-218a-4988-8c9a-8abcc6031c66
ms.openlocfilehash: df323e2d1b50dcd1b2087141deefa1c86723b346
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42930113"
---
# <a name="clr-stored-procedures"></a>CLR ストアド プロシージャ
ストアド プロシージャは、スカラー式では使用できないルーチンです。 ストアド プロシージャは、表形式の結果とメッセージをクライアントに返したり、データ定義言語 (DDL) ステートメントおよびデータ操作言語 (DML) ステートメントを呼び出したり、出力パラメーターを返したりすることができます。  
  
> [!NOTE]
>  Microsoft Visual Basic では、出力パラメーターのサポートが Microsoft Visual C# と異なります。 参照渡しでパラメーターを渡すし、適用を指定する必要があります、 \<Out() > 属性を次のように、出力パラメーターを表します。  
  
```vb
Public Shared Sub ExecuteToClient( <Out()> ByRef number As Integer)  
```
  
詳細については、のバージョンを参照してください。 [SQL Server のドキュメント](/sql)を使用する SQL Server のバージョン。
  
 **SQL Server のドキュメント**

1. [CLR ストアド プロシージャ](http://go.microsoft.com/fwlink/?LinkId=115400)  
  
## <a name="see-also"></a>関連項目  
 [マネージ コードで SQL Server 2005 のオブジェクトを作成します。](http://msdn.microsoft.com/library/5358a825-e19b-49aa-8214-674ce5fed1da)  
 
  [ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター](http://go.microsoft.com/fwlink/?LinkId=217917)
