---
title: '方法: ローカリゼーションに対応する Windows フォーム レイアウトをデザインします。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms]
- application design [Windows Forms], localization
- Windows Forms, localization
- localization [Windows Forms], Windows Forms layout
ms.assetid: d13eff2d-701c-4b6e-8838-3885cbfb7223
ms.openlocfilehash: 15f290f7d076eede7a8092d7295df810e4e51bf3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54563523"
---
# <a name="how-to-design-a-windows-forms-layout-that-responds-well-to-localization"></a>方法: ローカリゼーションに対応する Windows フォーム レイアウトをデザインします。
ローカライズが可能なフォームを作成すると、各国市場向けの開発期間が大幅に短縮されます。 <xref:System.Windows.Forms.TableLayoutPanel> コントロールを使用すると、<xref:System.Windows.Forms.Control.Text%2A> プロパティ値の変更によってコントロールのサイズが変更された際に、これに適切に応答するレイアウトを実装できます  
  
## <a name="example"></a>例  
 このフォームでは、表示される文字列値を他の言語に翻訳するときに、均等に調整されるレイアウトを作成する方法を示します。 この翻訳プロセスのことを "*ローカリゼーション*" といいます。 詳細については、「[ローカリゼーション](../../../../docs/standard/globalization-localization/localization.md)」を参照してください。  
  
 Visual Studio では、このタスクに対する広範なサポートが用意されています。  参照してください[チュートリアル。ローカライズの縦横比が調整されるレイアウトの作成](https://msdn.microsoft.com/library/7k9fa71y\(v=vs.110\))です。  
  
 [!code-csharp[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/CS/localizableform.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/VB/localizableform.vb#1)]  
  
1.  [方法: 配置して、コントロールを TableLayoutPanel コントロールで伸縮](how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control.md)  
  
2.  [チュートリアル: FlowLayoutPanel を使用して Windows フォーム コントロールの配置](https://msdn.microsoft.com/library/z9w7ek2f\(v=vs.110\))  
  
3.  [方法: TableLayoutPanel コントロールの行と列にまたがる](how-to-span-rows-and-columns-in-a-tablelayoutpanel-control.md)  
  
4.  [方法: TableLayoutPanel コントロールの列と行を編集します。](how-to-edit-columns-and-rows-in-a-tablelayoutpanel-control.md)  
  
5.  [チュートリアル: スマートを使用して一般的なタスクを実行する Windows フォーム コントロールをタグ](https://msdn.microsoft.com/library/xhz359sc\(v=vs.110\))  
  
6.  [チュートリアル: TableLayoutPanel を使用して Windows フォーム コントロールの配置](https://msdn.microsoft.com/library/w4yc3e8c\(v=vs.110\))  
  
7.  [チュートリアル: Windows フォーム コントロール Padding、Margin、および AutoSize プロパティをレイアウト](https://msdn.microsoft.com/library/3z3f9e8b\(v=vs.110\))  
  
8.  [方法: AutoSize と TableLayoutPanel コントロールを使用して Windows フォームのローカリゼーションをサポートします。](https://msdn.microsoft.com/library/1zkt8b33\(v=vs.110\))  
  
9. [チュートリアル: データ エントリのサイズ変更可能な Windows フォームを作成します。](https://msdn.microsoft.com/library/991eahec\(v=vs.110\))  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 この例で必要な要素は次のとおりです。  
  
-   System、System.Data、System.Drawing、および System.Windows.Forms の各アセンブリへの参照。  
  
 コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。 新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。  参照してください[方法。Visual Studio を使用して、完全な Windows フォームのコードの例をコンパイルして](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))します。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.TableLayoutPanel>
- <xref:System.Windows.Forms.FlowLayoutPanel>
- [ローカリゼーション](../../../../docs/standard/globalization-localization/localization.md)
