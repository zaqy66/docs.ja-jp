---
title: '方法: バッファリングされたグラフィックスを手動で管理します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flicker [Windows Forms], reducing by manually managing graphics
- graphics [Windows Forms], managing buffered
ms.assetid: 4c2a90ee-bbbe-4ff6-9170-1b06c195c918
ms.openlocfilehash: b27a013d2cf66fb12365bffc35a07ed32bc25a2e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54554492"
---
# <a name="how-to-manually-manage-buffered-graphics"></a>方法: バッファリングされたグラフィックスを手動で管理します。
高度なダブル バッファリングのシナリオで使用することができます、[!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)]ダブル バッファリング ロジックを実装するクラス。 割り当てと管理、個々 のグラフィックス バッファーを担当するクラスは、<xref:System.Drawing.BufferedGraphicsContext>クラス。 すべてのアプリケーションが独自の既定<xref:System.Drawing.BufferedGraphicsContext>ダブル バッファリングをそのアプリケーション用の既定のすべてを管理します。 このインスタンスへの参照を取得するには呼び出すことによって、<xref:System.Drawing.BufferedGraphicsManager.Current%2A>します。  
  
### <a name="to-obtain-a-reference-to-the-default-bufferedgraphicscontext"></a>既定 BufferedGraphicsContext への参照を取得するには  
  
-   設定、<xref:System.Drawing.BufferedGraphicsManager.Current%2A>プロパティは、次のコード例に示すようにします。  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#11)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#11)]  
  
    > [!NOTE]
    >  呼び出す必要はありません、`Dispose`メソッドを<xref:System.Drawing.BufferedGraphicsContext>から受信する参照、<xref:System.Drawing.BufferedGraphicsManager>クラス。 <xref:System.Drawing.BufferedGraphicsManager>すべてのメモリの割り当てと既定の配布処理<xref:System.Drawing.BufferedGraphicsContext>インスタンス。  
  
     アニメーションなどの画像を多用するアプリケーションは、場合によってパフォーマンスを向上できます専用を使用して<xref:System.Drawing.BufferedGraphicsContext>の代わりに、<xref:System.Drawing.BufferedGraphicsContext>によって提供される、<xref:System.Drawing.BufferedGraphicsManager>します。 これにより、作成してグラフィックス バッファーをすべて、その他のバッファリングされたグラフィックス管理、アプリケーションに関連付けられているアプリケーションによって消費されるメモリが大きい場合のパフォーマンスのオーバーヘッドを発生させずに、個別に管理できます。  
  
### <a name="to-create-a-dedicated-bufferedgraphicscontext"></a>専用 BufferedGraphicsContext を作成するには  
  
-   宣言しの新しいインスタンスを作成、<xref:System.Drawing.BufferedGraphicsContext>クラスに、次のコード例に示すようにします。  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#12](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#12)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#12](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#12)]  
  
## <a name="see-also"></a>関連項目
- <xref:System.Drawing.BufferedGraphicsContext>
- [ダブル バッファリングされたグラフィックス](../../../../docs/framework/winforms/advanced/double-buffered-graphics.md)
- [方法: バッファリングされたグラフィックスを手動で描画します。](../../../../docs/framework/winforms/advanced/how-to-manually-render-buffered-graphics.md)
