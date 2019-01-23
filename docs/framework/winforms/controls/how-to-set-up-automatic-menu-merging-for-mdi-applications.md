---
title: '方法: メニューの自動マージ MDI アプリケーションを設定します。'
ms.date: 03/30/2017
helpviewer_keywords:
- MenuStrip [Windows Forms], merging
- Merging [Windows Forms], automatic menu
ms.assetid: 55e32cad-1141-4a56-aa33-d9543ca3d393
ms.openlocfilehash: 3aeaf9ee4818b6689905c10d2bd46fc887609c35
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549825"
---
# <a name="how-to-set-up-automatic-menu-merging-for-mdi-applications"></a>方法: メニューの自動マージ MDI アプリケーションを設定します。
次の手順を使用するマルチ ドキュメント インターフェイス (MDI) アプリケーションでの自動マージを設定するための基本的な手順は、<xref:System.Windows.Forms.MenuStrip>します。  
  
### <a name="to-set-up-automatic-menu-merging"></a>メニューの自動マージを設定するには  
  
1.  設定して、MDI 親フォームを作成、<xref:System.Windows.Forms.Form.IsMdiContainer%2A>プロパティを`true`します。  
  
2.  追加、 <xref:System.Windows.Forms.MenuStrip> MDI 親の設定をその<xref:System.Windows.Forms.Form.MainMenuStrip%2A>プロパティに<xref:System.Windows.Forms.MenuStrip>します。  
  
3.  MDI 子フォームを作成し、設定、<xref:System.Windows.Forms.Form.MdiParent%2A>プロパティを親フォームの名前にします。  
  
4.  追加、 <xref:System.Windows.Forms.MenuStrip> MDI 子フォーム。  
  
5.  子フォームでは、設定、<xref:System.Windows.Forms.ToolStripItem.Visible%2A>のプロパティ、<xref:System.Windows.Forms.MenuStrip>に`false`します。  
  
6.  メニュー項目に子フォームの追加<xref:System.Windows.Forms.MenuStrip>親フォームのマージする<xref:System.Windows.Forms.MenuStrip>子フォームをアクティブにするタイミング。  
  
7.  使用して、<xref:System.Windows.Forms.ToolStripItem.MergeAction%2A>プロパティ メニュー項目を子フォームの<xref:System.Windows.Forms.MenuStrip>親フォームにマージする方法を制御します。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [MenuStrip コントロールの概要](../../../../docs/framework/winforms/controls/menustrip-control-overview-windows-forms.md)
