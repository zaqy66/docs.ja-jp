---
title: SaveFileDialog コンポーネントの概要 (Windows フォーム)
ms.date: 03/30/2017
f1_keywords:
- SaveFileDialog
helpviewer_keywords:
- Save File dialog box [Windows Forms], displaying
- SaveFileDialog component [Windows Forms], about SaveFileDialog
ms.assetid: be7a625f-46fd-4d06-9985-b613dcbf9bd2
ms.openlocfilehash: ab8eb5409d017c6ea73a44e4e57ccec9cece4824
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631062"
---
# <a name="savefiledialog-component-overview-windows-forms"></a>SaveFileDialog コンポーネントの概要 (Windows フォーム)
Windows フォームの <xref:System.Windows.Forms.SaveFileDialog> コンポーネントは、事前構成済みのダイアログ ボックスです。 これは、標準と同じ**ファイルを保存**Windows で使用されるダイアログ ボックス。 これは、<xref:System.Windows.Forms.CommonDialog> クラスを継承しています。  
  
## <a name="working-with-the-savefiledialog-component"></a>SaveFileDialog コンポーネントの操作  
 ダイアログ ボックスを構成する代わりにファイルを保存するユーザーを有効にするための単純なソリューションとして使用します。 標準の Windows ダイアログ ボックスで証明書利用者では、作成したアプリケーションの基本的な機能はすぐに、ユーザーにとって馴染み深いです。 ただし、時に使用して、<xref:System.Windows.Forms.SaveFileDialog>コンポーネント、独自のファイルの保存ロジックを記述する必要があります。  
  
 使用することができます、<xref:System.Windows.Forms.CommonDialog.ShowDialog%2A>メソッドを実行時にダイアログ ボックスを表示します。 読み取り/書き込みモードを使用してファイルを開くことができます、<xref:System.Windows.Forms.SaveFileDialog.OpenFile%2A>メソッド。  
  
 フォームに追加されたとき、<xref:System.Windows.Forms.SaveFileDialog>コンポーネント、Windows フォーム デザイナーの下部にあるトレイに表示されます。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.SaveFileDialog>
- [SaveFileDialog コンポーネント](../../../../docs/framework/winforms/controls/savefiledialog-component-windows-forms.md)
