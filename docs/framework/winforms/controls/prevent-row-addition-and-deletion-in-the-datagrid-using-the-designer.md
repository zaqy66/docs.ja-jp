---
title: '方法 : デザイナーを使用して Windows フォーム DataGridView コントロールで行が追加および削除されないようにする'
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], preventing row addition or deletion
ms.assetid: a17722bd-9400-41e6-8dcc-c9c151f0a749
ms.openlocfilehash: 8315f59c3a0862daf7591096ad2d34e5d442f310
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/30/2018
ms.locfileid: "43254807"
---
# <a name="how-to-prevent-row-addition-and-deletion-in-the-windows-forms-datagridview-control-using-the-designer"></a>方法 : デザイナーを使用して Windows フォーム DataGridView コントロールで行が追加および削除されないようにする
場合によっては、ユーザーが <xref:System.Windows.Forms.DataGridView> コントロールに新しいデータ行を入力したり、既存の行を削除したりできないようにする必要があります。 コントロールの下部に新しいレコードの特別な行では新しい行を入力します。 行の追加を無効にすると、新しいレコードの行は表示されません。 行うことができますし、コントロール全体は読み取り専用行の削除とセルの編集を無効にするとします。  
  
 次の手順が必要です、 **Windows アプリケーション**プロジェクトが含まれているフォームを<xref:System.Windows.Forms.DataGridView>コントロール。 このようなプロジェクトの設定の詳細については、次を参照してください。[方法: Windows アプリケーション プロジェクトを作成](http://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa)と[方法: Windows フォームにコントロールを追加](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)します。  
  
> [!NOTE]
>  実際に画面に表示されるダイアログ ボックスとメニュー コマンドは、アクティブな設定またはエディションによっては、ヘルプの説明と異なる場合があります。 設定を変更するには、 **[ツール]** メニューの **[設定のインポートとエクスポート]** をクリックします。 詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。  
  
### <a name="to-prevent-row-addition-and-deletion"></a>行の追加と削除を防止するには  
  
-   スマート タグ グリフをクリックします (![スマート タグ グリフ](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) の右上隅で、 <xref:System.Windows.Forms.DataGridView> 、制御し、オフ、**追加を有効にする****削除を有効にする**チェック ボックス。  
  
    > [!NOTE]
    >  コントロールを完全に読み取り専用にするには、オフ、**編集を有効にする** チェック ボックスもします。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A?displayProperty=nameWithType>  
 [方法: Windows アプリケーション プロジェクトを作成](http://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa)  
 [方法: Windows フォームにコントロールを追加する](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)
