---
title: DatePicker
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], DatePicker
- DatePicker control [WPF]
ms.assetid: 619765c8-8d25-4315-aec2-79aea08fed9f
ms.openlocfilehash: 34df32ceecf66061b74834dcecdef8a080b7af34
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54565600"
---
# <a name="datepicker"></a>DatePicker
<xref:System.Windows.Controls.DatePicker>コントロールによりユーザーはテキスト フィールドにいずれかを入力するか、ドロップダウンを使用して日付を選択する<xref:System.Windows.Controls.Calendar>コントロール。  
  
 次の図は、<xref:System.Windows.Controls.DatePicker>します。  
  
 ![DatePicker コントロール](../../../../docs/framework/wpf/controls/media/ndp-datepicker.png "NDP_DatePicker")  
DatePicker コントロール  
  
 多くを<xref:System.Windows.Controls.DatePicker>コントロールのプロパティは、その組み込みを管理するため<xref:System.Windows.Controls.Calendar>と同等のプロパティとまったく同様に関数<xref:System.Windows.Controls.Calendar>します。 具体的には、 <xref:System.Windows.Controls.DatePicker.IsTodayHighlighted%2A?displayProperty=nameWithType>、 <xref:System.Windows.Controls.DatePicker.FirstDayOfWeek%2A?displayProperty=nameWithType>、 <xref:System.Windows.Controls.DatePicker.BlackoutDates%2A?displayProperty=nameWithType>、 <xref:System.Windows.Controls.DatePicker.DisplayDateStart%2A?displayProperty=nameWithType>、 <xref:System.Windows.Controls.DatePicker.DisplayDateEnd%2A?displayProperty=nameWithType>、 <xref:System.Windows.Controls.DatePicker.DisplayDate%2A?displayProperty=nameWithType>、および<xref:System.Windows.Controls.DatePicker.SelectedDate%2A?displayProperty=nameWithType>プロパティ関数と同様に、<xref:System.Windows.Controls.Calendar>の対応します。 詳細については、「 <xref:System.Windows.Controls.Calendar> 」を参照してください。  
  
 ユーザーが日付を入力設定テキスト フィールドに直接、<xref:System.Windows.Controls.DatePicker.Text%2A>プロパティ。 場合、<xref:System.Windows.Controls.DatePicker>有効な日付を入力した文字列を変換することはできません、<xref:System.Windows.Controls.DatePicker.DateValidationError>イベントが発生します。 既定では、これにより、イベント ハンドラーが例外<xref:System.Windows.Controls.DatePicker.DateValidationError>を設定できます、<xref:System.Windows.Controls.DatePickerDateValidationErrorEventArgs.ThrowException%2A>プロパティを`false`と例外が発生しているようにします。  
  
## <a name="see-also"></a>関連項目
- [コントロール](../../../../docs/framework/wpf/controls/index.md)
- [スタイルとテンプレート](../../../../docs/framework/wpf/controls/styling-and-templating.md)
