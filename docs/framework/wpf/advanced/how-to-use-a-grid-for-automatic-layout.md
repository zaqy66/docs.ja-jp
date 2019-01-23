---
title: '方法: 自動レイアウト用のグリッドを使用する'
ms.date: 03/30/2017
helpviewer_keywords:
- grids [WPF], automatic layout
- automatic layout [WPF], grid use
ms.assetid: ab9de407-e0c1-4047-bdf0-24951bf73879
ms.openlocfilehash: 0eda70a7d8cc5abb70b5043cbaa1d4fc418bb1f4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54611424"
---
# <a name="how-to-use-a-grid-for-automatic-layout"></a>方法: 自動レイアウト用のグリッドを使用する
この例では、自動レイアウトの方法でグリッドを使用して、ローカライズ可能なアプリケーションを作成する方法について説明します。  
  
 ローカライズ、[!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)]時間がかかることができます。 多くの場合、ローカライザーは、テキストの翻訳だけでなく、要素のサイズ変更や位置変更を行う必要もあります。 過去の各言語を[!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)]が必要な調整を変更します。 機能を今すぐ[!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)]調整の必要性が軽減される要素を設計することができます。 簡単にサイズが変更および位置が変更された可能性のあるアプリケーションの作成方法と呼びます`auto layout`します。  
  
 次[!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]ボタンとテキストを配置するグリッドを使用する例を示します。 セルの幅と高さに設定されている通知`Auto`; イメージ付きのボタンを含むセルをそのため、イメージに合わせて調整します。 <xref:System.Windows.Controls.Grid>要素がローカライズされるアプリケーションの設計に自動レイアウトの方法を作成する際は、便利にすることができます、そのコンテンツを調整できます。  
  
## <a name="example"></a>例  
 次の例では、グリッドを使用する方法を示します。  
  
 [!code-xaml[LocalizationGrid#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LocalizationGrid/CS/Pane1.xaml#1)]  
  
 次の図は、コード サンプルの出力を示しています。  
  
 ![グリッドの例](../../../../docs/framework/wpf/advanced/media/glob-grid.png "glob_grid")  
グリッド  
  
## <a name="see-also"></a>関連項目
- [自動レイアウトの使用の概要](../../../../docs/framework/wpf/advanced/use-automatic-layout-overview.md)
- [自動レイアウトを使用してボタンを作成する](../../../../docs/framework/wpf/advanced/how-to-use-automatic-layout-to-create-a-button.md)
