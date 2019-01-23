---
title: '方法: PrintForm コンポーネント (Visual Basic) を使用して、フォームを印刷します。'
ms.date: 07/20/2015
helpviewer_keywords:
- Form [Visual Basic], printing
ms.assetid: df963bf6-3ee1-49f4-8b2e-1d95d1beb0be
ms.openlocfilehash: 0a1a62627390c8839625862b9d43d61fc07ebf12
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521570"
---
# <a name="how-to-print-a-form-by-using-the-printform-component-visual-basic"></a>方法: PrintForm コンポーネント (Visual Basic) を使用して、フォームを印刷します。
<xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> コンポーネントを使用すると、 <xref:System.Drawing.Printing.PrintDocument> コンポーネントを使わなくても、画面に表示されているとおりにフォームのイメージをすぐに印刷することができます。 次の手順では、プリンター、印刷プレビュー ウィンドウ、およびカプセル化された PostScript ファイルにフォームを印刷する方法を示します。  
  
 PowerPack コントロールは、Visual Studio には含まれなくなりましたが、 [ダウンロード センター](https://www.microsoft.com/en-us/download/details.aspx?id=25169)からダウンロードできます。  
  
### <a name="to-print-a-form-to-the-default-printer"></a>既定のプリンターにフォームを印刷するには  
  
1.  **ツールボックス**で、 **[Visual Basic PowerPacks]** タブをクリックして、 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> コンポーネントをフォームにドラッグします。  
  
     <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> コンポーネントをコンポーネント トレイに追加します。  
  
2.  **[プロパティ]** ウィンドウで、 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> プロパティを <xref:System.Drawing.Printing.PrintAction.PrintToPrinter>に設定します。  
  
3.  適切なイベント ハンドラー (たとえば `Click` [印刷] **の**`Button`イベント ハンドラー) に、次のコードを追加します。  
  
    ```  
    PrintForm1.Print()  
    ```  
  
### <a name="to-display-a-form-in-a-print-preview-window"></a>[印刷プレビュー] ウィンドウでフォームを表示するには  
  
1.  **ツールボックス**で、 **[Visual Basic PowerPacks]** タブをクリックして、 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> コンポーネントをフォームにドラッグします。  
  
     <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> コンポーネントをコンポーネント トレイに追加します。  
  
2.  **[プロパティ]** ウィンドウで、 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> プロパティを <xref:System.Drawing.Printing.PrintAction.PrintToPreview>に設定します。  
  
3.  適切なイベント ハンドラー (たとえば `Click` [印刷] **の**`Button`イベント ハンドラー) に、次のコードを追加します。  
  
    ```  
    PrintForm1.Print()  
    ```  
  
### <a name="to-print-a-form-to-a-file"></a>ファイルにフォームを印刷するには  
  
1.  **ツールボックス**で、 **[Visual Basic PowerPacks]** タブをクリックして、 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> コンポーネントをフォームにドラッグします。  
  
     <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> コンポーネントをコンポーネント トレイに追加します。  
  
2.  **[プロパティ]** ウィンドウで、 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> プロパティを <xref:System.Drawing.Printing.PrintAction.PrintToFile>に設定します。  
  
3.  必要に応じて、 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintFileName%2A> プロパティを選択して、対象ファイルの完全なパスとファイル名を入力します。  
  
     この手順をスキップすると、ユーザーは実行時にファイル名を求められます。  
  
4.  適切なイベント ハンドラー (たとえば `Click` [印刷] **の**`Button`イベント ハンドラー) に、次のコードを追加します。  
  
    ```  
    PrintForm1.Print()  
    ```  
  
## <a name="see-also"></a>関連項目
- <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A>
- <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintFileName%2A>
- [方法: フォームのクライアント領域を印刷する](../../../visual-basic/developing-apps/printing/how-to-print-the-client-area-of-a-form.md)
- [方法: フォームのクライアント領域と非クライアント領域を印刷する](../../../visual-basic/developing-apps/printing/how-to-print-client-and-non-client-areas-of-a-form.md)
- [方法: スクロール可能フォームを印刷する](../../../visual-basic/developing-apps/printing/how-to-print-a-scrollable-form.md)
- [PrintForm コンポーネント](../../../visual-basic/developing-apps/printing/printform-component.md)
