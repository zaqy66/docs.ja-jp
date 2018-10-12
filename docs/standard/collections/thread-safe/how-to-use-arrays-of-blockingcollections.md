---
title: '方法: パイプラインでブロッキング コレクションの配列を使用する'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- thread-safe collections, blocking collections in pipeline
ms.assetid: a39c7ec3-3ad7-4f4d-8fe4-b3e9dbabe2ed
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2e2e312668a7cf4fe39596ae018adaf62cd850e4
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2018
ms.locfileid: "44187547"
---
# <a name="how-to-use-arrays-of-blocking-collections-in-a-pipeline"></a>方法: パイプラインでブロッキング コレクションの配列を使用する
次の例は、<xref:System.Collections.Concurrent.BlockingCollection%601.TryAddToAny%2A> や <xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny%2A> などの静的メソッドで <xref:System.Collections.Concurrent.BlockingCollection%601?displayProperty=nameWithType> オブジェクトの配列を使用し、コンポーネント間の高速で柔軟なデータ転送を実装する方法を示しています。  
  
## <a name="example"></a>例  
 次の例では、各オブジェクトが同時にデータを入力コレクションから取得し、変換して、出力コレクションに渡す、基本的なパイプラインの実装を示します。  
  
 [!code-csharp[CDS_BlockingCollection#07](../../../../samples/snippets/csharp/VS_Snippets_Misc/cds_blockingcollection/cs/example07.cs#07)]
 [!code-vb[CDS_BlockingCollection#07](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/cds_blockingcollection/vb/bcpipeline.vb#07)]  
  
## <a name="see-also"></a>関連項目

- <xref:System.Collections.Concurrent?displayProperty=nameWithType>  
- [スレッドセーフなコレクション](../../../../docs/standard/collections/thread-safe/index.md)
