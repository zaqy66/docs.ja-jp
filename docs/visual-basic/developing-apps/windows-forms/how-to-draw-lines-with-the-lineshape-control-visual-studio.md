---
title: '方法: LineShape コントロール (Visual Studio) を使用して線を描画します。'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- LineShape control [Visual Basic]
- lines, drawing
ms.assetid: 83e71b4e-aa76-4f9b-b547-8704309fd1e5
ms.openlocfilehash: 46360c01dfaf2c6fe199725a9ecfba2248c72d6d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54596229"
---
# <a name="how-to-draw-lines-with-the-lineshape-control-visual-studio"></a>方法: LineShape コントロール (Visual Studio) を使用して線を描画します。
使用することができます、<xref:Microsoft.VisualBasic.PowerPacks.LineShape>デザイン時と実行時の両方に、フォームまたはコンテナー、水平、垂直、または対角線方向の線を描画するコントロール。  
  
 **注**コンピューター可能性がありますさまざまな名前や場所が一部の Visual Studio のユーザー インターフェイス要素、次の手順でします。 これらの要素は、使用している Visual Studio のエディションや独自の設定によって決まります。 詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。  
  
### <a name="to-draw-a-line-at-design-time"></a>デザイン時に線を描画するには  
  
1.  ドラッグ、<xref:Microsoft.VisualBasic.PowerPacks.LineShape>コントロールから、 **Visual Basic powerpacks**  タブで、**ツールボックス**をフォームまたはコンテナー コントロールにドラッグします。  
  
2.  サイズをドラッグし、サイズし、位置の行へのハンドルを移動します。  
  
     サイズを変更し、変更することで、行を配置することもできます、 `X1`、 `X2`、 `Y1`、および`Y2`プロパティで、**プロパティ**ウィンドウ。  
  
3.  **プロパティ**ウィンドウで、必要に応じて設定追加のプロパティなど`BorderStyle`または`BorderColor`行の外観を変更します。  
  
### <a name="to-draw-a-line-at-run-time"></a>実行時に線を描画するには  
  
1.  **[プロジェクト]** メニューの **[参照の追加]** をクリックします。  
  
2.  **参照の追加**ダイアログ ボックスで、 **[microsoft.visualbasic.powerpacks.vs]**、順にクリックします**OK**します。  
  
3.  **コード エディター**、追加、`Imports`または`using`モジュールの上部にあるステートメント。  
  
```vb  
Imports Microsoft.VisualBasic.PowerPacks  
```  
  
```csharp  
using Microsoft.VisualBasic.PowerPacks;  
```  
  
4.  `Event` プロシージャに次のコードを追加します。  
  
     [!code-csharp[VbPowerPacksLine#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-draw-lines-with-the-lineshape-control-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksLine#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-draw-lines-with-the-lineshape-control-visual-studio_1.vb)]  
  
## <a name="see-also"></a>関連項目
- <xref:Microsoft.VisualBasic.PowerPacks.LineShape>
- [ライン コントロールとシェイプ コントロールの概要](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-line-and-shape-controls-visual-studio.md)
- [方法: 図形、OvalShape コントロールおよび RectangleShape コントロールを描く](../../../visual-basic/developing-apps/windows-forms/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls.md)
