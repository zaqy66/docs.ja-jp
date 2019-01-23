---
title: '方法: TextBox から行のコレクションを取得する'
ms.date: 03/30/2017
helpviewer_keywords:
- lines [WPF], getting collection of
- TextBox control [WPF], getting collection of lines
ms.assetid: a12f529d-b926-47f6-92bf-cad5f17b532a
ms.openlocfilehash: a63470c6f0db72340f482bf638910685aa3f461f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54561765"
---
# <a name="how-to-get-a-collection-of-lines-from-a-textbox"></a>方法: TextBox から行のコレクションを取得する
この例からのテキストの行のコレクションを取得する方法を示しています、<xref:System.Windows.Controls.TextBox>します。  
  
## <a name="example"></a>例  
 次の例を受け取る単純なメソッドを示しています、<xref:System.Windows.Controls.TextBox>引数として返す、<xref:System.Collections.Specialized.StringCollection>内のテキストの行を含む、 **TextBox**。  <xref:System.Windows.Controls.TextBox.LineCount%2A>プロパティを使用して、現在の行の数を調べます、 **TextBox**と<xref:System.Windows.Controls.TextBox.GetLineText%2A>メソッドを使用して各行を抽出し、行のコレクションに追加します。  
  
 [!code-csharp[TextBox_MiscCode#_TextBox_GetLines](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_textbox_getlines)]  
  
## <a name="see-also"></a>関連項目
- [TextBox の概要](../../../../docs/framework/wpf/controls/textbox-overview.md)
- [RichTextBox の概要](../../../../docs/framework/wpf/controls/richtextbox-overview.md)
