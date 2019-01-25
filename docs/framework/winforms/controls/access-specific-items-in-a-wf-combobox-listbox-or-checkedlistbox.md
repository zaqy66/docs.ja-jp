---
title: '方法: 特定のアクセス フォーム ComboBox、ListBox、または CheckedListBox コントロールの項目を Windows'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ComboBox control [Windows Forms], accessing items
- ListBox control [Windows Forms], returning item information
- list boxes [Windows Forms], accessing items
- ListBox control [Windows Forms], accessing items
- combo boxes [Windows Forms], accessing items
- CheckedListBox control [Windows Forms], accessing items
ms.assetid: 1216742f-bcf9-4ff8-8a62-d7c9053c2b96
ms.openlocfilehash: b6478c24550f9f32ea75899521f7aa610ef12955
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54656701"
---
# <a name="how-to-access-specific-items-in-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a><span data-ttu-id="80bc2-102">方法: 特定のアクセス フォーム ComboBox、ListBox、または CheckedListBox コントロールの項目を Windows</span><span class="sxs-lookup"><span data-stu-id="80bc2-102">How to: Access Specific Items in a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>
<span data-ttu-id="80bc2-103">Windows フォームのコンボ ボックス、リスト ボックスで、またはチェックされたリスト ボックス内の特定の項目へのアクセスは、重要なタスクです。</span><span class="sxs-lookup"><span data-stu-id="80bc2-103">Accessing specific items in a Windows Forms combo box, list box, or checked list box is an essential task.</span></span> <span data-ttu-id="80bc2-104">一覧は、所定の位置にある項目をプログラムで判定できます。</span><span class="sxs-lookup"><span data-stu-id="80bc2-104">It enables you to programmatically determine what is in a list, at any given position.</span></span>  
  
### <a name="to-access-a-specific-item"></a><span data-ttu-id="80bc2-105">特定のアイテムにアクセスするには</span><span class="sxs-lookup"><span data-stu-id="80bc2-105">To access a specific item</span></span>  
  
1.  <span data-ttu-id="80bc2-106">クエリ、`Items`特定の項目のインデックスを使用してコレクション。</span><span class="sxs-lookup"><span data-stu-id="80bc2-106">Query the `Items` collection using the index of the specific item:</span></span>  
  
    ```vb  
    Private Function GetItemText(i As Integer) As String  
       ' Return the text of the item using the index:  
       Return ComboBox1.Items(i).ToString  
    End Function  
    ```  
  
    ```csharp  
    private string GetItemText(int i)  
    {  
       // Return the text of the item using the index:  
       return (comboBox1.Items[i].ToString());  
    }  
    ```  
  
    ```cpp  
    private:  
       String^ GetItemText(int i)  
       {  
          // Return the text of the item using the index:  
          return (comboBox1->Items->Item[i]->ToString());  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="80bc2-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="80bc2-107">See also</span></span>
- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.ListBox>
- <xref:System.Windows.Forms.CheckedListBox>
- [<span data-ttu-id="80bc2-108">オプションのリストを表示するための Windows フォーム コントロール</span><span class="sxs-lookup"><span data-stu-id="80bc2-108">Windows Forms Controls Used to List Options</span></span>](../../../../docs/framework/winforms/controls/windows-forms-controls-used-to-list-options.md)
