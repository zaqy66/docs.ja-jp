---
title: 複合 Windows フォーム コントロールの開発
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], composite controls
- composite controls [Windows Forms]
- composite controls [Windows Forms], Windows Forms
- controls [Windows Forms], composite
ms.assetid: d086f2a3-baa3-4e09-b40c-a5bb3cfc51a6
ms.openlocfilehash: 82d76c1656ff14c6d1c9bbbb1c79ec3a30708a90
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54635716"
---
# <a name="developing-a-composite-windows-forms-control"></a><span data-ttu-id="741f4-102">複合 Windows フォーム コントロールの開発</span><span class="sxs-lookup"><span data-stu-id="741f4-102">Developing a Composite Windows Forms Control</span></span>
<span data-ttu-id="741f4-103">異なる複数の Windows フォーム コントロールを組み合わせることによって、複合 Windows フォーム コントロールを開発できます。</span><span class="sxs-lookup"><span data-stu-id="741f4-103">You can develop a composite Windows Forms control by combining other Windows Forms controls.</span></span> <span data-ttu-id="741f4-104">派生した複合コントロール<xref:System.Web.UI.UserControl>ユーザー コントロールと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="741f4-104">Composite controls that derive from <xref:System.Web.UI.UserControl> are called user controls.</span></span> <span data-ttu-id="741f4-105">基底クラス <xref:System.Windows.Forms.UserControl> は、子コントロールに対してキーボード ルーティングを提供し、子コントロールがフォーカスを受け取れるようにします。</span><span class="sxs-lookup"><span data-stu-id="741f4-105">The base class, <xref:System.Windows.Forms.UserControl>, provides keyboard routing for the child controls, thus ensuring that child controls can receive focus.</span></span> <span data-ttu-id="741f4-106">ユーザー コントロールの例は、次を参照してください。、<xref:System.Windows.Forms.UserControl>サンプルは、[方法。Windows フォーム コントロールに属性を適用](../../../../docs/framework/winforms/controls/how-to-apply-attributes-in-windows-forms-controls.md)します。</span><span class="sxs-lookup"><span data-stu-id="741f4-106">For an example of a user control, see the <xref:System.Windows.Forms.UserControl> sample in [How to: Apply Attributes in Windows Forms Controls](../../../../docs/framework/winforms/controls/how-to-apply-attributes-in-windows-forms-controls.md).</span></span>  
  
 <span data-ttu-id="741f4-107">Visual Studio での Windows フォーム デザイナーは、ユーザー コントロールを作成するための豊富なデザイン時サポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="741f4-107">The Windows Forms designer in Visual Studio provides rich design-time support for authoring user controls.</span></span>  
  
-   <span data-ttu-id="741f4-108">[方法: 内のコントロールを表示、ツールボックス項目 ダイアログ ボックスの選択](https://msdn.microsoft.com/library/9yxtkx75\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="741f4-108">[How to: Display a Control in the Choose Toolbox Items Dialog Box](https://msdn.microsoft.com/library/9yxtkx75\(v=vs.110\))</span></span>  
  
-   [<span data-ttu-id="741f4-109">チュートリアル: Designerserializationvisibilityattribute を使用、基本データ型のコレクションをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="741f4-109">Walkthrough: Serializing Collections of Standard Types with the DesignerSerializationVisibilityAttribute</span></span>](serializing-collections-designerserializationvisibilityattribute.md)  
  
-   <span data-ttu-id="741f4-110">[チュートリアル: 視覚的にコントロールをフォーム、Windows からの継承C# ](https://msdn.microsoft.com/library/09476da0-8d4c-4a4c-b969-649519dfb438))</span><span class="sxs-lookup"><span data-stu-id="741f4-110">[Walkthrough: Inheriting from a Windows Forms Control with Visual C#](https://msdn.microsoft.com/library/09476da0-8d4c-4a4c-b969-649519dfb438))</span></span>  
  
-   <span data-ttu-id="741f4-111">[方法: コントロールにツールボックス ビットマップを指定します。](https://msdn.microsoft.com/library/4wk1wc0a\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="741f4-111">[How to: Provide a Toolbox Bitmap for a Control](https://msdn.microsoft.com/library/4wk1wc0a\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="741f4-112">[方法: 継承可能な既存の Windows フォーム コントロール](https://msdn.microsoft.com/library/7h62478z\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="741f4-112">[How to: Inherit from Existing Windows Forms Controls](https://msdn.microsoft.com/library/7h62478z\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="741f4-113">[チュートリアル: カスタム Windows フォーム コントロールのデザイン時のデバッグ](https://msdn.microsoft.com/library/5ytx0z24\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="741f4-113">[Walkthrough: Debugging Custom Windows Forms Controls at Design Time](https://msdn.microsoft.com/library/5ytx0z24\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="741f4-114">[方法: コントロール クラスから継承します。](https://msdn.microsoft.com/library/skcysbt2\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="741f4-114">[How to: Inherit from the Control Class](https://msdn.microsoft.com/library/skcysbt2\(v=vs.110\))</span></span>  
  
-   [<span data-ttu-id="741f4-115">方法: UserControl の実行時の動作をテストします。</span><span class="sxs-lookup"><span data-stu-id="741f4-115">How to: Test the Run-Time Behavior of a UserControl</span></span>](how-to-test-the-run-time-behavior-of-a-usercontrol.md)  
  
-   <span data-ttu-id="741f4-116">[方法: デザイン時にコントロールをフォームの端を揃える](https://msdn.microsoft.com/library/1fxyb15b\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="741f4-116">[How to: Align a Control to the Edges of Forms at Design Time](https://msdn.microsoft.com/library/1fxyb15b\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="741f4-117">[方法: UserControl クラスを継承します。](https://msdn.microsoft.com/library/00ctb4z0\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="741f4-117">[How to: Inherit from the UserControl Class](https://msdn.microsoft.com/library/00ctb4z0\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="741f4-118">[方法: Windows フォームのコントロールの作成](https://msdn.microsoft.com/library/bs3yhkh7\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="741f4-118">[How to: Author Controls for Windows Forms](https://msdn.microsoft.com/library/bs3yhkh7\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="741f4-119">[方法: 複合コントロールを作成](https://msdn.microsoft.com/library/3sf86w5h\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="741f4-119">[How to: Author Composite Controls](https://msdn.microsoft.com/library/3sf86w5h\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="741f4-120">[チュートリアル: Visual Basic による複合コントロールの作成](https://msdn.microsoft.com/library/c316f119\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="741f4-120">[Walkthrough: Authoring a Composite Control with Visual Basic](https://msdn.microsoft.com/library/c316f119\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="741f4-121">[チュートリアル: ビジュアルを含む複合コントロールの作成C# ](https://msdn.microsoft.com/library/f88481a8-c746-4a36-9479-374ce5f2e91f))</span><span class="sxs-lookup"><span data-stu-id="741f4-121">[Walkthrough: Authoring a Composite Control with Visual C#](https://msdn.microsoft.com/library/f88481a8-c746-4a36-9479-374ce5f2e91f))</span></span>  
  
-   <span data-ttu-id="741f4-122">[チュートリアル: Visual Basic による Windows フォーム コントロールから継承します。](https://msdn.microsoft.com/library/w2a8y03d\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="741f4-122">[Walkthrough: Inheriting from a Windows Forms Control with Visual Basic](https://msdn.microsoft.com/library/w2a8y03d\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="741f4-123">[方法: デザイン時機能を活用した Windows フォーム コントロールを作成します。](https://msdn.microsoft.com/library/307hck25\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="741f4-123">[How to: Create a Windows Forms Control That Takes Advantage of Design-Time Features](https://msdn.microsoft.com/library/307hck25\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="741f4-124">[方法: デザイン時機能を活用した Windows フォーム コントロールを作成します。](https://msdn.microsoft.com/library/307hck25\(v=vs.120\))</span><span class="sxs-lookup"><span data-stu-id="741f4-124">[How to: Create a Windows Forms Control That Takes Advantage of Design-Time Features](https://msdn.microsoft.com/library/307hck25\(v=vs.120\))</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="741f4-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="741f4-125">See also</span></span>
- [<span data-ttu-id="741f4-126">方法: Windows フォーム コントロールに属性を適用します。</span><span class="sxs-lookup"><span data-stu-id="741f4-126">How to: Apply Attributes in Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/how-to-apply-attributes-in-windows-forms-controls.md)
- [<span data-ttu-id="741f4-127">.NET Framework を使用したカスタム Windows フォーム コントロールの開発</span><span class="sxs-lookup"><span data-stu-id="741f4-127">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](../../../../docs/framework/winforms/controls/developing-custom-windows-forms-controls.md)
- [<span data-ttu-id="741f4-128">さまざまなカスタム コントロール</span><span class="sxs-lookup"><span data-stu-id="741f4-128">Varieties of Custom Controls</span></span>](../../../../docs/framework/winforms/controls/varieties-of-custom-controls.md)
