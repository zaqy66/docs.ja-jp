---
title: '方法: PrintDialog コンポーネントを表示します。'
ms.date: 03/30/2017
helpviewer_keywords:
- Print dialog box [Windows Forms], displaying
- PrintDialog component [Windows Forms], displaying
- printing [Windows Forms], displaying print dialog box
ms.assetid: 745a8db7-0526-4b21-b09d-18e13ed32014
ms.openlocfilehash: 5315dc8b47c8ca846376ac6d1da5a0bf46fd6241
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54543998"
---
# <a name="how-to-display-the-printdialog-component"></a>方法: PrintDialog コンポーネントを表示します。
<xref:System.Windows.Forms.PrintDialog>コンポーネントは、多くのユーザーは使い慣れている標準の Windows 印刷ダイアログ ボックス。 なので、ユーザーはすぐに慣れてを使用するには有益なります、<xref:System.Windows.Forms.PrintDialog>コンポーネント。  
  
### <a name="to-display-the-printdialog-component"></a>PrintDialog コンポーネントを表示するには  
  
-   呼び出す、<xref:System.Windows.Forms.Form.ShowDialog%2A>アプリケーションのコード内からメソッド。  
  
     コンポーネントが表示されると、ユーザーはそれを使用して印刷ジョブのプロパティを設定します。 保存されます、 <!--zz <xref:System.Drawing.Printing.PrinterSetting>--> `PrinterSetting`クラス (および<xref:System.Drawing.Printing.PageSettings>クラス、ユーザーがアクセスする場合、 [PageSetupDialog コンポーネント](../../../../docs/framework/winforms/controls/pagesetupdialog-component-windows-forms.md)を通じて、<xref:System.Windows.Forms.PrintDialog>コンポーネント) 印刷ジョブに関連付けられています。 その後で、設定されたプロパティを呼び出して印刷ジョブの詳細を確認できます。  
  
## <a name="see-also"></a>関連項目
- [方法: 標準の Windows フォーム印刷ジョブを作成します。](../../../../docs/framework/winforms/advanced/how-to-create-standard-windows-forms-print-jobs.md)
- [方法: 実行時に PrintDialog のユーザー入力をキャプチャします。](../../../../docs/framework/winforms/advanced/how-to-capture-user-input-from-a-printdialog-at-run-time.md)
- [PrintPreviewDialog コントロール](../../../../docs/framework/winforms/controls/printpreviewdialog-control-windows-forms.md)
- [PrintDialog コンポーネント](../../../../docs/framework/winforms/controls/printdialog-component-windows-forms.md)
- [Windows フォームにおける印刷のサポート](../../../../docs/framework/winforms/advanced/windows-forms-print-support.md)
- [Windows フォーム コントロール](../../../../docs/framework/winforms/controls/index.md)
