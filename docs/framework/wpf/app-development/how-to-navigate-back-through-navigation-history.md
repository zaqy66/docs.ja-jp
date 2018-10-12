---
title: '方法: ナビゲーション履歴を後方に移動'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- history [WPF], navigating back
- navigation [WPF], through navigation history (back)
ms.assetid: 9343234b-d864-441d-b8a7-d895cba80a87
ms.openlocfilehash: 7266c9486524e962a859c34c9be5ab8f6d7bf7d5
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47199321"
---
# <a name="how-to-navigate-back-through-navigation-history"></a>方法: ナビゲーション履歴を後方に移動
この例では、ナビゲーション履歴を戻るエントリに移動する方法を示します。  
  
## <a name="example"></a>例  
 ホストされているコンテンツから実行されているコードを<xref:System.Windows.Navigation.NavigationWindow>、<xref:System.Windows.Controls.Frame>を使用して<xref:System.Windows.Navigation.NavigationService>、または[!INCLUDE[TLA#tla_iegeneric](../../../../includes/tlasharptla-iegeneric-md.md)]ナビゲーション履歴に、一度に 1 つのエントリを後方に移動できます。  
  
 1 エントリは、最初にチェックを調べることによってナビゲーションの履歴にエントリが表示ことが必要です、 **CanGoBack**プロパティ、1 つのエントリを呼び出すことによってバックアップを移動する前に、 **GoBack**メソッド。 これは、次の例に示します。  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateBackCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigatebackcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateBackCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigatebackcode)]  
  
 **CanGoBack**と**GoBack**によって実装される<xref:System.Windows.Navigation.NavigationWindow>、 <xref:System.Windows.Controls.Frame>、および<xref:System.Windows.Navigation.NavigationService>します。  
  
> [!NOTE]
>  呼び出す場合**GoBack**、戻るナビゲーション履歴にエントリがないと、<xref:System.InvalidOperationException>が発生します。
