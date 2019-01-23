---
title: DataRepeater コントロールの概要 (Visual Studio)
ms.date: 07/20/2015
helpviewer_keywords:
- repeating data
- DataRepeater, overview
- DataRepeater
ms.assetid: 78a52a1d-65f0-4ecb-97ff-53bc114300c5
ms.openlocfilehash: c9d95f41e9857d70e81cafc94e5e3bffd4cbc3d1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54580708"
---
# <a name="introduction-to-the-datarepeater-control-visual-studio"></a>DataRepeater コントロールの概要 (Visual Studio)
Visual Basic Power Packs の <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> コントロールは、データベース テーブルの行などの繰り返されるデータを表示するコントロールの、スクロール可能なコンテナーです。 データのレイアウトを詳細に制御する必要がある場合は、 <xref:System.Windows.Forms.DataGridView> コントロールの代わりにこのコントロールを使用できます。 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>スクロール ビューで複数のインスタンスを作成して関連するコントロールのグループを「繰り返し」。 これにより、ユーザーが同時に複数のレコードを表示できます。  
  
## <a name="overview"></a>概要  
 デザイン時に、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールは、2 つのセクションで構成されています。 外部のセクションでは、*ビューポート*、スクロール可能なデータが実行時に表示されます。 内部の (上部) セクションと呼ばれる、*項目テンプレート*が実行時、データ ソースのフィールドごとに通常 1 つのコントロールに繰り返されるコントロールを配置します。 プロパティと項目テンプレート内のコントロールにカプセル化、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>プロパティ。  
  
 実行時に、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>バーチャル マシンにコピーされます<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>各レコードをスクロールして表示するときにデータを表示するために使用するオブジェクト。 内の個々 のレコードの表示をカスタマイズすることができます、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem>イベント、たとえば、それに含まれる値に基づくフィールドを強調表示します。 詳細については、「[方法 :DataRepeater コントロールの外観を変更](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)します。  
  
 最も一般的な用途、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールは、データベース テーブルまたはその他のバインドされたデータ ソースからデータを表示します。 ほかに[!INCLUDE[vstecado](~/includes/vstecado-md.md)]データ オブジェクト、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールを実装するクラスにバインドできます、<xref:System.Collections.IList>インターフェイス (配列を含む)、実装するクラス、<xref:System.ComponentModel.IListSource>インターフェイスを実装するクラス、 <xref:System.ComponentModel.IBindingList>インターフェイス、または実装するクラス、<xref:System.ComponentModel.IBindingListView>インターフェイス。  
  
### <a name="data-binding"></a>データ バインディング  
 通常からフィールドをドラッグしてデータ バインディングを行う、**データ ソース**ウィンドウ、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。 詳細については、「[方法 :DataRepeater コントロールにバインドされたデータを表示](../../../visual-basic/developing-apps/windows-forms/how-to-display-bound-data-in-a-datarepeater-control-visual-studio.md)します。  
  
 設定することが大量のデータを操作するとき、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.VirtualMode%2A>プロパティを`True`使用可能なデータのサブセットを表示します。 仮想モードには、元のデータ キャッシュの実装が必要です、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>の値が設定され、実行時にデータ キャッシュのすべての通信を制御する必要があります。 詳細については、次を参照してください。 [DataRepeater コントロールでの仮想モード](../../../visual-basic/developing-apps/windows-forms/virtual-mode-in-the-datarepeater-control-visual-studio.md)します。  
  
 バインドされていないコントロールを表示することも、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。 たとえば、各項目のイメージを繰り返すを表示できます。 詳細については、「[方法 :表示には、DataRepeater コントロールでコントロールがバインドされていない](../../../visual-basic/developing-apps/windows-forms/how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio.md)します。  
  
### <a name="events"></a>イベント  
 最も重要なイベント、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールは、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem>ビューに新しい項目がスクロールされたときに発生するイベントと<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CurrentItemIndexChanged>イベントで、項目が選択されている場合に発生します。 使用することができます、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem>項目の外観を変更するイベントです。 たとえば、負の値を強調表示することができます。 使用して、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CurrentItemIndexChanged>項目が選択されているときにコントロールの値にアクセスするイベントです。  
  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールは、コード エディターですべて標準コントロールのイベントを公開します。 ただし、一部のイベントは使用されません。 キーボードし、マウス イベントなど`KeyDown`、`Click`と`MouseDown`ために、実行時に発生しませんが、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール自体にフォーカスがあることはありません。  
  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>実行時にのみ作成されるので、デザイン時にイベントを公開しないしません。 追加できますキーボードとマウスのイベントを処理するかどうか、<xref:System.Windows.Forms.Panel>への制御、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>でのイベントを処理し、デザイン時と、<xref:System.Windows.Forms.Panel>します。 詳細については、次を参照してください。 [DataRepeater コントロールのトラブルシューティング](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)します。  
  
### <a name="customizations"></a>カスタマイズ  
 動作と外観をカスタマイズする方法はたくさんあります、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>実行時およびデザイン時の両方を制御します。 色を変更、非表示または変更項目ヘッダー、方向から水平方向、垂直な変更は、プロパティを設定できます。 詳細については、「[方法 :DataRepeater コントロールの外観を変更](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)、[方法。DataRepeater コントロールに項目ヘッダーを表示](../../../visual-basic/developing-apps/windows-forms/how-to-display-item-headers-in-a-datarepeater-control-visual-studio.md)、および[方法。DataRepeater コントロールのレイアウトを変更する](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-layout-of-a-datarepeater-control-visual-studio.md)します。  
  
 一部のプロパティに適用されます、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール自体にのみ適用されるものは、 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>。 プロパティを設定する前に、コントロールの適切なセクションがあることを確認します。 詳細については、「[方法 :DataRepeater コントロールの外観を変更](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)します。  
  
 その他のカスタマイズには、レコード追加または削除する機能を制御する、検索の機能の追加、およびマスター/詳細形式で関連データの表示が含まれます。 詳細については、「[方法 :追加と削除 DataRepeater の項目を無効にする](../../../visual-basic/developing-apps/windows-forms/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio.md)、[方法。DataRepeater コントロールでデータを検索](../../../visual-basic/developing-apps/windows-forms/how-to-search-data-in-a-datarepeater-control-visual-studio.md)、および[方法。2 つの DataRepeater コントロール (Visual Studio) を使用してマスター/詳細フォームを作成](../../../visual-basic/developing-apps/windows-forms/how-to-create-a-master-detail-form-by-using-two-datarepeater-controls.md)です。  
  
## <a name="see-also"></a>関連項目
- [DataRepeater コントロール](../../../visual-basic/developing-apps/windows-forms/datarepeater-control-visual-studio.md)
- [チュートリアル: DataRepeater コントロールにデータを表示します。](../../../visual-basic/developing-apps/windows-forms/walkthrough-displaying-data-in-a-datarepeater-control-visual-studio.md)
- [DataRepeater コントロールのトラブルシューティング](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
