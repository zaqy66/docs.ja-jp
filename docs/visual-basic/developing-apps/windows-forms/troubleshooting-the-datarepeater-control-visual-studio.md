---
title: DataRepeater コントロールのトラブルシューティング (Visual Studio)
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, troubleshooting
ms.assetid: c0ab9469-eced-4f52-aa18-4bd8dd4f1a9a
ms.openlocfilehash: 7b045e1c45221cbde82c88286da8e698a763d844
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54580604"
---
# <a name="troubleshooting-the-datarepeater-control-visual-studio"></a>DataRepeater コントロールのトラブルシューティング (Visual Studio)
このトピックで使用している場合に発生する一般的な問題、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。  
  
## <a name="datarepeater-keyboard-and-mouse-events-are-not-raised"></a>DataRepeater キーボードとマウス イベントは発生しません  
 いくつか<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>キーボードとマウスのイベントなどのコントロールのイベントは発生しません。 これは仕様に基づく制限事項です。 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール自体のコンテナーは、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>オブジェクトし、実行時にアクセスすることはできません。 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>はデザイン時にイベントを公開しません。 そのため、項目をクリックするか、項目にフォーカスがあるときにキーを押して、イベントは発生しません。  
  
 この例外は、<xref:System.Windows.Forms.Control.Padding%2A>プロパティが多数の端を公開するための十分な値、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。 この場合は、公開されている余白をクリックすると、マウス イベントが発生します。  
  
 この問題を解決するには、追加、<xref:System.Windows.Forms.Panel>への制御、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>のセクション、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールし、コントロールの残りの部分を追加し、 <xref:System.Windows.Forms.Panel>。 コードを追加することができますし、<xref:System.Windows.Forms.Panel>キーボードとマウスのイベントに対するコントロールのイベント ハンドラー。  
  
## <a name="the-datarepeater-is-partially-hidden-behind-the-binding-navigator"></a>DataRepeater がナビゲーターのバインドの背後にある部分的に非表示します。  
 追加すると、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>フォームへの制御し、からのデータ バインド コントロールを追加し、**データ ソース**ウィンドウで、<xref:System.Windows.Forms.BindingNavigator>の上にコントロールが表示される、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。 これは、既知の制限、**データ ソース**ウィンドウなどの他のコントロールの動作と一貫性のあるが、<xref:System.Windows.Forms.DataGridView>コントロール。  
  
 移動することができます、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>よりも低い、 <xref:System.Windows.Forms.BindingNavigator> 、デザイン時にコントロールまたはコードでは、次のような追加、`Load`イベント ハンドラー。  
  
```vb  
DataRepeater1.Top = ProductsBindingNavigator.Height  
```  
  
```csharp  
dataRepeater1.Top = productsBindingNavigator.Height;  
```  
  
## <a name="controls-are-not-displayed-correctly-at-run-time"></a>実行時にコントロールが正しく表示されません。  
 一部のコントロール、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>期待どおりに実行時にコントロールが表示されない場合があります。 コントロールからのクローンを作成するために使用するプロセス、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>を<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>すべてのコントロールのすべてのプロパティをいつでも確認することはできません。 非結合を追加する場合など、<xref:System.Windows.Forms.ListBox>コントロールを<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>デザイン時に制御し、設定、 <xref:System.Windows.Forms.ListBox.Items%2A> 、文字列のリストをコレクション、<xref:System.Windows.Forms.ListBox>実行時に空になります。 これは、複製のプロセスが考慮に入れてできないため、<xref:System.Windows.Forms.ListBox.Items%2A>プロパティ。  
  
 このなどの問題を修正するで不足しているプロパティを復元することによって、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemCloned>イベントで、既定の複製が完了した後に発生します。 次の例では、修復する方法、<xref:System.Windows.Forms.ListBox.Items%2A>のコレクションを<xref:System.Windows.Forms.ListBox>を制御、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemCloned>イベント ハンドラー。  
  
 [!code-csharp[VbPowerPacksDataRepeaterItemCloned#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/troubleshooting-the-datarepeater-control-visual-studio_1.cs)]
 [!code-vb[VbPowerPacksDataRepeaterItemCloned#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/troubleshooting-the-datarepeater-control-visual-studio_1.vb)]  
  
## <a name="the-selection-symbol-on-the-item-header-is-missing"></a>項目ヘッダーの選択範囲のシンボルがありません。  
 変更すると、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor%2A>内の項目ヘッダーのプロパティを<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール、いくつかの色を選択が消滅する選択記号発生可能性があります。 変更、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderSize%2A>プロパティが消滅する選択記号もあります。  
  
 選択範囲のシンボルのサイズと色を変更できません。  
  
-   設定した場合、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor%2A>に<xref:System.Drawing.Color.White%2A>項目が最初に選択されたときに、選択の記号は表示されません。  
  
-   設定した場合、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor%2A>に<xref:System.Drawing.Color.Black%2A>コントロールが選択されているし、コントロールが編集モードのとき、鉛筆のアイコンは表示されません選択記号は表示されません。  
  
-   場合、 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderSize%2A> 11 より小さい値に設定されて、項目ヘッダーのマークは表示されません。  
  
 使用して、独自の項目ヘッダーと選択のシンボルを行うことができます、<xref:System.Windows.Forms.PictureBox>を管理および監視、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem.IsCurrent%2A>のプロパティ、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>で、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem>のイベント、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。 詳細については、「 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem.IsCurrent%2A> 」を参照してください。  
  
## <a name="see-also"></a>関連項目
- [DataRepeater コントロールの概要](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [方法: DataRepeater コントロールにバインドされたデータを表示します。](../../../visual-basic/developing-apps/windows-forms/how-to-display-bound-data-in-a-datarepeater-control-visual-studio.md)
- [方法: DataRepeater コントロールにバインドされていないコントロールを表示します。](../../../visual-basic/developing-apps/windows-forms/how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio.md)
- [方法: DataRepeater コントロールのレイアウトを変更します。](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-layout-of-a-datarepeater-control-visual-studio.md)
- [方法: DataRepeater コントロールの外観を変更します。](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)
- [方法: DataRepeater コントロールに項目ヘッダーの表示](../../../visual-basic/developing-apps/windows-forms/how-to-display-item-headers-in-a-datarepeater-control-visual-studio.md)
- [方法: 追加と削除 DataRepeater の項目を無効にします。](../../../visual-basic/developing-apps/windows-forms/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio.md)
- [方法: DataRepeater コントロールでデータの検索](../../../visual-basic/developing-apps/windows-forms/how-to-search-data-in-a-datarepeater-control-visual-studio.md)
- [方法: 2 つの DataRepeater コントロール (Visual Studio) を使用してマスター/詳細フォームを作成します。](../../../visual-basic/developing-apps/windows-forms/how-to-create-a-master-detail-form-by-using-two-datarepeater-controls.md)
