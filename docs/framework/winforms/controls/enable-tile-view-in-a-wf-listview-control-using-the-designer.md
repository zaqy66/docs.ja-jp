---
title: '方法 : デザイナーを使って Windows フォーム ListView コントロールの "並べて表示" ビューを有効にする'
ms.date: 03/30/2017
helpviewer_keywords:
- tile view feature
- ListView control [Windows Forms], tile view
- tiling [Windows Forms], Windows Forms, controls
ms.assetid: 12f0816a-52b8-41ee-a6d9-ded3a8a5817a
ms.openlocfilehash: 86645396033ca1c3cfb025ba6db42b726f7e7969
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43862291"
---
# <a name="how-to-enable-tile-view-in-a-windows-forms-listview-control-using-the-designer"></a>方法 : デザイナーを使って Windows フォーム ListView コントロールの "並べて表示" ビューを有効にする
並べて表示ビュー機能、<xref:System.Windows.Forms.ListView>コントロールでは、グラフィカルとテキストの情報をバランスを提供することができます。 並べて表示ビューの項目で表示されるテキスト情報は、詳細ビュー用に定義されている列情報と同じ情報です。 グループ化またはカーソルのいずれかと組み合わせて、並べて表示ビューはマークの機能、<xref:System.Windows.Forms.ListView>コントロール。  
  
 並べて表示ビューでは、次の図のように、32 x 32 アイコンと数行のテキストを使用します。  
  
 ![ListView コントロール内のタイル ビュー](../../../../docs/framework/winforms/controls/media/listviewtile.gif "ListViewTile")  
  
 並べて表示ビューのプロパティとメソッドを使用すると、各項目を表示して、まとめてサイズとタイル ビュー ウィンドウ内のすべての項目の外観を制御する列フィールドを指定します。 わかりやすくするために、タイル内のテキストの最初の行は常に、項目の名前です。変更することはできません。  
  
 次の手順が必要です、 **Windows アプリケーション**プロジェクトが含まれているフォームを<xref:System.Windows.Forms.ListView>コントロール。 このようなプロジェクトの設定の詳細については、次を参照してください。[方法: Windows アプリケーション プロジェクトを作成](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa)と[方法: Windows フォームにコントロールを追加](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)します。  
  
> [!NOTE]
>  並べて表示ビューを [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)] で使用できるのは、アプリケーションから <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType> メソッドを呼び出した場合だけです。 旧バージョンのオペレーティング システムでは、並べて表示ビューに関するコードがすべて無効になり、<xref:System.Windows.Forms.ListView> コントロールは大きなアイコンのビューで表示されます。 詳細については、「<xref:System.Windows.Forms.ListView.View%2A?displayProperty=nameWithType>」を参照してください。  
>   
>  実際に画面に表示されるダイアログ ボックスとメニュー コマンドは、アクティブな設定またはエディションによっては、ヘルプの説明と異なる場合があります。 設定を変更するには、 **[ツール]** メニューの **[設定のインポートとエクスポート]** をクリックします。 詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。  
  
### <a name="to-set-tile-view-in-the-designer"></a>並べて表示ビューをデザイナーで設定するには  
  
1.  選択、<xref:System.Windows.Forms.ListView>フォーム上のコントロール。  
  
2.  **プロパティ**ウィンドウで、<xref:System.Windows.Forms.ListView.View%2A>プロパティ選択**タイル**します。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Windows.Forms.ListView.TileSize%2A>  
 [Windows XP の機能と Windows フォーム コントロール](https://msdn.microsoft.com/library/bc7fab94-fce9-4bf1-a8ad-a5837c91c3c0)  
 [ListView コントロールの概要](../../../../docs/framework/winforms/controls/listview-control-overview-windows-forms.md)
