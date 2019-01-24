---
title: ライン コントロールとシェイプ コントロールの概要 (Visual Studio)
ms.date: 07/20/2015
helpviewer_keywords:
- Line control [Visual Basic], overview
- Shape control [Visual Basic], overview
- lines, drawing
- shapes, drawing
ms.assetid: 5c4e8b1a-0733-4020-af6c-f582f4026728
ms.openlocfilehash: 3623c2363f39150fd4bb202ba61ebd51df383ca8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54699923"
---
# <a name="introduction-to-the-line-and-shape-controls-visual-studio"></a>ライン コントロールとシェイプ コントロールの概要 (Visual Studio)
Visual Basic Power Packs のラインと形状のコントロールとは、一連のフォームおよびコンテナーに直線と図形を描画するための 3 つのグラフィカル コントロールです。 <xref:Microsoft.VisualBasic.PowerPacks.LineShape>水平、垂直方向、および斜めの線を描画するコントロールを使用します。 <xref:Microsoft.VisualBasic.PowerPacks.OvalShape>円と、楕円を描画するためにコントロールを使用し、<xref:Microsoft.VisualBasic.PowerPacks.RectangleShape>四角形と四角形を描画するためにコントロールを使用します。  
  
## <a name="line-and-shape-controls"></a>ライン コントロールとシェイプ コントロール  
 行および形状のコントロールに含まれているグラフィックス メソッドの多くをカプセル化する、<xref:System.Drawing>名前空間。 これにより、グラフィック オブジェクト、ペン、およびブラシを作成することがなく、1 つの手順で線や図形を描画できます。 グラデーション塗りつぶしなどの複雑なグラフィック技法は、いくつかのプロパティを設定するだけで実現できます。  
  
 グラフィックス メソッドを使用して直線と図形を描画することは、行および形状のコントロールを使用するいくつかの利点があります。  
  
-   グラフィックス メソッドは、実行時にのみ呼び出すことができます。 デザイン時に、行および形状のコントロールをフォームに追加できます。 これにより、外観を確認し、; に正確に配置するには実行時に追加することもできます。  
  
-   行および形状のコントロールが選択可能な実行時に、イベントを提供するよう<xref:Microsoft.VisualBasic.PowerPacks.Shape.Click>と<xref:Microsoft.VisualBasic.PowerPacks.Shape.OnDoubleClick%2A>します。 グラフィックス メソッドの出力では、選択可能でないし、イベントを提供しません。  
  
-   行および形状のコントロールを提供<xref:Microsoft.VisualBasic.PowerPacks.Shape.BringToFront%2A>と<xref:Microsoft.VisualBasic.PowerPacks.Shape.SendToBack%2A>をデザイン時および実行時に、z オーダーを制御できるようにするメソッド。 グラフィックス メソッドの z オーダーは、実行時に実行の順序を変更することでのみ制御できます。  
  
-   行および形状のコントロールは、ウィンドウなしのコントロールウィンドウ ハンドルが表示されていない、システム リソースが使用して、そのためです。  
  
### <a name="object-model"></a>オブジェクト モデル  
 行および形状のコントロールは、ベースから派生<xref:Microsoft.VisualBasic.PowerPacks.Shape>共有のプロパティ、メソッド、およびイベントを定義するクラス。  
  
 次の図は、Line および Shape オブジェクト階層を示します。  
  
 ![Line および Shape オブジェクト階層のダイアグラム](../../../visual-basic/developing-apps/windows-forms/media/lineshapeobject.png "LineShapeObject")  
Line および Shape オブジェクト階層  
  
 派生した<xref:Microsoft.VisualBasic.PowerPacks.LineShape>クラスには、プロパティ、メソッド、および行に固有のイベントが含まれています。 派生した<xref:Microsoft.VisualBasic.PowerPacks.SimpleShape>クラスの基本クラスは、<xref:Microsoft.VisualBasic.PowerPacks.OvalShape>と<xref:Microsoft.VisualBasic.PowerPacks.RectangleShape>; プロパティ、メソッド、およびすべての図形に共通のイベントが含まれています。 派生することもできます。<xref:Microsoft.VisualBasic.PowerPacks.SimpleShape>独自に作成する`Shape`コントロール。  
  
 <xref:Microsoft.VisualBasic.PowerPacks.OvalShape>と<xref:Microsoft.VisualBasic.PowerPacks.RectangleShape>クラスは、円、楕円、四角形、および角の丸い四角形を描画するために使用できます。  
  
 行または形状のコントロールをフォームまたはコンテナーを非表示を追加するときに<xref:Microsoft.VisualBasic.PowerPacks.ShapeContainer>オブジェクトが作成されます。 <xref:Microsoft.VisualBasic.PowerPacks.ShapeContainer>各コンテナー コントロール内の図形をキャンバスとして機能します。 各<xref:Microsoft.VisualBasic.PowerPacks.ShapeContainer>対応しています<xref:Microsoft.VisualBasic.PowerPacks.ShapeCollection>行および形状のコントロールを反復処理することができます。 切り取りと貼り付けを使用して、またはドラッグ アンド ドロップして、別に 1 つのコンテナーから図形を移動できます。 最後の図形が、コンテナーから削除されると、<xref:Microsoft.VisualBasic.PowerPacks.ShapeContainer>も削除されます。  
  
> [!NOTE]
>  すべてのコンテナー コントロールでは、行および形状のコントロールをサポートします。 行または形状のコントロールをホストすることはできません、<xref:System.Windows.Forms.TableLayoutPanel>または<xref:System.Windows.Forms.FlowLayoutPanel>します。  
  
## <a name="see-also"></a>関連項目
- <xref:Microsoft.VisualBasic.PowerPacks>
- [方法: LineShape コントロールを使用して線を描画します。](../../../visual-basic/developing-apps/windows-forms/how-to-draw-lines-with-the-lineshape-control-visual-studio.md)
- [方法: 図形、OvalShape コントロールおよび RectangleShape コントロールを描く](../../../visual-basic/developing-apps/windows-forms/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls.md)
- [方法: 図形間のタブ移動を有効にします。](../../../visual-basic/developing-apps/windows-forms/how-to-enable-tabbing-between-shapes-visual-studio.md)
