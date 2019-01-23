---
title: '方法: デザイナーを使用して Windows フォーム DataGridView コントロール内の列を非表示にします。'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, columns
- columns [Windows Forms], hiding
- DataGridView control [Windows Forms], column hiding
- data [Windows Forms], displaying
ms.assetid: a81c38e6-2527-426a-bcb1-be691403be04
ms.openlocfilehash: 77aa5614d185a80c1f70ec5afad57834cff003d7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54517813"
---
# <a name="how-to-hide-columns-in-the-windows-forms-datagridview-control-using-the-designer"></a>方法: デザイナーを使用して Windows フォーム DataGridView コントロール内の列を非表示にします。
Windows フォームの <xref:System.Windows.Forms.DataGridView> コントロールで使用できる列の一部のみを表示したいときがあります。 たとえば、従業員を表示するたい給与の列には他のユーザーが非表示の管理資格情報を持つユーザーをします。 または、その一部のみを表示する多くの列を含むデータ ソースにコントロールをバインドすることがあります。 この場合、非表示にするのではなく、表示する必要のない列は通常削除されます。 詳細については、「[方法 :削除列で、Windows フォーム DataGridView コントロールのデザイナーを使用してを追加および](../../../../docs/framework/winforms/controls/add-and-remove-columns-in-the-datagrid-using-the-designer.md)します。  
  
 次の手順が必要です、 **Windows アプリケーション**プロジェクトが含まれているフォームを<xref:System.Windows.Forms.DataGridView>コントロール。 このようなプロジェクトの設定の詳細については、次を参照してください。[方法。Windows アプリケーション プロジェクトを作成](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa)と[方法。Windows フォームにコントロールを追加](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)します。  
  
> [!NOTE]
>  実際に画面に表示されるダイアログ ボックスとメニュー コマンドは、アクティブな設定またはエディションによっては、ヘルプの説明と異なる場合があります。 設定を変更するには、 **[ツール]** メニューの **[設定のインポートとエクスポート]** をクリックします。 詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。  
  
### <a name="to-hide-a-column-using-the-designer"></a>デザイナーを使用して列を非表示にするには  
  
1.  スマート タグ グリフをクリックします (![スマート タグ グリフ](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) の右上隅で、 <xref:System.Windows.Forms.DataGridView> 、制御し、**列の編集**します。  
  
2.  列を選択、**選択した列**一覧。  
  
3.  **列プロパティ**グリッドで、設定、<xref:System.Windows.Forms.DataGridViewColumn.Visible%2A>プロパティを`false`します。  
  
    > [!NOTE]
    >  オフにして追加する際に、列を隠すことも、 **Visible**  チェック ボックス、**列の追加** ダイアログ ボックス。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A?displayProperty=nameWithType>
- [方法: 追加して、デザイナーを使用して Windows フォーム DataGridView コントロールで列を削除](../../../../docs/framework/winforms/controls/add-and-remove-columns-in-the-datagrid-using-the-designer.md)
- [方法: Windows アプリケーション プロジェクトを作成する](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa)
- [方法: Windows フォームにコントロールを追加します。](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)
