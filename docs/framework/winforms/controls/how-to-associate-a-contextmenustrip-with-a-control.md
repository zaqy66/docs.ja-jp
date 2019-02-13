---
title: '方法: ContextMenuStrip をコントロールに関連付ける'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- context menus [Windows Forms], relating
- ContextMenuStrips [Windows Forms], associating with controls
- context menus [Windows Forms], associating with controls
- ContextMenuStrips [Windows Forms], relating
ms.assetid: 6fc40a42-5d69-427f-aa30-0a146193226b
ms.openlocfilehash: 979245291a03b07b7bad548193737c0577b5c107
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56221122"
---
# <a name="how-to-associate-a-contextmenustrip-with-a-control"></a>方法: ContextMenuStrip をコントロールに関連付ける
コントロールとショートカット メニューを作成した後、次の手順を使用することによって、ユーザーがコントロールを右クリックした時点で特定のショートカット メニューを表示します。 これらの手順は、<xref:System.Windows.Forms.ContextMenuStrip> を Windows フォームと <xref:System.Windows.Forms.ToolStrip> コントロールに関連付けます。  
  
### <a name="to-associate-a-contextmenustrip-with-a-windows-form"></a>ContextMenuStrip を Windows フォームに関連付けるには  
  
1.  <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> プロパティを関連付けられている <xref:System.Windows.Forms.ContextMenuStrip> の名前に設定します。  
  
### <a name="to-associate-a-contextmenustrip-with-a-toolstrip-control"></a>ContextMenuStrip を ToolStrip コントロールに関連付けるには  
  
1.  コントロールの <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> プロパティを関連付けられている <xref:System.Windows.Forms.ContextMenuStrip> の名前に設定します。  
  
## <a name="example"></a>例  
 次のコード例では、Windows フォームと <xref:System.Windows.Forms.ToolStrip> を作成して、別の <xref:System.Windows.Forms.ContextMenuStrip> コントロールをそれぞれに関連付けています。  
  
 [!code-csharp[System.Windows.Forms.ContextMenuStrip#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ContextMenuStrip/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ContextMenuStrip#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ContextMenuStrip/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 この例で必要な要素は次のとおりです。  
  
-   System、System.Data、System.Drawing、および System.Windows.Forms の各アセンブリへの参照。  
  
 コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。 新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.Windows.Forms.Control.ContextMenuStrip%2A>
- <xref:System.Windows.Forms.ToolStrip>
- [方法: メニュー項目を ContextMenuStrip に追加します。](../../../../docs/framework/winforms/controls/how-to-add-menu-items-to-a-contextmenustrip.md)
- [ContextMenuStrip コントロール](../../../../docs/framework/winforms/controls/contextmenustrip-control.md)
