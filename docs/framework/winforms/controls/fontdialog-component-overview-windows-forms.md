---
title: FontDialog コンポーネントの概要 (Windows フォーム)
ms.date: 03/30/2017
f1_keywords:
- FontDialog
helpviewer_keywords:
- Font dialog box [Windows Forms], Windows Forms
- Font dialog box
- FontDialog component [Windows Forms], about FontDialog component
ms.assetid: daf46e57-1b4b-4b7a-bad0-b50ca7ba75dc
ms.openlocfilehash: 854f54454c0c88f965d9ac8240c11f6821f0c64b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54594565"
---
# <a name="fontdialog-component-overview-windows-forms"></a>FontDialog コンポーネントの概要 (Windows フォーム)
Windows フォーム<xref:System.Windows.Forms.FontDialog>コンポーネントは構成済みのダイアログ ボックス、標準の Windows である**フォント** ダイアログ ボックスが、システムに現在インストールされているフォントを公開するために使用します。 フォントの選択ダイアログ ボックスを構成する代わりに、シンプルなソリューションとして、Windows ベースのアプリケーション内で使用します。  
  
 既定では、ダイアログ ボックスに表示リスト ボックスのフォント、フォント スタイル、およびサイズです。取り消し線、下線; などの効果のチェック ボックススクリプトのドロップダウン リストフォントの表示方法のサンプルです。 (スクリプトは、特定のフォントの使用可能な別の文字のスクリプトなど、ヘブライ語や日本語)。フォント ダイアログ ボックスを表示するには<xref:System.Windows.Forms.CommonDialog.ShowDialog%2A>メソッド。  
  
## <a name="key-properties"></a>キー プロパティ  
 コンポーネントには、さまざまな外観を構成するプロパティがあります。 ダイアログ ボックスの選択項目を設定するプロパティは<xref:System.Windows.Forms.FontDialog.Font%2A>と<xref:System.Windows.Forms.FontDialog.Color%2A>します。 <xref:System.Windows.Forms.FontDialog.Font%2A>プロパティは、フォント、スタイル、サイズ、スクリプト、および効果を設定します。 たとえば、`Arial, 10pt, style=Italic, Strikeout`します。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.FontDialog>
- [FontDialog コンポーネント](../../../../docs/framework/winforms/controls/fontdialog-component-windows-forms.md)
