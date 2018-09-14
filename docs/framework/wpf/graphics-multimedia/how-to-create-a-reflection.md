---
title: '方法 : 反射を作成する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- creating reflections [WPF]
- brushes [WPF], creating reflections
- reflections [WPF], creating
ms.assetid: 4f017e16-ab80-43c7-98df-03b6bddbb203
ms.openlocfilehash: 716adff5c5c41e6601e384b6669516cb6ba1041d
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/14/2018
ms.locfileid: "45596638"
---
# <a name="how-to-create-a-reflection"></a><span data-ttu-id="2c36e-102">方法 : 反射を作成する</span><span class="sxs-lookup"><span data-stu-id="2c36e-102">How to: Create a Reflection</span></span>
<span data-ttu-id="2c36e-103">この例は、使用する方法を示します、<xref:System.Windows.Media.VisualBrush>反射を作成します。</span><span class="sxs-lookup"><span data-stu-id="2c36e-103">This example shows how to use a <xref:System.Windows.Media.VisualBrush> to create a reflection.</span></span> <span data-ttu-id="2c36e-104"><xref:System.Windows.Media.VisualBrush>既存のビジュアルを表示することができます、反射や拡大などの興味深い視覚効果を生成するために、この機能を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="2c36e-104">Because a <xref:System.Windows.Media.VisualBrush> can display an existing visual, you can use this capability to produce interesting visual effects, such as reflections and magnification.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2c36e-105">例</span><span class="sxs-lookup"><span data-stu-id="2c36e-105">Example</span></span>  
 <span data-ttu-id="2c36e-106">次の例では、<xref:System.Windows.Media.VisualBrush>の反射を作成、<xref:System.Windows.Controls.Border>いくつかの要素を格納しています。</span><span class="sxs-lookup"><span data-stu-id="2c36e-106">The following example uses a <xref:System.Windows.Media.VisualBrush> to create a reflection of a <xref:System.Windows.Controls.Border> that contains several elements.</span></span> <span data-ttu-id="2c36e-107">次の図は、この例で生成される出力を示しています。</span><span class="sxs-lookup"><span data-stu-id="2c36e-107">The following illustration shows the output that this example produces.</span></span>  
  
 <span data-ttu-id="2c36e-108">![A がビジュアル オブジェクトを反映](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-visualbrush-reflection-small.jpg "graphicsmm_visualbrush_reflection_small")</span><span class="sxs-lookup"><span data-stu-id="2c36e-108">![A reflected Visual object](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-visualbrush-reflection-small.jpg "graphicsmm_visualbrush_reflection_small")</span></span>  
<span data-ttu-id="2c36e-109">反映された Visual オブジェクト</span><span class="sxs-lookup"><span data-stu-id="2c36e-109">A reflected Visual object</span></span>  
  
 [!code-csharp[visualbrush_markup_snip#GraphicsMMVisualBrushReflectionExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/visualbrush_markup_snip/CSharp/ReflectionExample.cs#graphicsmmvisualbrushreflectionexamplewholepage)]
 [!code-vb[visualbrush_markup_snip#GraphicsMMVisualBrushReflectionExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/visualbrush_markup_snip/visualbasic/reflectionexample.vb#graphicsmmvisualbrushreflectionexamplewholepage)]
 [!code-xaml[visualbrush_markup_snip#GraphicsMMVisualBrushReflectionExampleWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/visualbrush_markup_snip/XAML/ReflectionExample.xaml#graphicsmmvisualbrushreflectionexamplewholepage)]  
  
 <span data-ttu-id="2c36e-110">画面の一部を拡大する方法と反射を作成する方法を示す例が含まれているサンプル全体については、次を参照してください。 [VisualBrush のサンプル](https://go.microsoft.com/fwlink/?LinkID=160049)します。</span><span class="sxs-lookup"><span data-stu-id="2c36e-110">For the complete sample, which includes examples that show how to magnify parts of the screen and how to create reflections, see [VisualBrush Sample](https://go.microsoft.com/fwlink/?LinkID=160049).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c36e-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c36e-111">See Also</span></span>  
 <xref:System.Windows.Media.VisualBrush>  
 [<span data-ttu-id="2c36e-112">イメージ、描画、およびビジュアルによる塗りつぶし</span><span class="sxs-lookup"><span data-stu-id="2c36e-112">Painting with Images, Drawings, and Visuals</span></span>](../../../../docs/framework/wpf/graphics-multimedia/painting-with-images-drawings-and-visuals.md)
