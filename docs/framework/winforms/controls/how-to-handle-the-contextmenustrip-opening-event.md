---
title: '方法: ContextMenuStrip のオープン イベントを処理します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ContextMenuStrip control [Windows Forms]
- context menus [Windows Forms], event handling
- ToolStrip control [Windows Forms]
- event handling [Windows Forms], context menus
- shortcut menus [Windows Forms], event handling
ms.assetid: b661b3dd-7815-4cc2-a1aa-a9a391ab3427
ms.openlocfilehash: fe4c8fc3d2446b09add7336fa11670ff9ca8fed2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54532114"
---
# <a name="how-to-handle-the-contextmenustrip-opening-event"></a>方法: ContextMenuStrip のオープン イベントを処理します。
動作をカスタマイズすることができます、<xref:System.Windows.Forms.ContextMenuStrip>コントロールを処理することによって、<xref:System.Windows.Forms.ToolStripDropDown.Opening>イベント。  
  
## <a name="example"></a>例  
 次のコード例は、処理する方法を示します、<xref:System.Windows.Forms.ToolStripDropDown.Opening>イベント。 イベント ハンドラーを動的に項目を追加、<xref:System.Windows.Forms.ContextMenuStrip>コントロール。 完全なコード例では、次を参照してください。[方法。ToolStrip の項目を動的に追加](../../../../docs/framework/winforms/controls/how-to-add-toolstrip-items-dynamically.md)します。  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#42](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#42)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#42](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#42)]  
  
 設定、<xref:System.ComponentModel.CancelEventArgs.Cancel%2A?displayProperty=nameWithType>プロパティを`true`メニューを開かないようにします。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.ComponentModel.CancelEventArgs.Cancel%2A>
- <xref:System.Windows.Forms.ToolStripDropDown>
- [ToolStrip コントロール](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
