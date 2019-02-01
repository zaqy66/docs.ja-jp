---
title: トラブルシューティング:Windows サービスをデバッグする場合
ms.date: 03/30/2017
helpviewer_keywords:
- debugging Windows Service applications
- debugging [Visual Studio], Windows services
- troubleshooting service applications
- services, troubleshooting
- troubleshooting debugging, Windows Services
- Windows Service applications, debugging
- services, debugging
- Windows Service applications, troubleshooting
ms.assetid: cf859d4c-f04c-4cb7-81e3-bc7de8bea190
author: ghogen
ms.openlocfilehash: cdffb3a8ce9c5119a0a17a8bc7e6ca78276423f4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745676"
---
# <a name="troubleshooting-debugging-windows-services"></a>トラブルシューティング:Windows サービスをデバッグする場合
Windows サービス アプリケーションをデバッグするとき、サービスと **Windows Service Manager** の間でやり取りが行われます。 **Service Manager** は <xref:System.ServiceProcess.ServiceBase.OnStart%2A> メソッドを呼び出してサービスを開始した後、<xref:System.ServiceProcess.ServiceBase.OnStart%2A> メソッドから戻るのを 30 秒間待ちます。 この時間内にメソッドから戻らない場合、Manager はサービスを開始できないというエラーを表示します。  
  
 「[方法: Windows サービス アプリケーションをデバッグする](../../../docs/framework/windows-services/how-to-debug-windows-service-applications.md)」の説明に従って <xref:System.ServiceProcess.ServiceBase.OnStart%2A> メソッドをデバッグする場合、この 30 秒間のことを認識しておく必要があります。 <xref:System.ServiceProcess.ServiceBase.OnStart%2A> メソッドにブレークポイントを設定し、30 秒以内にメソッドを最後までステップ実行しないと、Manager はサービスを開始しません。  
  
## <a name="see-also"></a>関連項目
- [方法: Windows サービス アプリケーションをデバッグする](../../../docs/framework/windows-services/how-to-debug-windows-service-applications.md)
- [Windows サービス アプリケーションの概要](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)
