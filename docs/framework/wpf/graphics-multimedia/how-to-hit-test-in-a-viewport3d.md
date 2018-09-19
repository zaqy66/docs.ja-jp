---
title: '方法 : Viewport3D でヒット テストを実行する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- 3-D visuals [WPF], hit-testing for
- hit tests [WPF], for 3-D visuals
- Viewport3D [WPF]
ms.assetid: 42bfbd99-c7c6-43f1-940b-90448faa412e
ms.openlocfilehash: 297fe17b8844f7542255afcfe442fbf9b7a0d59d
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/18/2018
ms.locfileid: "46003920"
---
# <a name="how-to-hit-test-in-a-viewport3d"></a><span data-ttu-id="87ecd-102">方法 : Viewport3D でヒット テストを実行する</span><span class="sxs-lookup"><span data-stu-id="87ecd-102">How to: Hit Test in a Viewport3D</span></span>
<span data-ttu-id="87ecd-103">この例では、ヒット テストでの 3D ビジュアルの<xref:System.Windows.Controls.Viewport3D>します。</span><span class="sxs-lookup"><span data-stu-id="87ecd-103">This example shows how to hit test for 3D Visuals in a <xref:System.Windows.Controls.Viewport3D>.</span></span>  
  
 <span data-ttu-id="87ecd-104"><xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> 2D および 3D の情報を返します 3D のみの結果を確認するテスト結果を反復処理することができます。</span><span class="sxs-lookup"><span data-stu-id="87ecd-104">Because <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> returns 2D and 3D information, it is possible to iterate through the test results to read only 3D results.</span></span>  
  
 [!code-csharp[HitTest3D#HitTest3D3DN4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HitTest3D/CSharp/Window1.xaml.cs#hittest3d3dn4)]
 [!code-vb[HitTest3D#HitTest3D3DN4](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HitTest3D/visualbasic/window1.xaml.vb#hittest3d3dn4)]  
  
 <span data-ttu-id="87ecd-105"><xref:System.Windows.Media.HitTestResultBehavior>次のコードでヒット テストの結果を処理する方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="87ecd-105">The <xref:System.Windows.Media.HitTestResultBehavior> in the following code determines how the hit test results are processed.</span></span>  <span data-ttu-id="87ecd-106">`UpdateResultInfo` `UpdateMaterial`はローカルに定義されたメソッド。</span><span class="sxs-lookup"><span data-stu-id="87ecd-106">`UpdateResultInfo` and `UpdateMaterial` are locally defined methods.</span></span>  
  
 [!code-csharp[HitTest3D#HitTest3D3DN5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HitTest3D/CSharp/Window1.xaml.cs#hittest3d3dn5)]
 [!code-vb[HitTest3D#HitTest3D3DN5](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HitTest3D/visualbasic/window1.xaml.vb#hittest3d3dn5)]  
  
## <a name="see-also"></a><span data-ttu-id="87ecd-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="87ecd-107">See Also</span></span>  
 [<span data-ttu-id="87ecd-108">3-D のヒット テストのサンプル</span><span class="sxs-lookup"><span data-stu-id="87ecd-108">3-D Hit Testing Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=159959)
