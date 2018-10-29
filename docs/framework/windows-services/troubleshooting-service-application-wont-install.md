---
title: 'トラブルシューティング: サービス アプリケーションをインストールできない場合'
ms.date: 03/30/2017
helpviewer_keywords:
- troubleshooting service applications
- services, troubleshooting
- services, debugging
- Windows NT services, troubleshooting
- troubleshooting NT services
- Windows Service applications, troubleshooting
ms.assetid: 45c48e2e-b97d-44bc-8896-14f328e0ce33
author: ghogen
ms.openlocfilehash: 0912ff0909ffa5b22bed07543a2e514de4fb1ff5
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48035832"
---
# <a name="troubleshooting-service-application-won39t-install"></a>トラブルシューティング: サービス アプリケーションをインストールできない場合
サービス アプリケーションが正しくインストールされない場合は、サービス クラスの <xref:System.ServiceProcess.ServiceBase.ServiceName%2A> プロパティが、そのサービスのインストーラーで示されているのと同じ値に設定されていることを確認します。 サービスが正しくインストールされるためには、両方のインスタンスで同じ値になっている必要があります。  
  
> [!NOTE]
>  また、インストール ログを見て、インストール プロセスについてのフィードバックを確認することもできます。  
  
 同じ名前の別のサービスが既にインストールされているかどうかも確認する必要があります。 インストールが成功するには、サービス名が一意である必要があります。  
  
## <a name="see-also"></a>参照  
 [Windows サービス アプリケーションの概要](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)
