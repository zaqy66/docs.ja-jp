---
title: '方法: ToolBar のコントロールのスタイルを設定する'
ms.date: 03/30/2017
helpviewer_keywords:
- styling controls on toolbar [WPF]
- toolbars [WPF]
- customizing controls on toolbar [WPF]
ms.assetid: ba6ae056-d6a9-4c24-90f8-467ab0bc0b1a
ms.openlocfilehash: 097bb23a41ba68bf9c121a53920f19694508348b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54544862"
---
# <a name="how-to-style-controls-on-a-toolbar"></a>方法: ToolBar のコントロールのスタイルを設定する
<xref:System.Windows.Controls.ToolBar>定義<xref:System.Windows.ResourceKey>内のコントロールのスタイルを指定するオブジェクト、<xref:System.Windows.Controls.ToolBar>します。  内のコントロールのスタイルを設定する、 <xref:System.Windows.Controls.ToolBar>、設定、`x:key`するスタイルの属性を<xref:System.Windows.ResourceKey>で定義されている<xref:System.Windows.Controls.ToolBar>します。  
  
 <xref:System.Windows.Controls.ToolBar> 、次の定義<xref:System.Windows.ResourceKey>オブジェクト。  
  
-   <xref:System.Windows.Controls.ToolBar.ButtonStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.CheckBoxStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.ComboBoxStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.MenuStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.RadioButtonStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.SeparatorStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.TextBoxStyleKey%2A>  
  
-   <xref:System.Windows.Controls.ToolBar.ToggleButtonStyleKey%2A>  
  
## <a name="example"></a>例  
 次の例では、内のコントロールのスタイルを定義する、<xref:System.Windows.Controls.ToolBar>します。  
  
 [!code-xaml[ToolBar_snip#ToolBarAllStyles](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ToolBar_snip/CS/pane1.xaml#toolbarallstyles)]  
[!code-xaml[ToolBar_snip#ToolBar](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ToolBar_snip/CS/pane1.xaml#toolbar)]  
  
## <a name="see-also"></a>関連項目
- [スタイルとテンプレート](../../../../docs/framework/wpf/controls/styling-and-templating.md)
