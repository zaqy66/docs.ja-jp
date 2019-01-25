---
title: '方法: Windows フォームの NumericUpDown コントロールの形式を設定します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- NumericUpDown control [Windows Forms], formatting values
- up-down controls [Windows Forms], formatting numeric values
ms.assetid: fa7c5557-6bfb-45b2-975d-8887b23b0ba0
ms.openlocfilehash: 5574faf858c32752cfa99b6bf339ddf06cb6b345
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631010"
---
# <a name="how-to-set-the-format-for-the-windows-forms-numericupdown-control"></a>方法: Windows フォームの NumericUpDown コントロールの形式を設定します。
Windows フォームで値を表示する方法を構成する<xref:System.Windows.Forms.NumericUpDown>コントロール。 <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A>プロパティは、小数点より後に表示される番号の数を決定します。 既定値は 0。 <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A>プロパティが 3 桁ごとの間の区切り記号が挿入されるかどうかを決定します。 既定値は`false`します。 コントロールは、場合に、10 進数の形式ではなく 16 進数の値を表示できます、<xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A>プロパティに設定されて`true`; 既定値は`false`します。  
  
### <a name="to-format-the-numeric-value"></a>数値の書式設定  
  
-   10 進値を設定して、表示、<xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A>プロパティを整数に設定、<xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A>プロパティを`true`または`false`します。  
  
    ```vb  
    NumericUpDown1.DecimalPlaces = 2  
    NumericUpDown1.ThousandsSeparator = True  
    ```  
  
    ```csharp  
    numericUpDown1.DecimalPlaces = 2;  
    numericUpDown1.ThousandsSeparator = true;  
    ```  
  
    ```cpp  
    numericUpDown1->DecimalPlaces = 2;  
    numericUpDown1->ThousandsSeparator = true;  
    ```  
  
     - または -  
  
-   16 進数の値を設定して表示、<xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A>プロパティを`true`します。  
  
    ```vb  
    NumericUpDown1.Hexadecimal = True  
    ```  
  
    ```csharp  
    numericUpDown1.Hexadecimal = true;  
    ```  
  
    ```cpp  
    numericUpDown1->Hexadecimal = true;  
    ```  
  
    > [!NOTE]
    >  実行するすべてのテスト値は、16 進数としてフォームに表示されますが、場合でも、<xref:System.Windows.Forms.NumericUpDown.Value%2A>プロパティに、10 進値をテストします。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.NumericUpDown>
- [NumericUpDown コントロール](../../../../docs/framework/winforms/controls/numericupdown-control-windows-forms.md)
- [NumericUpDown コントロールの概要](../../../../docs/framework/winforms/controls/numericupdown-control-overview-windows-forms.md)
