---
title: Windows フォームでのデータ バインディング
ms.date: 03/30/2017
helpviewer_keywords:
- data [Windows Forms]
- Windows Forms, data binding
- data [Windows Forms], architecture
- Windows Forms controls, data binding
ms.assetid: c3826d8e-ea25-4ad4-a669-45bfb19192aa
ms.openlocfilehash: b33ad9d78230588b9c1afd5d59fd0333e2cd18a6
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/23/2019
ms.locfileid: "56747062"
---
# <a name="windows-forms-data-binding"></a>Windows フォームでのデータ バインディング
Windows フォームでのデータ バインディングは、データ ソースの情報をフォーム上のコントロールで表示したり変更したりする手段を提供します。 従来のデータ ソースに対してだけでなく、データを格納したほとんどすべての構造に対してバインドできます。  
  
## <a name="in-this-section"></a>このセクションの内容  
 [データ連結と Windows フォーム](../../../docs/framework/winforms/data-binding-and-windows-forms.md)  
 Windows フォームのデータ バインディングの概要を説明します。  
  
 [Windows フォームがサポートするデータ ソース](../../../docs/framework/winforms/data-sources-supported-by-windows-forms.md)  
 Windows フォームで使用できるデータ ソースについて説明します。  
  
 [データ連結に関連するインターフェイス](../../../docs/framework/winforms/interfaces-related-to-data-binding.md)  
 Windows フォームのデータ バインドで使用されるいくつかのインターフェイスについて説明します。  
  
 [方法: Windows フォームでデータを移動します。](../../../docs/framework/winforms/how-to-navigate-data-in-windows-forms.md)  
 データ ソースの項目間を移動する方法を示します。  
  
 [Windows フォーム データ バインドの変更通知](../../../docs/framework/winforms/change-notification-in-windows-forms-data-binding.md)  
 Windows フォーム データ バインドの異なる種類の変更通知について説明します。  
  
 [方法: INotifyPropertyChanged インターフェイスを実装します。](../../../docs/framework/winforms/how-to-implement-the-inotifypropertychanged-interface.md)  
 
  <xref:System.ComponentModel.INotifyPropertyChanged> インターフェイスを実装する方法について説明します。 インターフェイスは、バインドしたコントロールを通してビジネス オブジェクトのプロパティの変更内容を通信します。  
  
 [方法: PropertyNameChanged パターンを適用します。](../../../docs/framework/winforms/how-to-apply-the-propertynamechanged-pattern.md)  
 適用する方法を示しています、 *PropertyName*Changed パターンを Windows フォーム ユーザー コントロールのプロパティ。  
  
 [方法: ITypedList インターフェイスを実装します。](../../../docs/framework/winforms/how-to-implement-the-itypedlist-interface.md)  
 
  <xref:System.ComponentModel.ITypedList> インターフェイスを実装して、バインドできるリストのスキーマを検出できるようにする方法について説明します。  
  
 [方法: IListSource インターフェイスを実装します。](../../../docs/framework/winforms/how-to-implement-the-ilistsource-interface.md)  
 
  <xref:System.ComponentModel.IListSource> インターフェイスを実装して、<xref:System.Collections.IList> を実装する代わりに別の場所からリストを提供する、バインドできるクラスを作成する方法について説明します。  
  
 [方法: 複数のコントロールと同じデータ ソースにバインドが同期を維持](../../../docs/framework/winforms/multiple-controls-bound-to-data-source-synchronized.md)  
 
  <xref:System.Windows.Forms.BindingSource.BindingComplete> イベントを処理して、データ ソースにバインドされているすべてのコントロールの同期を保つ方法について説明します。  
  
 [方法: 子テーブルの選択行が正しい位置に保持することを確認します。](../../../docs/framework/winforms/ensure-the-selected-row-in-a-child-table-correct.md)  
 親テーブルのフィールドが変更された場合に、子テーブルの選択行が変更されないことを保証する方法について説明しています。  
  
 参照してください[データ バインディングに関連するインターフェイス](interfaces-related-to-data-binding.md)、[方法。Windows フォームでデータを移動](how-to-navigate-data-in-windows-forms.md)、および[方法。Windows フォームに単純バインド コントロールを作成する](how-to-create-a-simple-bound-control-on-a-windows-form.md)します。  
  
## <a name="reference"></a>参照  
 <xref:System.Windows.Forms.Binding?displayProperty=nameWithType>  
 バインドできるコンポーネントとデータ ソースの間のバインディングを表すクラスについて説明します。  
  
 <xref:System.Windows.Forms.BindingSource?displayProperty=nameWithType>  
 コントロールにバインドするためにデータ ソースをカプセル化するクラスについて説明します。  
  
## <a name="related-sections"></a>関連項目  
 [BindingSource コンポーネント](../../../docs/framework/winforms/controls/bindingsource-component.md)  
 
  <xref:System.Windows.Forms.BindingSource> コンポーネントの使用方法の例を示すトピックの一覧を示します。  
  
 [DataGridView コントロール](../../../docs/framework/winforms/controls/datagridview-control-windows-forms.md)  
 バインドできるデータ グリッド コントロールの使用方法の例を示すトピックの一覧を示します。  
  
 参照してください[Visual Studio でのデータへのアクセス](/visualstudio/data-tools/accessing-data-in-visual-studio)します。
