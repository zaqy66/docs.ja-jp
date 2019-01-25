---
title: '方法: GroupBox テンプレートを定義する'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], GroupBox
- GroupBox control [WPF], creating templates
ms.assetid: 85a4d1a7-4753-4f4a-b26d-14fa10c1ddb5
ms.openlocfilehash: 0e1b0487629bba3550a8b6b4a31c163a7ade6a87
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743724"
---
# <a name="how-to-define-a-groupbox-template"></a><span data-ttu-id="115e5-102">方法: GroupBox テンプレートを定義する</span><span class="sxs-lookup"><span data-stu-id="115e5-102">How to: Define a GroupBox Template</span></span>
<span data-ttu-id="115e5-103">この例のテンプレートを作成する方法を示しています、<xref:System.Windows.Controls.GroupBox>コントロール。</span><span class="sxs-lookup"><span data-stu-id="115e5-103">This example shows how to create a template for a <xref:System.Windows.Controls.GroupBox> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="115e5-104">例</span><span class="sxs-lookup"><span data-stu-id="115e5-104">Example</span></span>  
 <span data-ttu-id="115e5-105">次の例では、定義、<xref:System.Windows.Controls.GroupBox>コントロール テンプレートを使用して、<xref:System.Windows.Controls.Grid>レイアウトを制御します。</span><span class="sxs-lookup"><span data-stu-id="115e5-105">The following example defines a <xref:System.Windows.Controls.GroupBox> control template by using a <xref:System.Windows.Controls.Grid> control for layout.</span></span> <span data-ttu-id="115e5-106">テンプレートを使用して、<xref:System.Windows.Controls.BorderGapMaskConverter>の枠線を定義する、<xref:System.Windows.Controls.GroupBox>境界線が見えにくくならないように、<xref:System.Windows.Controls.HeaderedContentControl.Header%2A>コンテンツ。</span><span class="sxs-lookup"><span data-stu-id="115e5-106">The template uses a <xref:System.Windows.Controls.BorderGapMaskConverter> to define the border of the <xref:System.Windows.Controls.GroupBox> so that the border does not obscure the <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> content.</span></span>  
  
 [!code-xaml[GroupBoxSnippet#GroupBoxTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GroupBoxSnippet/CS/Window1.xaml#groupboxtemplate)]  
  
## <a name="see-also"></a><span data-ttu-id="115e5-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="115e5-107">See also</span></span>
- <xref:System.Windows.Controls.GroupBox>
- [<span data-ttu-id="115e5-108">GroupBox の操作方法に関するトピック</span><span class="sxs-lookup"><span data-stu-id="115e5-108">GroupBox How-to Topics</span></span>](https://msdn.microsoft.com/library/7692e155-a4c6-428c-b7e0-64b3740daca7)
