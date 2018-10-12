---
title: WPF コントロールの使用
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms Designer [Windows Forms], interoperability with WPF
- interoperability [WPF]
ms.assetid: 03c85dce-26ad-44cd-bc1d-8e0cb56de096
ms.openlocfilehash: be925bdceea3dd01c568d85fe025d6e037066454
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2018
ms.locfileid: "48841619"
---
# <a name="using-wpf-controls"></a>WPF コントロールの使用
Windows フォーム ベースのアプリケーションでは、Windows Presentation Foundation (WPF) コントロールを使用できます。 これらは、2 つの異なるビュー テクノロジが円滑に相互運用します。  
  
 Windows フォーム デザイナーでは、Windows Presentation Foundation コントロールをホストするためのビジュアル デ ザイン環境を提供します。 WPF コントロールがという特殊な Windows フォーム コントロールによってホストされている<xref:System.Windows.Forms.Integration.ElementHost>します。 このコントロールは、フォームのレイアウトに参加して、キーボードとマウスのメッセージを受信する WPF コントロールを使用します。 デザイン時に配置することができます、<xref:System.Windows.Forms.Integration.ElementHost>任意の Windows フォーム コントロールと同様に制御します。  
  
 Windows フォーム コントロールは WPF ベースのアプリケーションで使用することもできます。 詳細については、次を参照してください。 [Visual Studio で XAML をデザイン](/visualstudio/designers/designing-xaml-in-visual-studio)します。  
  
## <a name="in-this-section"></a>このセクションの内容  
 [方法: デザイン時に ElementHost コントロールをコピーして貼り付ける](../../../../docs/framework/winforms/advanced/how-to-copy-and-paste-an-elementhost-control-at-design-time.md)  
 Windows フォーム上の Windows Presentation Foundation コントロールをコピーする方法を示します。  
  
 [チュートリアル: デザイン時の Windows フォームでの WPF コンテンツの配置](../../../../docs/framework/winforms/advanced/walkthrough-arranging-wpf-content-on-windows-forms-at-design-time.md)  
 固定やスナップ線をなど、Windows フォームのレイアウト機能を使用して、Windows Presentation Foundation コントロールを配置する方法を示しています。
  
 [チュートリアル: デザイン時の Windows フォームでの新しい WPF コンテンツの作成](../../../../docs/framework/winforms/advanced/walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md)  
 Windows フォーム ベースのアプリケーションで使用するための Windows Presentation Foundation コントロールを作成する方法を示します。
  
 [チュートリアル: デザイン時の Windows フォームでの WPF コンテンツの割り当て](../../../../docs/framework/winforms/advanced/walkthrough-assigning-wpf-content-on-windows-forms-at-design-time.md)  
 フォームに表示する Windows Presentation Foundation コントロールの種類を選択する方法を示します。  
  
 [チュートリアル: WPF コンテンツへのスタイルの適用](../../../../docs/framework/winforms/advanced/walkthrough-styling-wpf-content.md)  
 Windows フォーム デザイナー間のワークフローを示しています、 [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)] Windows Presentation Foundation コントロールにスタイルを適用するためです。  
  
## <a name="reference"></a>参照  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 Windows フォーム ベースのアプリケーションでホストの Windows Presentation Foundation コントロールに使用できるクラスについて説明します。  
  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 Windows フォーム コントロールをホストする Windows Presentation Foundation ベースのアプリケーションで使用できるクラスについて説明します。  
  
## <a name="related-sections"></a>関連項目  
 [移行と相互運用性](../../../../docs/framework/wpf/advanced/migration-and-interoperability.md)  
 Windows Presentation Foundation と Windows フォーム テクノロジ間の相互運用をについて説明します。  
  
 [Visual Studio で XAML をデザインする](/visualstudio/designers/designing-xaml-in-visual-studio)  
 Visual Studio での Windows Presentation Foundation コントロールをデザインする方法について説明します。
