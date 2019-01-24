---
title: '方法: デザイナーを使用してデータ ソースへの Windows フォームの DataGrid コントロールのバインドします。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- datasets [Windows Forms], binding to DataGrid control
- data binding [Windows Forms], DataGrid control
- DataGrid control [Windows Forms], data binding
- Windows Forms controls, data binding
- bound controls [Windows Forms]
ms.assetid: 4e96e3d0-b1cc-4de1-8774-bc9970ec4554
ms.openlocfilehash: 414c989d258ca4b7a9097afa2b7f2407505fb629
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54687584"
---
# <a name="how-to-bind-the-windows-forms-datagrid-control-to-a-data-source-using-the-designer"></a>方法: デザイナーを使用してデータ ソースへの Windows フォームの DataGrid コントロールのバインドします。

> [!NOTE]
>  <xref:System.Windows.Forms.DataGridView> コントロールは、<xref:System.Windows.Forms.DataGrid> コントロールに代わると共に追加の機能を提供します。ただし、<xref:System.Windows.Forms.DataGrid> コントロールは、下位互換性を保つ目的および将来使用する目的で保持されます。 詳細については、「[Windows フォームの DataGridView コントロールと DataGrid コントロールの違いについて](../../../../docs/framework/winforms/controls/differences-between-the-windows-forms-datagridview-and-datagrid-controls.md)」を参照してください。  
  
 Windows フォーム<xref:System.Windows.Forms.DataGrid>コントロールが具体的には、データ ソースから情報を表示するように設計します。 デザイン時に設定して、コントロールをバインドする、<xref:System.Windows.Forms.DataGrid.DataSource%2A>と<xref:System.Windows.Forms.DataGrid.DataMember%2A>プロパティ、または呼び出すことによって実行時に、<xref:System.Windows.Forms.DataGrid.SetDataBinding%2A>メソッド。 さまざまなデータ ソースからデータを表示できますが、最も一般的なソース、データセットとデータのビューです。  
  
 デザイン時にデータ ソースが使用可能な場合: たとえば、フォームには、データセットまたはデータ ビューのインスタンスが含まれている場合: グリッドは、デザイン時に、データ ソースにバインドできます。 グリッドで、データの見た目をプレビューできます。  
  
 グリッドは実行時にプログラムでバインドすることもできます。 これは、実行時に取得した情報に基づくデータ ソースを設定する場合に便利です。 たとえば、アプリケーション ユーザーに表示するテーブルの名前を指定することができます。 場所、データ ソースがデザイン時に存在しない状況で必要です。 これには、配列、コレクション、型指定されていないデータセット、およびデータ リーダーなどのデータ ソースが含まれます。  
  
 次の手順が必要です、 **Windows アプリケーション**プロジェクトが含まれているフォームを<xref:System.Windows.Forms.DataGrid>コントロール。 このようなプロジェクトの設定の詳細については、次を参照してください。[方法。Windows アプリケーション プロジェクトを作成](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa)と[方法。Windows フォームにコントロールを追加](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)します。 Visual Studio 2005 で、<xref:System.Windows.Forms.DataGrid>制御されていない、**ツールボックス**既定。 追加の詳細については、次を参照してください。[方法。項目をツールボックスに追加](https://msdn.microsoft.com/library/458e119e-17fe-450b-b889-e31c128bd7e0)します。 さらに、Visual Studio 2005 で使用できます、**データソース**デザイン時のデータ バインディングのウィンドウ。 詳細については、次を参照してください。 [Visual Studio でのデータ コントロールをバインド](/visualstudio/data-tools/bind-controls-to-data-in-visual-studio)します。  
  
> [!NOTE]
>  実際に画面に表示されるダイアログ ボックスとメニュー コマンドは、アクティブな設定またはエディションによっては、ヘルプの説明と異なる場合があります。 設定を変更するには、 **[ツール]** メニューの **[設定のインポートとエクスポート]** をクリックします。 詳細については、「[Visual Studio IDE のカスタマイズ](/visualstudio/ide/personalizing-the-visual-studio-ide)」を参照してください。  
  
### <a name="to-data-bind-the-datagrid-control-to-a-single-table-in-the-designer"></a>デザイナーで 1 つのテーブルへ DataGrid コントロールのデータをバインドする  
  
1.  コントロールの設定<xref:System.Windows.Forms.DataGrid.DataSource%2A>プロパティにバインドするデータ項目を格納するオブジェクトをします。  
  
2.  データ ソースがデータセットの場合は、設定、<xref:System.Windows.Forms.DataGrid.DataMember%2A>プロパティにバインドするテーブルの名前にします。  
  
3.  データ ソースがデータセットまたはデータセットのテーブルに基づくデータ ビューの場合は、データセットを挿入するためのフォームにコードを追加します。  
  
     実際に使用するコードは、データセットがデータを取得する場所に依存します。 通常、呼び出す場合は、データセットをデータベースから直接登録されている、`Fill`メソッドという名前のデータセットを設定します次のコード例のように、データ アダプターの`DsCategories1`:。  
  
    ```vb  
    sqlDataAdapter1.Fill(DsCategories1)  
    ```  
  
    ```csharp  
    sqlDataAdapter1.Fill(DsCategories1);  
    ```  
  
    ```cpp  
    sqlDataAdapter1->Fill(dsCategories1);  
    ```  
  
4.  (省略可能)グリッドに適切なテーブルのスタイルおよび列のスタイルを追加します。  
  
     テーブル スタイルがない場合は、テーブルが表示されますが、最低限の書式と表示されているすべての列。  
  
### <a name="to-data-bind-the-datagrid-control-to-multiple-tables-in-a-dataset-in-the-designer"></a>デザイナーでデータセットの複数のテーブルへ DataGrid コントロールのデータをバインドする  
  
1.  コントロールの設定<xref:System.Windows.Forms.DataGrid.DataSource%2A>プロパティにバインドするデータ項目を格納するオブジェクトをします。  
  
2.  (リレーションシップ オブジェクトが含まれている) 場合は、データセットに関連するテーブルが含まれる場合、設定、<xref:System.Windows.Forms.DataGrid.DataMember%2A>プロパティを親テーブルの名前にします。  
  
3.  データセットを挿入するコードを記述します。  
  
## <a name="see-also"></a>関連項目
- [DataGrid コントロールの概要](../../../../docs/framework/winforms/controls/datagrid-control-overview-windows-forms.md)
- [方法: Windows フォームの DataGrid コントロールにテーブルと列を追加します。](../../../../docs/framework/winforms/controls/how-to-add-tables-and-columns-to-the-windows-forms-datagrid-control.md)
- [DataGrid コントロール](../../../../docs/framework/winforms/controls/datagrid-control-windows-forms.md)
- [Windows フォームでのデータ バインディング](../../../../docs/framework/winforms/windows-forms-data-binding.md)
- [Visual Studio でのデータへのアクセス](/visualstudio/data-tools/accessing-data-in-visual-studio)
