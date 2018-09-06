---
title: マネージド HTML DOM (Document Object Model) の使用
ms.date: 03/30/2017
helpviewer_keywords:
- managed HTML DOM
ms.assetid: a017dd5c-cd7b-47e4-952c-f4f54cb48409
ms.openlocfilehash: 7800311895d1c0fac43577076226a68712164f60
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43878750"
---
# <a name="using-the-managed-html-document-object-model"></a><span data-ttu-id="f3f90-102">マネージド HTML DOM (Document Object Model) の使用</span><span class="sxs-lookup"><span data-stu-id="f3f90-102">Using the Managed HTML Document Object Model</span></span>
<span data-ttu-id="f3f90-103">マネージ HTML ドキュメント オブジェクト モデル (DOM) に基づくラッパーを提供する、[!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)]の Internet Explorer によって公開されている HTML クラス。</span><span class="sxs-lookup"><span data-stu-id="f3f90-103">The managed HTML document object model (DOM) provides a wrapper based on the [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] for the HTML classes exposed by Internet Explorer.</span></span> <span data-ttu-id="f3f90-104">ホストされている HTML ページを操作するこれらのクラスを使用して、<xref:System.Windows.Forms.WebBrowser>コントロール、または最初から新しいページを構築します。</span><span class="sxs-lookup"><span data-stu-id="f3f90-104">Use these classes to manipulate HTML pages hosted in the <xref:System.Windows.Forms.WebBrowser> control, or to build new pages from the beginning.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f3f90-105">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="f3f90-105">In This Section</span></span>  
 [<span data-ttu-id="f3f90-106">方法: マネージド HTML DOM (Document Object Model) にアクセスする</span><span class="sxs-lookup"><span data-stu-id="f3f90-106">How to: Access the Managed HTML Document Object Model</span></span>](../../../../docs/framework/winforms/controls/how-to-access-the-managed-html-document-object-model.md)  
 <span data-ttu-id="f3f90-107">有効なインスタンスを取得する方法について説明します<xref:System.Windows.Forms.HtmlDocument>Windows フォーム アプリケーションから、または<xref:System.Windows.Forms.UserControl>Internet Explorer でホストされています。</span><span class="sxs-lookup"><span data-stu-id="f3f90-107">Describes how to obtain a valid instance of <xref:System.Windows.Forms.HtmlDocument> from either a Windows Forms application or a <xref:System.Windows.Forms.UserControl> hosted in Internet Explorer.</span></span>  
  
 [<span data-ttu-id="f3f90-108">方法: マネージド HTML DOM (Document Object Model) の HTML ソースにアクセスする</span><span class="sxs-lookup"><span data-stu-id="f3f90-108">How to: Access the HTML Source in the Managed HTML Document Object Model</span></span>](../../../../docs/framework/winforms/controls/how-to-access-the-html-source-in-the-managed-html-document-object-model.md)  
 <span data-ttu-id="f3f90-109">DOM の現在の状態を反映する「ライブ」のソースを取得する方法と、変更されていない元の HTML ソースを取得する方法について説明します</span><span class="sxs-lookup"><span data-stu-id="f3f90-109">Describes how to obtain the original, unmodified HTML source, and how to obtain the "live" source that reflects the current state of the DOM.</span></span>  
  
 [<span data-ttu-id="f3f90-110">方法: マネージド HTML DOM (Document Object Model) の要素のスタイルを変更する</span><span class="sxs-lookup"><span data-stu-id="f3f90-110">How to: Change Styles on an Element in the Managed HTML Document Object Model</span></span>](../../../../docs/framework/winforms/controls/how-to-change-styles-on-an-element-in-the-managed-html-document-object-model.md)  
 <span data-ttu-id="f3f90-111">要素のビジュアル表示を制御するためのスタイルを操作する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3f90-111">Describes how to manipulate styles, which are used to control the visual display of elements.</span></span>  
  
 [<span data-ttu-id="f3f90-112">マネージド HTML DOM (Document Object Model) へのアクセス</span><span class="sxs-lookup"><span data-stu-id="f3f90-112">Accessing Frames in the Managed HTML Document Object Model</span></span>](../../../../docs/framework/winforms/controls/accessing-frames-in-the-managed-html-document-object-model.md)  
 <span data-ttu-id="f3f90-113">フレームとフレーム セットとフレームの DOM にアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3f90-113">Describes what frames and framesets are, and how to access the DOM of a frame.</span></span>  
  
 [<span data-ttu-id="f3f90-114">マネージド HTML DOM (Document Object Model) の非公開メンバーへのアクセス</span><span class="sxs-lookup"><span data-stu-id="f3f90-114">Accessing Unexposed Members on the Managed HTML Document Object Model</span></span>](../../../../docs/framework/winforms/controls/accessing-unexposed-members-on-the-managed-html-document-object-model.md)  
 <span data-ttu-id="f3f90-115">基になる DOM の相当するマネージがないメンバーにアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3f90-115">Describes how to access members of the underlying DOM that do not have a managed equivalent.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="f3f90-116">参照</span><span class="sxs-lookup"><span data-stu-id="f3f90-116">Reference</span></span>  
 <xref:System.Windows.Forms.HtmlDocument>  
  
 <xref:System.Windows.Forms.HtmlElement>  
  
 <xref:System.Windows.Forms.HtmlWindow>  
  
## <a name="related-sections"></a><span data-ttu-id="f3f90-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="f3f90-117">Related Sections</span></span>  
 [<span data-ttu-id="f3f90-118">WebBrowser コントロール</span><span class="sxs-lookup"><span data-stu-id="f3f90-118">WebBrowser Control</span></span>](../../../../docs/framework/winforms/controls/webbrowser-control-windows-forms.md)  
  
## <a name="see-also"></a><span data-ttu-id="f3f90-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="f3f90-119">See Also</span></span>  
 [<span data-ttu-id="f3f90-120">DHTML オブジェクト モデルについて</span><span class="sxs-lookup"><span data-stu-id="f3f90-120">About the DHTML Object Model</span></span>](https://msdn.microsoft.com/library/default.asp?url=/workshop/author/om/doc_object.asp)
