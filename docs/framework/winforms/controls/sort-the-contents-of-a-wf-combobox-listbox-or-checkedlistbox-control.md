---
title: '方法: Windows の内容を並べ替えるフォーム ComboBox、ListBox、または CheckedListBox コントロール'
ms.date: 03/30/2017
helpviewer_keywords:
- CheckedListBox control [Windows Forms], sorting
- ComboBox control [Windows Forms], sorting contents
- combo boxes [Windows Forms], sorting contents
- list boxes [Windows Forms], sorting contents
- ListBox control [Windows Forms], sorting contents
ms.assetid: c268e387-3d1d-4d86-a940-19f6673c8d06
ms.openlocfilehash: 97965dcef1541aec51ba57a7cf314730f892f141
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54686323"
---
# <a name="how-to-sort-the-contents-of-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a>方法: Windows の内容を並べ替えるフォーム ComboBox、ListBox、または CheckedListBox コントロール
Windows フォーム コントロールでは、データ バインドされるときに並べ替えられません。 並べ替えられたデータを表示するには、並べ替えをサポートするデータ ソースを使用して、並べ替え、データ ソース。 並べ替えをサポートするデータ ソースはデータ ビュー、データのビュー マネージャー、および並べ替えられた配列。  
  
 コントロールがデータ バインドでない場合は、それを並べ替えることができます。  
  
### <a name="to-sort-the-list"></a>一覧を並べ替える  
  
1.  `Sorted` プロパティを `true`に設定します。  
  
     この設定は、並べ替えられた順序ですべての既存のリスト アイテムを再配置します。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.ListBox>
- <xref:System.Windows.Forms.CheckedListBox>
- [Windows フォームでのデータ バインディング](../../../../docs/framework/winforms/windows-forms-data-binding.md)
- [方法: 追加および削除項目、Windows からフォーム ComboBox、ListBox、または CheckedListBox コントロール](../../../../docs/framework/winforms/controls/add-and-remove-items-from-a-wf-combobox.md)
- [ListBox の代わりに Windows フォーム ComboBox を使用する場合](../../../../docs/framework/winforms/controls/when-to-use-a-windows-forms-combobox-instead-of-a-listbox.md)
- [オプションのリストを表示するための Windows フォーム コントロール](../../../../docs/framework/winforms/controls/windows-forms-controls-used-to-list-options.md)
