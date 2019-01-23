---
title: '方法: コードを使用してイベント ハンドラーを追加する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- event handlers [WPF], adding
- XAML [WPF], adding event handlers
ms.assetid: 269c61e0-6bd9-4291-9bed-1c5ee66da486
ms.openlocfilehash: 4e8344ebcb0406a7da29787c5a4377760f55597e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499133"
---
# <a name="how-to-add-an-event-handler-using-code"></a>方法: コードを使用してイベント ハンドラーを追加する
この例では、コードを使用して要素にイベント ハンドラーを追加する方法を示します。  
  
 イベント ハンドラーを追加する場合、[!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]要素と、要素を含むマークアップ ページが読み込まれた既に、コードを使用してハンドラーを追加する必要があります。 または、まったくコードを使用してとを使用して任意の要素が宣言されていないアプリケーションの要素ツリーを構築するかどうか[!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]、構築される要素ツリーにイベント ハンドラーを追加する特定のメソッドを呼び出すことができます。  
  
## <a name="example"></a>例  
 次の例は、新しい追加<xref:System.Windows.Controls.Button>で最初に定義されている既存のページに[!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]します。 分離コード ファイルは、イベント ハンドラー メソッドを実装してに新しいイベント ハンドラーとしてそのメソッドを追加、<xref:System.Windows.Controls.Button>します。  
  
 C#の例では、`+=`演算子をイベントにハンドラーを割り当てます。 これは、のハンドラーを割り当てるために使用する演算子と同じ、[!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)]イベント モデルを処理します。 Microsoft Visual Basic では、イベント ハンドラーを追加するための手段としてこの演算子はサポートされません。 代わりに、2 つの手法の 1 つ必要です。  
  
-   使用して、<xref:System.Windows.UIElement.AddHandler%2A>メソッド、と共に、`AddressOf`演算子、イベント ハンドラーの実装を参照します。  
  
-   使用して、`Handles`イベント ハンドラーの定義の一部としてキーワード。 この手法はここでは表示されません。参照してください[Visual Basic と WPF のイベント処理](../../../../docs/framework/wpf/advanced/visual-basic-and-wpf-event-handling.md)します。  
  
 [!code-xaml[RoutedEventAddRemoveHandler#XAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventAddRemoveHandler/CSharp/default.xaml#xaml)]  
  
 [!code-csharp[RoutedEventAddRemoveHandler#Handler](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventAddRemoveHandler/CSharp/default.xaml.cs#handler)]
 [!code-vb[RoutedEventAddRemoveHandler#Handler](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/RoutedEventAddRemoveHandler/VisualBasic/default.xaml.vb#handler)]  
  
> [!NOTE]
>  最初に解析済みのイベント ハンドラーの追加[!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]ページははるかに簡単です。 イベント ハンドラーを追加するオブジェクトの要素内で処理するイベントの名前に一致する属性を追加します。 分離コード ファイルで定義されているイベント ハンドラー メソッドの名前とその属性の値を指定し、[!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]ページ。 詳細については、次を参照してください。 [XAML の概要 (WPF)](../../../../docs/framework/wpf/advanced/xaml-overview-wpf.md)または[ルーティング イベントの概要](../../../../docs/framework/wpf/advanced/routed-events-overview.md)します。  
  
## <a name="see-also"></a>関連項目
- [ルーティング イベントの概要](../../../../docs/framework/wpf/advanced/routed-events-overview.md)
- [方法トピック](../../../../docs/framework/wpf/advanced/events-how-to-topics.md)
