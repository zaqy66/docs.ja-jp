---
title: '方法: ThicknessConverter オブジェクトを使用する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- border thickness [WPF]
- ThicknessConverter objects [WPF]
ms.assetid: 52682194-d7fd-499c-8005-73fcc84e7b2c
ms.openlocfilehash: 22215a155f4a204e3edeebc464413d5718290bb4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577072"
---
# <a name="how-to-use-a-thicknessconverter-object"></a><span data-ttu-id="acbae-102">方法: ThicknessConverter オブジェクトを使用する</span><span class="sxs-lookup"><span data-stu-id="acbae-102">How to: Use a ThicknessConverter Object</span></span>
## <a name="example"></a><span data-ttu-id="acbae-103">例</span><span class="sxs-lookup"><span data-stu-id="acbae-103">Example</span></span>  
 <span data-ttu-id="acbae-104">この例のインスタンスを作成する方法を示しています。<xref:System.Windows.ThicknessConverter>境界線の太さを変更するとします。</span><span class="sxs-lookup"><span data-stu-id="acbae-104">This example shows how to create an instance of <xref:System.Windows.ThicknessConverter> and use it to change the thickness of a border.</span></span>  
  
 <span data-ttu-id="acbae-105">例では、呼び出されるカスタム メソッドを定義します`changeThickness`; このメソッドは、最初の内容を変換、<xref:System.Windows.Controls.ListBoxItem>個別で定義されている、[!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]のインスタンスへのファイル<xref:System.Windows.Thickness>、後に、コンテンツに変換します、 <xref:System.String>。</span><span class="sxs-lookup"><span data-stu-id="acbae-105">The example defines a custom method called `changeThickness`; this method first converts the contents of a <xref:System.Windows.Controls.ListBoxItem>, as defined in a separate [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] file, to an instance of <xref:System.Windows.Thickness>, and later converts the content into a <xref:System.String>.</span></span> <span data-ttu-id="acbae-106">このメソッドは、<xref:System.Windows.Controls.ListBoxItem>に、<xref:System.Windows.ThicknessConverter>オブジェクトで、変換、<xref:System.Windows.Controls.ContentControl.Content%2A>の<xref:System.Windows.Controls.ListBoxItem>のインスタンスに<xref:System.Windows.Thickness>。</span><span class="sxs-lookup"><span data-stu-id="acbae-106">This method passes the <xref:System.Windows.Controls.ListBoxItem> to a <xref:System.Windows.ThicknessConverter> object, which converts the <xref:System.Windows.Controls.ContentControl.Content%2A> of a <xref:System.Windows.Controls.ListBoxItem> to an instance of <xref:System.Windows.Thickness>.</span></span> <span data-ttu-id="acbae-107">この値の値として戻されますが、<xref:System.Windows.Controls.Border.BorderThickness%2A>のプロパティ、<xref:System.Windows.Controls.Border>します。</span><span class="sxs-lookup"><span data-stu-id="acbae-107">This value is then passed back as the value of the <xref:System.Windows.Controls.Border.BorderThickness%2A> property of the <xref:System.Windows.Controls.Border>.</span></span>  
  
 <span data-ttu-id="acbae-108">この例は実行できません。</span><span class="sxs-lookup"><span data-stu-id="acbae-108">This example does not run.</span></span>  
  
 [!code-csharp[ThicknessConverter#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ThicknessConverter/CSharp/Window1.xaml.cs#1)]
 [!code-vb[ThicknessConverter#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ThicknessConverter/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="acbae-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="acbae-109">See also</span></span>
- <xref:System.Windows.Thickness>
- <xref:System.Windows.ThicknessConverter>
- <xref:System.Windows.Controls.Border>
- [<span data-ttu-id="acbae-110">方法: Margin プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="acbae-110">How to: Change the Margin Property</span></span>](https://msdn.microsoft.com/library/8a313efd-5f99-4097-b4c1-8fa49d8379a2)
- [<span data-ttu-id="acbae-111">方法: ListBoxItem を新しいデータ型に変換します。</span><span class="sxs-lookup"><span data-stu-id="acbae-111">How to: Convert a ListBoxItem to a new Data Type</span></span>](https://msdn.microsoft.com/library/7a080b88-184e-4b27-bb61-d42bafba9727)
- [<span data-ttu-id="acbae-112">パネルの概要</span><span class="sxs-lookup"><span data-stu-id="acbae-112">Panels Overview</span></span>](../../../../docs/framework/wpf/controls/panels-overview.md)
