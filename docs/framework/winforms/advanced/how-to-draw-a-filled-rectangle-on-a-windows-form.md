---
title: '方法: Windows フォームに塗りつぶした四角形を描画します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- Graphics.FillRectangle
helpviewer_keywords:
- drawing [Windows Forms], rectangles
- rectangles [Windows Forms], drawing
- drawing rectangles
ms.assetid: d656a93c-987d-4809-aafd-493fe17450f0
ms.openlocfilehash: a9722b2939e77282453743a4dea165a340412a21
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587035"
---
# <a name="how-to-draw-a-filled-rectangle-on-a-windows-form"></a>方法: Windows フォームに塗りつぶした四角形を描画します。
この例では、フォームに塗りつぶした四角形を描画します。  
  
## <a name="example"></a>例  
 [!code-cpp[System.Drawing.ConceptualHowTos#2](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#2)]
 [!code-csharp[System.Drawing.ConceptualHowTos#2](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#2)]
 [!code-vb[System.Drawing.ConceptualHowTos#2](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#2)]  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 このメソッドを呼び出すことはできません、<xref:System.Windows.Forms.Form.Load>イベント ハンドラー。 フォームのサイズを変更または別の形式によって隠されている場合、描画のコンテンツを再描画されませんされます。 コンテンツを自動的に再描画するために、オーバーライドする必要があります、<xref:System.Windows.Forms.Control.OnPaint%2A>メソッド。  
  
## <a name="robust-programming"></a>信頼性の高いプログラミング  
 常に呼び出す必要があります<xref:System.IDisposable.Dispose%2A>などのシステム リソースを消費するすべてのオブジェクトに対する<xref:System.Drawing.Brush>と<xref:System.Drawing.Graphics>オブジェクト。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Drawing.Graphics.FillRectangle%2A>
- <xref:System.Windows.Forms.Control.OnPaint%2A>
- [グラフィックス プログラミングについて](../../../../docs/framework/winforms/advanced/getting-started-with-graphics-programming.md)
- [Windows フォームにおけるグラフィックスと描画](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)
- [ペンを使用した直線と図形の描画](../../../../docs/framework/winforms/advanced/using-a-pen-to-draw-lines-and-shapes.md)
- [GDI+ でのブラシと塗りつぶされた図形](../../../../docs/framework/winforms/advanced/brushes-and-filled-shapes-in-gdi.md)
