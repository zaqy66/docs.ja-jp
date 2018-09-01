---
title: '方法 : フォームに標準メニュー項目を追加する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- menu items [Windows Forms], standard
- ToolStrip control [Windows Forms]
ms.assetid: 75db9126-e70c-4e81-921d-b83c0a4a9f50
ms.openlocfilehash: bf43d27ed728d11b5cde5b9250cfc4614077ed94
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43395710"
---
# <a name="how-to-provide-standard-menu-items-to-a-form"></a>方法 : フォームに標準メニュー項目を追加する
フォームの標準のメニューを <xref:System.Windows.Forms.MenuStrip> コントロールに提供できます。  
  
 Visual Studio でこの機能の広範なサポートがあります。  
  
 「[チュートリアル: 標準メニュー項目をフォームに用意する](walkthrough-providing-standard-menu-items-to-a-form.md)」も参照してください。  
  
## <a name="example"></a>例  
 <xref:System.Windows.Forms.MenuStrip> コントロールを使用して標準メニューを持つフォームを作成する方法を、次のコード例に示します。 メニュー項目の選択は、<xref:System.Windows.Forms.StatusStrip> コントロールに表示されます。  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.StandardMenu#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.StandardMenu#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 この例で必要な要素は次のとおりです。  
  
-   System、System.Drawing、および System.Windows.Forms の各アセンブリへの参照。  
  
 コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。 新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。  「[方法: 完成した Windows フォーム コードの例を Visual Studio を使ってコンパイルして実行する](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))」も参照してください。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Windows.Forms.MenuStrip>  
 <xref:System.Windows.Forms.ToolStrip>  
 <xref:System.Windows.Forms.StatusStrip>  
 [MenuStrip コントロール](../../../../docs/framework/winforms/controls/menustrip-control-windows-forms.md)
