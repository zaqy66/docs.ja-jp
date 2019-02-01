---
title: '方法: Windows サービスを作成する'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Service applications, creating
- templates, Windows Service
ms.assetid: 0f5e2cbb-d95d-477c-b2b5-4b990e6b86ff
author: ghogen
ms.openlocfilehash: d0a450483c05a272fe799c7ee04e691cefbd2085
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54533755"
---
# <a name="how-to-create-windows-services"></a><span data-ttu-id="00b38-102">方法: Windows サービスを作成する</span><span class="sxs-lookup"><span data-stu-id="00b38-102">How to: Create Windows Services</span></span>
<span data-ttu-id="00b38-103">サービスを作成するときには、**Windows サービス**と呼ばれる、Visual Studio プロジェクトのテンプレートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="00b38-103">When you create a service, you can use a Visual Studio project template called **Windows Service**.</span></span> <span data-ttu-id="00b38-104">このテンプレートを使用すると、作業の多くを自動化できます。この自動化は、適切なクラスと名前空間を参照し、サービスの基底クラスからの継承を設定し、メソッドのいくつかをオーバーライドすることで実現されます。</span><span class="sxs-lookup"><span data-stu-id="00b38-104">This template automatically does much of the work for you by referencing the appropriate classes and namespaces, setting up the inheritance from the base class for services, and overriding several of the methods you're likely to want to override.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="00b38-105">Windows サービスのプロジェクト テンプレートは、Visual Studio の Express Edition では使用できません。</span><span class="sxs-lookup"><span data-stu-id="00b38-105">The Windows Services project template is not available in the Express edition of Visual Studio.</span></span>  
  
 <span data-ttu-id="00b38-106">実用的なサービスを作成するには、少なくとも以下の作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="00b38-106">At a minimum, to create a functional service you must:</span></span>  
  
-   <span data-ttu-id="00b38-107"><xref:System.ServiceProcess.ServiceBase.ServiceName%2A> プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="00b38-107">Set the <xref:System.ServiceProcess.ServiceBase.ServiceName%2A> property.</span></span>  
  
-   <span data-ttu-id="00b38-108">サービス アプリケーションに必要なインストーラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="00b38-108">Create the necessary installers for your service application.</span></span>  
  
-   <span data-ttu-id="00b38-109"><xref:System.ServiceProcess.ServiceBase.OnStart%2A> メソッドと <xref:System.ServiceProcess.ServiceBase.OnStop%2A> メソッドのオーバーライドとコーディングを行い、サービスの動作をカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="00b38-109">Override and specify code for the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> and <xref:System.ServiceProcess.ServiceBase.OnStop%2A> methods to customize the ways in which your service behaves.</span></span>  
  
### <a name="to-create-a-windows-service-application"></a><span data-ttu-id="00b38-110">Windows サービス アプリケーションを作成するには</span><span class="sxs-lookup"><span data-stu-id="00b38-110">To create a Windows Service application</span></span>  
  
1.  <span data-ttu-id="00b38-111">**Windows サービス** プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="00b38-111">Create a **Windows Service** project.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="00b38-112">テンプレートを使用せずにサービスを記述する方法については、「[方法: プログラムでサービスを作成する](../../../docs/framework/windows-services/how-to-write-services-programmatically.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00b38-112">For instructions on writing a service without using the template, see [How to: Write Services Programmatically](../../../docs/framework/windows-services/how-to-write-services-programmatically.md).</span></span>  
  
2.  <span data-ttu-id="00b38-113">**[プロパティ]** ウィンドウで、サービスの <xref:System.ServiceProcess.ServiceBase.ServiceName%2A> プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="00b38-113">In the **Properties** window, set the <xref:System.ServiceProcess.ServiceBase.ServiceName%2A> property for your service.</span></span>  
  
     <span data-ttu-id="00b38-114">![ServiceName プロパティを設定する。](../../../docs/framework/windows-services/media/windowsservice-servicename.PNG "WindowsService_ServiceName")</span><span class="sxs-lookup"><span data-stu-id="00b38-114">![Set the ServiceName property.](../../../docs/framework/windows-services/media/windowsservice-servicename.PNG "WindowsService_ServiceName")</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="00b38-115"><xref:System.ServiceProcess.ServiceBase.ServiceName%2A> プロパティの値は、各インストーラー クラスに記録されている名前と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00b38-115">The value of the <xref:System.ServiceProcess.ServiceBase.ServiceName%2A> property must always match the name recorded in the installer classes.</span></span> <span data-ttu-id="00b38-116">このプロパティを変更した場合は、インストーラー クラスの <xref:System.ServiceProcess.ServiceBase.ServiceName%2A> プロパティも変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00b38-116">If you change this property, you must update the <xref:System.ServiceProcess.ServiceBase.ServiceName%2A> property of installer classes as well.</span></span>  
  
3.  <span data-ttu-id="00b38-117">次のいずれかのプロパティを設定して、サービスの動作を決定します。</span><span class="sxs-lookup"><span data-stu-id="00b38-117">Set any of the following properties to determine how your service will function.</span></span>  
  
    |<span data-ttu-id="00b38-118">プロパティ</span><span class="sxs-lookup"><span data-stu-id="00b38-118">Property</span></span>|<span data-ttu-id="00b38-119">設定</span><span class="sxs-lookup"><span data-stu-id="00b38-119">Setting</span></span>|  
    |--------------|-------------|  
    |<xref:System.ServiceProcess.ServiceBase.CanStop%2A>|<span data-ttu-id="00b38-120">サービスが実行停止要求を受け付ける場合は `True` を設定します。サービスの実行を停止しない場合は `false` を設定します。</span><span class="sxs-lookup"><span data-stu-id="00b38-120">`True` to indicate that the service will accept requests to stop running; `false` to prevent the service from being stopped.</span></span>|  
    |<xref:System.ServiceProcess.ServiceBase.CanShutdown%2A>|<span data-ttu-id="00b38-121">サービスがコンピューターのシャットダウン時に通知を受けて `True` プロシージャを呼び出す場合は、<xref:System.ServiceProcess.ServiceBase.OnShutdown%2A> を設定します。</span><span class="sxs-lookup"><span data-stu-id="00b38-121">`True` to indicate that the service wants to receive notification when the computer on which it lives shuts down, enabling it to call the <xref:System.ServiceProcess.ServiceBase.OnShutdown%2A> procedure.</span></span>|  
    |<xref:System.ServiceProcess.ServiceBase.CanPauseAndContinue%2A>|<span data-ttu-id="00b38-122">サービスが一時停止要求または再開要求を受け付ける場合は `True` を設定します。サービスを一時停止または再開しない場合は `false` を設定します。</span><span class="sxs-lookup"><span data-stu-id="00b38-122">`True` to indicate that the service will accept requests to pause or to resume running; `false` to prevent the service from being paused and resumed.</span></span>|  
    |<xref:System.ServiceProcess.ServiceBase.CanHandlePowerEvent%2A>|<span data-ttu-id="00b38-123">コンピューターの電源状態の変化をサービスに通知する場合は `True` を設定します。サービスに電源状態の変化を通知しない場合は、`false` を設定します。</span><span class="sxs-lookup"><span data-stu-id="00b38-123">`True` to indicate that the service can handle notification of changes to the computer's power status; `false` to prevent the service from being notified of these changes.</span></span>|  
    |<xref:System.ServiceProcess.ServiceBase.AutoLog%2A>|<span data-ttu-id="00b38-124">サービスがアクションを実行したときにアプリケーション イベント ログに情報を入力する場合は `True` を設定します。この機能を無効にする場合は `false` を設定します。</span><span class="sxs-lookup"><span data-stu-id="00b38-124">`True` to write informational entries to the Application event log when your service performs an action; `false` to disable this functionality.</span></span> <span data-ttu-id="00b38-125">詳細については、「[方法 :サービスに関する情報のログを記録する](../../../docs/framework/windows-services/how-to-log-information-about-services.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00b38-125">For more information, see [How to: Log Information About Services](../../../docs/framework/windows-services/how-to-log-information-about-services.md).</span></span> <span data-ttu-id="00b38-126">**注:** 既定では、<xref:System.ServiceProcess.ServiceBase.AutoLog%2A> は `true` に設定されています。</span><span class="sxs-lookup"><span data-stu-id="00b38-126">**Note:**  By default, <xref:System.ServiceProcess.ServiceBase.AutoLog%2A> is set to `true`.</span></span>|  
  
    > [!NOTE]
    >  <span data-ttu-id="00b38-127"><xref:System.ServiceProcess.ServiceBase.CanStop%2A> または <xref:System.ServiceProcess.ServiceBase.CanPauseAndContinue%2A> を `false` に設定すると、**サービス コントロール マネージャー**は、対応するメニュー オプション (サービスの停止、一時停止、または継続) を無効にします。</span><span class="sxs-lookup"><span data-stu-id="00b38-127">When <xref:System.ServiceProcess.ServiceBase.CanStop%2A> or <xref:System.ServiceProcess.ServiceBase.CanPauseAndContinue%2A> are set to `false`, the **Service Control Manager** will disable the corresponding menu options to stop, pause, or continue the service.</span></span>  
  
4.  <span data-ttu-id="00b38-128">コード エディターを起動し、<xref:System.ServiceProcess.ServiceBase.OnStart%2A> プロシージャと <xref:System.ServiceProcess.ServiceBase.OnStop%2A> プロシージャの処理を記述します。</span><span class="sxs-lookup"><span data-stu-id="00b38-128">Access the Code Editor and fill in the processing you want for the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> and <xref:System.ServiceProcess.ServiceBase.OnStop%2A> procedures.</span></span>  
  
5.  <span data-ttu-id="00b38-129">ほかに動作を定義するメソッドがある場合は、それをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="00b38-129">Override any other methods for which you want to define functionality.</span></span>  
  
6.  <span data-ttu-id="00b38-130">サービス アプリケーションの必要なインストーラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="00b38-130">Add the necessary installers for your service application.</span></span> <span data-ttu-id="00b38-131">詳細については、「[方法 :サービス アプリケーションにインストーラーを追加する](../../../docs/framework/windows-services/how-to-add-installers-to-your-service-application.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00b38-131">For more information, see [How to: Add Installers to Your Service Application](../../../docs/framework/windows-services/how-to-add-installers-to-your-service-application.md).</span></span>  
  
7.  <span data-ttu-id="00b38-132">**[ビルド]** メニューの **[ソリューションのビルド]** をクリックして、プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="00b38-132">Build your project by selecting **Build Solution** from the **Build** menu.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="00b38-133">F5 キーを押してプロジェクトを実行しないでください。この方法ではサービス プロジェクトを実行できません。</span><span class="sxs-lookup"><span data-stu-id="00b38-133">Do not press F5 to run your project — you cannot run a service project in this way.</span></span>  
  
8.  <span data-ttu-id="00b38-134">サービスをインストールします。</span><span class="sxs-lookup"><span data-stu-id="00b38-134">Install the service.</span></span> <span data-ttu-id="00b38-135">詳細については、「[方法 :サービスをインストールおよびアンインストールする](../../../docs/framework/windows-services/how-to-install-and-uninstall-services.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00b38-135">For more information, see [How to: Install and Uninstall Services](../../../docs/framework/windows-services/how-to-install-and-uninstall-services.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="00b38-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="00b38-136">See also</span></span>
- [<span data-ttu-id="00b38-137">Windows サービス アプリケーションの概要</span><span class="sxs-lookup"><span data-stu-id="00b38-137">Introduction to Windows Service Applications</span></span>](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)
- [<span data-ttu-id="00b38-138">方法: プログラムでサービスを作成する</span><span class="sxs-lookup"><span data-stu-id="00b38-138">How to: Write Services Programmatically</span></span>](../../../docs/framework/windows-services/how-to-write-services-programmatically.md)
- [<span data-ttu-id="00b38-139">方法: サービス アプリケーションにインストーラーを追加する</span><span class="sxs-lookup"><span data-stu-id="00b38-139">How to: Add Installers to Your Service Application</span></span>](../../../docs/framework/windows-services/how-to-add-installers-to-your-service-application.md)
- [<span data-ttu-id="00b38-140">方法: サービスに関する情報のログを記録する</span><span class="sxs-lookup"><span data-stu-id="00b38-140">How to: Log Information About Services</span></span>](../../../docs/framework/windows-services/how-to-log-information-about-services.md)
- [<span data-ttu-id="00b38-141">方法: サービスを開始する</span><span class="sxs-lookup"><span data-stu-id="00b38-141">How to: Start Services</span></span>](../../../docs/framework/windows-services/how-to-start-services.md)
- [<span data-ttu-id="00b38-142">方法: サービスのセキュリティ コンテキストを指定する</span><span class="sxs-lookup"><span data-stu-id="00b38-142">How to: Specify the Security Context for Services</span></span>](../../../docs/framework/windows-services/how-to-specify-the-security-context-for-services.md)
- [<span data-ttu-id="00b38-143">方法: サービスをインストールおよびアンインストールする</span><span class="sxs-lookup"><span data-stu-id="00b38-143">How to: Install and Uninstall Services</span></span>](../../../docs/framework/windows-services/how-to-install-and-uninstall-services.md)
- [<span data-ttu-id="00b38-144">チュートリアル: コンポーネント デザイナーによる Windows サービス アプリケーションの作成</span><span class="sxs-lookup"><span data-stu-id="00b38-144">Walkthrough: Creating a Windows Service Application in the Component Designer</span></span>](../../../docs/framework/windows-services/walkthrough-creating-a-windows-service-application-in-the-component-designer.md)
