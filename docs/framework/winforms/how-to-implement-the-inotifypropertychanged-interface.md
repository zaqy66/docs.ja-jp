---
title: '方法: INotifyPropertyChanged インターフェイスを実装します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- INotifyPropertyChanged interface [Windows Forms], implementing
ms.assetid: eac428af-b43b-46ac-80d9-1a5f88658725
ms.openlocfilehash: c92406899cffa56a1001f50f89cb53303df5da39
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54560075"
---
# <a name="how-to-implement-the-inotifypropertychanged-interface"></a>方法: INotifyPropertyChanged インターフェイスを実装します。
次のコード例は、実装する方法を示します、<xref:System.ComponentModel.INotifyPropertyChanged>インターフェイス。 Windows フォーム データ バインディングで使用されているビジネス オブジェクトでこのインターフェイスを実装します。 実装された場合、インターフェイスは、ビジネス オブジェクトでプロパティの変更をバインドされたコントロールに通信します。  
  
## <a name="example"></a>例  
 [!code-csharp[System.ComponentModel.IPropertyChangeExample#1](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.IPropertyChangeExample#1](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/VB/Form1.vb#1)]  
  
## <a name="see-also"></a>関連項目
- [方法: PropertyNameChanged パターンを適用します。](../../../docs/framework/winforms/how-to-apply-the-propertynamechanged-pattern.md)
- [Windows フォームでのデータ バインディング](../../../docs/framework/winforms/windows-forms-data-binding.md)
- [方法: BindingSource と INotifyPropertyChanged インターフェイスを使用して変更通知を発生させる](../../../docs/framework/winforms/controls/raise-change-notifications--bindingsource.md)
- [Windows フォーム データ バインドの変更通知](../../../docs/framework/winforms/change-notification-in-windows-forms-data-binding.md)
