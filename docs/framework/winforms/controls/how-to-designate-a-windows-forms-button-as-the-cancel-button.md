---
title: '方法: Windows フォームの Button をキャンセル ボタンとして指定します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- buttons [Windows Forms], cancel buttons
- Button control [Windows Forms], designating as cancel button
ms.assetid: 252f0834-e54b-44d9-96f7-ee5f50e94f2c
ms.openlocfilehash: 74d025677682735fc7f1c68116b2364887f0519c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54701470"
---
# <a name="how-to-designate-a-windows-forms-button-as-the-cancel-button"></a><span data-ttu-id="85c34-102">方法: Windows フォームの Button をキャンセル ボタンとして指定します。</span><span class="sxs-lookup"><span data-stu-id="85c34-102">How to: Designate a Windows Forms Button as the Cancel Button</span></span>
<span data-ttu-id="85c34-103">任意の Windows フォームで指定することができます、<xref:System.Windows.Forms.Button>コントロールをキャンセル ボタン。</span><span class="sxs-lookup"><span data-stu-id="85c34-103">On any Windows Form, you can designate a <xref:System.Windows.Forms.Button> control to be the cancel button.</span></span> <span data-ttu-id="85c34-104">ユーザーがフォーム上の他のコントロールにフォーカスがあるか、ESC キーを押すと [キャンセル] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c34-104">A cancel button is clicked whenever the user presses the ESC key, regardless of which other control on the form has the focus.</span></span> <span data-ttu-id="85c34-105">このようなボタンは通常、ユーザーは、すばやく操作をコミットせずに操作を終了できるようにする設定します。</span><span class="sxs-lookup"><span data-stu-id="85c34-105">Such a button is usually programmed to enable the user to quickly exit an operation without committing to any action.</span></span>  
  
### <a name="to-designate-the-cancel-button"></a><span data-ttu-id="85c34-106">[キャンセル] ボタンを指定するには</span><span class="sxs-lookup"><span data-stu-id="85c34-106">To designate the cancel button</span></span>  
  
1.  <span data-ttu-id="85c34-107">フォームの設定<xref:System.Windows.Forms.Form.CancelButton%2A>プロパティを適切な<xref:System.Windows.Forms.Button>コントロール。</span><span class="sxs-lookup"><span data-stu-id="85c34-107">Set the form's <xref:System.Windows.Forms.Form.CancelButton%2A> property to the appropriate <xref:System.Windows.Forms.Button> control.</span></span>  
  
    ```vb  
    Private Sub SetCancelButton(ByVal myCancelBtn As Button)  
       Me.CancelButton = myCancelBtn  
    End Sub  
    ```  
  
    ```csharp  
    private void SetCancelButton(Button myCancelBtn)  
    {  
       this.CancelButton = myCancelBtn;  
    }  
    ```  
  
    ```cpp  
    private:  
       void SetCancelButton(Button ^ myCancelBtn)  
       {  
          this->CancelButton = myCancelBtn;  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="85c34-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="85c34-108">See also</span></span>
- <xref:System.Windows.Forms.Form.CancelButton%2A>
- [<span data-ttu-id="85c34-109">Button コントロールの概要</span><span class="sxs-lookup"><span data-stu-id="85c34-109">Button Control Overview</span></span>](../../../../docs/framework/winforms/controls/button-control-overview-windows-forms.md)
- [<span data-ttu-id="85c34-110">Windows フォームの Button コントロールを選択する方法</span><span class="sxs-lookup"><span data-stu-id="85c34-110">Ways to Select a Windows Forms Button Control</span></span>](../../../../docs/framework/winforms/controls/ways-to-select-a-windows-forms-button-control.md)
- [<span data-ttu-id="85c34-111">方法: Windows フォームのボタン クリックに応答するには</span><span class="sxs-lookup"><span data-stu-id="85c34-111">How to: Respond to Windows Forms Button Clicks</span></span>](../../../../docs/framework/winforms/controls/how-to-respond-to-windows-forms-button-clicks.md)
- [<span data-ttu-id="85c34-112">方法: Windows フォームの Button を承認ボタンとして指定します。</span><span class="sxs-lookup"><span data-stu-id="85c34-112">How to: Designate a Windows Forms Button as the Accept Button</span></span>](../../../../docs/framework/winforms/controls/how-to-designate-a-windows-forms-button-as-the-accept-button.md)
- [<span data-ttu-id="85c34-113">Button コントロール</span><span class="sxs-lookup"><span data-stu-id="85c34-113">Button Control</span></span>](../../../../docs/framework/winforms/controls/button-control-windows-forms.md)
