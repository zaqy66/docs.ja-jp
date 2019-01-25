---
title: '方法: CompositeCollection を実装する'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], CompositeCollection class
ms.assetid: 0d8fc84c-7920-427f-8ad7-d55ca656c170
ms.openlocfilehash: 2021ed83a8f2a6896631fa69d5dd55a74cad8a8d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54691867"
---
# <a name="how-to-implement-a-compositecollection"></a><span data-ttu-id="2b917-102">方法: CompositeCollection を実装する</span><span class="sxs-lookup"><span data-stu-id="2b917-102">How to: Implement a CompositeCollection</span></span>
## <a name="example"></a><span data-ttu-id="2b917-103">例</span><span class="sxs-lookup"><span data-stu-id="2b917-103">Example</span></span>  
 <span data-ttu-id="2b917-104">次の例では、1 つのリストを使用して複数のコレクションと項目を表示する方法を示しています、<xref:System.Windows.Data.CompositeCollection>クラス。</span><span class="sxs-lookup"><span data-stu-id="2b917-104">The following example shows how to display multiple collections and items as one list using the <xref:System.Windows.Data.CompositeCollection> class.</span></span> <span data-ttu-id="2b917-105">この例で`GreekGods`は、<xref:System.Collections.ObjectModel.ObservableCollection%601>の`GreekGod`カスタム オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="2b917-105">In this example, `GreekGods` is an <xref:System.Collections.ObjectModel.ObservableCollection%601> of `GreekGod` custom objects.</span></span> <span data-ttu-id="2b917-106">データ テンプレートが定義されているように`GreekGod`オブジェクトと`GreekHero`オブジェクトは、gold とシアンの前景の色をそれぞれ表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b917-106">Data templates are defined so that `GreekGod` objects and `GreekHero` objects appear with a gold and a cyan foreground color respectively.</span></span>  
  
 [!code-xaml[CompositeCollections#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CompositeCollections/CS/Window1.xaml#1)]  
  
## <a name="see-also"></a><span data-ttu-id="2b917-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b917-107">See also</span></span>
- <xref:System.Windows.Data.CollectionContainer>
- <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A>
- <xref:System.Windows.Data.XmlDataProvider>
- <xref:System.Windows.DataTemplate>
- [<span data-ttu-id="2b917-108">データ バインディングの概要</span><span class="sxs-lookup"><span data-stu-id="2b917-108">Data Binding Overview</span></span>](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [<span data-ttu-id="2b917-109">方法トピック</span><span class="sxs-lookup"><span data-stu-id="2b917-109">How-to Topics</span></span>](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
