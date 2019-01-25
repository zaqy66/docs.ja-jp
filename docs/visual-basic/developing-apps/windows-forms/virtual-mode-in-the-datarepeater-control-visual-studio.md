---
title: DataRepeater コントロールの仮想モード (Visual Studio)
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- virtual data binding [Visual Basic]
- DataRepeater
- DataRepeater, virtual mode
ms.assetid: 5fb805dc-2d8b-4139-b1e3-86e4c2667221
ms.openlocfilehash: 3988c16746606de9f20f9a66b87539b6cea04758
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54700807"
---
# <a name="virtual-mode-in-the-datarepeater-control-visual-studio"></a>DataRepeater コントロールの仮想モード (Visual Studio)
大量の表形式データを表示する場合、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールを設定してパフォーマンスを向上させることができます、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.VirtualMode%2A>プロパティを`True`と明示的にそのデータ ソース コントロールの相互作用を管理します。 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールは、データ ソースを操作し、実行時に、必要に応じてデータの表示を処理できるいくつかのイベントを提供します。  
  
## <a name="how-virtual-mode-works"></a>仮想モードの動作  
 最も一般的なシナリオ、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールは、の子コントロールをバインドする、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A>データにでき、デザイン時にソース、<xref:System.Windows.Forms.BindingSource>データに応じて前後へ渡す。 仮想モードを使用して、コントロールがデータ ソースにバインドされていないデータは、受け渡しが行われる、基になるデータ ソースを実行時にします。  
  
 ときに、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.VirtualMode%2A>プロパティに設定されて`True`からコントロールを追加して、ユーザー インターフェイスを作成する、**ツールボックス**からバインドされたコントロールを追加する代わりに、**データソース**ウィンドウ。  
  
 コントロールごとにイベントが発生して、データの表示を処理するコードを追加する必要があります。 新しい<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>スクロールして、表示、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValueNeeded>イベントには各コントロールの 1 つの時間が発生し、内の各コントロールの値を指定する必要があります、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValueNeeded>イベント ハンドラー。  
  
 1 つのコントロールのデータは、ユーザーによって変更された場合、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValuePushed>イベントが発生し、データを検証し、データ ソースに保存する必要があります。  
  
 ユーザーは、新しいアイテムを追加する場合、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.NewItemNeeded>イベントが発生します。 このイベントのハンドラーを使用すると、データ ソースに新しいレコードを作成します。 意図しない変更を防ぐためには、監視する必要も、<xref:System.Windows.Forms.Control.KeyDown>コントロールおよび呼び出しごとにイベント<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CancelEdit%2A>ユーザーが ESC キーを押した場合。  
  
 データ ソースが変更する場合は、更新、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールを呼び出すことによって、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.BeginResetItemTemplate%2A>と<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.EndResetItemTemplate%2A>メソッド。 順序では、両方のメソッドを呼び出す必要があります。  
  
 最後に、イベント ハンドラーを実装する必要があります、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemsRemoved>の直接的および必要に応じて項目が削除されたときに発生するイベント、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.UserDeletingItems>と<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.UserDeletedItems>イベントで、ユーザーが DELETE キーを押して、項目を削除するたびに発生します。  
  
## <a name="implementing-virtual-mode"></a>仮想モードの実装  
 仮想モードを実装するために必要な手順を次に示します。  
  
#### <a name="to-implement-virtual-mode"></a>仮想モードを実装するには  
  
1.  ドラッグ、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロールから、 **Visual Basic powerpacks**  タブで、**ツールボックス**フォームまたはコンテナー コントロールにします。 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.VirtualMode%2A> プロパティを `True`に設定します。  
  
2.  コントロールをドラッグして、**ツールボックス**の項目テンプレート領域 (上部領域)、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。 表示するデータ ソースのフィールドごとに 1 つのコントロールを必要があります。  
  
3.  ハンドラーを実装、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValueNeeded>イベントの各コントロールの値を指定します。 このイベントは、新しい<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>スクロールして表示します。 という名前のデータ ソース用の次の例のようになりますが、コード`Employees`します。  
  
     [!code-vb[VbPowerPacksDataRepeaterVirtualMode#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/virtual-mode-in-the-datarepeater-control-visual-studio_1.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterVirtualMode#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/virtual-mode-in-the-datarepeater-control-visual-studio_1.cs)]  
  
4.  ハンドラーを実装、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValuePushed>データを格納するイベントです。 このイベントは、ユーザーの子コントロールへの変更をコミットするときに発生しますが、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>します。 という名前のデータ ソース用の次の例のようになりますが、コード`Employees`します。  
  
     [!code-vb[VbPowerPacksDataRepeaterVirtualMode#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/virtual-mode-in-the-datarepeater-control-visual-studio_2.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterVirtualMode#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/virtual-mode-in-the-datarepeater-control-visual-studio_2.cs)]  
  
5.  各子コントロールのハンドラーを実装<xref:System.Windows.Forms.Control.KeyDown>イベントおよび ESC キーを監視します。 呼び出す、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CancelEdit%2A>メソッドを防ぐために、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValuePushed>イベントの発生します。 コードは次の例のようになります。  
  
     [!code-vb[VbPowerPacksDataRepeaterVirtualMode#3](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/virtual-mode-in-the-datarepeater-control-visual-studio_3.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterVirtualMode#3](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/virtual-mode-in-the-datarepeater-control-visual-studio_3.cs)]  
  
6.  ハンドラーを実装、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.NewItemNeeded>イベント。 このイベントは、ユーザーに新しい項目を追加するときに、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。 という名前のデータ ソース用の次の例のようになりますが、コード`Employees`します。  
  
     [!code-vb[VbPowerPacksDataRepeaterVirtualMode#4](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/virtual-mode-in-the-datarepeater-control-visual-studio_4.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterVirtualMode#4](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/virtual-mode-in-the-datarepeater-control-visual-studio_4.cs)]  
  
7.  ハンドラーを実装、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemsRemoved>イベント。 このイベントは、ユーザーが既存の項目を削除するときに発生します。 という名前のデータ ソース用の次の例のようになりますが、コード`Employees`します。  
  
     [!code-vb[VbPowerPacksDataRepeaterVirtualMode#5](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/virtual-mode-in-the-datarepeater-control-visual-studio_5.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterVirtualMode#5](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/virtual-mode-in-the-datarepeater-control-visual-studio_5.cs)]  
  
8.  ハンドラーを必要に応じてコントロール レベルの検証の実装、<xref:System.Windows.Forms.Control.Validating>子コントロールのイベント。 コードは次の例のようになります。  
  
     [!code-vb[VbPowerPacksDataRepeaterVirtualMode#6](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/virtual-mode-in-the-datarepeater-control-visual-studio_6.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterVirtualMode#6](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/virtual-mode-in-the-datarepeater-control-visual-studio_6.cs)]  
  
## <a name="see-also"></a>関連項目
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValuePushed>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.NewItemNeeded>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValueNeeded>
- [DataRepeater コントロールの概要](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
