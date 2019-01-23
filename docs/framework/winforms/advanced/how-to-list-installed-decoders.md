---
title: '方法: インストールされたデコーダーの一覧'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image codecs [Windows Forms], listing
- image decoders [Windows Forms], listing
ms.assetid: 11417191-8c95-40ca-8024-779e61706fb6
ms.openlocfilehash: 3d24eadca23aa6da4a8557cc2db3189b6e232e78
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54605211"
---
# <a name="how-to-list-installed-decoders"></a><span data-ttu-id="98c3f-102">方法: インストールされたデコーダーの一覧</span><span class="sxs-lookup"><span data-stu-id="98c3f-102">How to: List Installed Decoders</span></span>
<span data-ttu-id="98c3f-103">アプリケーションが特定のイメージ ファイル形式を読み取るかどうかを判断するコンピューターでは、使用可能なイメージ デコーダーの一覧を表示することがあります。</span><span class="sxs-lookup"><span data-stu-id="98c3f-103">You may want to list the image decoders available on a computer, to determine whether your application can read a particular image file format.</span></span> <span data-ttu-id="98c3f-104"><xref:System.Drawing.Imaging.ImageCodecInfo>クラスには、<xref:System.Drawing.Imaging.ImageCodecInfo.GetImageDecoders%2A>静的メソッド イメージ デコーダーは、使用可能なを確認できるようにします。</span><span class="sxs-lookup"><span data-stu-id="98c3f-104">The <xref:System.Drawing.Imaging.ImageCodecInfo> class provides the <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageDecoders%2A> static methods so that you can determine which image decoders are available.</span></span> <span data-ttu-id="98c3f-105"><xref:System.Drawing.Imaging.ImageCodecInfo.GetImageDecoders%2A> 配列を返します<xref:System.Drawing.Imaging.ImageCodecInfo>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="98c3f-105"><xref:System.Drawing.Imaging.ImageCodecInfo.GetImageDecoders%2A> returns an array of <xref:System.Drawing.Imaging.ImageCodecInfo> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="98c3f-106">例</span><span class="sxs-lookup"><span data-stu-id="98c3f-106">Example</span></span>  
 <span data-ttu-id="98c3f-107">次のコード例では、インストールされたデコーダーの一覧とそのプロパティ値を出力します。</span><span class="sxs-lookup"><span data-stu-id="98c3f-107">The following code example outputs the list of installed decoders and their property values.</span></span>  
  
 [!code-csharp[UsingImageEncodersDecoders#2](../../../../samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#2)]
 [!code-vb[UsingImageEncodersDecoders#2](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#2)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="98c3f-108">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="98c3f-108">Compiling the Code</span></span>  
 <span data-ttu-id="98c3f-109">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="98c3f-109">This example requires:</span></span>  
  
-   <span data-ttu-id="98c3f-110">Windows フォーム アプリケーション</span><span class="sxs-lookup"><span data-stu-id="98c3f-110">A Windows Forms application.</span></span>  
  
-   <span data-ttu-id="98c3f-111">A<xref:System.Windows.Forms.PaintEventArgs>はのパラメーター<xref:System.Windows.Forms.PaintEventHandler>します。</span><span class="sxs-lookup"><span data-stu-id="98c3f-111">A <xref:System.Windows.Forms.PaintEventArgs>, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="98c3f-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="98c3f-112">See also</span></span>
- [<span data-ttu-id="98c3f-113">方法: インストールされたエンコーダーの一覧</span><span class="sxs-lookup"><span data-stu-id="98c3f-113">How to: List Installed Encoders</span></span>](../../../../docs/framework/winforms/advanced/how-to-list-installed-encoders.md)
- [<span data-ttu-id="98c3f-114">マネージド GDI+ でのイメージ エンコーダーおよびイメージ デコーダーの使用</span><span class="sxs-lookup"><span data-stu-id="98c3f-114">Using Image Encoders and Decoders in Managed GDI+</span></span>](../../../../docs/framework/winforms/advanced/using-image-encoders-and-decoders-in-managed-gdi.md)
