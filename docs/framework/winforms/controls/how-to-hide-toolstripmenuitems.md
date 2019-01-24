---
title: '方法: ToolStripMenuItems を非表示にします。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ToolStripMenuItems [Windows Forms], hiding
- MenuStrip control [Windows Forms], hiding menu items
- menus [Windows Forms], hiding menu items
- menu items [Windows Forms], hiding
- hiding menu items
ms.assetid: 418a768f-808a-44cd-8cef-f4e161883621
ms.openlocfilehash: 73e49c96c20f145490a2d494177e21bc957605b8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54727626"
---
# <a name="how-to-hide-toolstripmenuitems"></a><span data-ttu-id="ab583-102">方法: ToolStripMenuItems を非表示にします。</span><span class="sxs-lookup"><span data-stu-id="ab583-102">How to: Hide ToolStripMenuItems</span></span>
<span data-ttu-id="ab583-103">メニュー項目を非表示には、アプリケーションのユーザー インターフェイスを制御し、ユーザーのコマンドを制限する方法です。</span><span class="sxs-lookup"><span data-stu-id="ab583-103">Hiding menu items is a way to control the user interface of your application and restrict user commands.</span></span> <span data-ttu-id="ab583-104">多くの場合、すべてのメニュー項目が利用できない場合は、メニュー全体を非表示にするされます。</span><span class="sxs-lookup"><span data-stu-id="ab583-104">Often, you will want to hide an entire menu when all of the menu items on it are unavailable.</span></span> <span data-ttu-id="ab583-105">これは、ユーザーの混乱を表示します。</span><span class="sxs-lookup"><span data-stu-id="ab583-105">This presents fewer distractions for the user.</span></span> <span data-ttu-id="ab583-106">さらに、非表示だけでは、ユーザーはショートカット キーを使用してメニュー コマンドへのアクセスを非表示にして、メニューまたはメニュー項目を無効にする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ab583-106">Furthermore, you might want to both hide and disable the menu or menu item, as hiding alone does not prevent the user from accessing a menu command by using a shortcut key.</span></span>  
  
### <a name="to-hide-any-menu-item-programmatically"></a><span data-ttu-id="ab583-107">任意のメニュー項目をプログラムで非表示にするには</span><span class="sxs-lookup"><span data-stu-id="ab583-107">To hide any menu item programmatically</span></span>  
  
-   <span data-ttu-id="ab583-108">メニュー項目のプロパティを設定するメソッド内で設定するコードを追加、<xref:System.Windows.Forms.ToolStripItem.Visible%2A>プロパティを`false`します。</span><span class="sxs-lookup"><span data-stu-id="ab583-108">Within the method where you set the properties of the menu item, add code to set the <xref:System.Windows.Forms.ToolStripItem.Visible%2A> property to `false`.</span></span>  
  
    ```vb  
    MenuItem3.Visible = False  
    ```  
  
    ```csharp  
    menuItem3.Visible = false;  
    ```  
  
    ```cpp  
    menuItem3->Visible = false;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="ab583-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab583-109">See also</span></span>
- <xref:System.Windows.Forms.ToolStripItem.Visible%2A>
- <xref:System.Windows.Forms.MenuStrip>
- [<span data-ttu-id="ab583-110">MenuStrip コントロールの概要</span><span class="sxs-lookup"><span data-stu-id="ab583-110">MenuStrip Control Overview</span></span>](../../../../docs/framework/winforms/controls/menustrip-control-overview-windows-forms.md)
- [<span data-ttu-id="ab583-111">方法: ToolStripMenuItems を無効にします。</span><span class="sxs-lookup"><span data-stu-id="ab583-111">How to: Disable ToolStripMenuItems</span></span>](../../../../docs/framework/winforms/controls/how-to-disable-toolstripmenuitems.md)
