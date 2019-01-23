---
title: UI オートメーションを使用した、テキスト ボックスへのコンテンツの追加
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adding content to text boxes
- text boxes, adding content
- UI Automation, adding content to text boxes
ms.assetid: 8bdd1a73-1ecb-4a05-a891-a7827ebb767f
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: b8f64b12400098d94d0e25590559877d61519777
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54582166"
---
# <a name="add-content-to-a-text-box-using-ui-automation"></a><span data-ttu-id="28ebe-102">UI オートメーションを使用した、テキスト ボックスへのコンテンツの追加</span><span class="sxs-lookup"><span data-stu-id="28ebe-102">Add Content to a Text Box Using UI Automation</span></span>
> [!NOTE]
>  <span data-ttu-id="28ebe-103">このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="28ebe-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="28ebe-104">に関する最新情報については[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]を参照してください[Windows Automation API:UI オートメーション](https://go.microsoft.com/fwlink/?LinkID=156746)します。</span><span class="sxs-lookup"><span data-stu-id="28ebe-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="28ebe-105">このトピックを使用する方法を示すコード例が含まれています。[!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]に 1 行のテキスト ボックスにテキストを挿入します。</span><span class="sxs-lookup"><span data-stu-id="28ebe-105">This topic contains example code that demonstrates how to use [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] to insert text into a single-line text box.</span></span> <span data-ttu-id="28ebe-106">複数行、およびリッチ テキスト コントロールの別の方法が提供されている場所[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]は適用されません。</span><span class="sxs-lookup"><span data-stu-id="28ebe-106">An alternate method is provided for multi-line and rich text controls where [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] is not applicable.</span></span> <span data-ttu-id="28ebe-107">比較のために、この例は Win32 メソッドを使用して同じ結果を達成する方法も示します。</span><span class="sxs-lookup"><span data-stu-id="28ebe-107">For comparison purposes, the example also demonstrates how to use Win32 methods to accomplish the same results.</span></span>  
  
## <a name="example"></a><span data-ttu-id="28ebe-108">例</span><span class="sxs-lookup"><span data-stu-id="28ebe-108">Example</span></span>  
 <span data-ttu-id="28ebe-109">ターゲット アプリケーション内のテキスト コントロールの順序で次の例の手順。</span><span class="sxs-lookup"><span data-stu-id="28ebe-109">The following example steps through a sequence of text controls in a target application.</span></span> <span data-ttu-id="28ebe-110">各テキスト コントロールがかどうかをテストする<xref:System.Windows.Automation.ValuePattern>を使用してオブジェクトを取得できる、<xref:System.Windows.Automation.AutomationElement.TryGetCurrentPattern%2A>メソッド。</span><span class="sxs-lookup"><span data-stu-id="28ebe-110">Each text control is tested to see if a <xref:System.Windows.Automation.ValuePattern> object can be obtained from it using the <xref:System.Windows.Automation.AutomationElement.TryGetCurrentPattern%2A> method.</span></span> <span data-ttu-id="28ebe-111">テキスト コントロールはサポートしている場合<xref:System.Windows.Automation.ValuePattern>、<xref:System.Windows.Automation.ValuePattern.SetValue%2A>テキスト コントロールにユーザー定義の文字列を挿入するメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="28ebe-111">If the text control does support <xref:System.Windows.Automation.ValuePattern>, the <xref:System.Windows.Automation.ValuePattern.SetValue%2A> method is used to insert a user-defined string into the text control.</span></span> <span data-ttu-id="28ebe-112">それ以外の場合、<xref:System.Windows.Forms.SendKeys.SendWait%2A?displayProperty=nameWithType>メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="28ebe-112">Otherwise, the <xref:System.Windows.Forms.SendKeys.SendWait%2A?displayProperty=nameWithType> method is used.</span></span>  
  
 [!code-csharp[InsertText#InsertText](../../../samples/snippets/csharp/VS_Snippets_Wpf/InsertText/CSharp/Window1.xaml.cs#inserttext)]
 [!code-vb[InsertText#InsertText](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/InsertText/VisualBasic/Window1.xaml.vb#inserttext)]  
  
## <a name="see-also"></a><span data-ttu-id="28ebe-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="28ebe-113">See also</span></span>
- [<span data-ttu-id="28ebe-114">TextPattern の挿入テキスト サンプル</span><span class="sxs-lookup"><span data-stu-id="28ebe-114">TextPattern Insert Text Sample</span></span>](https://msdn.microsoft.com/library/67353f93-7ee2-42f2-ab76-5c078cf6ca16)
