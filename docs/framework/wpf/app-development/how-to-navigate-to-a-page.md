---
title: '方法: ページに移動します'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- pages [WPF], navigating to
- navigation [WPF], to page
ms.assetid: 2a556fc0-748b-417f-a58a-0d05a7afb66f
ms.openlocfilehash: 7b76a12cbe6e1622e5624f5416abf24a4ca292a4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54536911"
---
# <a name="how-to-navigate-to-a-page"></a>方法: ページに移動します
この例で、ページからナビゲートできますをいくつかの方法を示しています、<xref:System.Windows.Navigation.NavigationWindow>します。  
  
## <a name="example"></a>例  
 可能性があります、<xref:System.Windows.Navigation.NavigationWindow>を使用して、次のいずれかのページに移動します。  
  
-   <xref:System.Windows.Navigation.NavigationWindow.Source%2A> プロパティ。  
  
-   <xref:System.Windows.Navigation.NavigationWindow.Navigate%2A> メソッド。  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateToPageCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/MainWindow.xaml.cs#navigatetopagecode)]
 [!code-vb[HOWTONavigationSnippets#NavigateToPageCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/mainwindow.xaml.vb#navigatetopagecode)]  
  
> [!NOTE]
>  [!INCLUDE[TLA#tla_uri#initcap#plural](../../../../includes/tlasharptla-urisharpinitcapsharpplural-md.md)] 相対または絶対のいずれかを指定できます。 詳細については、「[WPF におけるパック URI](../../../../docs/framework/wpf/app-development/pack-uris-in-wpf.md)」を参照してください。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Controls.Frame>
- <xref:System.Windows.Controls.Page>
- <xref:System.Windows.Navigation.NavigationService>
