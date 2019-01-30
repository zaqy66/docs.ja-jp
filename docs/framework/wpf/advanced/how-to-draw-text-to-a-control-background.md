---
title: '方法: コントロールの背景にテキストを描画する'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], drawing text to backgrounds
- text [WPF], drawing to control backgrounds
- drawing [WPF], text to control backgrounds
- backgrounds [WPF], drawing text to
- typography [WPF], drawing text to control backgrounds
ms.assetid: 686d8fba-f61c-4974-a871-c635d67a7f69
ms.openlocfilehash: 9be4eb92021a62baaf6b43198587616d00cc265e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55259255"
---
# <a name="how-to-draw-text-to-a-controls-background"></a>方法: コントロールの背景にテキストを描画する
コントロールの背景に直接テキストを描画するにはテキスト文字列を変換することで、<xref:System.Windows.Media.FormattedText>オブジェクト、およびコントロールのオブジェクトを描画<xref:System.Windows.Media.DrawingContext>します。 派生したオブジェクトの背景を描画のために、この手法を使用することもできます<xref:System.Windows.Controls.Panel>など<xref:System.Windows.Controls.Canvas>と<xref:System.Windows.Controls.StackPanel>します。  
  
 ![背景にテキストを表示するコントロール](../../../../docs/framework/wpf/advanced/media/drawtext2background01.png "DrawText2Background01")  
カスタム テキスト背景のコントロールの例  
  
## <a name="example"></a>例  
 コントロールの背景を描画するには、新しい作成<xref:System.Windows.Media.DrawingBrush>オブジェクトし、オブジェクトの変換後のテキストを描画<xref:System.Windows.Media.DrawingContext>します。 次に、割り当てる新しい<xref:System.Windows.Media.DrawingBrush>をコントロールの背景のプロパティ。  
  
 次のコード例を作成する方法を示しています、<xref:System.Windows.Media.FormattedText>オブジェクトし、の背景を描画、<xref:System.Windows.Controls.Label>と<xref:System.Windows.Controls.Button>オブジェクト。  
  
 [!code-csharp[DrawTextToControlBackground#DrawTextToControlBackground1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawTextToControlBackground/CSHARP/Window1.xaml.cs#drawtexttocontrolbackground1)]  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Media.FormattedText>
- [書式設定されたテキストの描画](../../../../docs/framework/wpf/advanced/drawing-formatted-text.md)
