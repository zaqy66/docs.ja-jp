---
title: '方法: 追加して、Windows フォーム TreeView コントロールでノードを削除'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- examples [Windows Forms], TreeView control
- TreeView control [Windows Forms], removing nodes
- tree nodes in TreeView control
- TreeView control [Windows Forms], adding nodes
ms.assetid: de1b82db-4905-449a-9f59-af271a6b6673
ms.openlocfilehash: 30dbe55711d92ea1fdbbbfd147a65b27d0dc9a50
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54711506"
---
# <a name="how-to-add-and-remove-nodes-with-the-windows-forms-treeview-control"></a>方法: 追加して、Windows フォーム TreeView コントロールでノードを削除
Windows フォーム<xref:System.Windows.Forms.TreeView>コントロール内の最上位ノードを保存します。 その<xref:System.Windows.Forms.TreeView.Nodes%2A>コレクション。 各<xref:System.Windows.Forms.TreeNode>独自もが<xref:System.Windows.Forms.TreeNode.Nodes%2A>その子ノードを格納するコレクション。 両方のコレクション プロパティは型<xref:System.Windows.Forms.TreeNodeCollection>、高を追加するための標準的なコレクションのメンバーを削除して、ノード階層の 1 つのレベルにあるノードの再配置します。  
  
### <a name="to-add-nodes-programmatically"></a>プログラムでノードを追加するには  
  
1.  使用して、<xref:System.Windows.Forms.TreeNodeCollection.Add%2A>のツリー ビューのメソッド<xref:System.Windows.Forms.TreeView.Nodes%2A>プロパティ。  
  
    ```vb  
    ' Adds new node as a child node of the currently selected node.  
    Dim newNode As TreeNode = New TreeNode("Text for new node")  
    TreeView1.SelectedNode.Nodes.Add(newNode)  
    ```  
  
    ```csharp  
    // Adds new node as a child node of the currently selected node.  
    TreeNode newNode = new TreeNode("Text for new node");  
    treeView1.SelectedNode.Nodes.Add(newNode);  
    ```  
  
    ```cpp  
    // Adds new node as a child node of the currently selected node.  
    TreeNode ^ newNode = new TreeNode("Text for new node");  
    treeView1->SelectedNode->Nodes->Add(newNode);  
    ```  
  
### <a name="to-remove-nodes-programmatically"></a>プログラムでノードを削除するには  
  
1.  使用して、<xref:System.Windows.Forms.TreeNodeCollection.Remove%2A>のツリー ビューのメソッド<xref:System.Windows.Forms.TreeView.Nodes%2A>1 つのノードを削除するプロパティまたは<xref:System.Windows.Forms.TreeNodeCollection.Clear%2A>メソッドをすべてのノードをオフにします。  
  
    ```vb  
    ' Removes currently selected node, or root if nothing is selected.  
    TreeView1.Nodes.Remove(TreeView1.SelectedNode)  
    ' Clears all nodes.  
    TreeView1.Nodes.Clear()  
    ```  
  
    ```csharp  
    // Removes currently selected node, or root if nothing   
    // is selected.  
    treeView1.Nodes.Remove(treeView1.SelectedNode);  
    // Clears all nodes.  
    TreeView1.Nodes.Clear();  
    ```  
  
    ```cpp  
    // Removes currently selected node, or root if nothing  
    // is selected.  
    treeView1->Nodes->Remove(treeView1->SelectedNode);  
    // Clears all nodes.  
    treeView1->Nodes->Clear();  
    ```  
  
## <a name="see-also"></a>関連項目
- [TreeView コントロール](../../../../docs/framework/winforms/controls/treeview-control-windows-forms.md)
- [TreeView コントロールの概要](../../../../docs/framework/winforms/controls/treeview-control-overview-windows-forms.md)
- [方法: Windows フォーム TreeView コントロールのアイコンを設定します。](../../../../docs/framework/winforms/controls/how-to-set-icons-for-the-windows-forms-treeview-control.md)
- [方法: Windows フォーム TreeView コントロールのすべてのノードを反復処理します。](../../../../docs/framework/winforms/controls/how-to-iterate-through-all-nodes-of-a-windows-forms-treeview-control.md)
- [方法: クリックしてされた TreeView ノードを決定します。](../../../../docs/framework/winforms/controls/how-to-determine-which-treeview-node-was-clicked-windows-forms.md)
- [方法: TreeView コントロールまたは ListView コントロール (Windows フォーム) にカスタム情報を追加します。](../../../../docs/framework/winforms/controls/add-custom-information-to-a-treeview-or-listview-control-wf.md)
