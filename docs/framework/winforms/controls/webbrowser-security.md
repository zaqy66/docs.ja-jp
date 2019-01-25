---
title: WebBrowser セキュリティ
ms.date: 03/30/2017
helpviewer_keywords:
- WebBrowser control [Windows Forms], security
- security [Windows Forms], WebBrowser control
ms.assetid: 0968846e-48ee-485a-9797-65b5b9a622f8
ms.openlocfilehash: 4c69f1c39d3a22db361fef1ffb65f21aa9d75128
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54736274"
---
# <a name="webbrowser-security"></a><span data-ttu-id="e7d9e-102">WebBrowser セキュリティ</span><span class="sxs-lookup"><span data-stu-id="e7d9e-102">WebBrowser Security</span></span>
<span data-ttu-id="e7d9e-103"><xref:System.Windows.Forms.WebBrowser>コントロールがデザインされた、完全な信頼のみで機能します。</span><span class="sxs-lookup"><span data-stu-id="e7d9e-103">The <xref:System.Windows.Forms.WebBrowser> control is designed to work in full trust only.</span></span> <span data-ttu-id="e7d9e-104">コントロールに表示される HTML コンテンツでは、外部の Web サーバーから取得でき、スクリプトまたは Web コントロールの形式でアンマネージ コードを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="e7d9e-104">The HTML content displayed in the control can come from external Web servers and may contain unmanaged code in the form of scripts or Web controls.</span></span> <span data-ttu-id="e7d9e-105">使用する場合、<xref:System.Windows.Forms.WebBrowser>この状況では、コントロール内のコントロールは Internet Explorer である場合は、管理ですがより安全性が<xref:System.Windows.Forms.WebBrowser>コントロールが実行されているからこのようなアンマネージ コードを妨げません。</span><span class="sxs-lookup"><span data-stu-id="e7d9e-105">If you use the <xref:System.Windows.Forms.WebBrowser> control in this situation, the control is no less secure than Internet Explorer would be, but the managed <xref:System.Windows.Forms.WebBrowser> control does not prevent such unmanaged code from running.</span></span>  
  
 <span data-ttu-id="e7d9e-106">基になる ActiveX に関連するセキュリティ問題の詳細については`WebBrowser`コントロールを参照してください[WebBrowser コントロール](https://go.microsoft.com/fwlink/?LinkId=198812)します。</span><span class="sxs-lookup"><span data-stu-id="e7d9e-106">For more information about security issues relating to the underlying ActiveX `WebBrowser` control, see [WebBrowser Control](https://go.microsoft.com/fwlink/?LinkId=198812).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7d9e-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7d9e-107">See also</span></span>
- <xref:System.Windows.Forms.WebBrowser>
- [<span data-ttu-id="e7d9e-108">WebBrowser コントロールの概要</span><span class="sxs-lookup"><span data-stu-id="e7d9e-108">WebBrowser Control Overview</span></span>](../../../../docs/framework/winforms/controls/webbrowser-control-overview.md)
- [<span data-ttu-id="e7d9e-109">WebBrowser コントロール</span><span class="sxs-lookup"><span data-stu-id="e7d9e-109">WebBrowser Control</span></span>](https://go.microsoft.com/fwlink/?LinkId=198812)
