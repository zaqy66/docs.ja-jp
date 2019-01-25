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
# <a name="how-to-add-and-remove-nodes-with-the-windows-forms-treeview-control"></a><span data-ttu-id="653d8-102">方法: 追加して、Windows フォーム TreeView コントロールでノードを削除</span><span class="sxs-lookup"><span data-stu-id="653d8-102">How to: Add and Remove Nodes with the Windows Forms TreeView Control</span></span>
<span data-ttu-id="653d8-103">Windows フォーム<xref:System.Windows.Forms.TreeView>コントロール内の最上位ノードを保存します。 その<xref:System.Windows.Forms.TreeView.Nodes%2A>コレクション。</span><span class="sxs-lookup"><span data-stu-id="653d8-103">The Windows Forms <xref:System.Windows.Forms.TreeView> control stores the top-level nodes in its <xref:System.Windows.Forms.TreeView.Nodes%2A> collection.</span></span> <span data-ttu-id="653d8-104">各<xref:System.Windows.Forms.TreeNode>独自もが<xref:System.Windows.Forms.TreeNode.Nodes%2A>その子ノードを格納するコレクション。</span><span class="sxs-lookup"><span data-stu-id="653d8-104">Each <xref:System.Windows.Forms.TreeNode> also has its own <xref:System.Windows.Forms.TreeNode.Nodes%2A> collection to store its child nodes.</span></span> <span data-ttu-id="653d8-105">両方のコレクション プロパティは型<xref:System.Windows.Forms.TreeNodeCollection>、高を追加するための標準的なコレクションのメンバーを削除して、ノード階層の 1 つのレベルにあるノードの再配置します。</span><span class="sxs-lookup"><span data-stu-id="653d8-105">Both collection properties are of type <xref:System.Windows.Forms.TreeNodeCollection>, which provides standard collection members that enable you to add, remove, and rearrange the nodes at a single level of the node hierarchy.</span></span>  
  
### <a name="to-add-nodes-programmatically"></a><span data-ttu-id="653d8-106">プログラムでノードを追加するには</span><span class="sxs-lookup"><span data-stu-id="653d8-106">To add nodes programmatically</span></span>  
  
1.  <span data-ttu-id="653d8-107">使用して、<xref:System.Windows.Forms.TreeNodeCollection.Add%2A>のツリー ビューのメソッド<xref:System.Windows.Forms.TreeView.Nodes%2A>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="653d8-107">Use the <xref:System.Windows.Forms.TreeNodeCollection.Add%2A> method of the tree view's <xref:System.Windows.Forms.TreeView.Nodes%2A> property.</span></span>  
  
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
  
### <a name="to-remove-nodes-programmatically"></a><span data-ttu-id="653d8-108">プログラムでノードを削除するには</span><span class="sxs-lookup"><span data-stu-id="653d8-108">To remove nodes programmatically</span></span>  
  
1.  <span data-ttu-id="653d8-109">使用して、<xref:System.Windows.Forms.TreeNodeCollection.Remove%2A>のツリー ビューのメソッド<xref:System.Windows.Forms.TreeView.Nodes%2A>1 つのノードを削除するプロパティまたは<xref:System.Windows.Forms.TreeNodeCollection.Clear%2A>メソッドをすべてのノードをオフにします。</span><span class="sxs-lookup"><span data-stu-id="653d8-109">Use the <xref:System.Windows.Forms.TreeNodeCollection.Remove%2A> method of the tree view's <xref:System.Windows.Forms.TreeView.Nodes%2A> property to remove a single node, or the <xref:System.Windows.Forms.TreeNodeCollection.Clear%2A> method to clear all nodes.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="653d8-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="653d8-110">See also</span></span>
- [<span data-ttu-id="653d8-111">TreeView コントロール</span><span class="sxs-lookup"><span data-stu-id="653d8-111">TreeView Control</span></span>](../../../../docs/framework/winforms/controls/treeview-control-windows-forms.md)
- [<span data-ttu-id="653d8-112">TreeView コントロールの概要</span><span class="sxs-lookup"><span data-stu-id="653d8-112">TreeView Control Overview</span></span>](../../../../docs/framework/winforms/controls/treeview-control-overview-windows-forms.md)
- [<span data-ttu-id="653d8-113">方法: Windows フォーム TreeView コントロールのアイコンを設定します。</span><span class="sxs-lookup"><span data-stu-id="653d8-113">How to: Set Icons for the Windows Forms TreeView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-set-icons-for-the-windows-forms-treeview-control.md)
- [<span data-ttu-id="653d8-114">方法: Windows フォーム TreeView コントロールのすべてのノードを反復処理します。</span><span class="sxs-lookup"><span data-stu-id="653d8-114">How to: Iterate Through All Nodes of a Windows Forms TreeView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-iterate-through-all-nodes-of-a-windows-forms-treeview-control.md)
- [<span data-ttu-id="653d8-115">方法: クリックしてされた TreeView ノードを決定します。</span><span class="sxs-lookup"><span data-stu-id="653d8-115">How to: Determine Which TreeView Node Was Clicked</span></span>](../../../../docs/framework/winforms/controls/how-to-determine-which-treeview-node-was-clicked-windows-forms.md)
- [<span data-ttu-id="653d8-116">方法: TreeView コントロールまたは ListView コントロール (Windows フォーム) にカスタム情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="653d8-116">How to: Add Custom Information to a TreeView or ListView Control (Windows Forms)</span></span>](../../../../docs/framework/winforms/controls/add-custom-information-to-a-treeview-or-listview-control-wf.md)
