---
title: '方法: フォームに標準メニュー項目を提供します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- menu items [Windows Forms], standard
- ToolStrip control [Windows Forms]
ms.assetid: 75db9126-e70c-4e81-921d-b83c0a4a9f50
ms.openlocfilehash: 823cc774e4bfd9ba94ea84efeda493b225a04a35
ms.sourcegitcommit: af0a22a4eb11bbcd33baec49150d551955b50a16
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2019
ms.locfileid: "56260908"
---
# <a name="how-to-provide-standard-menu-items-to-a-form"></a><span data-ttu-id="09e59-102">方法: フォームに標準メニュー項目を提供します。</span><span class="sxs-lookup"><span data-stu-id="09e59-102">How to: Provide Standard Menu Items to a Form</span></span>
<span data-ttu-id="09e59-103">フォームの標準のメニューを <xref:System.Windows.Forms.MenuStrip> コントロールに提供できます。</span><span class="sxs-lookup"><span data-stu-id="09e59-103">You can provide a standard menu for your forms with the <xref:System.Windows.Forms.MenuStrip> control.</span></span>  
  
 <span data-ttu-id="09e59-104">Visual Studio でこの機能の広範なサポートがあります。</span><span class="sxs-lookup"><span data-stu-id="09e59-104">There is extensive support for this feature in Visual Studio.</span></span>  
  
 <span data-ttu-id="09e59-105">参照してください[チュートリアル。フォームに標準メニュー項目を用意する](walkthrough-providing-standard-menu-items-to-a-form.md)します。</span><span class="sxs-lookup"><span data-stu-id="09e59-105">Also see [Walkthrough: Providing Standard Menu Items to a Form](walkthrough-providing-standard-menu-items-to-a-form.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="09e59-106">例</span><span class="sxs-lookup"><span data-stu-id="09e59-106">Example</span></span>  
 <span data-ttu-id="09e59-107">
  <xref:System.Windows.Forms.MenuStrip> コントロールを使用して標準メニューを持つフォームを作成する方法を、次のコード例に示します。</span><span class="sxs-lookup"><span data-stu-id="09e59-107">The following code example demonstrates how to use a <xref:System.Windows.Forms.MenuStrip> control to create a form with a standard menu.</span></span> <span data-ttu-id="09e59-108">メニュー項目の選択は、<xref:System.Windows.Forms.StatusStrip> コントロールに表示されます。</span><span class="sxs-lookup"><span data-stu-id="09e59-108">Menu item selections are displayed in a <xref:System.Windows.Forms.StatusStrip> control.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.StandardMenu#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.StandardMenu#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="09e59-109">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="09e59-109">Compiling the Code</span></span>  
 <span data-ttu-id="09e59-110">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="09e59-110">This example requires:</span></span>  
  
-   <span data-ttu-id="09e59-111">System、System.Drawing、および System.Windows.Forms の各アセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="09e59-111">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="09e59-112">コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。</span><span class="sxs-lookup"><span data-stu-id="09e59-112">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="09e59-113">新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="09e59-113">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09e59-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="09e59-114">See also</span></span>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="09e59-115">MenuStrip コントロール</span><span class="sxs-lookup"><span data-stu-id="09e59-115">MenuStrip Control</span></span>](../../../../docs/framework/winforms/controls/menustrip-control-windows-forms.md)
