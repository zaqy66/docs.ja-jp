---
title: '方法 : ToolStripContentPanel にコントロールを追加する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStripContentPanel [Windows Forms], adding controls
ms.assetid: fa410960-bf1a-42fc-80e8-f2e27fb3dbb8
ms.openlocfilehash: fc907eb078044ae06e0da19e38a4bbff28192346
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43395465"
---
# <a name="how-to-add-a-control-to-a-toolstripcontentpanel"></a>方法 : ToolStripContentPanel にコントロールを追加する
<xref:System.Windows.Forms.ToolStripContentPanel> に対して、1 つまたは複数のコントロールをプログラムで追加できます。  
  
## <a name="example"></a>例  
 次のコード例は、<xref:System.Windows.Forms.RichTextBox> を <xref:System.Windows.Forms.ToolStripContentPanel> に追加する方法を示しています。  
  
 [!code-csharp[System.Windows.Forms.ToolStripContainer#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStripContainer/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStripContainer#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStripContainer/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 このコード例で必要な要素は次のとおりです。  
  
-   System、System.Data、および System.Windows.Forms の各アセンブリへの参照。  
  
 コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。 新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。  また、「[方法: 完成した Windows フォーム コードの例を Visual Studio を使ってコンパイルして実行する](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))」または「[[ToolStripContainer タスク] ダイアログ ボックス](https://msdn.microsoft.com/library/ms233647\(v=vs.110\))」も参照してください。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Windows.Forms.ToolStripContentPanel>  
 <xref:System.Windows.Forms.ToolStripContainer>  
 [ToolStripContainer コントロール](../../../../docs/framework/winforms/controls/toolstripcontainer-control.md)  
 [ToolStrip コントロール](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
