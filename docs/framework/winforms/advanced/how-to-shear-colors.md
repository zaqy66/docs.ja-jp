---
title: '方法: 色の傾斜'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [Windows Forms], transforming with color matrices
- colors [Windows Forms], shearing
ms.assetid: 0a424171-5b8b-45c4-afef-e9720a6c3e22
ms.openlocfilehash: bde3271398c6bc6a37c975476b76acb85511c1a4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54589833"
---
# <a name="how-to-shear-colors"></a>方法: 色の傾斜
傾斜増加またはカラー コンポーネントを別の色コンポーネントに比例した量ずつ減少します。 たとえば、赤のコンポーネントを増加して青のコンポーネントの値の半分して変換を検討してください。 このような変換では、(0.2, 0.5, 1) の色になります (0.7, 0.5, 1)。 新しいの赤のコンポーネントが 0.2 + (1/2)(1) 0.7 を = です。  
  
## <a name="example"></a>例  
 次の例では、構築、 <xref:System.Drawing.Image> ColorBars4.bmp ファイルからのオブジェクト。 コードは、イメージ内の各ピクセルに前の段落で説明されている傾斜変換を適用します。  
  
 次の図は、右側の左側に、元のイメージと傾斜のイメージを示します。  
  
 ![色を傾斜](../../../../docs/framework/winforms/advanced/media/colortrans6.png "colortrans6")  
  
 次の表は、傾斜変換の前後に 4 つのバーの色のベクターを示します。  
  
|元|傾斜|  
|--------------|-------------|  
|(0, 0, 1, 1)|(0.5, 0, 1, 1)|  
|(0.5, 1, 0.5, 1)|(0.75, 1, 0.5, 1)|  
|(1, 1, 0, 1)|(1, 1, 0, 1)|  
|(0.4, 0.4, 0.4, 1)|(0.6, 0.4, 0.4, 1)|  
  
 [!code-csharp[System.Drawing.Misc3#9](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Misc3/CS/Form1.cs#9)]
 [!code-vb[System.Drawing.Misc3#9](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Misc3/VB/Form1.vb#9)]  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 前の例は、Windows フォームで使用するために設計されていて、<xref:System.Windows.Forms.PaintEventArgs> イベント ハンドラーのパラメーターである `e`<xref:System.Windows.Forms.Control.Paint> を必要とします。 置換`ColorBars.bmp`イメージ名とパス、システムでは無効です。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [Windows フォームにおけるグラフィックスと描画](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)
- [イメージの色の変更](../../../../docs/framework/winforms/advanced/recoloring-images.md)
