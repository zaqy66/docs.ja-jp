---
title: トラブルシューティング:サービス アプリケーションをインストールできない場合
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
ms.openlocfilehash: ecbaa3b2fb0e0fc85ed383385368617bf361f497
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55289436"
---
# <a name="troubleshooting-service-application-wont-install"></a><span data-ttu-id="30fa9-102">トラブルシューティング:サービス アプリケーションをインストールできない場合</span><span class="sxs-lookup"><span data-stu-id="30fa9-102">Troubleshooting: Service Application Won't Install</span></span>
<span data-ttu-id="30fa9-103">サービス アプリケーションが正しくインストールされない場合は、サービス クラスの <xref:System.ServiceProcess.ServiceBase.ServiceName%2A> プロパティが、そのサービスのインストーラーで示されているのと同じ値に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="30fa9-103">If your service application will not install correctly, check to make sure that the <xref:System.ServiceProcess.ServiceBase.ServiceName%2A> property for the service class is set to the same value as is shown in the installer for that service.</span></span> <span data-ttu-id="30fa9-104">サービスが正しくインストールされるためには、両方のインスタンスで同じ値になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="30fa9-104">The value must be the same in both instances in order for your service to install correctly.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="30fa9-105">また、インストール ログを見て、インストール プロセスについてのフィードバックを確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="30fa9-105">You can also look at the installation logs to get feedback on the installation process.</span></span>  
  
 <span data-ttu-id="30fa9-106">同じ名前の別のサービスが既にインストールされているかどうかも確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30fa9-106">You should also check to determine whether you have another service with the same name already installed.</span></span> <span data-ttu-id="30fa9-107">インストールが成功するには、サービス名が一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="30fa9-107">Service names must be unique for installation to succeed.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30fa9-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="30fa9-108">See also</span></span>
- [<span data-ttu-id="30fa9-109">Windows サービス アプリケーションの概要</span><span class="sxs-lookup"><span data-stu-id="30fa9-109">Introduction to Windows Service Applications</span></span>](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)
