---
title: Windows フォーム コントロールのプロパティ
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], properties overview (using code)
- controls [Windows Forms], properties
- properties [Windows Forms]
ms.assetid: 2785279b-fb57-4937-8f6b-2050e475db6f
ms.openlocfilehash: 37db3f16a17acc7f3a6e594bd284ba368801e70a
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2018
ms.locfileid: "45748953"
---
# <a name="properties-in-windows-forms-controls"></a>Windows フォーム コントロールのプロパティ
Windows フォーム コントロールは多くのプロパティ フォームの基本クラスを継承して<xref:System.Windows.Forms.Control?displayProperty=nameWithType>します。 などのプロパティが含まれます<xref:System.Windows.Forms.Control.Font%2A>、 <xref:System.Windows.Forms.Control.ForeColor%2A>、 <xref:System.Windows.Forms.Control.BackColor%2A>、 <xref:System.Windows.Forms.Control.Bounds%2A>、 <xref:System.Windows.Forms.Control.ClientRectangle%2A>、 <xref:System.Windows.Forms.Control.DisplayRectangle%2A>、 <xref:System.Windows.Forms.Control.Enabled%2A>、 <xref:System.Windows.Forms.Control.Focused%2A>、 <xref:System.Windows.Forms.Control.Height%2A>、 <xref:System.Windows.Forms.Control.Width%2A>、 <xref:System.Windows.Forms.Control.Visible%2A>、 <xref:System.Windows.Forms.Control.AutoSize%2A>、その他の多くとします。 詳細については、継承されたプロパティは、次を参照してください。<xref:System.Windows.Forms.Control?displayProperty=nameWithType>します。  
  
 コントロールで継承されたプロパティをオーバーライドしたり、新しいプロパティを定義したりできます。  
  
## <a name="in-this-section"></a>このセクションの内容  
 [プロパティの定義](../../../../docs/framework/winforms/controls/defining-a-property-in-windows-forms-controls.md)  
 カスタム コントロールまたはカスタム コンポーネントのプロパティを実装する方法と、そのプロパティをデザイン環境に統合する方法について説明します。  
  
 [ShouldSerialize メソッドと Reset メソッドによる既定値の定義](../../../../docs/framework/winforms/controls/defining-default-values-with-the-shouldserialize-and-reset-methods.md)  
 カスタム コントロールまたはカスタム コンポーネントの既定のプロパティ値を定義する方法について説明します。  
  
 [プロパティ変更イベント](../../../../docs/framework/winforms/controls/property-changed-events.md)  
 プロパティ値が変更されたときに、プロパティ変更通知を有効にする方法について説明します。  
  
 [方法 : 内在コントロールのプロパティを公開する](../../../../docs/framework/winforms/controls/how-to-expose-properties-of-constituent-controls.md)  
 カスタム複合コントロール内の内在コントロールのプロパティを公開する方法について説明します。  
  
 [カスタム コントロールへのメソッドの実装](../../../../docs/framework/winforms/controls/method-implementation-in-custom-controls.md)  
 カスタム コントロールおよびカスタム コンポーネントにメソッドを実装する方法について説明します。  
  
## <a name="reference"></a>参照  
 <xref:System.Windows.Forms.UserControl>  
 複合コントロールを実装するための基本クラスについて説明します。  
  
 <xref:System.ComponentModel.TypeConverterAttribute>  
 指定する属性について、<xref:System.ComponentModel.TypeConverter>カスタム プロパティの型を使用します。  
  
 <xref:System.ComponentModel.EditorAttribute>  
 指定する属性について、<xref:System.Drawing.Design.UITypeEditor>カスタム プロパティに使用します。  
  
## <a name="related-sections"></a>関連項目  
 [Windows フォーム コントロールの属性](../../../../docs/framework/winforms/controls/attributes-in-windows-forms-controls.md)  
 カスタム コントロールとコンポーネントのプロパティや他のメンバーに適用できる属性について説明します。  
  
 [コンポーネントのデザイン時属性](https://msdn.microsoft.com/library/12050fe3-9327-4509-9e21-4ee2494b95c3)  
 ビジュアル デザイナーでデザインするときに正しく表示されるようにコンポーネントとコントロールに適用するメタデータ属性の一覧を表示します。  
  
 [デザイン時サポートの拡張](https://msdn.microsoft.com/library/d6ac8a6a-42fd-4bc8-bf33-b212811297e2)  
 デザイン時サポートを提供するエディターやデザイナーなどのクラスを実装する方法について説明します。
