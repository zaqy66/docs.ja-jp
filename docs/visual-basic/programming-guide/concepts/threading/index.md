---
title: スレッド処理 (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 704bb04b-ff23-471d-ab12-3cec1c2bca59
ms.openlocfilehash: 366c88db5d229120b1e626f275b4eeb8ecd42dba
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2018
ms.locfileid: "48844996"
---
# <a name="threading-visual-basic"></a>スレッド処理 (Visual Basic)
スレッド処理により、Visual Basic プログラムが同時処理を実行できるようになり、一度に複数の操作を行うことが可能になります。 たとえば、スレッド処理を使用してユーザーの入力を監視したり、バックグラウンド タスクを実行したり、入力の同時ストリームを処理したりできます。  
  
 スレッドには次のようなプロパティがあります。  
  
-   スレッドにより、プログラムの同時処理の実行が可能になります。  
  
-   .NET Framework の <xref:System.Threading> 名前空間により、スレッドの使用が簡単になります。  
  
-   スレッドは、アプリケーションのリソースを共有します。 詳細については、「[Using Threads and Threading](../../../../standard/threading/using-threads-and-threading.md)」(スレッドの使用とスレッド処理) を参照してください。  
  
 既定では、Visual Basic プログラムにはスレッドが 1 つあります。 ただし、補助スレッドを作成し、プライマリ スレッドと並行してコードを実行するために使用することができます。 このようなスレッドは、よく*ワーカー スレッド*と呼ばれます。  
  
 ワーカー スレッドを使用すると、プライマリ スレッドに拘束されることなく、時間がかかるタスクやタイム クリティカルなタスクを実行することができます。 たとえば、ワーカー スレッドは、前の要求が完了するのを待たずに受信する要求を処理するために、サーバー アプリケーションで多く使用されます。 ワーカー スレッドは、デスクトップ アプリケーションで "バックグラウンド" タスクを実行するためにも使用されます。これにより、ユーザー インターフェイス要素を動かすメイン スレッドは引き続きユーザー操作に応答できます。  
  
 スレッド処理はスループットと応答速度の問題を解決しますが、その一方で、デッドロックや競合状態のようなリソース共有の問題を発生させます。 複数のスレッドは、ファイル ハンドルやネットワーク接続など、さまざまなリソースを必要とするタスクに最適です。 複数のスレッドを 1 つのリソースに割り当てると、同期の問題が発生しやすくなり、他のスレッドの待機中に頻繁にブロックされるスレッドがあると、複数のスレッドを使用する目的が果たされなくなります。  
  
 一般的な方法としては、ワーカー スレッドを使用して、他のスレッドで使用されるリソースをあまり必要としない、時間がかかるタスクやタイム クリティカルなタスクを実行します。 当然ながら、プログラムの一部のリソースは、複数のスレッドによってアクセスされます。 このような場合に、<xref:System.Threading> 名前空間によってスレッドを同期するためのクラスが提供されます。 これらのクラスには、<xref:System.Threading.Mutex>、<xref:System.Threading.Monitor>、<xref:System.Threading.Interlocked>、<xref:System.Threading.AutoResetEvent>、および <xref:System.Threading.ManualResetEvent> があります。  
  
 これらのクラスの一部またはすべてを使用して、複数のスレッドのアクティビティを同期できますが、スレッド処理一部のサポートは Visual Basic 言語によりサポートされています。 たとえば、[SyncLock ステートメント](../../../../visual-basic/language-reference/statements/synclock-statement.md)は、<xref:System.Threading.Monitor> を暗黙的に使用することで同期機能を提供します。  
  
> [!NOTE]
>  [!INCLUDE[net_v40_long](~/includes/net-v40-long-md.md)] 以降では、<xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType> クラスおよび <xref:System.Threading.Tasks.Task?displayProperty=nameWithType> クラス、[Parallel LINQ (PLINQ)](../../../../standard/parallel-programming/parallel-linq-plinq.md)、<xref:System.Collections.Concurrent?displayProperty=nameWithType> 名前空間の新しい同時実行コレクション クラス、スレッドではなくタスクの概念をベースにした新しいプログラミング モデルにより、マルチスレッド プログラミングが大幅に簡略化されています。 詳細については、[並列プログラミング](../../../../standard/parallel-programming/index.md)に関するページをご覧ください。  
  
## <a name="related-topics"></a>関連トピック  
  
|Title|説明|  
|-----------|-----------------|  
|[スレッド化](../../../../standard/threading/index.md)|.NET Framework でのスレッドの実装方法について説明します。|
