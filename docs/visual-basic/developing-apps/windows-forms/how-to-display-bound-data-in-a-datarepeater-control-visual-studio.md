---
title: '方法 : DataRepeater コントロールにバインドされたデータを表示する (Visual Studio)'
ms.date: 07/20/2015
helpviewer_keywords:
- DataRepeater, data-binding
- DataRepeater, displaying bound controls
ms.assetid: 56a15326-1334-4275-af4e-075cad79e6f7
ms.openlocfilehash: b96fb33a0dcf80a86d1fcb6e219e5f35b1f7351c
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42933407"
---
# <a name="how-to-display-bound-data-in-a-datarepeater-control-visual-studio"></a>方法 : DataRepeater コントロールにバインドされたデータを表示する (Visual Studio)
最も一般的な用途、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールは、データベースまたは他のデータ ソースからバインドされたデータを表示します。  
  
 バインドされたコントロールのほかに静的ラベルなどの各項目に繰り返されるイメージの他のコントロールを追加したい場合があります、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。 詳細については、次を参照してください。[方法: DataRepeater コントロールにバインドされていないコントロールを表示](../../../visual-basic/developing-apps/windows-forms/how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio.md)します。  
  
 バインドすることできますもデータ ソースに実行時に設定して、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.VirtualMode%2A>プロパティを`True`とするデータ ソースを割り当て、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DataSource%2A>プロパティ。 この場合、データ ソースとのすべての相互作用を管理する必要があります。 詳細については、次を参照してください。 [DataRepeater コントロールでの仮想モード](../../../visual-basic/developing-apps/windows-forms/virtual-mode-in-the-datarepeater-control-visual-studio.md)します。  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-data-bound-datarepeater"></a>データ バインド DataRepeater を作成するには  
  
1.  ドラッグ、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールから、 **Visual Basic powerpacks**  タブで、**ツールボックス**フォームまたはコンテナー コントロールにします。  
  
2.  サイズにサイズと位置のハンドルをドラッグし、コントロールを配置します。  
  
     コントロールに 2 つの四角形領域があることに注意してください。 上部の領域は、*項目テンプレート*; 内の各項目で、テンプレートに追加されたコントロールが繰り返されます、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>実行時にコントロール。 下部の領域は、*ビューポート*項目が表示されます。  
  
     サイズを変更し、変更することで、コントロールまたは項目テンプレートを配置することもできます、**サイズ**と**位置**プロパティ ウィンドウでプロパティ。  
  
3.  **[データ]** メニューの **[データ ソースの表示]** をクリックします。  
  
    > [!NOTE]
    >  場合、**データソース**ウィンドウが空の場合、データ ソースを追加します。 詳細については、「[新しいデータ ソースの追加](/visualstudio/data-tools/add-new-data-sources)」を参照してください。  
  
4.  **データソース**ウィンドウで、最上位ノードにバインドするデータを含むテーブルを選択します。  
  
5.  変更するテーブルのドロップ タイプ`Details`をクリックして`Details`テーブル ノードのドロップダウン リストでします。  
  
6.  テーブル ノードを選択し、項目テンプレート領域にドラッグ、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。  
  
     フィールドごとに表示されるコントロールの種類を指定できます。 詳細については、次を参照してください。[設定、データ ソース ウィンドウからドラッグするときに作成されるコントロール](/visualstudio/data-tools/set-the-control-to-be-created-when-dragging-from-the-data-sources-window)します。  
  
## <a name="see-also"></a>関連項目  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>  
 [DataRepeater コントロールの概要](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)  
 [方法: DataRepeater コントロールに非バインド コントロールを表示する](../../../visual-basic/developing-apps/windows-forms/how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio.md)  
 [方法: 2 つの DataRepeater コントロール (Visual Studio) を使用してマスター/詳細フォームを作成します。](../../../visual-basic/developing-apps/windows-forms/how-to-create-a-master-detail-form-by-using-two-datarepeater-controls.md)  
 [方法: DataRepeater コントロールの外観を変更する](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)  
 [DataRepeater コントロールのトラブルシューティング](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
