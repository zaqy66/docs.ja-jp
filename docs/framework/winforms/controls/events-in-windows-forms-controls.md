---
title: Windows フォーム コントロールのイベント
ms.date: 03/30/2017
helpviewer_keywords:
- events [Windows Forms], custom controls (using code)
- custom controls [Windows Forms], events overview (using code)
ms.assetid: 7e3d1379-87aa-437c-afce-c99454eff30e
ms.openlocfilehash: d18938565c302be085b7ac51f878d83ae5ab533d
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/13/2018
ms.locfileid: "45560176"
---
# <a name="events-in-windows-forms-controls"></a>Windows フォーム コントロールのイベント
Windows フォーム コントロールを継承から 60 を超えるイベント<xref:System.Windows.Forms.Control?displayProperty=nameWithType>します。 以下の<xref:System.Windows.Forms.Control.Paint>イベント、コントロールを描画する、ウィンドウの表示などに関連するイベント、<xref:System.Windows.Forms.Control.Resize>と<xref:System.Windows.Forms.Control.Layout>イベント、および低レベルのマウスとキーボード イベント。 一部の下位イベントは合成<xref:System.Windows.Forms.Control>などのセマンティック イベントに<xref:System.Windows.Forms.Control.Click>と<xref:System.Windows.Forms.Control.DoubleClick>します。 詳細については、継承されたイベントは、次を参照してください。<xref:System.Windows.Forms.Control>します。  
  
 継承されたイベントの機能をカスタム コントロールでオーバーライドする必要がある場合、デリゲートを結び付けるのではなく、継承された `On`*EventName* メソッドをオーバーライドします。 .NET Framework でのイベント モデルに詳しくない場合は、「[コンポーネントからのイベントの生成](https://msdn.microsoft.com/library/9aebf605-a87d-470b-b7c8-f9abfc8360a0)」を参照してください。  
  
## <a name="see-also"></a>関連項目  
 [OnPaint メソッドのオーバーライド](../../../../docs/framework/winforms/controls/overriding-the-onpaint-method.md)  
 [ユーザーの入力の処理](../../../../docs/framework/winforms/controls/handling-user-input.md)  
 [イベントの定義](../../../../docs/framework/winforms/controls/defining-an-event-in-windows-forms-controls.md)  
 [イベント](../../../../docs/standard/events/index.md)
