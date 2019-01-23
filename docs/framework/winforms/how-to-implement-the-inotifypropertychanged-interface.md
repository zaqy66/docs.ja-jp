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
# <a name="how-to-implement-the-inotifypropertychanged-interface"></a><span data-ttu-id="131bb-102">方法: INotifyPropertyChanged インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="131bb-102">How to: Implement the INotifyPropertyChanged Interface</span></span>
<span data-ttu-id="131bb-103">次のコード例は、実装する方法を示します、<xref:System.ComponentModel.INotifyPropertyChanged>インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="131bb-103">The following code example demonstrates how to implement the <xref:System.ComponentModel.INotifyPropertyChanged> interface.</span></span> <span data-ttu-id="131bb-104">Windows フォーム データ バインディングで使用されているビジネス オブジェクトでこのインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="131bb-104">Implement this interface on business objects that are used in Windows Forms data binding.</span></span> <span data-ttu-id="131bb-105">実装された場合、インターフェイスは、ビジネス オブジェクトでプロパティの変更をバインドされたコントロールに通信します。</span><span class="sxs-lookup"><span data-stu-id="131bb-105">When implemented, the interface  communicates to a bound control the property changes on a business object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="131bb-106">例</span><span class="sxs-lookup"><span data-stu-id="131bb-106">Example</span></span>  
 [!code-csharp[System.ComponentModel.IPropertyChangeExample#1](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.IPropertyChangeExample#1](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/VB/Form1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="131bb-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="131bb-107">See also</span></span>
- [<span data-ttu-id="131bb-108">方法: PropertyNameChanged パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="131bb-108">How to: Apply the PropertyNameChanged Pattern</span></span>](../../../docs/framework/winforms/how-to-apply-the-propertynamechanged-pattern.md)
- [<span data-ttu-id="131bb-109">Windows フォームでのデータ バインディング</span><span class="sxs-lookup"><span data-stu-id="131bb-109">Windows Forms Data Binding</span></span>](../../../docs/framework/winforms/windows-forms-data-binding.md)
- [<span data-ttu-id="131bb-110">方法: BindingSource と INotifyPropertyChanged インターフェイスを使用して変更通知を発生させる</span><span class="sxs-lookup"><span data-stu-id="131bb-110">How to: Raise Change Notifications Using a BindingSource and the INotifyPropertyChanged Interface</span></span>](../../../docs/framework/winforms/controls/raise-change-notifications--bindingsource.md)
- [<span data-ttu-id="131bb-111">Windows フォーム データ バインドの変更通知</span><span class="sxs-lookup"><span data-stu-id="131bb-111">Change Notification in Windows Forms Data Binding</span></span>](../../../docs/framework/winforms/change-notification-in-windows-forms-data-binding.md)
