---
title: '方法: イメージを持つ Button を作成する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Button controls [WPF], creating
ms.assetid: 607a193c-4098-4dd8-8dc0-51256cec2020
ms.openlocfilehash: cfebe53047531ecddde42a3a0596dfd949629ecd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54682063"
---
# <a name="how-to-create-a-button-that-has-an-image"></a>方法: イメージを持つ Button を作成する
この例の画像を含める方法を示しています、<xref:System.Windows.Controls.Button>します。  
  
## <a name="example"></a>例  
 次の例では、2 つ作成されます<xref:System.Windows.Controls.Button>コントロール。 1 つ<xref:System.Windows.Controls.Button>テキストを含む、他のイメージが含まれています。 イメージは、例のプロジェクト フォルダーのサブフォルダーであるデータをという名前のフォルダーです。 ユーザーがクリックすると、<xref:System.Windows.Controls.Button>イメージ、バック グラウンド、およびその他のテキストを持つ<xref:System.Windows.Controls.Button>を変更します。  
  
 この例で作成<xref:System.Windows.Controls.Button>マークアップを使用して制御しますが、コードを使用して書き込む、<xref:System.Windows.Controls.Primitives.ButtonBase.Click>イベント ハンドラー。  
  
 [!code-xaml[BtnColor#4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BtnColor/CSharp/Pane1.xaml#4)]  
  
 [!code-csharp[BtnColor#6](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BtnColor/CSharp/Pane1.xaml.cs#6)]
 [!code-vb[BtnColor#6](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BtnColor/VisualBasic/Pane1.xaml.vb#6)]  
  
## <a name="see-also"></a>関連項目
- [コントロール](../../../../docs/framework/wpf/controls/index.md)
- [コントロール ライブラリ](../../../../docs/framework/wpf/controls/control-library.md)
