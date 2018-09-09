---
title: '方法 : GroupBox テンプレートを定義する'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], GroupBox
- GroupBox control [WPF], creating templates
ms.assetid: 85a4d1a7-4753-4f4a-b26d-14fa10c1ddb5
ms.openlocfilehash: a47ce896be4d1c38147584dd80b1bc841737d526
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2018
ms.locfileid: "44227023"
---
# <a name="how-to-define-a-groupbox-template"></a>方法 : GroupBox テンプレートを定義する
この例のテンプレートを作成する方法を示しています、<xref:System.Windows.Controls.GroupBox>コントロール。  
  
## <a name="example"></a>例  
 次の例では、定義、<xref:System.Windows.Controls.GroupBox>コントロール テンプレートを使用して、<xref:System.Windows.Controls.Grid>レイアウトを制御します。 テンプレートを使用して、<xref:System.Windows.Controls.BorderGapMaskConverter>の枠線を定義する、<xref:System.Windows.Controls.GroupBox>境界線が見えにくくならないように、<xref:System.Windows.Controls.HeaderedContentControl.Header%2A>コンテンツ。  
  
 [!code-xaml[GroupBoxSnippet#GroupBoxTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GroupBoxSnippet/CS/Window1.xaml#groupboxtemplate)]  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Windows.Controls.GroupBox>  
 [GroupBox の操作方法に関するトピック](https://msdn.microsoft.com/library/7692e155-a4c6-428c-b7e0-64b3740daca7)
