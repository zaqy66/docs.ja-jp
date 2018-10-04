---
title: '方法 : オブジェクトに複数の変換を適用する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- grouping Transform objects [WPF]
- Transform objects [WPF], grouping
- graphics [WPF], grouping Transform objects
- TransformGroup [WPF]
ms.assetid: 98cd1921-12bc-4bf5-8193-529228fb7402
ms.openlocfilehash: 0700a7ae3f18f745b0d479ace3acbf2d7fbd9722
ms.sourcegitcommit: 700b9003ea6bdd83a53458bbc436c9b5778344f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48265952"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a>方法 : オブジェクトに複数の変換を適用する
この例は、使用する方法を示します、<xref:System.Windows.Media.TransformGroup>を 2 つ以上のグループに<xref:System.Windows.Media.Transform>に 1 つの複合オブジェクト<xref:System.Windows.Media.Transform>します。  
  
## <a name="example"></a>例  
 次の例では、<xref:System.Windows.Media.TransformGroup>を適用する、<xref:System.Windows.Media.ScaleTransform>と<xref:System.Windows.Media.RotateTransform>を<xref:System.Windows.Controls.Button>します。  
  
 [!code-xaml[Transforms_snip#MultipleTransformExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/MultipleTransformExample.xaml#multipletransformexamplewholepage)]  
  
 [!code-csharp[Transforms_Procedural_snip#MultipleTransformsCodeExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/MultipleTransformsExample.cs#multipletransformscodeexamplewholepage)]
 [!code-vb[Transforms_Procedural_snip#MultipleTransformsCodeExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/MultipleTransformsExample.vb#multipletransformscodeexamplewholepage)]  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Windows.UIElement.RenderTransform%2A>  
 <xref:System.Windows.Media.TransformGroup>  
 [変換の概要](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)  
 [2-D 変換のサンプル](https://go.microsoft.com/fwlink/?LinkID=158252)
