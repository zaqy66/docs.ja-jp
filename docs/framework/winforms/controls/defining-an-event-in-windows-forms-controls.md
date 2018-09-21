---
title: Windows フォーム コントロールのイベントの定義
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- events [Windows Forms], defining within Windows Forms custom controls
- custom controls [Windows Forms], events using code
ms.assetid: d89f1096-8061-42e2-a855-a1f053f1940a
ms.openlocfilehash: 60ae01ca63f895bfb1c7aabbe3337596cd13933d
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2018
ms.locfileid: "46489654"
---
# <a name="defining-an-event-in-windows-forms-controls"></a><span data-ttu-id="c7e4c-102">Windows フォーム コントロールのイベントの定義</span><span class="sxs-lookup"><span data-stu-id="c7e4c-102">Defining an Event in Windows Forms Controls</span></span>
<span data-ttu-id="c7e4c-103">カスタム イベントを定義する方法の詳細については、次を参照してください。[イベント](../../../../docs/standard/events/index.md)します。</span><span class="sxs-lookup"><span data-stu-id="c7e4c-103">For details about defining custom events, see [Events](../../../../docs/standard/events/index.md).</span></span> <span data-ttu-id="c7e4c-104">関連データがないイベントを定義する場合、イベント データの基本型である <xref:System.EventArgs> を使用し、イベント デリゲートとして <xref:System.EventHandler> を使用します。</span><span class="sxs-lookup"><span data-stu-id="c7e4c-104">If you define an event that does not have any associated data, use the base type for event data, <xref:System.EventArgs>, and use <xref:System.EventHandler> as the event delegate.</span></span> <span data-ttu-id="c7e4c-105">イベント メンバーとプロテクトを定義する操作は、すべて`On` *EventName*イベントを発生させるメソッド。</span><span class="sxs-lookup"><span data-stu-id="c7e4c-105">All that remains to do is to define an event member and a protected `On`*EventName* method that raises the event.</span></span>  
  
 <span data-ttu-id="c7e4c-106">`FlashTrackBar` カスタム コントロールによる `ValueChanged` カスタム イベントの定義方法を示すコードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="c7e4c-106">The following code fragment shows how the `FlashTrackBar` custom control defines a custom event, `ValueChanged`.</span></span> <span data-ttu-id="c7e4c-107">完全なコード、`FlashTrackBar`サンプルを参照してください、[方法: 作成、Windows フォーム コントロール進行状況を示す](../../../../docs/framework/winforms/controls/how-to-create-a-windows-forms-control-that-shows-progress.md)します。</span><span class="sxs-lookup"><span data-stu-id="c7e4c-107">For the complete code for the `FlashTrackBar` sample, see the [How to: Create a Windows Forms Control That Shows Progress](../../../../docs/framework/winforms/controls/how-to-create-a-windows-forms-control-that-shows-progress.md).</span></span>  
  
```vb  
Option Explicit  
Option Strict  
  
Imports System  
Imports System.Windows.Forms  
Imports System.Drawing  
  
Public Class FlashTrackBar  
   Inherits Control  
  
   ' The event does not have any data, so EventHandler is adequate   
   ' as the event delegate.          
   ' Define the event member using the event keyword.  
   ' In this case, for efficiency, the event is defined   
   ' using the event property construct.  
   Public Event ValueChanged As EventHandler  
   ' The protected method that raises the ValueChanged   
   ' event when the value has actually   
   ' changed. Derived controls can override this method.    
   Protected Overridable Sub OnValueChanged(e As EventArgs)  
      RaiseEvent ValueChanged(Me, e)  
   End Sub  
End Class  
```  
  
```csharp  
using System;  
using System.Windows.Forms;  
using System.Drawing;  
  
public class FlashTrackBar : Control {  
   // The event does not have any data, so EventHandler is adequate   
   // as the event delegate.  
   private EventHandler onValueChanged;  
   // Define the event member using the event keyword.  
   // In this case, for efficiency, the event is defined   
   // using the event property construct.  
   public event EventHandler ValueChanged {  
            add {  
                onValueChanged += value;  
            }  
            remove {  
                onValueChanged -= value;  
            }  
        }  
   // The protected method that raises the ValueChanged  
   // event when the value has actually   
   // changed. Derived controls can override this method.    
   protected virtual void OnValueChanged(EventArgs e) 
   {  
       ValueChanged?.Invoke(this, e);  
   }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="c7e4c-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7e4c-108">See also</span></span>

- [<span data-ttu-id="c7e4c-109">Windows フォーム コントロールのイベント</span><span class="sxs-lookup"><span data-stu-id="c7e4c-109">Events in Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/events-in-windows-forms-controls.md)
- [<span data-ttu-id="c7e4c-110">イベント</span><span class="sxs-lookup"><span data-stu-id="c7e4c-110">Events</span></span>](../../../../docs/standard/events/index.md)
