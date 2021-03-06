---
title: '方法: カラー リマップ テーブルを使用して、'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- color tables [Windows Forms], remapping colors with
- custom colors [Windows Forms], creating with color remap table
- color remap tables [Windows Forms], using
ms.assetid: 977df1ce-8665-42d4-9fb1-ef7f0ff63419
ms.openlocfilehash: 06a25179a3afc004029972bbf7d4d5691d42b25b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54683912"
---
# <a name="how-to-use-a-color-remap-table"></a>方法: カラー リマップ テーブルを使用して、
カラー リマップ テーブルをに従ってイメージの色を変換するプロセスは、再マップします。 カラー リマップ テーブルの配列は、<xref:System.Drawing.Imaging.ColorMap>オブジェクト。 各<xref:System.Drawing.Imaging.ColorMap>、配列内のオブジェクトは、<xref:System.Drawing.Imaging.ColorMap.OldColor%2A>プロパティと<xref:System.Drawing.Imaging.ColorMap.NewColor%2A>プロパティ。  
  
 ときに[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)]イメージ、イメージの各ピクセルの描画は古い色の配列と比較されます。 ピクセルの色が以前の色に一致する場合、その色は、対応する新しい色に変更されます。 表示のみの色を変更、イメージ自体の色の値 (に格納されている、<xref:System.Drawing.Image>または<xref:System.Drawing.Bitmap>オブジェクト) は変更されません。  
  
 マップが変更されたイメージを描画するには、配列を初期化<xref:System.Drawing.Imaging.ColorMap>オブジェクト。 その配列を渡す、<xref:System.Drawing.Imaging.ImageAttributes.SetRemapTable%2A>のメソッド、<xref:System.Drawing.Imaging.ImageAttributes>オブジェクト、し、渡します、<xref:System.Drawing.Imaging.ImageAttributes>オブジェクトを<xref:System.Drawing.Graphics.DrawImage%2A>のメソッドを<xref:System.Drawing.Graphics>オブジェクト。  
  
## <a name="example"></a>例  
 次の例では、作成、 <xref:System.Drawing.Image> RemapInput.bmp ファイルからのオブジェクト。 コードが単一のカラー リマップ テーブルを作成します<xref:System.Drawing.Imaging.ColorMap>オブジェクト。 <xref:System.Drawing.Imaging.ColorMap.OldColor%2A>のプロパティ、`ColorRemap`オブジェクトは赤い、および<xref:System.Drawing.Imaging.ColorMap.NewColor%2A>プロパティは青です。 イメージは、描画せず、再マップと再マップが 1 回です。 再マッピング プロセスを青の赤のすべてのピクセルを変更します。  
  
 次の図は、左側の元のイメージ、右側のマップが変更されたイメージを示しています。  
  
 ![カラー リマップ](../../../../docs/framework/winforms/advanced/media/colortrans7.png "colortrans7")  
  
 [!code-csharp[System.Drawing.RecoloringImages#31](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.RecoloringImages#31](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 前の例は、Windows フォームで使用するために設計されていて、<xref:System.Windows.Forms.PaintEventArgs> イベント ハンドラーのパラメーターである `e`<xref:System.Windows.Forms.Control.Paint> を必要とします。  
  
## <a name="see-also"></a>関連項目
- [イメージの色の変更](../../../../docs/framework/winforms/advanced/recoloring-images.md)
- [イメージ、ビットマップ、メタファイル](../../../../docs/framework/winforms/advanced/images-bitmaps-and-metafiles.md)
