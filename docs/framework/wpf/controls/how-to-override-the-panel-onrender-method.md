---
title: '方法: パネルの OnRender メソッドをオーバーライドする'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- overriding OnRender method
- Panel control, overriding OnRender method
- OnRender method
- controls, Panel, overriding OnRender method
helpviewer_keywords:
- overriding OnRender method of Panel control [WPF]
- OnRender method [WPF], overriding
- Panel control [WPF], overriding OnRender method
ms.assetid: 57397834-a085-4e36-90ab-416fad98f341
ms.openlocfilehash: bb2ccffd9eda46eff2c7ee098a5261fc8f128cab
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702874"
---
# <a name="how-to-override-the-panel-onrender-method"></a><span data-ttu-id="766c7-102">方法: パネルの OnRender メソッドをオーバーライドする</span><span class="sxs-lookup"><span data-stu-id="766c7-102">How to: Override the Panel OnRender Method</span></span>
<span data-ttu-id="766c7-103">この例は、オーバーライドする方法を示します、<xref:System.Windows.Controls.Panel.OnRender%2A>メソッドの<xref:System.Windows.Controls.Panel>レイアウト要素にカスタムのグラフィカルな効果を追加するためにします。</span><span class="sxs-lookup"><span data-stu-id="766c7-103">This example shows how to override the <xref:System.Windows.Controls.Panel.OnRender%2A> method of <xref:System.Windows.Controls.Panel> in order to add custom graphical effects to a layout element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="766c7-104">例</span><span class="sxs-lookup"><span data-stu-id="766c7-104">Example</span></span>  
 <span data-ttu-id="766c7-105">使用して、<xref:System.Windows.Controls.Panel.OnRender%2A>表示パネル要素にグラフィック効果を追加するにはメソッドです。</span><span class="sxs-lookup"><span data-stu-id="766c7-105">Use the <xref:System.Windows.Controls.Panel.OnRender%2A> method in order to add graphical effects to a rendered panel element.</span></span> <span data-ttu-id="766c7-106">たとえば、このメソッドを使用すると、カスタム境界線や背景の効果を追加します。</span><span class="sxs-lookup"><span data-stu-id="766c7-106">For example, you can use this method to add custom border or background effects.</span></span> <span data-ttu-id="766c7-107">A<xref:System.Windows.Media.DrawingContext>オブジェクトは、図形、テキスト、画像、またはビデオを描画するためのメソッドを提供する引数として渡されます。</span><span class="sxs-lookup"><span data-stu-id="766c7-107">A <xref:System.Windows.Media.DrawingContext> object is passed as an argument, which provides methods for drawing shapes, text, images, or videos.</span></span> <span data-ttu-id="766c7-108">その結果、このメソッドは、パネル オブジェクトのカスタマイズに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="766c7-108">As a result, this method is useful for customization of a panel object.</span></span>  
  
 [!code-csharp[LightWeightCustomPanel#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LightWeightCustomPanel/CSharp/OffsetPanel.cs#1)]
 [!code-vb[LightWeightCustomPanel#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/LightWeightCustomPanel/visualbasic/offsetpanel.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="766c7-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="766c7-109">See also</span></span>
- <xref:System.Windows.Controls.Panel>
- [<span data-ttu-id="766c7-110">パネルの概要</span><span class="sxs-lookup"><span data-stu-id="766c7-110">Panels Overview</span></span>](../../../../docs/framework/wpf/controls/panels-overview.md)
- [<span data-ttu-id="766c7-111">カスタム放射状パネルのサンプル</span><span class="sxs-lookup"><span data-stu-id="766c7-111">Custom Radial Panel Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=159982)
- [<span data-ttu-id="766c7-112">方法トピック</span><span class="sxs-lookup"><span data-stu-id="766c7-112">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/panel-how-to-topics.md)
