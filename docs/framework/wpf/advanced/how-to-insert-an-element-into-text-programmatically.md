---
title: '方法: プログラムでテキストに要素を挿入する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Text Animation sample [WPF]
- elements [WPF], inserting into text
- inserting elements into text [WPF]
- TextPointer objects [WPF]
- text [WPF], inserting elements
ms.assetid: 97bd950a-25ac-4e42-a311-94b6420d4136
ms.openlocfilehash: 460524a88427ef5fa822461a7bb985426fefea53
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54693189"
---
# <a name="how-to-insert-an-element-into-text-programmatically"></a><span data-ttu-id="7b2eb-102">方法: プログラムでテキストに要素を挿入する</span><span class="sxs-lookup"><span data-stu-id="7b2eb-102">How to: Insert an Element Into Text Programmatically</span></span>
<span data-ttu-id="7b2eb-103">次の例は、2 つを使用する方法を示しています。<xref:System.Windows.Documents.TextPointer>を適用するテキスト内の範囲を指定するオブジェクト、<xref:System.Windows.Documents.Span>する要素。</span><span class="sxs-lookup"><span data-stu-id="7b2eb-103">The following example shows how to use two <xref:System.Windows.Documents.TextPointer> objects to specify a range within text to apply a <xref:System.Windows.Documents.Span> element to.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7b2eb-104">例</span><span class="sxs-lookup"><span data-stu-id="7b2eb-104">Example</span></span>  
 [!code-csharp[FlowMiscSnippets_procedural_snip#InsertInlineIntoTextExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowMiscSnippets_procedural_snip/CSharp/InsertInlineIntoTextExample.cs#insertinlineintotextexamplewholepage)]
 [!code-vb[FlowMiscSnippets_procedural_snip#InsertInlineIntoTextExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FlowMiscSnippets_procedural_snip/VisualBasic/InsertInlineIntoTextExample.vb#insertinlineintotextexamplewholepage)]  
  
 <span data-ttu-id="7b2eb-105">次の図は、この例の結果を示したものです。</span><span class="sxs-lookup"><span data-stu-id="7b2eb-105">The illustration below shows what this example looks like.</span></span>  
  
 <span data-ttu-id="7b2eb-106">![テキストの範囲に適用される Span 要素](../../../../docs/framework/wpf/advanced/media/flow-insertelementintotextprogrammatically.png "Flow_InsertElementIntoTextProgrammatically")</span><span class="sxs-lookup"><span data-stu-id="7b2eb-106">![A Span element applied to a range of text](../../../../docs/framework/wpf/advanced/media/flow-insertelementintotextprogrammatically.png "Flow_InsertElementIntoTextProgrammatically")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b2eb-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="7b2eb-107">See also</span></span>
- [<span data-ttu-id="7b2eb-108">フロー ドキュメントの概要</span><span class="sxs-lookup"><span data-stu-id="7b2eb-108">Flow Document Overview</span></span>](../../../../docs/framework/wpf/advanced/flow-document-overview.md)
