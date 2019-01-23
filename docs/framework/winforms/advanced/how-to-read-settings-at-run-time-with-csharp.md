---
title: '方法: 実行時の設定の読み取りC#'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], reading
- application settings [Windows Forms], run time
- application settings [Windows Forms], C#
ms.assetid: dbe8bf09-5e1c-49da-9192-154033d7240b
ms.openlocfilehash: d798b40e5e337ea7652c8e82cb7fa860a87528b9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521752"
---
# <a name="how-to-read-settings-at-run-time-with-c"></a>方法: 実行時の設定の読み取りC# #
アプリケーション スコープの設定とユーザー スコープの設定は、どちらも実行時に Properties オブジェクトを使用して読み取ることができます。 Properties オブジェクトは、プロジェクトのすべての既定の設定を、Properties.Settings.Default メンバーを介して公開します。  
  
### <a name="to-read-settings-at-run-time-with-c"></a>実行時に設定を C# で読み取るには  
  
-   Properties.Settings.Default メンバーを介して適切な設定にアクセスします。 BackColor プロパティに `myColor` という名前の設定を割り当てる方法を次の例に示します。 この例を実行する前に、`myColor` という名前の `System.Drawing.Color` 型の設定を含む設定ファイルを作成しておく必要があります。 設定ファイルを作成する方法の詳細については、次を参照してください[How To:。デザイン時に新しい設定を作成](../../../../docs/framework/winforms/advanced/how-to-create-a-new-setting-at-design-time.md)です。  
  
    ```  
    // C#  
    this.BackColor = Properties.Settings.Default.myColor;  
    ```  
  
## <a name="see-also"></a>関連項目
- [アプリケーション設定とユーザー設定の使用](../../../../docs/framework/winforms/advanced/using-application-settings-and-user-settings.md)
- [方法: 実行時にユーザー設定を書き込みC#](../../../../docs/framework/winforms/advanced/how-to-write-user-settings-at-run-time-with-csharp.md)
- [アプリケーション設定の概要](../../../../docs/framework/winforms/advanced/application-settings-overview.md)
