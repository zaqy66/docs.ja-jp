---
title: '方法 : BindingSource と INotifyPropertyChanged の各インターフェイスを使用して変更通知を発生させる'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- change notifications [Windows Forms], raising
- BindingSource component [Windows Forms], and IPropertyChange
- data sources [Windows Forms], detecting changes
- examples [Windows Forms], BindingSource component
- change notifications
- INotifyPropertyChanged interface [Windows Forms], using with BindingSource
- BindingSource component [Windows Forms], examples
ms.assetid: 7fa2cf51-c09f-4375-adf0-e36c5617f099
ms.openlocfilehash: 039875473fe3bd1702ad43465edae2c73ffcadca
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/14/2018
ms.locfileid: "45609464"
---
# <a name="how-to-raise-change-notifications-using-a-bindingsource-and-the-inotifypropertychanged-interface"></a>方法 : BindingSource と INotifyPropertyChanged の各インターフェイスを使用して変更通知を発生させる
データ ソースに含まれる型が <xref:System.ComponentModel.INotifyPropertyChanged> インターフェイスを実装し、プロパティ値が変更されると <xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged> イベントを発生させる場合に、<xref:System.Windows.Forms.BindingSource> コンポーネントがデータ ソースの変更を自動的に検出します。 これは、データ ソースの値が変わると、<xref:System.Windows.Forms.BindingSource> にバインドされるコントロールが自動的に更新されるため便利です。  
  
> [!NOTE]
>  データ ソースが <xref:System.ComponentModel.INotifyPropertyChanged> を実装し、非同期操作を実行している場合は、バック グラウンド スレッド上のデータ ソースを変更しないようにします。 代わりに、バック グラウンド スレッド上のデータを読み取り、UI スレッドでリストにデータをマージする必要があります。  
  
## <a name="example"></a>例  
 次のコード例は、<xref:System.ComponentModel.INotifyPropertyChanged> インターフェイスの簡単な実装を示します。 <xref:System.Windows.Forms.BindingSource> が <xref:System.ComponentModel.INotifyPropertyChanged> 型の一覧にバインドされるときに、<xref:System.Windows.Forms.BindingSource> がバインドされたコントロールにデータ ソースの変更を自動的に渡す方法も示します。  
  
 `CallerMemberName` 属性を使用する場合、`NotifyPropertyChanged` メソッドの呼び出しが、文字列引数としてプロパティ名を指定する必要はありません。 詳細については、次を参照してください。[呼び出し元情報](https://msdn.microsoft.com/library/9cb2b8c0-c4f6-44b8-9c90-38948455b373)します。  
  
 [!code-csharp[System.ComponentModel.IPropertyChangeExample#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.IPropertyChangeExample#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 この例で必要な要素は次のとおりです。  
  
-   System、System.Data、System.Drawing、および System.Windows.Forms の各アセンブリへの参照。  
  
 コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。 新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。  参照してください[HYPERLINK"http://msdn.microsoft.com/library/Bb129228(v=vs.110)"する方法: コンパイルおよび実行を完全な Windows フォーム コードの例を使用して Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))します。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ComponentModel.INotifyPropertyChanged>  
 [BindingSource コンポーネント](../../../../docs/framework/winforms/controls/bindingsource-component.md)  
 [方法: BindingSource ResetItem メソッドを使用して変更通知を発生させる](../../../../docs/framework/winforms/controls/how-to-raise-change-notifications-using-the-bindingsource-resetitem-method.md)
