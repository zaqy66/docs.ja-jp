---
title: '方法: MatrixTransform を使用してカスタム変換を作成する'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], custom Transforms
ms.assetid: 919381ca-989f-47cf-86b4-1094060236e4
ms.openlocfilehash: 3b5a6fbedd30c859dffadad00c8faab74fc0773b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54628800"
---
# <a name="how-to-use-a-matrixtransform-to-create-custom-transforms"></a><span data-ttu-id="9bef0-102">方法: MatrixTransform を使用してカスタム変換を作成する</span><span class="sxs-lookup"><span data-stu-id="9bef0-102">How to: Use a MatrixTransform to Create Custom Transforms</span></span>
<span data-ttu-id="9bef0-103">この例は、使用する方法を示します、<xref:System.Windows.Media.MatrixTransform>変換 (移動) する位置を stretch との差を<xref:System.Windows.Controls.Button>します。</span><span class="sxs-lookup"><span data-stu-id="9bef0-103">This example shows how to use a <xref:System.Windows.Media.MatrixTransform> to translate (move) the position, stretch, and skew of a <xref:System.Windows.Controls.Button>.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9bef0-104">使用、<xref:System.Windows.Media.MatrixTransform>によって提供されないカスタム変換を作成するクラス、 <xref:System.Windows.Media.RotateTransform>、 <xref:System.Windows.Media.SkewTransform>、 <xref:System.Windows.Media.ScaleTransform>、または<xref:System.Windows.Media.TranslateTransform>のクラス。</span><span class="sxs-lookup"><span data-stu-id="9bef0-104">Use the <xref:System.Windows.Media.MatrixTransform> class to create custom transformations that are not provided by the <xref:System.Windows.Media.RotateTransform>, <xref:System.Windows.Media.SkewTransform>, <xref:System.Windows.Media.ScaleTransform>, or <xref:System.Windows.Media.TranslateTransform> classes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9bef0-105">例</span><span class="sxs-lookup"><span data-stu-id="9bef0-105">Example</span></span>  
 [!code-xaml[Transforms_snip#MatrixTransform](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/MatrixTransformExample.xaml#matrixtransform)]  
  
## <a name="see-also"></a><span data-ttu-id="9bef0-106">関連項目</span><span class="sxs-lookup"><span data-stu-id="9bef0-106">See also</span></span>
- <xref:System.Windows.Media.MatrixTransform>
- <xref:System.Windows.Media.Transform>
- [<span data-ttu-id="9bef0-107">変換の概要</span><span class="sxs-lookup"><span data-stu-id="9bef0-107">Transforms Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
- [<span data-ttu-id="9bef0-108">方法トピック</span><span class="sxs-lookup"><span data-stu-id="9bef0-108">How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/transformations-how-to-topics.md)
- [<span data-ttu-id="9bef0-109">WPF での図形と基本描画の概要</span><span class="sxs-lookup"><span data-stu-id="9bef0-109">Shapes and Basic Drawing in WPF Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/shapes-and-basic-drawing-in-wpf-overview.md)
