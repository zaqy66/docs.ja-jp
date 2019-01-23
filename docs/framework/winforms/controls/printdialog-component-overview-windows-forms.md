---
title: PrintDialog コンポーネントの概要 (Windows フォーム)
ms.date: 03/30/2017
f1_keywords:
- PrintDialog
helpviewer_keywords:
- Print dialog box [Windows Forms], displaying
- PrintDialog component [Windows Forms], about PrintDialog component
ms.assetid: 8327b8ac-1017-4b5e-a88b-fea9dd56999c
ms.openlocfilehash: 4df3266cecd080d11d13af8d4678a5303fd669cf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54516929"
---
# <a name="printdialog-component-overview-windows-forms"></a>PrintDialog コンポーネントの概要 (Windows フォーム)
Windows フォーム[PrintDialog](../../../../docs/framework/winforms/controls/printdialog-component-windows-forms.md)コンポーネントは構成済みのダイアログ ボックスがプリンターを選択し、印刷するページを選択して、Windows ベースのアプリケーションで他の印刷関連の設定を決定するために使用します。 独自のダイアログ ボックスを構成する代わりに、プリンターと印刷関連の設定の選択のための簡単なソリューションとして使用します。 ユーザーが自分のドキュメントの多くの部分の印刷を有効にすることができます。 すべてを印刷、印刷を選択したページ範囲または選択範囲を印刷します。 Windows の標準のダイアログ ボックスを使用して、ユーザーがすぐに慣れる基本的な機能を持つアプリケーションを作成します。 <xref:System.Windows.Forms.PrintDialog>コンポーネントが継承、<xref:System.Windows.Forms.CommonDialog>クラス。  
  
## <a name="working-with-the-component"></a>コンポーネントの操作  
 使用して、<xref:System.Windows.Forms.CommonDialog.ShowDialog%2A>メソッドを実行時にダイアログ ボックスを表示します。 このコンポーネントには 1 つの印刷ジョブをいずれかに関連するプロパティ (<xref:System.Drawing.Printing.PrintDocument>クラス)、または個々 のプリンターの設定 (<xref:System.Drawing.Printing.PrinterSettings>クラス)。 さらに、これらのうち、いずれかには複数のプリンターで共有することがあります。  
  
 フォームに追加されたとき、<xref:System.Windows.Forms.PrintDialog>コンポーネント、Windows フォーム デザイナーの下部にあるトレイに表示されます。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.PrintDialog>
- [PrintDialog コンポーネント](../../../../docs/framework/winforms/controls/printdialog-component-windows-forms.md)
