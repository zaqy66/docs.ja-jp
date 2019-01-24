---
title: '方法: DataRepeater コントロール (Visual Studio) の外観を変更します。'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, customizing
- DataRepeater, changing run time appearance
ms.assetid: 2af6dfce-760b-489e-b863-8da967f315c3
ms.openlocfilehash: e5508329ba716b53eff0c9e1bfe13e190fa1fd85
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54716636"
---
# <a name="how-to-change-the-appearance-of-a-datarepeater-control-visual-studio"></a>方法: DataRepeater コントロール (Visual Studio) の外観を変更します。
外観を変更することができます、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール プロパティの設定では、デザイン時または処理することによって実行時に、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem>イベント。  
  
 各コントロールの項目テンプレートのセクションを選択すると、デザイン時に設定するプロパティが繰り返されます<xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>実行時にします。 外観に関連するプロパティ、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール自体が検出された場合にのみ、コンテナーの一部の左の実行時に表示されます (場合など、<xref:System.Windows.Forms.Control.Padding%2A>プロパティが大きな値に設定)。  
  
 実行時に、外観に関連するプロパティ設定できますベースの条件に。 たとえば、スケジューリング アプリケーションでは、項目が過ぎたときにユーザーに警告する項目の背景色を変更する可能性があります。 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem>など、条件付きステートメントのプロパティを設定する場合、イベント ハンドラー `If…Then`、使用することも必要があります、`Else`条件が満たされないときに、外観を指定する句。  
  
### <a name="to-change-the-appearance-at-design-time"></a>デザイン時の外観を変更するには  
  
1.  Windows フォーム デザイナーでの項目テンプレート (上部) のリージョンを選択、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>コントロール。  
  
2.  [プロパティ] ウィンドウでプロパティを選択し、値を変更します。 外観に影響する一般的なプロパティが含まれます<xref:System.Windows.Forms.Control.BackColor%2A>、 <xref:System.Windows.Forms.Control.BackgroundImage%2A>、 <xref:System.Windows.Forms.Panel.BorderStyle%2A>、および<xref:System.Windows.Forms.Control.ForeColor%2A>します。  
  
### <a name="to-change-the-appearance-at-run-time"></a>実行時に外観を変更するには  
  
1.  コード エディターで、[イベント] ボックスの一覧の **[DrawItem]** をクリックします。  
  
2.  <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem>イベント ハンドラーでは、プロパティを設定するコードを追加します。  
  
     [!code-csharp[VbPowerPacksDataRepeaterAppearance#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksDataRepeaterAppearance#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio_1.vb)]  
  
## <a name="example"></a>例  
 用のいくつかの一般的なカスタマイズ、<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>色を交互に条件に基づくフィールドの色を変更する行を表示するコントロールが含まれます。 次の例では、これらのカスタマイズを実行する方法を示します。 この例では、ある、 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> Northwind データベースの Products テーブルにバインドされているコントロール。  
  
 [!code-vb[VbPowerPacksDataRepeaterAlternateBackColor#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio_2.vb)]
 [!code-csharp[VbPowerPacksDataRepeaterAlternateBackColor#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio_2.cs)]  
  
 これらのカスタマイズの両方の条件の両方の側のプロパティを設定するコードを提供する必要がありますに注意してください。 指定しない場合、`Else`条件、実行時に予期しない結果が表示されます。  
  
## <a name="see-also"></a>関連項目
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem>
- [DataRepeater コントロールの概要](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [DataRepeater コントロールのトラブルシューティング](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
- [方法: DataRepeater コントロールにバインドされたデータを表示します。](../../../visual-basic/developing-apps/windows-forms/how-to-display-bound-data-in-a-datarepeater-control-visual-studio.md)
- [方法: DataRepeater コントロールにバインドされていないコントロールを表示します。](../../../visual-basic/developing-apps/windows-forms/how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio.md)
- [方法: DataRepeater コントロールに項目ヘッダーの表示](../../../visual-basic/developing-apps/windows-forms/how-to-display-item-headers-in-a-datarepeater-control-visual-studio.md)
