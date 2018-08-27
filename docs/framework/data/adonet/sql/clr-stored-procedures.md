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
# <a name="clr-stored-procedures"></a><span data-ttu-id="b813b-102">CLR ストアド プロシージャ</span><span class="sxs-lookup"><span data-stu-id="b813b-102">CLR Stored Procedures</span></span>
<span data-ttu-id="b813b-103">ストアド プロシージャは、スカラー式では使用できないルーチンです。</span><span class="sxs-lookup"><span data-stu-id="b813b-103">Stored procedures are routines that cannot be used in scalar expressions.</span></span> <span data-ttu-id="b813b-104">ストアド プロシージャは、表形式の結果とメッセージをクライアントに返したり、データ定義言語 (DDL) ステートメントおよびデータ操作言語 (DML) ステートメントを呼び出したり、出力パラメーターを返したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="b813b-104">They can return tabular results and messages to the client, invoke data definition language (DDL) and data manipulation language (DML) statements, and return output parameters.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b813b-105">Microsoft Visual Basic では、出力パラメーターのサポートが Microsoft Visual C# と異なります。</span><span class="sxs-lookup"><span data-stu-id="b813b-105">Microsoft Visual Basic does not support output parameters in the same way that Microsoft Visual C# does.</span></span> <span data-ttu-id="b813b-106">参照渡しでパラメーターを渡すし、適用を指定する必要があります、 \<Out() > 属性を次のように、出力パラメーターを表します。</span><span class="sxs-lookup"><span data-stu-id="b813b-106">You must specify to pass the parameter by reference and apply the \<Out()> attribute to represent an output parameter, as in the following:</span></span>  
  
```vb
Public Shared Sub ExecuteToClient( <Out()> ByRef number As Integer)  
```
  
<span data-ttu-id="b813b-107">詳細については、のバージョンを参照してください。 [SQL Server のドキュメント](/sql)を使用する SQL Server のバージョン。</span><span class="sxs-lookup"><span data-stu-id="b813b-107">For more detailed information, see the version of [SQL Server documentation](/sql) for the version of SQL Server you're using.</span></span>
  
 <span data-ttu-id="b813b-108">**SQL Server のドキュメント**</span><span class="sxs-lookup"><span data-stu-id="b813b-108">**SQL Server documentation**</span></span>

1. [<span data-ttu-id="b813b-109">CLR ストアド プロシージャ</span><span class="sxs-lookup"><span data-stu-id="b813b-109">CLR Stored Procedures</span></span>](http://go.microsoft.com/fwlink/?LinkId=115400)  
  
## <a name="see-also"></a><span data-ttu-id="b813b-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="b813b-110">See Also</span></span>  
 [<span data-ttu-id="b813b-111">マネージ コードで SQL Server 2005 のオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="b813b-111">Creating SQL Server 2005 Objects In Managed Code</span></span>](http://msdn.microsoft.com/library/5358a825-e19b-49aa-8214-674ce5fed1da)  
 <span data-ttu-id="b813b-112">
  [ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター](http://go.microsoft.com/fwlink/?LinkId=217917)</span><span class="sxs-lookup"><span data-stu-id="b813b-112">[ADO.NET Managed Providers and DataSet Developer Center](http://go.microsoft.com/fwlink/?LinkId=217917)</span></span>
