---
title: '方法 : サービスを開始する'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Service applications, starting
- services, starting
ms.assetid: 9ea77955-2d96-4c3d-913c-14db7604cdad
author: ghogen
ms.openlocfilehash: b3f04deb11a23957198864c444b4872aef45b2e4
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47176748"
---
# <a name="how-to-start-services"></a><span data-ttu-id="8c5d2-102">方法 : サービスを開始する</span><span class="sxs-lookup"><span data-stu-id="8c5d2-102">How to: Start Services</span></span>
<span data-ttu-id="8c5d2-103">サービスをインストールした後で、サービスを起動します。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-103">After a service is installed, it must be started.</span></span> <span data-ttu-id="8c5d2-104">起動することで、サービス クラスの <xref:System.ServiceProcess.ServiceBase.OnStart%2A> メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-104">Starting calls the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method on the service class.</span></span> <span data-ttu-id="8c5d2-105">通常、<xref:System.ServiceProcess.ServiceBase.OnStart%2A> メソッドにはサービスが本来行う処理を定義します。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-105">Usually, the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method defines the useful work the service will perform.</span></span> <span data-ttu-id="8c5d2-106">サービスの起動後は、手動で一時停止または停止するまで、アクティブの状態を維持します。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-106">After a service starts, it remains active until it is manually paused or stopped.</span></span>  
  
 <span data-ttu-id="8c5d2-107">サービスを自動で起動するか手動で起動するかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-107">Services can be set up to start automatically or manually.</span></span> <span data-ttu-id="8c5d2-108">自動的に起動するサービスは、そのサービスがインストールされているコンピューターを再起動したとき、または初めて電源を入れたときに起動します。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-108">A service that starts automatically will be started when the computer on which it is installed is rebooted or first turned on.</span></span> <span data-ttu-id="8c5d2-109">手動で起動するサービスは、ユーザーが起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-109">A user must start a service that starts manually.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8c5d2-110">既定では、Visual Studio で作成されたサービスは手動で起動するように設定されます。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-110">By default, services created with Visual Studio are set to start manually.</span></span>  
  
 <span data-ttu-id="8c5d2-111">サービスを手動で起動するには、**サーバー エクスプローラー**または**サービス コントロール マネージャー**を使用します。<xref:System.ServiceProcess.ServiceController> コンポーネントを使ってコードによって起動することもできます。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-111">There are several ways you can manually start a service — from **Server Explorer**, from the **Services Control Manager**, or from code using a component called the <xref:System.ServiceProcess.ServiceController>.</span></span>  
  
 <span data-ttu-id="8c5d2-112"><xref:System.ServiceProcess.ServiceInstaller.StartType%2A> クラスの <xref:System.ServiceProcess.ServiceInstaller> プロパティを設定し、サービスを手動で起動するか自動で起動するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-112">You set the <xref:System.ServiceProcess.ServiceInstaller.StartType%2A> property on the <xref:System.ServiceProcess.ServiceInstaller> class to determine whether a service should be started manually or automatically.</span></span>  
  
### <a name="to-specify-how-a-service-should-start"></a><span data-ttu-id="8c5d2-113">サービスの起動方法を指定するには</span><span class="sxs-lookup"><span data-stu-id="8c5d2-113">To specify how a service should start</span></span>  
  
1.  <span data-ttu-id="8c5d2-114">サービスの作成後、必要なインストーラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-114">After creating your service, add the necessary installers for it.</span></span> <span data-ttu-id="8c5d2-115">詳しくは、「[方法: サービス アプリケーションにインストーラーを追加する](../../../docs/framework/windows-services/how-to-add-installers-to-your-service-application.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-115">For more information, see [How to: Add Installers to Your Service Application](../../../docs/framework/windows-services/how-to-add-installers-to-your-service-application.md).</span></span>  
  
2.  <span data-ttu-id="8c5d2-116">デザイナーで、対象となるサービスのインストーラーをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-116">In the designer, click the service installer for the service you are working with.</span></span>  
  
3.  <span data-ttu-id="8c5d2-117">**[プロパティ]** ウィンドウで、<xref:System.ServiceProcess.ServiceInstaller.StartType%2A> プロパティに次のいずれかの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-117">In the **Properties** window, set the <xref:System.ServiceProcess.ServiceInstaller.StartType%2A> property to one of the following:</span></span>  
  
    |<span data-ttu-id="8c5d2-118">サービスを起動するタイミング</span><span class="sxs-lookup"><span data-stu-id="8c5d2-118">To have your service install</span></span>|<span data-ttu-id="8c5d2-119">設定値</span><span class="sxs-lookup"><span data-stu-id="8c5d2-119">Set this value</span></span>|  
    |----------------------------------|--------------------|  
    |<span data-ttu-id="8c5d2-120">コンピューターを再起動したとき。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-120">When the computer is restarted</span></span>|<span data-ttu-id="8c5d2-121">**自動**</span><span class="sxs-lookup"><span data-stu-id="8c5d2-121">**Automatic**</span></span>|  
    |<span data-ttu-id="8c5d2-122">明示的なユーザー アクションによってサービスを開始するとき。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-122">When an explicit user action starts the service</span></span>|<span data-ttu-id="8c5d2-123">**手動**</span><span class="sxs-lookup"><span data-stu-id="8c5d2-123">**Manual**</span></span>|  
  
    > [!TIP]
    >  <span data-ttu-id="8c5d2-124">サービスが起動しないようにするには、<xref:System.ServiceProcess.ServiceInstaller.StartType%2A> プロパティを **[無効]** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-124">To prevent your service from being started at all, you can set the <xref:System.ServiceProcess.ServiceInstaller.StartType%2A> property to **Disabled**.</span></span> <span data-ttu-id="8c5d2-125">サーバーを数回再起動することが見込まれる場合は、サービスを自動的に起動しないように設定することで、再起動の時間を短縮できます。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-125">You might do this if you are going to reboot a server several times and want to save time by preventing the services that would normally start from starting up.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="8c5d2-126">以上のプロパティやその他のプロパティの設定は、サービスのインストール後に変更できます。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-126">These and other properties can be changed after your service is installed.</span></span>  
  
     <span data-ttu-id="8c5d2-127"><xref:System.ServiceProcess.ServiceInstaller.StartType%2A> プロパティが **[手動]** に設定されているサービスを起動するには、**サーバー エクスプローラー**または **Windows サービス コントロール マネージャー**を使います。また、コードで起動することもできます。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-127">There are several ways you can start a service that has its <xref:System.ServiceProcess.ServiceInstaller.StartType%2A> process set to **Manual** — from **Server Explorer**, from the **Windows Services Control Manager**, or from code.</span></span> <span data-ttu-id="8c5d2-128">起動方法によっては、**サービス コントロール マネージャー**のコンテキストではサービスを起動しません。**サーバー エクスプローラー**によるサービスの起動とコードによるサービスの起動の場合は、実際にはコントローラーを操作しています。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-128">It is important to note that not all of these methods actually start the service in the context of the **Services Control Manager**; **Server Explorer** and programmatic methods of starting the service actually manipulate the controller.</span></span>  
  
### <a name="to-manually-start-a-service-from-server-explorer"></a><span data-ttu-id="8c5d2-129">サーバー エクスプローラーでサービスを手動起動するには</span><span class="sxs-lookup"><span data-stu-id="8c5d2-129">To manually start a service from Server Explorer</span></span>  
  
1.  <span data-ttu-id="8c5d2-130">サーバーが**サーバー エクスプローラー**の一覧にない場合は追加します。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-130">In **Server Explorer**, add the server you want if it is not already listed.</span></span> <span data-ttu-id="8c5d2-131">詳しくは、「方法: サーバー エクスプローラー/データベース エクスプローラーにアクセスして初期化する」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-131">For more information, see How to: Access and Initialize Server Explorer-Database Explorer.</span></span>  
  
2.  <span data-ttu-id="8c5d2-132">**[サービス]** ノードを展開し、開始するサービスを検索します。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-132">Expand the **Services** node, and then locate the service you want to start.</span></span>  
  
3.  <span data-ttu-id="8c5d2-133">サービス名を右クリックし、**[開始]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-133">Right-click the name of the service, and click **Start**.</span></span>  
  
### <a name="to-manually-start-a-service-from-services-control-manager"></a><span data-ttu-id="8c5d2-134">サービス制御マネージャーでサービスを手動起動するには</span><span class="sxs-lookup"><span data-stu-id="8c5d2-134">To manually start a service from Services Control Manager</span></span>  
  
1.  <span data-ttu-id="8c5d2-135">**サービス コントロール マネージャー**を次のいずれかの方法で開きます。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-135">Open the **Services Control Manager** by doing one of the following:</span></span>  
  
    -   <span data-ttu-id="8c5d2-136">Windows XP および Windows 2000 Professional のデスクトップで、**[マイ コンピューター]** を右クリックし、**[管理]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-136">In Windows XP and 2000 Professional, right-click **My Computer** on the desktop, and then click **Manage**.</span></span> <span data-ttu-id="8c5d2-137">表示されるダイアログ ボックスで、**[サービスとアプリケーション]** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-137">In the dialog box that appears, expand the **Services and Applications** node.</span></span>  
  
         <span data-ttu-id="8c5d2-138">\- または</span><span class="sxs-lookup"><span data-stu-id="8c5d2-138">\- or -</span></span>  
  
    -   <span data-ttu-id="8c5d2-139">Windows Server 2003 および Windows 2000 Server では、**[スタート]** メニューの **[プログラム]** をポイントし、**[管理ツール]** をポイントして、**[サービス]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-139">In Windows Server 2003 and Windows 2000 Server, click **Start**, point to **Programs**, click **Administrative Tools**, and then click **Services**.</span></span>  
  
        > [!NOTE]
        >  <span data-ttu-id="8c5d2-140">Windows NT Version 4.0 では、**[コントロール パネル]** でこのダイアログ ボックスを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-140">In Windows NT version 4.0, you can open this dialog box from **Control Panel**.</span></span>  
  
     <span data-ttu-id="8c5d2-141">ウィンドウの **[サービス]** セクションに、サービスが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-141">You should now see your service listed in the **Services** section of the window.</span></span>  
  
2.  <span data-ttu-id="8c5d2-142">一覧で目的のサービスを右クリックし、**[開始]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-142">Select your service in the list, right-click it, and then click **Start**.</span></span>  
  
### <a name="to-manually-start-a-service-from-code"></a><span data-ttu-id="8c5d2-143">コードでサービスを手動起動するには</span><span class="sxs-lookup"><span data-stu-id="8c5d2-143">To manually start a service from code</span></span>  
  
1.  <span data-ttu-id="8c5d2-144"><xref:System.ServiceProcess.ServiceController> クラスのインスタンスを作成し、管理対象となるサービスと対話するように設定します。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-144">Create an instance of the <xref:System.ServiceProcess.ServiceController> class, and configure it to interact with the service you want to administer.</span></span>  
  
2.  <span data-ttu-id="8c5d2-145"><xref:System.ServiceProcess.ServiceController.Start%2A> メソッドを呼び出してサービスを起動します。</span><span class="sxs-lookup"><span data-stu-id="8c5d2-145">Call the <xref:System.ServiceProcess.ServiceController.Start%2A> method to start the service.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8c5d2-146">参照</span><span class="sxs-lookup"><span data-stu-id="8c5d2-146">See Also</span></span>  
 [<span data-ttu-id="8c5d2-147">Windows サービス アプリケーションの概要</span><span class="sxs-lookup"><span data-stu-id="8c5d2-147">Introduction to Windows Service Applications</span></span>](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)  
 [<span data-ttu-id="8c5d2-148">方法 : Windows サービスを作成する</span><span class="sxs-lookup"><span data-stu-id="8c5d2-148">How to: Create Windows Services</span></span>](../../../docs/framework/windows-services/how-to-create-windows-services.md)  
 [<span data-ttu-id="8c5d2-149">方法 : サービス アプリケーションにインストーラーを追加する</span><span class="sxs-lookup"><span data-stu-id="8c5d2-149">How to: Add Installers to Your Service Application</span></span>](../../../docs/framework/windows-services/how-to-add-installers-to-your-service-application.md)
