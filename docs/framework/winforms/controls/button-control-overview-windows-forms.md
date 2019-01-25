---
title: Button コントロールの概要 (Windows フォーム)
ms.date: 03/30/2017
f1_keywords:
- Button
helpviewer_keywords:
- Button control [Windows Forms], about Button control
- buttons [Windows Forms], about buttons
ms.assetid: 255b291b-51a9-4a92-a1a4-2400cd82443f
ms.openlocfilehash: 042ff7cb868b62778691348cb6c1ba464b794993
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54656441"
---
# <a name="button-control-overview-windows-forms"></a>Button コントロールの概要 (Windows フォーム)
Windows フォームの <xref:System.Windows.Forms.Button> コントロールを使用すると、ユーザーはそれをクリックしてアクションを実行できます。 ボタンをクリックすると、ボタンを実際に押して離したかのように表示されます。 ユーザーがクリックされるたびに、<xref:System.Windows.Forms.Control.Click>イベント ハンドラーが呼び出されます。 内のコードを配置する、<xref:System.Windows.Forms.Control.Click>イベント ハンドラーを選択したアクションを実行します。  
  
 ボタンに表示されるテキストが含まれている、<xref:System.Windows.Forms.Control.Text%2A>プロパティ。 テキストは、ボタンの幅を超えている場合は、次の行に折り返されます。 ただし、コントロールが全体の高さの増加に対応できない場合、このことがクリッピングされます。 詳細については、「[方法 :によって表示されるテキストを設定、Windows フォーム コントロール](../../../../docs/framework/winforms/controls/how-to-set-the-text-displayed-by-a-windows-forms-control.md)します。 <xref:System.Windows.Forms.Control.Text%2A>プロパティは、ユーザーをアクセス キーと ALT キーを押して、コントロールを「クリックして」に許可するアクセス キーを含めることができます。 詳細については、次を参照してください。[方法。Windows フォーム コントロールのアクセス キーを作成](../../../../docs/framework/winforms/controls/how-to-create-access-keys-for-windows-forms-controls.md)です。 テキストの外観はによって制御されます、<xref:System.Windows.Forms.Control.Font%2A>プロパティおよび<xref:System.Windows.Forms.ButtonBase.TextAlign%2A>プロパティ。  
  
 <xref:System.Windows.Forms.Button>コントロールできますを使用してイメージを表示しても、<xref:System.Windows.Forms.ButtonBase.Image%2A>と<xref:System.Windows.Forms.ButtonBase.ImageList%2A>プロパティ。 詳細については、「[方法 :によって表示されるイメージの設定を Windows フォーム コントロール](../../../../docs/framework/winforms/controls/how-to-set-the-image-displayed-by-a-windows-forms-control.md)します。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.Button>
- [方法: Windows フォームのボタン クリックに応答するには](../../../../docs/framework/winforms/controls/how-to-respond-to-windows-forms-button-clicks.md)
- [Windows フォームの Button コントロールを選択する方法](../../../../docs/framework/winforms/controls/ways-to-select-a-windows-forms-button-control.md)
- [方法: Windows フォームの Button をデザイナーの使用を承認ボタンとして指定します。](../../../../docs/framework/winforms/controls/designate-a-wf-button-as-the-accept-button-using-the-designer.md)
- [方法: デザイナーを使用して、[キャンセル] ボタンとして Windows フォームの Button を指定します。](../../../../docs/framework/winforms/controls/designate-a-wf-button-as-the-cancel-button-using-the-designer.md)
- [Button コントロール](../../../../docs/framework/winforms/controls/button-control-windows-forms.md)
