---
title: '方法: Windows フォームでの実行時に ToolStrip 項目を並べ替えを有効にします。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], examples
- examples [Windows Forms], toolbars
- toolbars [Windows Forms], rearranging controls
- ToolStrip control [Windows Forms], reordering items
ms.assetid: 8480b69a-379f-4dc2-8dcf-365ed93692b2
ms.openlocfilehash: 0b3662a700d897607780e8d5032c498faff97753
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577020"
---
# <a name="how-to-enable-reordering-of-toolstrip-items-at-run-time-in-windows-forms"></a>方法: Windows フォームでの実行時に ToolStrip 項目を並べ替えを有効にします。
再配置するユーザーを有効にすることができます<xref:System.Windows.Forms.ToolStripItem>のコントロールに対して、<xref:System.Windows.Forms.ToolStrip>します。  
  
### <a name="to-enable-toolstripitem-rearrangement-at-run-time"></a>実行時に ToolStripItem 再配置を有効にするには  
  
-   <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A> プロパティを `true`に設定します。 既定では、<xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A>は`false`します。  
  
     ALT キーを押しながらマウスの左ボタンをドラッグする、実行時にユーザーを保持して、<xref:System.Windows.Forms.ToolStripItem>で別の場所に、<xref:System.Windows.Forms.ToolStrip>します。  
  
    ```vb  
    toolStrip1.AllowItemReorder = True  
    ```  
  
    ```csharp  
    toolStrip1.AllowItemReorder = true;  
    ```  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A>
- [ToolStrip コントロールの概要](../../../../docs/framework/winforms/controls/toolstrip-control-overview-windows-forms.md)
- [ToolStrip コントロールのアーキテクチャ](../../../../docs/framework/winforms/controls/toolstrip-control-architecture.md)
- [ToolStrip テクノロジの概要](../../../../docs/framework/winforms/controls/toolstrip-technology-summary.md)
