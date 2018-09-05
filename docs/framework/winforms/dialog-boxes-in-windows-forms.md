---
title: Windows フォームのダイアログ ボックス
ms.date: 03/30/2017
helpviewer_keywords:
- dialog boxes [Windows Forms], Windows Forms
- Windows Forms dialog boxes
- dialogs [Windows Forms], using in Windows Forms
ms.assetid: d43d022b-451b-490d-9386-dc79d98fbf8a
ms.openlocfilehash: ef07c087ca43efaf99231453fcb56af0db24234a
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43733249"
---
# <a name="dialog-boxes-in-windows-forms"></a><span data-ttu-id="55637-102">Windows フォームのダイアログ ボックス</span><span class="sxs-lookup"><span data-stu-id="55637-102">Dialog Boxes in Windows Forms</span></span>
<span data-ttu-id="55637-103">ダイアログ ボックスは、ユーザーとのやり取りおよび情報の取得のために使用します。</span><span class="sxs-lookup"><span data-stu-id="55637-103">Dialog boxes are used to interact with the user and retrieve information.</span></span> <span data-ttu-id="55637-104">簡単に言えば、ダイアログ ボックスとは <xref:System.Windows.Forms.FormBorderStyle> 列挙値のプロパティが `FixedDialog` に設定されたフォームのことです。</span><span class="sxs-lookup"><span data-stu-id="55637-104">In simple terms, a dialog box is a form with its <xref:System.Windows.Forms.FormBorderStyle> enumeration property set to `FixedDialog`.</span></span> <span data-ttu-id="55637-105">Visual Studio で、Windows フォーム デザイナーを使用して、独自のカスタム ダイアログ ボックスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="55637-105">You can construct your own custom dialog boxes by using the Windows Forms Designer in Visual Studio.</span></span> <span data-ttu-id="55637-106">`Label`、`Textbox`、および `Button` などのコントロールを追加し、ダイアログ ボックスを特定のニーズに合わせてカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="55637-106">Add controls such as `Label`, `Textbox`, and `Button` to customize dialog boxes to your specific needs.</span></span> <span data-ttu-id="55637-107">[!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)]もなど、定義済みのダイアログ ボックスが含まれます**ファイルを開く**とメッセージ ボックスは、独自のアプリケーションを調整できます。</span><span class="sxs-lookup"><span data-stu-id="55637-107">The [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] also includes predefined dialog boxes, such as **File Open** and message boxes, which you can adapt for your own applications.</span></span> <span data-ttu-id="55637-108">詳細については、次を参照してください。 [ ダイアログ ボックス コントロールおよびコンポーネント](../../../docs/framework/winforms/controls/dialog-box-controls-and-components-windows-forms.md)します。</span><span class="sxs-lookup"><span data-stu-id="55637-108">For more information, see [Dialog-Box Controls and Components](../../../docs/framework/winforms/controls/dialog-box-controls-and-components-windows-forms.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="55637-109">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="55637-109">In This Section</span></span>  
 [<span data-ttu-id="55637-110">方法: Windows フォームのダイアログ ボックスを表示する</span><span class="sxs-lookup"><span data-stu-id="55637-110">How to: Display Dialog Boxes for Windows Forms</span></span>](../../../docs/framework/winforms/how-to-display-dialog-boxes-for-windows-forms.md)  
 <span data-ttu-id="55637-111">ダイアログ ボックスを表示する手順を示します。</span><span class="sxs-lookup"><span data-stu-id="55637-111">Gives directions for showing dialog boxes.</span></span>  
  
-   <span data-ttu-id="55637-112">[方法: 選択的に複数のプロパティを使用してダイアログ ボックスの情報を取得](https://msdn.microsoft.com/library/56taefba\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="55637-112">[How to: Retrieve Dialog Box Information Selectively Using Multiple Properties](https://msdn.microsoft.com/library/56taefba\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="55637-113">[方法: ダイアログ ボックスの親フォームから情報を取得](https://msdn.microsoft.com/library/k70t19bb\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="55637-113">[How to: Retrieve Information from the Parent Form of a Dialog Box](https://msdn.microsoft.com/library/k70t19bb\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="55637-114">[ダイアログ ボックスへのユーザー入力](https://msdn.microsoft.com/library/1s9ws53w\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="55637-114">[User Input to Dialog Boxes](https://msdn.microsoft.com/library/1s9ws53w\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="55637-115">[方法: ダイアログ ボックスの結果の取得](https://msdn.microsoft.com/library/40x40td1\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="55637-115">[How to: Retrieve the Result for Dialog Boxes](https://msdn.microsoft.com/library/40x40td1\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="55637-116">[チュートリアル: オブジェクトをまとめて使用する ダイアログ ボックスの情報を取得します。](https://msdn.microsoft.com/library/cakx2hdw\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="55637-116">[Walkthrough: Retrieving Dialog Box Information Collectively Using Objects](https://msdn.microsoft.com/library/cakx2hdw\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="55637-117">[方法: ダイアログ ボックスを閉じて、ユーザー入力を保持](https://msdn.microsoft.com/library/65ad5907\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="55637-117">[How to: Close Dialog Boxes and Retain User Input](https://msdn.microsoft.com/library/65ad5907\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="55637-118">[方法: デザイン時にダイアログ ボックスの作成](https://msdn.microsoft.com/library/55cz5x2c\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="55637-118">[How to: Create Dialog Boxes at Design Time](https://msdn.microsoft.com/library/55cz5x2c\(v=vs.110\))</span></span>  
  
-   <span data-ttu-id="55637-119">[方法: メッセージ ボックスを表示](https://msdn.microsoft.com/library/3tt9e94f\(v=vs.110\))</span><span class="sxs-lookup"><span data-stu-id="55637-119">[How to: Display Message Boxes](https://msdn.microsoft.com/library/3tt9e94f\(v=vs.110\))</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="55637-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="55637-120">Related Sections</span></span>  
 [<span data-ttu-id="55637-121">ダイアログ ボックス コントロールおよびコンポーネント</span><span class="sxs-lookup"><span data-stu-id="55637-121">Dialog-Box Controls and Components</span></span>](../../../docs/framework/winforms/controls/dialog-box-controls-and-components-windows-forms.md)  
 <span data-ttu-id="55637-122">定義済みダイアログ ボックス コントロールの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="55637-122">Lists the predefined dialog box controls.</span></span>  
  
 [<span data-ttu-id="55637-123">Windows フォームの表示形式の変更</span><span class="sxs-lookup"><span data-stu-id="55637-123">Changing the Appearance of Windows Forms</span></span>](../../../docs/framework/winforms/changing-the-appearance-of-windows-forms.md)  
 <span data-ttu-id="55637-124">Windows フォーム アプリケーションの外観を変更する方法について説明したトピックへのリンクを示します。</span><span class="sxs-lookup"><span data-stu-id="55637-124">Contains links to topics that describe how to change the appearance of Windows Forms applications.</span></span>  
  
 [<span data-ttu-id="55637-125">TabControl コントロールの概要</span><span class="sxs-lookup"><span data-stu-id="55637-125">TabControl Control Overview</span></span>](../../../docs/framework/winforms/controls/tabcontrol-control-overview-windows-forms.md)  
 <span data-ttu-id="55637-126">ダイアログ ボックスにタブ コントロールを組み込む方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="55637-126">Explains how you incorporate the tab control into a dialog box.</span></span>
