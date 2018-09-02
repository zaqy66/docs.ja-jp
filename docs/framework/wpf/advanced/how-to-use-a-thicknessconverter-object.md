---
title: '方法 : ThicknessConverter オブジェクトを使用する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- border thickness [WPF]
- ThicknessConverter objects [WPF]
ms.assetid: 52682194-d7fd-499c-8005-73fcc84e7b2c
ms.openlocfilehash: 6c8f9e83468a7b189b96efca2e175c0f3fe0dfff
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43399354"
---
# <a name="how-to-use-a-thicknessconverter-object"></a>方法 : ThicknessConverter オブジェクトを使用する
## <a name="example"></a>例  
 この例のインスタンスを作成する方法を示しています。<xref:System.Windows.ThicknessConverter>境界線の太さを変更するとします。  
  
 例では、呼び出されるカスタム メソッドを定義します`changeThickness`; このメソッドは、最初の内容を変換、<xref:System.Windows.Controls.ListBoxItem>個別で定義されている、[!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]のインスタンスへのファイル<xref:System.Windows.Thickness>、後に、コンテンツに変換します、 <xref:System.String>。 このメソッドは、<xref:System.Windows.Controls.ListBoxItem>に、<xref:System.Windows.ThicknessConverter>オブジェクトで、変換、<xref:System.Windows.Controls.ContentControl.Content%2A>の<xref:System.Windows.Controls.ListBoxItem>のインスタンスに<xref:System.Windows.Thickness>。 この値の値として戻されますが、<xref:System.Windows.Controls.Border.BorderThickness%2A>のプロパティ、<xref:System.Windows.Controls.Border>します。  
  
 この例は実行できません。  
  
 [!code-csharp[ThicknessConverter#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ThicknessConverter/CSharp/Window1.xaml.cs#1)]
 [!code-vb[ThicknessConverter#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ThicknessConverter/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Windows.Thickness>  
 <xref:System.Windows.ThicknessConverter>  
 <xref:System.Windows.Controls.Border>  
 [方法: Margin プロパティの変更](https://msdn.microsoft.com/library/8a313efd-5f99-4097-b4c1-8fa49d8379a2)  
 [方法: ListBoxItem を新しいデータ型に変換します。](https://msdn.microsoft.com/library/7a080b88-184e-4b27-bb61-d42bafba9727)  
 [パネルの概要](../../../../docs/framework/wpf/controls/panels-overview.md)
