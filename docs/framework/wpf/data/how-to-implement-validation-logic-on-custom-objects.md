---
title: '方法 : カスタム オブジェクトに検証ロジックを実装する'
ms.date: 08/02/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- checking for validation errors [WPF]
- validation errors [WPF], checking for
- implementing validation logic on custom objects [WPF]
- custom objects [WPF], implementing validation logic on
ms.assetid: 751fda9b-44f9-4d63-b4f2-1df07ac41e0f
ms.openlocfilehash: dbeddb5eb6996d5758717ddd2d4d5af0b6f57f3c
ms.sourcegitcommit: 78bcb629abdbdbde0e295b4e81f350a477864aba
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/08/2018
ms.locfileid: "33555965"
---
# <a name="how-to-implement-validation-logic-on-custom-objects"></a><span data-ttu-id="14519-102">方法 : カスタム オブジェクトに検証ロジックを実装する</span><span class="sxs-lookup"><span data-stu-id="14519-102">How to: Implement Validation Logic on Custom Objects</span></span>
<span data-ttu-id="14519-103">この例では、カスタム オブジェクトに検証ロジックを実装し、それにバインドする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="14519-103">This example shows how to implement validation logic on a custom object and then bind to it.</span></span>  
  
## <a name="example"></a><span data-ttu-id="14519-104">例</span><span class="sxs-lookup"><span data-stu-id="14519-104">Example</span></span>  
 <span data-ttu-id="14519-105">ソース オブジェクトが実装されている場合、ビジネス層の検証ロジックを行うことができます<xref:System.ComponentModel.IDataErrorInfo>を定義する次の例のように、`Person`を実装するオブジェクト<xref:System.ComponentModel.IDataErrorInfo>:</span><span class="sxs-lookup"><span data-stu-id="14519-105">You can provide validation logic on the business layer if your source object implements <xref:System.ComponentModel.IDataErrorInfo>, as in the following example, which defines a `Person` object that implements <xref:System.ComponentModel.IDataErrorInfo>:</span></span>  
  
 [!code-csharp[BusinessLayerValidation#IDataErrorInfo](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BusinessLayerValidation/CSharp/Data.cs#idataerrorinfo)]
 [!code-vb[BusinessLayerValidation#IDataErrorInfo](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BusinessLayerValidation/VisualBasic/Data.vb#idataerrorinfo)]  
  
 <span data-ttu-id="14519-106">次の例で、テキスト ボックスのテキスト プロパティにバインド、`Person.Age`バインドが指定されたリソースの宣言で使用可能なされていますが、プロパティ、 `x:Key` `data`します。</span><span class="sxs-lookup"><span data-stu-id="14519-106">In the following example, the text property of the text box binds to the `Person.Age` property, which has been made available for binding through a resource declaration that is given the `x:Key` `data`.</span></span> <span data-ttu-id="14519-107"><xref:System.Windows.Controls.DataErrorValidationRule>によって発生した検証エラーをチェック、<xref:System.ComponentModel.IDataErrorInfo>実装します。</span><span class="sxs-lookup"><span data-stu-id="14519-107">The <xref:System.Windows.Controls.DataErrorValidationRule> checks for the validation errors raised by the <xref:System.ComponentModel.IDataErrorInfo> implementation.</span></span>  
  
 [!code-xaml[BusinessLayerValidation#BoundTextBox](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BusinessLayerValidation/CSharp/Window1.xaml?highlight=8,11-19,25-42)]  
  
 <span data-ttu-id="14519-108">使用する代わりに、代わりに、 <xref:System.Windows.Controls.DataErrorValidationRule>、設定することができます、<xref:System.Windows.Data.Binding.ValidatesOnDataErrors%2A>プロパティを`true`します。</span><span class="sxs-lookup"><span data-stu-id="14519-108">Alternatively, instead of using the <xref:System.Windows.Controls.DataErrorValidationRule>, you can set the <xref:System.Windows.Data.Binding.ValidatesOnDataErrors%2A> property to `true`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="14519-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="14519-109">See Also</span></span>  
 <xref:System.Windows.Controls.ExceptionValidationRule>  
 [<span data-ttu-id="14519-110">バインディングの検証の実装</span><span class="sxs-lookup"><span data-stu-id="14519-110">Implement Binding Validation</span></span>](../../../../docs/framework/wpf/data/how-to-implement-binding-validation.md)  
 [<span data-ttu-id="14519-111">方法トピック</span><span class="sxs-lookup"><span data-stu-id="14519-111">How-to Topics</span></span>](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
