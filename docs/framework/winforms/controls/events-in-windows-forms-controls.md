---
title: Windows フォーム コントロールのイベント
ms.date: 03/30/2017
helpviewer_keywords:
- events [Windows Forms], custom controls (using code)
- custom controls [Windows Forms], events overview (using code)
ms.assetid: 7e3d1379-87aa-437c-afce-c99454eff30e
ms.openlocfilehash: 56de08f039fd4dee9dcc5a1b3f86cc0e8e577b43
ms.sourcegitcommit: acd8ed14fe94e9d4e3a7fb685fe83d05e941073c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/20/2019
ms.locfileid: "56442439"
---
# <a name="events-in-windows-forms-controls"></a>Windows フォーム コントロールのイベント
Windows フォーム コントロールを継承から 60 を超えるイベント<xref:System.Windows.Forms.Control?displayProperty=nameWithType>します。 以下の<xref:System.Windows.Forms.Control.Paint>イベント、コントロールを描画する、ウィンドウの表示などに関連するイベント、<xref:System.Windows.Forms.Control.Resize>と<xref:System.Windows.Forms.Control.Layout>イベント、および低レベルのマウスとキーボード イベント。 一部の下位イベントは合成<xref:System.Windows.Forms.Control>などのセマンティック イベントに<xref:System.Windows.Forms.Control.Click>と<xref:System.Windows.Forms.Control.DoubleClick>します。 詳細については、継承されたイベントは、次を参照してください。<xref:System.Windows.Forms.Control>します。  
  
 継承されたイベントの機能をカスタム コントロールでオーバーライドする必要がある場合、デリゲートを結び付けるのではなく、継承された `On`*EventName* メソッドをオーバーライドします。 .NET Framework でのイベント モデルに詳しくない場合は、「[コンポーネントからのイベントの生成](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120))」を参照してください。  
  
## <a name="see-also"></a>関連項目
- [OnPaint メソッドのオーバーライド](../../../../docs/framework/winforms/controls/overriding-the-onpaint-method.md)
- [ユーザーの入力の処理](../../../../docs/framework/winforms/controls/handling-user-input.md)
- [イベントの定義](../../../../docs/framework/winforms/controls/defining-an-event-in-windows-forms-controls.md)
- [イベント](../../../../docs/standard/events/index.md)
