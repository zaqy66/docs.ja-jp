---
title: '方法: ハッチ パターンで図形を塗りつぶす'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- patterns [Windows Forms], adding to shapes
- shapes [Windows Forms], filling with patterns
- brushes [Windows Forms], using hatch brushes
ms.assetid: 9c8300ff-187b-404f-af1f-ebd499f5b16f
ms.openlocfilehash: 3fb5b443aac710a5490a238e2a571ed899dec463
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54512395"
---
# <a name="how-to-fill-a-shape-with-a-hatch-pattern"></a>方法: ハッチ パターンで図形を塗りつぶす
2 つの色からハッチ パターンが行われます。 バック グラウンドとバック グラウンドでパターンを形成する行のいずれかのいずれか。 ハッチ パターンでは、閉じた図形を塗りつぶすを使用して、<xref:System.Drawing.Drawing2D.HatchBrush>オブジェクト。 次の例では、ハッチ パターンで楕円の塗りつぶし方法を示します。  
  
## <a name="example"></a>例  
 <xref:System.Drawing.Drawing2D.HatchBrush.%23ctor%2A>コンス トラクターは 3 つの引数を受け取ります。 陰影のスタイル、ハッチ線の色および背景の色。 陰影のスタイル引数は、任意の値を指定できます、<xref:System.Drawing.Drawing2D.HatchStyle>列挙体。 50 人を超える要素がある、<xref:System.Drawing.Drawing2D.HatchStyle>列挙体。 いくつかの要素の次のリストに表示されます。  
  
-   <xref:System.Drawing.Drawing2D.HatchStyle.Horizontal>  
  
-   <xref:System.Drawing.Drawing2D.HatchStyle.Vertical>  
  
-   <xref:System.Drawing.Drawing2D.HatchStyle.ForwardDiagonal>  
  
-   <xref:System.Drawing.Drawing2D.HatchStyle.BackwardDiagonal>  
  
-   <xref:System.Drawing.Drawing2D.HatchStyle.Cross>  
  
-   <xref:System.Drawing.Drawing2D.HatchStyle.DiagonalCross>  
  
 次の図は、塗りつぶされた楕円を示します。  
  
 ![ハッチ パターン](../../../../docs/framework/winforms/advanced/media/hatch1.png "hatch1")  
  
 [!code-csharp[System.Drawing.UsingABrush#41](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.UsingABrush#41](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 前の例は、Windows フォームで使用するために設計されていて、<xref:System.Windows.Forms.PaintEventArgs> イベント ハンドラーのパラメーターである `e`<xref:System.Windows.Forms.Control.Paint> を必要とします。  
  
## <a name="see-also"></a>関連項目
- [ブラシを使用した図形の塗りつぶし](../../../../docs/framework/winforms/advanced/using-a-brush-to-fill-shapes.md)
