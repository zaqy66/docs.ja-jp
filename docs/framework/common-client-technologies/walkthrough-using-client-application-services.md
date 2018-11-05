---
title: 'チュートリアル : クライアント アプリケーション サービスの使用'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- application services host [client application services]
- client application services, walkthroughs
ms.assetid: bb7c8950-4517-4dae-b705-b74a14059b26
ms.openlocfilehash: d09ad4b1f518ac6f4c42dffd4b3ca17249b95700
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50194320"
---
# <a name="walkthrough-using-client-application-services"></a><span data-ttu-id="3cb95-102">チュートリアル : クライアント アプリケーション サービスの使用</span><span class="sxs-lookup"><span data-stu-id="3cb95-102">Walkthrough: Using Client Application Services</span></span>
<span data-ttu-id="3cb95-103">このトピックでは、ユーザーを認証し、ユーザーのロールと設定を取得するクライアント アプリケーション サービスを使用する Windows アプリケーションを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-103">This topic describes how to create a Windows application that uses client application services to authenticate users and retrieve user roles and settings.</span></span>  
  
 <span data-ttu-id="3cb95-104">このチュートリアルでは次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-104">In this walkthrough, you perform the following tasks:</span></span>  
  
-   <span data-ttu-id="3cb95-105">Windows フォーム アプリケーションを作成し、Visual Studio プロジェクト デザイナーを使用してクライアント アプリケーション サービスの有効化および構成を行います。</span><span class="sxs-lookup"><span data-stu-id="3cb95-105">Create a Windows Forms application and use the Visual Studio project designer to enable and configure client application services.</span></span>  
  
-   <span data-ttu-id="3cb95-106">アプリケーション サービスのホストと、クライアント構成のテストを行う、簡単な ASP.NET Web サービス アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-106">Create a simple ASP.NET Web Service application to host the application services and test your client configuration.</span></span>  
  
-   <span data-ttu-id="3cb95-107">フォーム認証をアプリケーションに追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-107">Add forms authentication to your application.</span></span> <span data-ttu-id="3cb95-108">最初に、ハード コーディングされたユーザー名とパスワードを使用して、サービスをテストします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-108">You will start by using a hard-coded user name and password to test the service.</span></span> <span data-ttu-id="3cb95-109">次に、アプリケーション構成でログイン フォームを資格情報プロバイダーとして指定して、ログイン フォームを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-109">You will then add a login form by specifying it as a credentials provider in your application configuration.</span></span>  
  
-   <span data-ttu-id="3cb95-110">"manager” ロールのユーザーのみに対してボタンを有効にして表示し、ロール ベースの機能を追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-110">Add role-based functionality, enabling and displaying a button only for users in the "manager" role.</span></span>  
  
-   <span data-ttu-id="3cb95-111">Web 設定にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-111">Access Web settings.</span></span> <span data-ttu-id="3cb95-112">最初に、プロジェクト デザイナーの **[設定]** ページで認証済みの (テスト) ユーザーの Web 設定を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-112">You will start by loading Web settings for an authenticated (test) user on the **Settings** page of the project designer.</span></span> <span data-ttu-id="3cb95-113">次に、Windows フォーム デザイナーを使用して、テキスト ボックスを Web 設定にバインドします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-113">You will then use the Windows Forms Designer to bind a text box to a Web setting.</span></span> <span data-ttu-id="3cb95-114">最後に、変更済みの値をサーバーに保存し直します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-114">Finally, you will save the modified value back to the server.</span></span>  
  
-   <span data-ttu-id="3cb95-115">ログアウトを実装します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-115">Implement logout.</span></span> <span data-ttu-id="3cb95-116">フォームにログアウト オプションを追加して、logout メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-116">You will add a logout option to the form and call a logout method.</span></span>  
  
-   <span data-ttu-id="3cb95-117">オフライン モードを有効にします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-117">Enable offline mode.</span></span> <span data-ttu-id="3cb95-118">ユーザーが接続状態を指定できるように、チェック ボックスを用意します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-118">You will provide a check box so that users can specify their connection status.</span></span> <span data-ttu-id="3cb95-119">次に、この値を使用して、クライアント アプリケーション サービス プロバイダーが Web サービスにアクセスするのではなく、ローカルにキャッシュされたデータを使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-119">You will then use this value to specify whether the client application service providers will use locally cached data instead of accessing their Web services.</span></span> <span data-ttu-id="3cb95-120">最後に、アプリケーションがオンライン モードに戻るときに、現在のユーザーを再認証します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-120">Finally, you will re-authenticate the current user when the application returns to online mode.</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="3cb95-121">必須コンポーネント</span><span class="sxs-lookup"><span data-stu-id="3cb95-121">Prerequisites</span></span>  

<span data-ttu-id="3cb95-122">このチュートリアルを完了するには Visual Studio が必要です。</span><span class="sxs-lookup"><span data-stu-id="3cb95-122">You need Visual Studio to complete this walkthrough.</span></span>
  
## <a name="creating-the-client-application"></a><span data-ttu-id="3cb95-123">クライアント アプリケーションの作成</span><span class="sxs-lookup"><span data-stu-id="3cb95-123">Creating the Client Application</span></span>  
 <span data-ttu-id="3cb95-124">最初に、Windows フォーム プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-124">The first thing that you will do is create a Windows Forms project.</span></span> <span data-ttu-id="3cb95-125">このチュートリアルでは Windows フォームを使用します。これはより多くの人が使い慣れているためです。しかし、プロセスは Windows Presentation Foundation (WPF) プロジェクトと類似しています。</span><span class="sxs-lookup"><span data-stu-id="3cb95-125">This walkthrough uses Windows Forms because more people are familiar with it, but the process is similar for Windows Presentation Foundation (WPF) projects.</span></span>  
  
#### <a name="to-create-a-client-application-and-enable-client-application-services"></a><span data-ttu-id="3cb95-126">クライアント アプリケーションを作成し、クライアント アプリケーション サービスを有効にするには</span><span class="sxs-lookup"><span data-stu-id="3cb95-126">To create a client application and enable client application services</span></span>  
  
1.  <span data-ttu-id="3cb95-127">Visual Studio で、**[ファイル] &#124; [新規作成] &#124; [プロジェクト]** メニュー オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-127">In Visual Studio, select the **File &#124; New &#124; Project** menu option.</span></span>  
  
2.  <span data-ttu-id="3cb95-128">**[新しいプロジェクト]** ダイアログ ボックスの **[プロジェクトの種類]** ペインで、**[Visual Basic]** または **[Visual C#]** ノードを展開し、プロジェクトの種類 **[Windows]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-128">In the **New Project** dialog box, in the **Project types** pane, expand the **Visual Basic** or **Visual C#** node and select the **Windows** project type.</span></span>  
  
3.  <span data-ttu-id="3cb95-129">**[.NET Framework 3.5]** が選択されていることを確認してから、 **[Windows フォーム アプリケーション]** テンプレートをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-129">Make sure that **.NET Framework 3.5** is selected, and then select the **Windows Forms Application** template.</span></span>  
  
4.  <span data-ttu-id="3cb95-130">プロジェクトの **[名前]** を `ClientAppServicesDemo`に変更してから、 **[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-130">Change the project **Name** to `ClientAppServicesDemo`, and then click **OK**.</span></span>  
  
     <span data-ttu-id="3cb95-131">Visual Studio に新しい Windows フォーム プロジェクトが開きます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-131">A new Windows Forms project is opened in Visual Studio.</span></span>  
  
5.  <span data-ttu-id="3cb95-132">**[プロジェクト]** メニューで、 **ClientAppServicesDemo**プロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-132">On the **Project** menu, select **ClientAppServicesDemo Properties**.</span></span>  
  
     <span data-ttu-id="3cb95-133">プロジェクト デザイナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-133">The project designer appears.</span></span>  
  
6.  <span data-ttu-id="3cb95-134">**[サービス]** タブで、 **[クライアント アプリケーション サービスを有効にする]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-134">On the **Services** tab, select **Enable client application services**.</span></span>  
  
7.  <span data-ttu-id="3cb95-135">**[フォーム認証]** が選択されていることを確認してから、 **[認証サービスの場所]**、 **[ロール サービスの場所]**、および **[Web 設定サービスの場所]** を `http://localhost:55555/AppServices`に設定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-135">Make sure that **Use Forms authentication** is selected, and then set **Authentication service location**, **Roles service location**, and **Web settings service location** to `http://localhost:55555/AppServices`.</span></span>  
  
8.  <span data-ttu-id="3cb95-136">Visual Basic では、**[アプリケーション]** タブで、**[認証モード]** を **[アプリケーション定義]** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-136">For Visual Basic, on the **Application** tab, set **Authentication mode** to **Application-defined**.</span></span>  
  
 <span data-ttu-id="3cb95-137">デザイナーは、アプリケーションの app.config ファイルに指定された設定を格納します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-137">The designer stores the specified settings in the application's app.config file.</span></span>  
  
 <span data-ttu-id="3cb95-138">この時点で、アプリケーションは、同じホストの 3 つのすべてのサービスにアクセスするように構成されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-138">At this point, the application is configured to access all three services from the same host.</span></span> <span data-ttu-id="3cb95-139">次のセクションでは、簡単な Web サービス アプリケーションとしてホストを作成し、クライアントの構成をテストできるようにします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-139">In the next section, you will create the host as a simple Web service application, enabling you to test your client configuration.</span></span>  
  
## <a name="creating-the-application-services-host"></a><span data-ttu-id="3cb95-140">アプリケーションのサービス ホストを作成する</span><span class="sxs-lookup"><span data-stu-id="3cb95-140">Creating the Application Services Host</span></span>  
 <span data-ttu-id="3cb95-141">このセクションでは、ローカルの SQL Server Compact データベース ファイルのユーザー データにアクセスする簡単な Web サービス アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-141">In this section, you will create a simple Web service application that accesses user data from a local SQL Server Compact database file.</span></span> <span data-ttu-id="3cb95-142">次に、 [ASP.NET Web Site Administration Tool](https://msdn.microsoft.com/library/100ddd8b-7d11-4df9-91ef-0bbbe92e5aec)を使用してデータベースにデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-142">Then, you will populate the database using the [ASP.NET Web Site Administration Tool](https://msdn.microsoft.com/library/100ddd8b-7d11-4df9-91ef-0bbbe92e5aec).</span></span> <span data-ttu-id="3cb95-143">この簡単な構成では、クライアント アプリケーションを短時間でテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-143">This simple configuration enables you to quickly test your client application.</span></span> <span data-ttu-id="3cb95-144">あるいは、Web サービス ホストを構成して、完全な SQL Server データベースから、またはユーザー設定の <xref:System.Web.Security.MembershipProvider> クラスと <xref:System.Web.Security.RoleProvider> クラスを介してユーザー データにアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-144">As an alternative, you can configure the Web service host to access user data from a full SQL Server database or through custom <xref:System.Web.Security.MembershipProvider> and <xref:System.Web.Security.RoleProvider> classes.</span></span> <span data-ttu-id="3cb95-145">詳細については、「 [Creating and Configuring the Application Services Database for SQL Server](https://msdn.microsoft.com/library/ab894e83-7e2f-4af8-a116-b1bff8f815b2)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cb95-145">For more information, see [Creating and Configuring the Application Services Database for SQL Server](https://msdn.microsoft.com/library/ab894e83-7e2f-4af8-a116-b1bff8f815b2).</span></span>  
  
 <span data-ttu-id="3cb95-146">次の手順では、AppServices の Web サービスを作成および構成します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-146">In the following procedure, you create and configure the AppServices Web service.</span></span>  
  
#### <a name="to-create-and-configure-the-application-services-host"></a><span data-ttu-id="3cb95-147">アプリケーション サービス ホストを作成および構成するには</span><span class="sxs-lookup"><span data-stu-id="3cb95-147">To create and configure the application services host</span></span>  
  
1.  <span data-ttu-id="3cb95-148">**[ソリューション エクスプローラー]** で、ClientAppServicesDemo ソリューションを選択してから、**[ファイル]** メニューで **[追加] &#124; [新しいプロジェクト]** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-148">In **Solution Explorer**, select the ClientAppServicesDemo solution, and then on the **File** menu, select **Add &#124; New Project**.</span></span>  
  
2.  <span data-ttu-id="3cb95-149">**[新しいプロジェクトの追加]** ダイアログ ボックスの **[プロジェクトの種類]** ペインで、**[Visual Basic]** または **[Visual C#]** ノードを展開し、プロジェクトの種類 **[Web]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-149">In the **Add New Project** dialog box, in the **Project types** pane, expand the **Visual Basic** or **Visual C#** node and select the **Web** project type.</span></span>  
  
3.  <span data-ttu-id="3cb95-150">**[.NET Framework 3.5]** が選択されていることを確認してから、 **[ASP.NET サービス アプリケーション]** テンプレートをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-150">Make sure that **.NET Framework 3.5** is selected, and then select the **ASP.NET Web Service Application** template.</span></span>  
  
4.  <span data-ttu-id="3cb95-151">プロジェクトの **[名前]** を `AppServices` に変更してから、 **[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-151">Change the project **Name** to `AppServices` and then click **OK**.</span></span>  
  
     <span data-ttu-id="3cb95-152">新しい ASP.NET Web サービス アプリケーション プロジェクトがソリューションに追加され、Service1.asmx.vb または Service1.asmx.cs ファイルがエディターに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-152">A new ASP.NET Web service application project is added to the solution, and the Service1.asmx.vb or Service1.asmx.cs file appears in the editor.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="3cb95-153">この例では、Service1.asmx.vb または Service1.asmx.cs ファイルは使用しません。</span><span class="sxs-lookup"><span data-stu-id="3cb95-153">The Service1.asmx.vb or Service1.asmx.cs file is not used in this example.</span></span> <span data-ttu-id="3cb95-154">作業環境をきちんと整頓したい場合は、このファイルを閉じて **[ソリューション エクスプローラー]** から削除してください。</span><span class="sxs-lookup"><span data-stu-id="3cb95-154">If you want to keep your work environment uncluttered, you can close it and delete it from **Solution Explorer**.</span></span>  
  
5.  <span data-ttu-id="3cb95-155">**[ソリューション エクスプローラー]** で、AppServices プロジェクトを選択し、 **[プロジェクト]** メニューで **[AppServices のプロパティ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-155">In **Solution Explorer**, select the AppServices project, and then on the **Project** menu, select **AppServices Properties**.</span></span>  
  
     <span data-ttu-id="3cb95-156">プロジェクト デザイナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-156">The project designer appears.</span></span>  
  
6.  <span data-ttu-id="3cb95-157">**[Web]** タブで、 **[Visual Studio 開発サーバーを使用する]** が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-157">On the **Web** tab, make sure that **Use Visual Studio Development Server** is selected.</span></span>  
  
7.  <span data-ttu-id="3cb95-158">**[特定のポート]** をクリックし、値に `55555`を指定してから、 **[仮想パス]** を `/AppServices`に設定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-158">Select **Specific port**, specify a value of `55555`, and then set **Virtual path** to `/AppServices`.</span></span>  
  
8.  <span data-ttu-id="3cb95-159">すべてのファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-159">Save all files.</span></span>  
  
9. <span data-ttu-id="3cb95-160">**[ソリューション エクスプローラー]** で、Web.config を開き、 `<system.web>` の開始タグを検索します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-160">In **Solution Explorer**, open Web.config and find the `<system.web>` opening tag.</span></span>  
  
10. <span data-ttu-id="3cb95-161">`<system.web>` タグの前に次のマークアップを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-161">Add the following markup before the `<system.web>` tag.</span></span>  
  
     <span data-ttu-id="3cb95-162">このマークアップの `authenticationService`、 `profileService`、および `roleService` の各要素で、アプリケーション サービスの有効化と構成を行います。</span><span class="sxs-lookup"><span data-stu-id="3cb95-162">The `authenticationService`, `profileService`, and `roleService` elements in this markup enable and configure the application services.</span></span> <span data-ttu-id="3cb95-163">テスト目的で、 `requireSSL` 要素の `authenticationService` 属性が "false" に設定されています。</span><span class="sxs-lookup"><span data-stu-id="3cb95-163">For testing purposes, the `requireSSL` attribute of the `authenticationService` element is set to "false".</span></span> <span data-ttu-id="3cb95-164">`readAccessProperties` 要素の `writeAccessProperties` 属性と `profileService` 属性は、 `WebSettingsTestText` プロパティが読み取りと書き込みが可能であることを示しています。</span><span class="sxs-lookup"><span data-stu-id="3cb95-164">The `readAccessProperties` and `writeAccessProperties` attributes of the `profileService` element indicate that the `WebSettingsTestText` property is read/write.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="3cb95-165">実稼働コードでは、HTTPS プロトコルを使用して、常に Secure Socket Layer (SSL) 上の認証サービスにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-165">In production code, you should always access the authentication service over the secure sockets layer (SSL, by using the HTTPS protocol).</span></span> <span data-ttu-id="3cb95-166">SSL の設定方法については、「 [SSL (Secure Sockets Layer) を構成する](https://go.microsoft.com/fwlink/?LinkId=91844)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cb95-166">For information about how to set up SSL, see [Configuring Secure Sockets Layer (IIS 6.0 Operations Guide)](https://go.microsoft.com/fwlink/?LinkId=91844).</span></span>  
  
    ```xml  
    <system.web.extensions>  
      <scripting>  
        <webServices>  
          <authenticationService enabled="true" requireSSL = "false"/>  
          <profileService enabled="true"  
            readAccessProperties="WebSettingsTestText"  
            writeAccessProperties="WebSettingsTestText" />  
          <roleService enabled="true"/>  
        </webServices>  
      </scripting>  
    </system.web.extensions>  
    ```  
  
11. <span data-ttu-id="3cb95-167">次のマークアップを、 `<system.web>` 要素内に収まるように、 `<system.web>` の開始タグの後に追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-167">Add the following markup after the `<system.web>` opening tag so that it is within the `<system.web>` element.</span></span>  
  
     <span data-ttu-id="3cb95-168">`profile` 要素は、 `WebSettingsTestText`という名前の 1 つの Web 設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-168">The `profile` element configures a single Web setting named `WebSettingsTestText`.</span></span>  
  
    ```xml  
    <profile enabled="true" >  
      <properties>  
        <add name="WebSettingsTestText" type="string"   
          readOnly="false" defaultValue="DefaultText"   
          serializeAs="String" allowAnonymous="false" />  
      </properties>  
    </profile>  
    ```  
  
 <span data-ttu-id="3cb95-169">次の手順では、ASP.NET Web サイト管理ツールを使用して、サービスの構成を完了するとともに、ローカル データベース ファイルにデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-169">In the following procedure, you use the ASP.NET Web Site Administration tool to complete the service configuration and populate the local database file.</span></span> <span data-ttu-id="3cb95-170">同じ名前の 2 つのロールに属する、 `employee` と `manager` という名前の 2 人のユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-170">You will add two users named `employee` and `manager` belonging to two roles with the same names.</span></span> <span data-ttu-id="3cb95-171">ユーザーのパスワードはそれぞれ、 `employee!` と `manager!` です。</span><span class="sxs-lookup"><span data-stu-id="3cb95-171">The user passwords are `employee!` and `manager!` respectively.</span></span>  
  
#### <a name="to-configure-membership-and-roles"></a><span data-ttu-id="3cb95-172">メンバーシップとロールを構成するには</span><span class="sxs-lookup"><span data-stu-id="3cb95-172">To configure membership and roles</span></span>  
  
1.  <span data-ttu-id="3cb95-173">**[ソリューション エクスプローラー]** で、AppServices プロジェクトを選択し、 **[プロジェクト]** メニューで **[ASP.NET の構成]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-173">In **Solution Explorer**, select the AppServices project, and then on the **Project** menu, select **ASP.NET Configuration**.</span></span>  
  
     <span data-ttu-id="3cb95-174">**ASP.NET Web サイト管理ツール** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-174">The **ASP.NET Web Site Administration Tool** appears.</span></span>  
  
2.  <span data-ttu-id="3cb95-175">**[セキュリティ]** タブで、 **[セキュリティ設定ウィザードを使用して手順に従ってセキュリティを構成する]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-175">On the **Security** tab, click **Use the security Setup Wizard to configure security step by step**.</span></span>  
  
     <span data-ttu-id="3cb95-176">**[セキュリティ セットアップ ウィザード]** が表示され、 **[ようこそ]** 手順が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-176">The **Security Setup Wizard** appears and displays the **Welcome** step.</span></span>  
  
3.  <span data-ttu-id="3cb95-177">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-177">Click **Next**.</span></span>  
  
     <span data-ttu-id="3cb95-178">**[アクセス方法の選択]** 手順が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-178">The **Select Access Method** step appears.</span></span>  
  
4.  <span data-ttu-id="3cb95-179">**[インターネットから]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-179">Select **From the internet**.</span></span> <span data-ttu-id="3cb95-180">そうすることで、Windows 認証ではなくフォーム認証を使用するようサービスが構成されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-180">This configures the service to use Forms authentication instead of Windows authentication.</span></span>  
  
5.  <span data-ttu-id="3cb95-181">**[次へ]** を 2 回クリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-181">Click **Next** twice.</span></span>  
  
     <span data-ttu-id="3cb95-182">**[ロールの定義]** 手順が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-182">The **Define Roles** step appears.</span></span>  
  
6.  <span data-ttu-id="3cb95-183">**[この Web サイトのロールを有効化]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-183">Select **Enable roles for this Web site**.</span></span>  
  
7.  <span data-ttu-id="3cb95-184">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-184">Click **Next**.</span></span> <span data-ttu-id="3cb95-185">**[新しいロールの作成]** フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-185">The **Create New Role** form appears.</span></span>  
  
8.  <span data-ttu-id="3cb95-186">**[新しいロール名]** テキスト ボックスで、「 `manager` 」と入力してから、 **[ロールの追加]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-186">In the **New Role Name** text box, type `manager` and then click **Add Role**.</span></span>  
  
     <span data-ttu-id="3cb95-187">指定した値が入った **[既存のロール]** テーブルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-187">The **Existing Roles** table appears with the specified value.</span></span>  
  
9. <span data-ttu-id="3cb95-188">**[新しいロール名]** テキスト ボックスで、 `manager` を `employee` に置き換えてから、 **[ロールの追加]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-188">In the **New Role Name** text box, replace `manager` with `employee` and then click **Add Role**.</span></span>  
  
     <span data-ttu-id="3cb95-189">**[既存のロール]** テーブルに新しい値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-189">The new value appears in the **Existing Roles** table.</span></span>  
  
10. <span data-ttu-id="3cb95-190">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-190">Click **Next**.</span></span>  
  
     <span data-ttu-id="3cb95-191">**[新しいユーザーの追加]** 手順が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-191">The **Add New Users** step appears.</span></span>  
  
11. <span data-ttu-id="3cb95-192">**[ユーザーの作成]** フォームで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-192">In the **Create User** form, specify the following values.</span></span>  
  
  	|||  
  	|-|-|  
  	|<span data-ttu-id="3cb95-193">**ユーザー名**</span><span class="sxs-lookup"><span data-stu-id="3cb95-193">**User Name**</span></span>|`manager`|  
  	|<span data-ttu-id="3cb95-194">**パスワード**</span><span class="sxs-lookup"><span data-stu-id="3cb95-194">**Password**</span></span>|`manager!`|  
  	|<span data-ttu-id="3cb95-195">**パスワードの確認入力**</span><span class="sxs-lookup"><span data-stu-id="3cb95-195">**Confirm Password**</span></span>|`manager!`|  
  	|<span data-ttu-id="3cb95-196">**電子メール**</span><span class="sxs-lookup"><span data-stu-id="3cb95-196">**Email**</span></span>|`manager@contoso.com`|  
  	|<span data-ttu-id="3cb95-197">**セキュリティの質問**</span><span class="sxs-lookup"><span data-stu-id="3cb95-197">**Security Question**</span></span>|`manager`|  
  	|<span data-ttu-id="3cb95-198">**セキュリティ返答**</span><span class="sxs-lookup"><span data-stu-id="3cb95-198">**Security Answer**</span></span>|`manager`|  
  
12. <span data-ttu-id="3cb95-199">**[ユーザーの作成]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-199">Click **Create User**.</span></span>  
  
     <span data-ttu-id="3cb95-200">成功のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-200">A success message appears.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="3cb95-201">フォームでは **[電子メール]**、**[秘密の質問]**、**[秘密の答え]** の値が必要ですが、この例では使用しません。</span><span class="sxs-lookup"><span data-stu-id="3cb95-201">The **Email**, **Security Question**, and **Security Answer** values are required by the form, but are not used in this example.</span></span>  
  
13. <span data-ttu-id="3cb95-202">**[続行]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-202">Click **Continue**.</span></span>  
  
     <span data-ttu-id="3cb95-203">**[ユーザーの作成]** フォームが再表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-203">The **Create User** form reappears.</span></span>  
  
14. <span data-ttu-id="3cb95-204">**[ユーザーの作成]** フォームで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-204">In the **Create User** form, specify the following values.</span></span>  
  
  	|||  
  	|-|-|  
  	|<span data-ttu-id="3cb95-205">**ユーザー名**</span><span class="sxs-lookup"><span data-stu-id="3cb95-205">**User Name**</span></span>|`employee`|  
  	|<span data-ttu-id="3cb95-206">**パスワード**</span><span class="sxs-lookup"><span data-stu-id="3cb95-206">**Password**</span></span>|`employee!`|  
  	|<span data-ttu-id="3cb95-207">**パスワードの確認入力**</span><span class="sxs-lookup"><span data-stu-id="3cb95-207">**Confirm Password**</span></span>|`employee!`|  
  	|<span data-ttu-id="3cb95-208">**電子メール**</span><span class="sxs-lookup"><span data-stu-id="3cb95-208">**Email**</span></span>|`employee@contoso.com`|  
  	|<span data-ttu-id="3cb95-209">**セキュリティの質問**</span><span class="sxs-lookup"><span data-stu-id="3cb95-209">**Security Question**</span></span>|`Employee`|  
  	|<span data-ttu-id="3cb95-210">**セキュリティ返答**</span><span class="sxs-lookup"><span data-stu-id="3cb95-210">**Security Answer**</span></span>|`employee`|  
  
15. <span data-ttu-id="3cb95-211">**[ユーザーの作成]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-211">Click **Create User**.</span></span>  
  
     <span data-ttu-id="3cb95-212">成功のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-212">A success message appears.</span></span>  
  
16. <span data-ttu-id="3cb95-213">**[完了]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-213">Click **Finish**.</span></span>  
  
     <span data-ttu-id="3cb95-214">**Web サイト管理ツール** が再表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-214">The **Web Site Administration Tool** reappears.</span></span>  
  
17. <span data-ttu-id="3cb95-215">**[管理者ユーザー]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-215">Click **Manager users**.</span></span>  
  
     <span data-ttu-id="3cb95-216">ユーザーの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-216">The list of users appears.</span></span>  
  
18. <span data-ttu-id="3cb95-217">**employee** ユーザーの **[ロールの編集]** をクリックしてから、 **employee** ロールをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-217">Click **Edit roles** for the **employee** user, and then select the **employee** role.</span></span>  
  
19. <span data-ttu-id="3cb95-218">**manager** ユーザーの **[ロールの編集]** をクリックしてから、 **manager** ロールをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-218">Click **Edit roles** for the **manager** user, and then select the **manager** role.</span></span>  
  
20. <span data-ttu-id="3cb95-219">**Web サイト管理ツール**をホストするブラウザのウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-219">Close the browser window that hosts the **Web Site Administration Tool**.</span></span>  
  
21. <span data-ttu-id="3cb95-220">変更した Web.config ファイルを再度読み込むかどうかを尋ねるメッセージ ボックスが表示された場合は、 **[はい]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-220">If a message box appears asking if you want to reload the modified Web.config file, click **Yes**.</span></span>  
  
 <span data-ttu-id="3cb95-221">これにより、Web サービスのセットアップが完了します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-221">This completes the Web service setup.</span></span> <span data-ttu-id="3cb95-222">この時点で、F5 キーを押すとクライアント アプリケーションを実行します。 **ASP.NET 開発サーバー** は、クライアント アプリケーションとともに自動的に起動します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-222">At this point, you can press F5 to run the client application, and the **ASP.NET Development Server** will start automatically along with your client application.</span></span> <span data-ttu-id="3cb95-223">サーバーは、アプリケーションが終了しても引き続き実行しますが、アプリケーションを再起動するとサーバーも再起動します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-223">The server will continue to run after you exit the application, but will restart when you restart the application.</span></span> <span data-ttu-id="3cb95-224">そうすることで、Web.config に対して行われたすべての変更を検出することができます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-224">This allows it to detect any changes you have made to Web.config.</span></span>  
  
 <span data-ttu-id="3cb95-225">サーバーを手動で停止するには、タスク バーの通知領域にある ASP.NET 開発サーバーのアイコンを右クリックしてから、 **[停止]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-225">To stop the server manually, right-click the ASP.NET Development Server icon in the notification area of the taskbar and then click **Stop**.</span></span> <span data-ttu-id="3cb95-226">これは、時折クリーン再起動を確実に行うために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-226">This is useful occasionally to make sure that a clean restart occurs.</span></span>  
  
## <a name="adding-forms-authentication"></a><span data-ttu-id="3cb95-227">フォーム認証を追加する</span><span class="sxs-lookup"><span data-stu-id="3cb95-227">Adding Forms Authentication</span></span>  
 <span data-ttu-id="3cb95-228">次の手順では、ユーザーの検証を試みるとともに、ユーザーが無効な資格情報を指定した場合にアクセスを拒否するコードをメイン フォームに追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-228">In the following procedure, you add code to the main form that attempts to validate the user, and denies access when the user supplies invalid credentials.</span></span> <span data-ttu-id="3cb95-229">ハードコーディングされたユーザー名とパスワードを使用して、サービスをテストします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-229">You use a hard-coded user name and password to test the service.</span></span>  
  
#### <a name="to-validate-the-user-in-your-application-code"></a><span data-ttu-id="3cb95-230">アプリケーション コードでユーザーを検証するには</span><span class="sxs-lookup"><span data-stu-id="3cb95-230">To validate the user in your application code</span></span>  
  
1.  <span data-ttu-id="3cb95-231">**[ソリューション エクスプローラー]** の ClientAppServicesDemo プロジェクトで、System.Web アセンブリへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-231">In **Solution Explorer**, in the ClientAppServicesDemo project, add a reference to the System.Web assembly.</span></span>  
  
2.  <span data-ttu-id="3cb95-232">Form1 ファイルを選択し、Visual Studio のメイン メニューから **[表示] &#124; [コード]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-232">Select the Form1 file and then select **View &#124; Code** from the Visual Studio main menu.</span></span>  
  
3.  <span data-ttu-id="3cb95-233">コード エディターで、Form1 ファイルの先頭に次のステートメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-233">In the code editor, add the following statements to the top of the Form1 file.</span></span>  
  
     [!code-csharp[ClientApplicationServices#001](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Form1.cs#001)]
     [!code-vb[ClientApplicationServices#001](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Form1.vb#001)]  
  
4.  <span data-ttu-id="3cb95-234">**[ソリューション エクスプローラー]** で、Form1 をダブルクリックしてデザイナーを表示します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-234">In **Solution Explorer**, double-click Form1 to display the designer.</span></span>  
  
5.  <span data-ttu-id="3cb95-235">デザイナーで、フォーム領域をダブルクリックして、 <xref:System.Windows.Forms.Form.Load?displayProperty=nameWithType> という名前の `Form1_Load`イベント ハンドラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-235">In the designer, double-click the form surface to generate a <xref:System.Windows.Forms.Form.Load?displayProperty=nameWithType> event handler named `Form1_Load`.</span></span>  
  
     <span data-ttu-id="3cb95-236">`Form1_Load` メソッドにカーソルがある状態でコード エディターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-236">The code editor appears with the cursor in the `Form1_Load` method.</span></span>  
  
6.  <span data-ttu-id="3cb95-237">`Form1_Load` メソッドに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-237">Add the following code to the `Form1_Load` method.</span></span>  
  
     <span data-ttu-id="3cb95-238">このコードは認証されていないユーザー アクセスを拒否してアプリケーションを終了します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-238">This code denies access to unauthenticated users by exiting the application.</span></span> <span data-ttu-id="3cb95-239">あるいは、認証されていないユーザーによるフォームへのアクセスを許可するものの、特定の機能へのアクセスを拒否することもできます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-239">Alternatively, you could allow unauthenticated users access to the form, but deny access to specific functionality.</span></span> <span data-ttu-id="3cb95-240">通常、このようにユーザー名とパスワードをハードコーディングすることはありませんが、テスト目的には役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-240">Normally, you will not hard-code the user name and password like this, but it is useful for testing purposes.</span></span> <span data-ttu-id="3cb95-241">次のセクションではこのコードをより堅牢なコードに置き換えて、ログイン ダイアログ ボックスを表示する、例外処理を含んだものにします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-241">In the next section, you will replace this code with more robust code that displays a login dialog box and includes exception handling.</span></span>  
  
     <span data-ttu-id="3cb95-242">`static` <xref:System.Web.Security.Membership.ValidateUser%2A?displayProperty=nameWithType> メソッドが [!INCLUDE[dnprdnext](../../../includes/dnprdnext-md.md)]にあることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3cb95-242">Note that the `static` <xref:System.Web.Security.Membership.ValidateUser%2A?displayProperty=nameWithType> method is in the [!INCLUDE[dnprdnext](../../../includes/dnprdnext-md.md)].</span></span> <span data-ttu-id="3cb95-243">このメソッドは、構成済みの認証プロバイダーに作業を委任し、認証が成功した場合は `true` を返します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-243">This method delegates its work to the configured authentication provider, and returns `true` if authentication is successful.</span></span> <span data-ttu-id="3cb95-244">アプリケーションに、クライアントの認証プロバイダーへの直接の参照は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="3cb95-244">Your application does not require a direct reference to the client authentication provider.</span></span>  
  
     [!code-csharp[ClientApplicationServices#300](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Class1.cs#300)]
     [!code-vb[ClientApplicationServices#300](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Class1.vb#300)]  
  
 <span data-ttu-id="3cb95-245">ここで、F5 キーを押してアプリケーションを実行します。正しいユーザー名とパスワードを指定しているため、フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-245">You can now press F5 to run the application, and because you provide a correct user name and password, you will see the form.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3cb95-246">アプリケーションを実行できない場合は、ASP.NET 開発サーバーを停止してください。</span><span class="sxs-lookup"><span data-stu-id="3cb95-246">If you are unable to run the application, try stopping the ASP.NET Development Server.</span></span> <span data-ttu-id="3cb95-247">サーバーを再起動する際、ポートが 55555 に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-247">When the server restarts, verify that the port is set to 55555.</span></span>  
  
 <span data-ttu-id="3cb95-248">代わりにエラー メッセージを表示するには、 <xref:System.Web.Security.Membership.ValidateUser%2A> のパラメーターを変更します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-248">To see the error message instead, change the <xref:System.Web.Security.Membership.ValidateUser%2A> parameters.</span></span> <span data-ttu-id="3cb95-249">たとえば、2 番目の `"manager!"` パラメーターを `"MANAGER"`などの正しくないパスワードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-249">For example, replace the second `"manager!"` parameter with an incorrect password like `"MANAGER"`.</span></span>  
  
## <a name="adding-a-login-form-as-a-credentials-provider"></a><span data-ttu-id="3cb95-250">資格情報プロバイダーとしてログイン フォームを追加する</span><span class="sxs-lookup"><span data-stu-id="3cb95-250">Adding a Login Form as a Credentials Provider</span></span>  
 <span data-ttu-id="3cb95-251">アプリケーション コードでユーザーの資格情報を取得して、 <xref:System.Web.Security.Membership.ValidateUser%2A> メソッドに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-251">You can acquire the user credentials in your application code and pass them to the <xref:System.Web.Security.Membership.ValidateUser%2A> method.</span></span> <span data-ttu-id="3cb95-252">しかし、資格情報を取得するコードをアプリケーション コードと分けておくと、後でこれを変更するときに便利な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-252">However, it is often useful to keep your credentials-acquiring code separate from your application code, in case you want to change it later.</span></span>  
  
 <span data-ttu-id="3cb95-253">次の手順では、資格情報プロバイダーを使用するようにアプリケーションを構成してから、両方のパラメーターに <xref:System.Web.Security.Membership.ValidateUser%2A> を渡すように <xref:System.String.Empty> メソッドの呼び出しを変更します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-253">In the following procedure, you configure your application to use a credentials provider, and then change your <xref:System.Web.Security.Membership.ValidateUser%2A> method call to pass <xref:System.String.Empty> for both parameters.</span></span> <span data-ttu-id="3cb95-254">文字列が空の場合、 <xref:System.Web.Security.Membership.ValidateUser%2A> メソッドは構成済みの資格情報プロバイダーの <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider.GetCredentials%2A> メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-254">The empty strings signal the <xref:System.Web.Security.Membership.ValidateUser%2A> method to call the <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider.GetCredentials%2A> method of the configured credentials provider.</span></span>  
  
#### <a name="to-configure-your-application-to-use-a-credentials-provider"></a><span data-ttu-id="3cb95-255">アプリケーションが資格情報プロバイダーを使用するように構成するには</span><span class="sxs-lookup"><span data-stu-id="3cb95-255">To configure your application to use a credentials provider</span></span>  
  
1.  <span data-ttu-id="3cb95-256">**[ソリューション エクスプローラー]** で、ClientAppServicesDemo プロジェクトを選択し、 **[プロジェクト]** メニューで **[ClientAppServicesDemo のプロパティ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-256">In **Solution Explorer**, select the ClientAppServicesDemo project, and then on the **Project** menu, select **ClientAppServicesDemo Properties**.</span></span>  
  
     <span data-ttu-id="3cb95-257">プロジェクト デザイナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-257">The project designer appears.</span></span>  
  
2.  <span data-ttu-id="3cb95-258">**[サービス]** タブで、 **[省略可能な資格情報プロバイダー]** を次の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-258">On the **Services** tab, set **Optional: Credential provider** to the following value.</span></span> <span data-ttu-id="3cb95-259">この値は、アセンブリ修飾型名を示しています。</span><span class="sxs-lookup"><span data-stu-id="3cb95-259">This value indicates the assembly-qualified type name.</span></span>  
  
    ```  
    ClientAppServicesDemo.Login, ClientAppServicesDemo  
    ```  
  
3.  <span data-ttu-id="3cb95-260">Form1 コード ファイルで、 `Form1_Load` メソッドのコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-260">In the Form1 code file, replace the code in the `Form1_Load` method with the following code.</span></span>  
  
     <span data-ttu-id="3cb95-261">このコードは、ようこそメッセージを表示してから、次の手順で追加する `ValidateUsingCredentialsProvider` メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-261">This code displays a welcome message and then calls the `ValidateUsingCredentialsProvider` method that you will add in the next step.</span></span> <span data-ttu-id="3cb95-262">ユーザーが認証されない場合、 `ValidateUsingCredentialsProvider` メソッドは `false` を返し、 `Form1_Load` メソッドが戻ります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-262">If the user is not authenticated, the `ValidateUsingCredentialsProvider` method returns `false` and the `Form1_Load` method returns.</span></span> <span data-ttu-id="3cb95-263">これにより、アプリケーションが終了するまでそれ以上コードを実行できなくなります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-263">This prevents any additional code from running before the application exits.</span></span> <span data-ttu-id="3cb95-264">ようこそメッセージは、アプリケーションが再起動するときが明確になるため便利です。</span><span class="sxs-lookup"><span data-stu-id="3cb95-264">The welcome message is useful to make it clear when the application restarts.</span></span> <span data-ttu-id="3cb95-265">このチュートリアルの後半でログアウトを実装するときに、アプリケーションを再起動するコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-265">You will add code to restart the application when you implement logout later in this walkthrough.</span></span>  
  
     [!code-csharp[ClientApplicationServices#011](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Form1.cs#011)]
     [!code-vb[ClientApplicationServices#011](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Form1.vb#011)]  
  
4.  <span data-ttu-id="3cb95-266">`Form1_Load` メソッドの後に次のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-266">Add the following method after the `Form1_Load` method.</span></span>  
  
     <span data-ttu-id="3cb95-267">このメソッドは、 `static` <xref:System.Web.Security.Membership.ValidateUser%2A?displayProperty=nameWithType> メソッドに空の文字列を渡すことによって、[ログイン] ダイアログ ボックスを表示させます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-267">This method passes empty strings to the `static` <xref:System.Web.Security.Membership.ValidateUser%2A?displayProperty=nameWithType> method, which causes the Login dialog box to appear.</span></span> <span data-ttu-id="3cb95-268">認証サービスが使用できない場合、 <xref:System.Web.Security.Membership.ValidateUser%2A> メソッドは <xref:System.Net.WebException>をスローします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-268">If the authentication service is unavailable, the <xref:System.Web.Security.Membership.ValidateUser%2A> method will throw a <xref:System.Net.WebException>.</span></span> <span data-ttu-id="3cb95-269">この場合、 `ValidateUsingCredentialsProvider` メソッドは警告メッセージを表示し、オフライン モードで再試行するかどうかをユーザーに尋ねます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-269">In this case, the `ValidateUsingCredentialsProvider` method displays a warning message and asks if the user wants to try again in offline mode.</span></span> <span data-ttu-id="3cb95-270">この機能には、「 **How to: Configure Client Application Services** 」で説明する [[オフラインでログインできるようにパスワードのハッシュをローカルに保存する]](../../../docs/framework/common-client-technologies/how-to-configure-client-application-services.md)機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="3cb95-270">This functionality requires the **Save password hash locally to enable offline login** feature described in [How to: Configure Client Application Services](../../../docs/framework/common-client-technologies/how-to-configure-client-application-services.md).</span></span> <span data-ttu-id="3cb95-271">この機能は、新しいプロジェクトでは既定で有効になっています。</span><span class="sxs-lookup"><span data-stu-id="3cb95-271">This feature is enabled by default for new projects.</span></span>  
  
     <span data-ttu-id="3cb95-272">ユーザーが検証されない場合、 `ValidateUsingCredentialsProvider` メソッドはエラー メッセージを表示し、アプリケーションを終了します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-272">If the user is not validated, the `ValidateUsingCredentialsProvider` method displays an error message and exits the application.</span></span> <span data-ttu-id="3cb95-273">最後に、このメソッドは、認証の結果を返します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-273">Finally, this method returns the result of the authentication attempt.</span></span>  
  
     [!code-csharp[ClientApplicationServices#020](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Form1.cs#020)]
     [!code-vb[ClientApplicationServices#020](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Form1.vb#020)]  
  
### <a name="creating-a-login-form"></a><span data-ttu-id="3cb95-274">ログイン フォームを作成する</span><span class="sxs-lookup"><span data-stu-id="3cb95-274">Creating a Login Form</span></span>  
 <span data-ttu-id="3cb95-275">資格情報プロバイダーとは、 <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider> インターフェイスを実装するクラスです。</span><span class="sxs-lookup"><span data-stu-id="3cb95-275">A credentials provider is a class that implements the <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider> interface.</span></span> <span data-ttu-id="3cb95-276">このインターフェイスには、 <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider.GetCredentials%2A> オブジェクトを返す <xref:System.Web.ClientServices.Providers.ClientFormsAuthenticationCredentials> という名前の 1 つのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-276">This interface has a single method named <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider.GetCredentials%2A> that returns a <xref:System.Web.ClientServices.Providers.ClientFormsAuthenticationCredentials> object.</span></span> <span data-ttu-id="3cb95-277">次の手順ではログイン ダイアログ ボックスの作成方法を示します。これは <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider.GetCredentials%2A> を実装してダイアログ ボックスを表示し、ユーザー指定の資格情報を返します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-277">The following procedures describe how to create a login dialog box that implements <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider.GetCredentials%2A> to display itself and return the user-specified credentials.</span></span>  
  
 <span data-ttu-id="3cb95-278">Visual Basic は **[ログイン フォーム]** テンプレートを備えているため、Visual Basic と C# で手順が別々に説明されています。</span><span class="sxs-lookup"><span data-stu-id="3cb95-278">Separate procedures are provided for Visual Basic and C# because Visual Basic provides a **Login Form** template.</span></span> <span data-ttu-id="3cb95-279">このテンプレートを使用すると、時間の節約になり、コーディングの手間も省けます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-279">This saves some time and coding effort.</span></span>  
  
##### <a name="to-create-a-login-dialog-box-as-a-credentials-provider-in-visual-basic"></a><span data-ttu-id="3cb95-280">Visual Basic で資格情報プロバイダーとしてログイン ダイアログ ボックスを作成するには</span><span class="sxs-lookup"><span data-stu-id="3cb95-280">To create a login dialog box as a credentials provider in Visual Basic</span></span>  
  
1.  <span data-ttu-id="3cb95-281">**[ソリューション エクスプローラー]** で、ClientAppServicesDemo プロジェクトを選択してから、 **[プロジェクト]** メニューで **[新しい項目の追加]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-281">In **Solution Explorer**, select the ClientAppServicesDemo project, and then on the **Project** menu, select **Add New Item**.</span></span>  
  
2.  <span data-ttu-id="3cb95-282">**[新しい項目の追加]** ダイアログ ボックスで、 **[ログイン フォーム]** テンプレートを選択し、項目の **[名前]** を `Login.vb`に変更してから、 **[追加]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-282">In the **Add New Item** dialog box, select the **Login Form** template, change the item **Name** to `Login.vb`, and then click **Add**.</span></span>  
  
     <span data-ttu-id="3cb95-283">Windows フォーム デザイナーにログイン ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-283">The login dialog box appears in the Windows Forms Designer.</span></span>  
  
3.  <span data-ttu-id="3cb95-284">デザイナーで、 **[OK]** ボタンをクリックし、 **[プロパティ]** ウィンドウで、[ `DialogResult` ] を ” `OK`" に設定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-284">In the designer, select the **OK** button and then, in the **Properties** window, set `DialogResult` to `OK`.</span></span>  
  
4.  <span data-ttu-id="3cb95-285">デザイナーで、 `CheckBox` コントロールを、 **[パスワード]** テキスト ボックスの下にあるフォームに追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-285">In the designer, add a `CheckBox` control to the form under the **Password** text box.</span></span>  
  
5.  <span data-ttu-id="3cb95-286">**[プロパティ]** ウィンドウで、**[(名前)]** の値を "`rememberMeCheckBox`" と指定し、**[テキスト]** の値を "`&Remember me`" と指定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-286">In the **Properties** window, specify a **(Name)** value of `rememberMeCheckBox` and a **Text** value of `&Remember me`.</span></span>  
  
6.  <span data-ttu-id="3cb95-287">Visual Studio のメイン メニューで、**[表示] &#124; [コード]** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-287">Select **View &#124; Code** from the Visual Studio main menu.</span></span>  
  
7.  <span data-ttu-id="3cb95-288">コード エディターで、ファイルの先頭に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-288">In the code editor, add the following code to the top of the file.</span></span>  
  
     [!code-vb[ClientApplicationServices#101](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Login.vb#101)]  
  
8.  <span data-ttu-id="3cb95-289">クラスが <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider> インターフェイスを実装するようにクラスのシグネチャを変更します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-289">Modify the class signature so that the class implements the <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider> interface.</span></span>  
  
     [!code-vb[ClientApplicationServices#110](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Class1.vb#110)]  
  
9. <span data-ttu-id="3cb95-290">カーソルが `IClientformsAuthenticationCredentialsProvider` の後にあることを確認してから、Enter キーを押して `GetCredentials` メソッドを生成します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-290">Make sure that the cursor is after `IClientformsAuthenticationCredentialsProvider`, and then press ENTER to generate the `GetCredentials` method.</span></span>  
  
10. <span data-ttu-id="3cb95-291"><xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider.GetCredentials%2A> の実装を見つけて、次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-291">Locate the <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider.GetCredentials%2A> implementation and then replace it with the following code.</span></span>  
  
     [!code-vb[ClientApplicationServices#120](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Login.vb#120)]  
  
 <span data-ttu-id="3cb95-292">次の C# の手順では、簡単なログイン ダイアログ ボックス用のコード全体を一覧で示します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-292">The following C# procedure provides the entire code listing for a simple login dialog box.</span></span> <span data-ttu-id="3cb95-293">このダイアログ ボックスのレイアウトは少し粗雑ですが、重要な部分は <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider.GetCredentials%2A> の実装です。</span><span class="sxs-lookup"><span data-stu-id="3cb95-293">The layout for this dialog box is a bit crude, but the important part is the <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider.GetCredentials%2A> implementation.</span></span>  
  
##### <a name="to-create-a-login-dialog-box-as-a-credentials-provider-in-c"></a><span data-ttu-id="3cb95-294">C# で資格情報プロバイダーとしてログイン ダイアログ ボックスを作成するには</span><span class="sxs-lookup"><span data-stu-id="3cb95-294">To create a login dialog box as a credentials provider in C#</span></span>  
  
1.  <span data-ttu-id="3cb95-295">**[ソリューション エクスプローラー]** で、ClientAppServicesDemo プロジェクトを選択してから、 **[プロジェクト]** メニューで **[クラスの追加]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-295">In **Solution Explorer**, select the ClientAppServicesDemo project, and then on the **Project** menu, select **Add Class**.</span></span>  
  
2.  <span data-ttu-id="3cb95-296">**[新しい項目の追加]** ダイアログ ボックスで、 **[名前]** を `Login.cs`に変更してから、 **[追加]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-296">In the **Add New Item** dialog box, change the **Name** to `Login.cs`, and then click **Add**.</span></span>  
  
     <span data-ttu-id="3cb95-297">コード エディターで Login.cs ファイルが開きます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-297">The Login.cs file opens in the code editor.</span></span>  
  
3.  <span data-ttu-id="3cb95-298">既定のコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-298">Replace the default code with the following code.</span></span>  
  
     [!code-csharp[ClientApplicationServices#200](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Login.cs#200)]  
  
 <span data-ttu-id="3cb95-299">アプリケーションを実行してログイン ダイアログ ボックスを表示できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="3cb95-299">You can now run the application and see the login dialog box appear.</span></span> <span data-ttu-id="3cb95-300">このコードをテストするには、有効と無効の両方のさまざまな資格情報を試し、資格情報が有効な場合にのみフォームにアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-300">To test this code, try different credentials, both valid and invalid, and confirm that you can access the form only with valid credentials.</span></span> <span data-ttu-id="3cb95-301">有効なユーザー名は、 `employee` と `manager` になります。パスワードはそれぞれ、 `employee!` と `manager!` です。</span><span class="sxs-lookup"><span data-stu-id="3cb95-301">Valid user names are `employee` and `manager` with passwords `employee!` and `manager!` respectively.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3cb95-302">この時点で **[アカウントを記憶]** は選択しないでください。そうしないと、このチュートリアルの後半でログアウトを実装するまで、別のユーザーとしてログインできなくなります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-302">Do not select **Remember me** at this point or you will not be able to login as another user until you implement logout later in this walkthrough.</span></span>  
  
## <a name="adding-role-based-functionality"></a><span data-ttu-id="3cb95-303">ロール ベースの機能を追加する</span><span class="sxs-lookup"><span data-stu-id="3cb95-303">Adding Role-Based Functionality</span></span>  
 <span data-ttu-id="3cb95-304">次の手順では、フォームにボタンを追加して、manager ロールのユーザーにだけこれを表示します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-304">In the following procedure, you add a button to the form and display it only for users in the manager role.</span></span>  
  
#### <a name="to-change-the-user-interface-based-on-user-role"></a><span data-ttu-id="3cb95-305">ユーザーのロールに基づいてユーザー インターフェイスを変更するには</span><span class="sxs-lookup"><span data-stu-id="3cb95-305">To change the user interface based on user role</span></span>  
  
1.  <span data-ttu-id="3cb95-306">**[ソリューション エクスプローラー]** の ClientAppServicesDemo プロジェクトで、Form1 を選択してから、Visual Studio のメイン メニューで **[表示] &#124; [デザイナー]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-306">In **Solution Explorer**, in the ClientAppServicesDemo project, select Form1 and then select **View &#124; Designer** from the Visual Studio main menu.</span></span>  
  
2.  <span data-ttu-id="3cb95-307">デザイナーで、**[ツールボックス]** からフォームに <xref:System.Windows.Forms.Button> コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-307">In the designer, add a <xref:System.Windows.Forms.Button> control to the form from the **ToolBox**.</span></span>  
  
3.  <span data-ttu-id="3cb95-308">**[プロパティ]** ウィンドウで、ボタンの次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-308">In the **Properties** window, set the following properties for the button.</span></span>  
  
  	|<span data-ttu-id="3cb95-309">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3cb95-309">Property</span></span>|<span data-ttu-id="3cb95-310">[値]</span><span class="sxs-lookup"><span data-stu-id="3cb95-310">Value</span></span>|  
  	|--------------|-----------|  
  	|<span data-ttu-id="3cb95-311">**[(名前)]**</span><span class="sxs-lookup"><span data-stu-id="3cb95-311">**(Name)**</span></span>|<span data-ttu-id="3cb95-312">managerOnlyButton</span><span class="sxs-lookup"><span data-stu-id="3cb95-312">managerOnlyButton</span></span>|  
  	|<span data-ttu-id="3cb95-313">**[テキスト]**</span><span class="sxs-lookup"><span data-stu-id="3cb95-313">**Text**</span></span>|<span data-ttu-id="3cb95-314">&Manager task</span><span class="sxs-lookup"><span data-stu-id="3cb95-314">&Manager task</span></span>|  
  	|<span data-ttu-id="3cb95-315">**Visible**</span><span class="sxs-lookup"><span data-stu-id="3cb95-315">**Visible**</span></span>|`False`|  
  
4.  <span data-ttu-id="3cb95-316">Form1 のコード エディターで、 `Form1_Load` メソッドの末尾に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-316">In the code editor for Form1, add the following code to the end of the `Form1_Load` method.</span></span>  
  
     <span data-ttu-id="3cb95-317">このコードは、次の手順で追加する `DisplayButtonForManagerRole` メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-317">This code calls the `DisplayButtonForManagerRole` method that you will add in the next step.</span></span>  
  
     [!code-csharp[ClientApplicationServices#012](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Form1.cs#012)]
     [!code-vb[ClientApplicationServices#012](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Form1.vb#012)]  
  
5.  <span data-ttu-id="3cb95-318">次のメソッドを Form1 クラスの末尾に追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-318">Add the following method to the end of the Form1 class.</span></span>  
  
     <span data-ttu-id="3cb95-319">このメソッドは、`static` <xref:System.Threading.Thread.CurrentPrincipal%2A?displayProperty=nameWithType> プロパティによって返される <xref:System.Security.Principal.IPrincipal> の <xref:System.Security.Principal.IPrincipal.IsInRole%2A> メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-319">This method calls the <xref:System.Security.Principal.IPrincipal.IsInRole%2A> method of the <xref:System.Security.Principal.IPrincipal> returned by the `static` <xref:System.Threading.Thread.CurrentPrincipal%2A?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="3cb95-320">クライアント アプリケーション サービスを使用するように構成されたアプリケーションで、このプロパティは <xref:System.Web.ClientServices.ClientRolePrincipal> を返します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-320">For applications configured to use client application services, this property returns a <xref:System.Web.ClientServices.ClientRolePrincipal>.</span></span> <span data-ttu-id="3cb95-321">このクラスは <xref:System.Security.Principal.IPrincipal> インターフェイスを実装しているため、明示的に参照する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3cb95-321">Because this class implements the <xref:System.Security.Principal.IPrincipal> interface, you do not need to reference it explicitly.</span></span>  
  
     <span data-ttu-id="3cb95-322">ユーザーが "manager" ロールの場合、 `DisplayButtonForManagerRole` メソッドは <xref:System.Windows.Forms.Control.Visible%2A> の `managerOnlyButton` プロパティを `true`に設定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-322">If the user is in the "manager" role, the `DisplayButtonForManagerRole` method sets the <xref:System.Windows.Forms.Control.Visible%2A> property of the `managerOnlyButton` to `true`.</span></span> <span data-ttu-id="3cb95-323">また、このメソッドは、 <xref:System.Net.WebException> がスローされるとエラー メッセージを表示します。これは、ロール サービスが使用できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-323">This method also displays an error message if a <xref:System.Net.WebException> is thrown, which indicates that the roles service is unavailable.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="3cb95-324">ユーザー ログインの有効期限が切れている場合、 <xref:System.Web.ClientServices.ClientRolePrincipal.IsInRole%2A> メソッドは常に `false` を返します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-324">The <xref:System.Web.ClientServices.ClientRolePrincipal.IsInRole%2A> method will always return `false` if the user login has expired.</span></span> <span data-ttu-id="3cb95-325">このチュートリアルのコードの使用例に示すように、アプリケーションが認証のすぐ後に <xref:System.Security.Principal.IPrincipal.IsInRole%2A> メソッドを 1 回呼び出した場合、これは発生しません。</span><span class="sxs-lookup"><span data-stu-id="3cb95-325">This will not occur if your application calls the <xref:System.Security.Principal.IPrincipal.IsInRole%2A> method one time shortly after authentication, as shown in the example code for this walkthrough.</span></span> <span data-ttu-id="3cb95-326">アプリケーションが他のタイミングでユーザーのロールを取得する必要がある場合は、ログインの有効期限が切れたユーザーを再検証するコードを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-326">If your application must retrieve user roles at other times, you might want to add code to revalidate users whose login has expired.</span></span> <span data-ttu-id="3cb95-327">有効なユーザーすべてにロールが割り当てられている場合は、 <xref:System.Web.ClientServices.Providers.ClientRoleProvider.GetRolesForUser%2A?displayProperty=nameWithType> メソッドを呼び出してログインの有効期限が切れていないか判断できます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-327">If all valid users are assigned to roles, you can determine whether the login has expired by calling the <xref:System.Web.ClientServices.Providers.ClientRoleProvider.GetRolesForUser%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="3cb95-328">ロールが返されない場合は、ログインの有効期限が切れています。</span><span class="sxs-lookup"><span data-stu-id="3cb95-328">If no roles are returned, the login has expired.</span></span> <span data-ttu-id="3cb95-329">この機能の例については、 <xref:System.Web.ClientServices.Providers.ClientRoleProvider.GetRolesForUser%2A> メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cb95-329">For an example of this functionality, see the <xref:System.Web.ClientServices.Providers.ClientRoleProvider.GetRolesForUser%2A> method.</span></span> <span data-ttu-id="3cb95-330">この機能が必要なのは、アプリケーションの構成で **[サーバー クッキーの期限が切れた場合は常に再度ログオンすることをユーザーに要求する]** を選択した場合だけです。</span><span class="sxs-lookup"><span data-stu-id="3cb95-330">This functionality is only necessary if you have selected **Require users to log on again whenever the server cookie expires** in your application configuration.</span></span> <span data-ttu-id="3cb95-331">詳細については、「 [How to: Configure Client Application Services](../../../docs/framework/common-client-technologies/how-to-configure-client-application-services.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cb95-331">For more information, see [How to: Configure Client Application Services](../../../docs/framework/common-client-technologies/how-to-configure-client-application-services.md).</span></span>  
  
     [!code-csharp[ClientApplicationServices#030](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Form1.cs#030)]
     [!code-vb[ClientApplicationServices#030](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Form1.vb#030)]  
  
 <span data-ttu-id="3cb95-332">認証が成功した場合に、クライアント認証プロバイダーは <xref:System.Threading.Thread.CurrentPrincipal%2A?displayProperty=nameWithType> プロパティを <xref:System.Web.ClientServices.ClientRolePrincipal> クラスのインスタンスに設定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-332">If authentication is successful, the client authentication provider sets the <xref:System.Threading.Thread.CurrentPrincipal%2A?displayProperty=nameWithType> property to an instance of the <xref:System.Web.ClientServices.ClientRolePrincipal> class.</span></span> <span data-ttu-id="3cb95-333">このクラスは、構成済みのロール プロバイダーに作業を委任するよう、 <xref:System.Security.Principal.IPrincipal.IsInRole%2A> メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-333">This class implements the <xref:System.Security.Principal.IPrincipal.IsInRole%2A> method so that the work is delegated to the configured role provider.</span></span> <span data-ttu-id="3cb95-334">上記と同様、アプリケーションのコードにサービス プロバイダーへの直接の参照は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="3cb95-334">As before, your application code does not require a direct reference to the service provider.</span></span>  
  
 <span data-ttu-id="3cb95-335">ここでアプリケーションを実行し、従業員としてログインして、ボタンが表示されないことを確認できます。次いで、管理者としてログインして、ボタンが表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-335">You can now run the application and log in as employee to see that the button does not appear, and then log in as manager to see the button.</span></span>  
  
## <a name="accessing-web-settings"></a><span data-ttu-id="3cb95-336">Web 設定にアクセスする</span><span class="sxs-lookup"><span data-stu-id="3cb95-336">Accessing Web Settings</span></span>  
 <span data-ttu-id="3cb95-337">次の手順では、フォームにテキスト ボックスを追加するとともに、Web 設定にバインドします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-337">In the following procedure, you add a text box to the form and bind it to a Web setting.</span></span> <span data-ttu-id="3cb95-338">認証とロールを使用する前のコードと同様、設定コードは設定プロバイダーに直接アクセスしません。</span><span class="sxs-lookup"><span data-stu-id="3cb95-338">Like the previous code that uses authentication and roles, your settings code does not access the settings provider directly.</span></span> <span data-ttu-id="3cb95-339">代わりに、Visual Studio がプロジェクト用に生成する、厳密に型指定された `Settings` クラスを使用します (C# では `Properties.Settings.Default` として、Visual Basic では `My.Settings` としてアクセスします)。</span><span class="sxs-lookup"><span data-stu-id="3cb95-339">Instead, it uses the strongly-typed `Settings` class (accessed as `Properties.Settings.Default` in C# and `My.Settings` in Visual Basic) generated for your project by Visual Studio.</span></span>  
  
#### <a name="to-use-web-settings-in-your-user-interface"></a><span data-ttu-id="3cb95-340">ユーザー インターフェイスで Web 設定を使用するには</span><span class="sxs-lookup"><span data-stu-id="3cb95-340">To use Web settings in your user interface</span></span>  
  
1.  <span data-ttu-id="3cb95-341">タスクバーの通知領域をチェックして、 **ASP.NET Web 開発サーバー** がまだ実行中であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-341">Make sure that the **ASP.NET Web Development Server** is still running by checking the notification area of the taskbar.</span></span> <span data-ttu-id="3cb95-342">サーバーが停止している場合は、アプリケーションを再起動して (これによりサーバーが自動的に起動します)、その後、ログイン ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-342">If you have stopped the server, restart the application (which starts the server automatically) then close the login dialog box.</span></span>  
  
2.  <span data-ttu-id="3cb95-343">**[ソリューション エクスプローラー]** で、ClientAppServicesDemo プロジェクトを選択し、 **[プロジェクト]** メニューで **[ClientAppServicesDemo のプロパティ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-343">In **Solution Explorer**, select the ClientAppServicesDemo project, and then on the **Project** menu, select **ClientAppServicesDemo Properties**.</span></span>  
  
     <span data-ttu-id="3cb95-344">プロジェクト デザイナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-344">The project designer appears.</span></span>  
  
3.  <span data-ttu-id="3cb95-345">**[設定]** タブで、 **[Web 設定の読み込み]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-345">On the **Settings** tab, click **Load Web Settings**.</span></span>  
  
     <span data-ttu-id="3cb95-346">**[ログイン]** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-346">A **Login** dialog box appears.</span></span>  
  
4.  <span data-ttu-id="3cb95-347">従業員またはマネージャーの資格情報を入力してから、 **[ログイン]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-347">Enter credentials for employee or manager and click **Log In**.</span></span> <span data-ttu-id="3cb95-348">使用する Web 設定は認証されたユーザーのみがアクセスできるように構成されているため、 **[ログインのスキップ]** をクリックすると設定は読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="3cb95-348">The Web setting you will use is configured for access by authenticated users only, so clicking **Skip Login** will not load any settings.</span></span>  
  
     <span data-ttu-id="3cb95-349">`WebSettingsTestText` の設定が、既定値の `DefaultText`でデザイナーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-349">The `WebSettingsTestText` setting appears in the designer with the default value of `DefaultText`.</span></span> <span data-ttu-id="3cb95-350">さらに、`WebSettingsTestText` プロパティを含む `Settings` クラスがプロジェクトに生成されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-350">Additionally, a `Settings` class that contains a `WebSettingsTestText` property is generated for your project.</span></span>  
  
5.  <span data-ttu-id="3cb95-351">**[ソリューション エクスプローラー]** の ClientAppServicesDemo プロジェクトで、Form1 を選択してから、Visual Studio のメイン メニューで **[表示] &#124; [デザイナー]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-351">In **Solution Explorer**, in the ClientAppServicesDemo project, select Form1 and then select **View &#124; Designer** from the Visual Studio main menu.</span></span>  
  
6.  <span data-ttu-id="3cb95-352">デザイナーで、フォームに <xref:System.Windows.Forms.TextBox> コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-352">In the designer, add a <xref:System.Windows.Forms.TextBox> control to the form.</span></span>  
  
7.  <span data-ttu-id="3cb95-353">**[プロパティ]** ウィンドウで、 **[(名前)]** の値を " `webSettingsTestTextBox`" と指定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-353">In the **Properties** window, specify a **(Name)** value of `webSettingsTestTextBox`.</span></span>  
  
8.  <span data-ttu-id="3cb95-354">コード エディターで、 `Form1_Load` メソッドの末尾に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-354">In the code editor, add the following code to the end of the `Form1_Load` method.</span></span>  
  
     <span data-ttu-id="3cb95-355">このコードは、次の手順で追加する `BindWebSettingsTestTextBox` メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-355">This code calls the `BindWebSettingsTestTextBox` method that you will add in the next step.</span></span>  
  
     [!code-csharp[ClientApplicationServices#013](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Form1.cs#013)]
     [!code-vb[ClientApplicationServices#013](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Form1.vb#013)]  
  
9. <span data-ttu-id="3cb95-356">次のメソッドを Form1 クラスの末尾に追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-356">Add the following method to the end of the Form1 class.</span></span>  
  
     <span data-ttu-id="3cb95-357">このメソッドは、 <xref:System.Windows.Forms.TextBox.Text%2A> の `webSettingsTestTextBox` プロパティを、この手順の前半で生成した `WebSettingsTestText` クラスの `Settings` プロパティにバインドします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-357">This method binds the <xref:System.Windows.Forms.TextBox.Text%2A> property of the `webSettingsTestTextBox` to the `WebSettingsTestText` property of the `Settings` class generated earlier in this procedure.</span></span> <span data-ttu-id="3cb95-358">また、このメソッドは、 <xref:System.Net.WebException> がスローされるとエラー メッセージを表示します。これは、Web 設定サービスが使用できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-358">This method also displays an error message if a <xref:System.Net.WebException> is thrown, which indicates that the Web settings service is unavailable.</span></span>  
  
     [!code-csharp[ClientApplicationServices#040](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Form1.cs#040)]
     [!code-vb[ClientApplicationServices#040](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Form1.vb#040)]  
  
    > [!NOTE]
    >  <span data-ttu-id="3cb95-359">通常は、データ バインドを使用して、コントロールと Web 設定間の自動双方向通信を有効にします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-359">You will typically use data binding to enable automatic two-way communication between a control and a Web setting.</span></span> <span data-ttu-id="3cb95-360">しかし、次の例に示すとおり、直接 Web 設定にアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-360">However, you can also access Web settings directly as shown in the following example:</span></span>  
  
     [!code-csharp[ClientApplicationServices#322](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Class1.cs#322)]
     [!code-vb[ClientApplicationServices#322](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Class1.vb#322)]  
  
10. <span data-ttu-id="3cb95-361">デザイナーで、フォームを選択してから、 **[プロパティ]** ウィンドウの **[イベント]** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-361">In the designer, select the form, and then, in the **Properties** window, click the **Events** button.</span></span>  
  
11. <span data-ttu-id="3cb95-362"><xref:System.Windows.Forms.Form.FormClosing> イベントをクリックしてから、Enter キーを押すとイベント ハンドラーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-362">Select the <xref:System.Windows.Forms.Form.FormClosing> event and then press ENTER to generate an event handler.</span></span>  
  
12. <span data-ttu-id="3cb95-363">生成されたメソッドを次のコードで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-363">Replace the generated method with the following code.</span></span>  
  
     <span data-ttu-id="3cb95-364"><xref:System.Windows.Forms.Form.FormClosing> イベント ハンドラーが `SaveSettings` メソッドを呼び出します。このメソッドは、次のセクションで追加するログアウト機能でも使用されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-364">The <xref:System.Windows.Forms.Form.FormClosing> event handler calls the `SaveSettings` method, which is also used by the logout functionality that you will add in the next section.</span></span> <span data-ttu-id="3cb95-365">まず、 `SaveSettings` メソッドは、ユーザーがログアウトしていないことを確認します。これは、現在のプリンシパルによって返される <xref:System.Security.Principal.IIdentity.AuthenticationType%2A> の <xref:System.Security.Principal.IIdentity> プロパティをチェックして行います。</span><span class="sxs-lookup"><span data-stu-id="3cb95-365">The `SaveSettings` method first confirms that the user has not logged out. It does this by checking the <xref:System.Security.Principal.IIdentity.AuthenticationType%2A> property of the <xref:System.Security.Principal.IIdentity> returned by the current principal.</span></span> <span data-ttu-id="3cb95-366">現在のプリンシパルは `static` <xref:System.Threading.Thread.CurrentPrincipal%2A> プロパティを介して取得します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-366">The current principal is retrieved through the `static` <xref:System.Threading.Thread.CurrentPrincipal%2A> property.</span></span> <span data-ttu-id="3cb95-367">ユーザーがクライアント アプリケーション サービスで認証済みであれば、認証の種類は "ClientForms" になります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-367">If the user has been authenticated for client application services, the authentication type will be "ClientForms".</span></span> <span data-ttu-id="3cb95-368">`SaveSettings` メソッドは、単に <xref:System.Security.Principal.IIdentity.IsAuthenticated%2A?displayProperty=nameWithType> プロパティをチェックすることはできません。これは、ユーザーがログアウト後に有効な Windows ID を持っていることがあるためです。</span><span class="sxs-lookup"><span data-stu-id="3cb95-368">The `SaveSettings` method cannot just check the <xref:System.Security.Principal.IIdentity.IsAuthenticated%2A?displayProperty=nameWithType> property because the user might have a valid Windows identity after logout.</span></span>  
  
     <span data-ttu-id="3cb95-369">ユーザーがログアウトしていない場合、 `SaveSettings` メソッドは、この手順の前半で生成された <xref:System.Configuration.ApplicationSettingsBase.Save%2A> クラスの `Settings` メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-369">If the user has not logged out, the `SaveSettings` method calls the <xref:System.Configuration.ApplicationSettingsBase.Save%2A> method of the `Settings` class generated earlier in this procedure.</span></span> <span data-ttu-id="3cb95-370">認証クッキーの有効期限が切れている場合、このメソッドは <xref:System.Net.WebException> をスローすることがあります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-370">This method can throw a <xref:System.Net.WebException> if the authentication cookie has expired.</span></span> <span data-ttu-id="3cb95-371">これが発生するのは、アプリケーションの構成で **[サーバー クッキーの期限が切れた場合は常に再度ログオンすることをユーザーに要求する]** を選択した場合だけです。</span><span class="sxs-lookup"><span data-stu-id="3cb95-371">This occurs only if you have selected **Require users to log on again whenever the server cookie expires** in your application configuration.</span></span> <span data-ttu-id="3cb95-372">詳細については、「 [How to: Configure Client Application Services](../../../docs/framework/common-client-technologies/how-to-configure-client-application-services.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cb95-372">For more information, see [How to: Configure Client Application Services](../../../docs/framework/common-client-technologies/how-to-configure-client-application-services.md).</span></span> <span data-ttu-id="3cb95-373">`SaveSettings` メソッドは、 <xref:System.Web.Security.Membership.ValidateUser%2A> を呼び出してログイン ダイアログ ボックスを表示することで、クッキーの有効期限を処理します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-373">The `SaveSettings` method handles cookie expiration by calling <xref:System.Web.Security.Membership.ValidateUser%2A> to display the login dialog box.</span></span> <span data-ttu-id="3cb95-374">ユーザーが正常にログインすると、 `SaveSettings` メソッドは自身を呼び出して設定を再度保存しようとします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-374">If the user logs in successfully, the `SaveSettings` method tries to save the settings again by calling itself.</span></span>  
  
     <span data-ttu-id="3cb95-375">前のコードと同様、リモート サービスが使用できない場合、 `SaveSettings` メソッドはエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-375">Like in previous code, the `SaveSettings` method displays an error message if the remote service is unavailable.</span></span> <span data-ttu-id="3cb95-376">設定プロバイダーがリモート サービスにアクセスできない場合、設定はローカル キャッシュに保存されたままとなり、アプリケーションの再起動時に再度読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-376">If the settings provider cannot access the remote service, the settings are still saved to the local cache and reloaded when the application restarts.</span></span>  
  
     [!code-csharp[ClientApplicationServices#050](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Form1.cs#050)]
     [!code-vb[ClientApplicationServices#050](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Form1.vb#050)]  
  
13. <span data-ttu-id="3cb95-377">次のメソッドを Form1 クラスの末尾に追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-377">Add the following method to the end of the Form1 class.</span></span>  
  
     <span data-ttu-id="3cb95-378">このコードは <xref:System.Web.ClientServices.Providers.ClientSettingsProvider.SettingsSaved?displayProperty=nameWithType> イベントを処理し、設定のいずれかが保存できなかった場合は警告を表示します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-378">This code handles the <xref:System.Web.ClientServices.Providers.ClientSettingsProvider.SettingsSaved?displayProperty=nameWithType> event and displays a warning if any of the settings could not be saved.</span></span> <span data-ttu-id="3cb95-379">設定サービスが使用できない場合、または認証クッキーの有効期限が切れている場合、 <xref:System.Web.ClientServices.Providers.ClientSettingsProvider.SettingsSaved> イベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="3cb95-379">The <xref:System.Web.ClientServices.Providers.ClientSettingsProvider.SettingsSaved> event does not occur if the settings service is unavailable or if the authentication cookie has expired.</span></span> <span data-ttu-id="3cb95-380"><xref:System.Web.ClientServices.Providers.ClientSettingsProvider.SettingsSaved> イベントが発生する 1 つの例は、ユーザーが既にログアウトしている場合です。このイベント ハンドラーは、 `SaveSettings` メソッドの呼び出しの直前にある <xref:System.Configuration.ApplicationSettingsBase.Save%2A> メソッドにログアウトのコードを追加することでテストできます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-380">One example of when the <xref:System.Web.ClientServices.Providers.ClientSettingsProvider.SettingsSaved> event will occur is if the user has already logged out. You can test this event handler by adding logout code to the `SaveSettings` method directly before the <xref:System.Configuration.ApplicationSettingsBase.Save%2A> method call.</span></span> <span data-ttu-id="3cb95-381">使用できるログアウトのコードは、次のセクションで説明します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-381">Logout code that you can use is described in the next section.</span></span>  
  
     [!code-csharp[ClientApplicationServices#090](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Form1.cs#090)]
     [!code-vb[ClientApplicationServices#090](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Form1.vb#090)]  
  
14. <span data-ttu-id="3cb95-382">C# では、 `Form1_Load` メソッドの末尾に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-382">For C#, add the following code to the end of the `Form1_Load` method.</span></span> <span data-ttu-id="3cb95-383">このコードは、最後の手順で追加したメソッドと <xref:System.Web.ClientServices.Providers.ClientSettingsProvider.SettingsSaved> イベントを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-383">This code associates the method you added in the last step with the <xref:System.Web.ClientServices.Providers.ClientSettingsProvider.SettingsSaved> event.</span></span>  
  
     [!code-csharp[ClientApplicationServices#015](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Form1.cs#015)]  
  
 <span data-ttu-id="3cb95-384">この時点でアプリケーションをテストするため、従業員として、およびマネージャーとして複数回これを実行し、テキスト ボックスに異なる値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-384">To test the application at this point, run it multiple times as both employee and manager, and type different values into the text box.</span></span> <span data-ttu-id="3cb95-385">値は、ユーザーごとにセッションをまたいで保持されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-385">The values will persist across sessions on a per-user basis.</span></span>  
  
## <a name="implementing-logout"></a><span data-ttu-id="3cb95-386">ログアウトを実装する</span><span class="sxs-lookup"><span data-stu-id="3cb95-386">Implementing Logout</span></span>  
 <span data-ttu-id="3cb95-387">ユーザーがログイン時に **[アカウントを記憶]** チェック ボックスをオンにすると、アプリケーションは以降の実行時に自動的にユーザーを認証します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-387">When the user selects the **Remember me** check box when logging in, the application will automatically authenticate the user on subsequent runs.</span></span> <span data-ttu-id="3cb95-388">自動認証は、アプリケーションがオフライン モードの場合、または認証クッキーの有効期限が切れるまで継続します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-388">Automatic authentication will then continue while the application is in offline mode or until the authentication cookie expires.</span></span> <span data-ttu-id="3cb95-389">ただし、場合によっては、複数のユーザーがアプリケーションにアクセスしなければならなくなることや、1 人のユーザーが別の資格情報でログインすることもあります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-389">Sometimes, however, multiple users will need access to the application or a single user might occasionally log in with different credentials.</span></span> <span data-ttu-id="3cb95-390">このシナリオを有効にするには、次の手順に説明するログアウト機能を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-390">To enable this scenario, you must implement logout functionality, as described in the following procedure.</span></span>  
  
#### <a name="to-implement-logout-functionality"></a><span data-ttu-id="3cb95-391">ログアウト機能を実装するには</span><span class="sxs-lookup"><span data-stu-id="3cb95-391">To implement logout functionality</span></span>  
  
1.  <span data-ttu-id="3cb95-392">Form1 デザイナーで、**[ツールボックス]** から <xref:System.Windows.Forms.Button> コントロールをフォームに追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-392">In the Form1 designer, add a <xref:System.Windows.Forms.Button> control to the form from the **ToolBox**.</span></span>  
  
2.  <span data-ttu-id="3cb95-393">**[プロパティ]** ウィンドウで、**[(名前)]** の値を "`logoutButton`" と指定し、**[テキスト]** の値を "**&Log Out**" と指定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-393">In the **Properties** window, specify a **(Name)** value of `logoutButton` and a **Text** value of **&Log Out**.</span></span>  
  
3.  <span data-ttu-id="3cb95-394">`logoutButton` をダブルクリックすると、<xref:System.Windows.Forms.Control.Click> イベント ハンドラーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-394">Double-click the `logoutButton` to generate a <xref:System.Windows.Forms.Control.Click> event handler.</span></span>  
  
     <span data-ttu-id="3cb95-395">`logoutButton_Click` メソッドにカーソルがある状態でコード エディターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-395">The code editor appears with the cursor in the `logoutButton_Click` method.</span></span>  
  
4.  <span data-ttu-id="3cb95-396">生成された `logoutButton_Click` メソッドを次のコードで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-396">Replace the generated `logoutButton_Click` method with the following code.</span></span>  
  
     <span data-ttu-id="3cb95-397">まず、このイベント ハンドラーは、前のセクションで追加した `SaveSettings` メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-397">This event handler first calls the `SaveSettings` method that you added in the previous section.</span></span> <span data-ttu-id="3cb95-398">次に、イベント ハンドラーは <xref:System.Web.ClientServices.Providers.ClientFormsAuthenticationMembershipProvider.Logout%2A?displayProperty=nameWithType> メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-398">Then, the event handler calls the <xref:System.Web.ClientServices.Providers.ClientFormsAuthenticationMembershipProvider.Logout%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="3cb95-399">認証サービスが使用できない場合、 <xref:System.Web.ClientServices.Providers.ClientFormsAuthenticationMembershipProvider.Logout%2A> メソッドは <xref:System.Net.WebException>をスローします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-399">If the authentication service is unavailable, the <xref:System.Web.ClientServices.Providers.ClientFormsAuthenticationMembershipProvider.Logout%2A> method will throw a <xref:System.Net.WebException>.</span></span> <span data-ttu-id="3cb95-400">この場合、 `logoutButton_Click` メソッドは警告メッセージを表示し、一時的にオフライン モードに切り替えてユーザーをログアウトします。オフライン モードについては、次のセクションで説明します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-400">In this case, the `logoutButton_Click` method displays a warning message and switches temporarily to offline mode to log the user out. Offline mode is described in the next section.</span></span>  
  
     <span data-ttu-id="3cb95-401">ログアウトすると、アプリケーションの再起動時にログインが必要になるように、ローカルの認証クッキーが削除されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-401">Logout deletes the local authentication cookie so that login will be required when the application is restarted.</span></span> <span data-ttu-id="3cb95-402">ログアウト後、イベント ハンドラーは、アプリケーションを再起動します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-402">After logout, the event handler restarts the application.</span></span> <span data-ttu-id="3cb95-403">アプリケーションは、再起動すると、ようこそメッセージに続いてログイン ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-403">When the application restarts, it displays the welcome message followed by the login dialog box.</span></span> <span data-ttu-id="3cb95-404">ようこそメッセージにより、アプリケーションが再起動したことが明確になります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-404">The welcome message makes it clear that the application has restarted.</span></span> <span data-ttu-id="3cb95-405">こうすることで、ユーザーが設定の保存のためのログインに続いて、アプリケーションの再起動に伴うログインを再度行わなければならない場合に、起こりうる混乱を避けられます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-405">This prevents potential confusion if the user must log in to save settings, and then must log in again because the application has restarted.</span></span>  
  
     [!code-csharp[ClientApplicationServices#070](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Form1.cs#070)]
     [!code-vb[ClientApplicationServices#070](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Form1.vb#070)]  
  
 <span data-ttu-id="3cb95-406">ログアウト機能をテストするには、アプリケーションを実行し、[ログイン] ダイアログ ボックスで **[アカウントを記憶]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-406">To test the logout functionality, run the application and select **Remember me** on the Login dialog box.</span></span> <span data-ttu-id="3cb95-407">次に、ログインする必要がなくなることを確認するため、アプリケーションを閉じて再起動します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-407">Next, close and restart the application to confirm that you no longer have to log in.</span></span> <span data-ttu-id="3cb95-408">最後に、[Log out] をクリックして、アプリケーションを再起動します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-408">Finally, restart the application by clicking Log out.</span></span>  
  
## <a name="enabling-offline-mode"></a><span data-ttu-id="3cb95-409">オフライン モードを有効にする</span><span class="sxs-lookup"><span data-stu-id="3cb95-409">Enabling Offline Mode</span></span>  
 <span data-ttu-id="3cb95-410">次の手順では、ユーザーがオフライン モードに入れるようにするチェック ボックスをフォームに追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-410">In the following procedure, you add a check box to the form to enable the user to enter offline mode.</span></span> <span data-ttu-id="3cb95-411">`static` <xref:System.Web.ClientServices.ConnectivityStatus.IsOffline%2A?displayProperty=nameWithType> プロパティを `true`に設定すると、アプリケーションはオフライン モードを示します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-411">Your application indicates offline mode by setting the `static` <xref:System.Web.ClientServices.ConnectivityStatus.IsOffline%2A?displayProperty=nameWithType> property to `true`.</span></span> <span data-ttu-id="3cb95-412">オフラインの状態は、ローカルのハード ディスク上の、 <xref:System.Windows.Forms.Application.UserAppDataPath%2A?displayProperty=nameWithType> プロパティが示す場所に格納されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-412">The offline status is stored on the local hard disk at the location indicated by the <xref:System.Windows.Forms.Application.UserAppDataPath%2A?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="3cb95-413">つまり、オフラインの状態は、ユーザーごと、アプリケーションごとに格納されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-413">This means that the offline status is stored on a per-user, per-application basis.</span></span>  
  
 <span data-ttu-id="3cb95-414">オフライン モードの場合、クライアント アプリケーション サービス要求はどれも、サービスへのアクセスを試みることなく、ローカル キャッシュからデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-414">In offline mode, all client application service requests retrieve data from the local cache instead of trying to access the services.</span></span> <span data-ttu-id="3cb95-415">既定の構成では、ローカル データには暗号化された形式のユーザーのパスワードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3cb95-415">In the default configuration, the local data includes an encrypted form of the user's password.</span></span> <span data-ttu-id="3cb95-416">これにより、ユーザーは、アプリケーションがオフライン モードのときにログインできます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-416">This enables the user to log in while the application is in offline mode.</span></span> <span data-ttu-id="3cb95-417">詳細については、「 [How to: Configure Client Application Services](../../../docs/framework/common-client-technologies/how-to-configure-client-application-services.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cb95-417">For more information, see [How to: Configure Client Application Services](../../../docs/framework/common-client-technologies/how-to-configure-client-application-services.md).</span></span>  
  
#### <a name="to-enable-offline-mode-in-your-application"></a><span data-ttu-id="3cb95-418">アプリケーションでオフライン モードを有効にするには</span><span class="sxs-lookup"><span data-stu-id="3cb95-418">To enable offline mode in your application</span></span>  
  
1.  <span data-ttu-id="3cb95-419">**[ソリューション エクスプローラー]** の ClientAppServicesDemo プロジェクトで、Form1 を選択してから、Visual Studio のメイン メニューで **[表示] &#124; [デザイナー]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-419">In **Solution Explorer**, in the ClientAppServicesDemo project, select Form1 and then select **View &#124; Designer** from the Visual Studio main menu.</span></span>  
  
2.  <span data-ttu-id="3cb95-420">デザイナーで、フォームに <xref:System.Windows.Forms.CheckBox> コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-420">In the designer, add a <xref:System.Windows.Forms.CheckBox> control to the form.</span></span>  
  
3.  <span data-ttu-id="3cb95-421">**[プロパティ]** ウィンドウで、**[(名前)]** の値を "`workOfflineCheckBox`" と指定し、**[テキスト]** の値を "**&Work offline**" と指定します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-421">In the **Properties** window, specify a **(Name)** value of `workOfflineCheckBox` and a **Text** value of **&Work offline**.</span></span>  
  
4.  <span data-ttu-id="3cb95-422">**[プロパティ]** ウィンドウで、 **[イベント]** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-422">In the **Properties** window, click the **Events** button.</span></span>  
  
5.  <span data-ttu-id="3cb95-423"><xref:System.Windows.Forms.CheckBox.CheckedChanged> イベントをクリックしてから、Enter キーを押すとイベント ハンドラーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-423">Select the <xref:System.Windows.Forms.CheckBox.CheckedChanged> event and then press ENTER to generate an event handler.</span></span>  
  
6.  <span data-ttu-id="3cb95-424">生成されたメソッドを次のコードで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-424">Replace the generated method with the following code.</span></span>  
  
     <span data-ttu-id="3cb95-425">このコードは、 <xref:System.Web.ClientServices.ConnectivityStatus.IsOffline%2A> の値を更新し、オンライン モードに戻るときに、ダイアログを表示せずにユーザーを再検証します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-425">This code updates the <xref:System.Web.ClientServices.ConnectivityStatus.IsOffline%2A> value and silently revalidates the user when they return to online mode.</span></span> <span data-ttu-id="3cb95-426"><xref:System.Web.ClientServices.ClientFormsIdentity.RevalidateUser%2A?displayProperty=nameWithType> メソッドでは、ユーザーが明示的にログインする必要がないように、キャッシュされた資格情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-426">The <xref:System.Web.ClientServices.ClientFormsIdentity.RevalidateUser%2A?displayProperty=nameWithType> method uses the cached credentials so that the user does not have to explicitly log in.</span></span> <span data-ttu-id="3cb95-427">認証サービスが使用できない場合、警告メッセージが表示され、アプリケーションはオフラインのままになります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-427">If the authentication service is unavailable, a warning message appears and the application stays offline.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="3cb95-428"><xref:System.Web.ClientServices.ClientFormsIdentity.RevalidateUser%2A> メソッドは便宜的なものに過ぎません。</span><span class="sxs-lookup"><span data-stu-id="3cb95-428">The <xref:System.Web.ClientServices.ClientFormsIdentity.RevalidateUser%2A> method is for convenience only.</span></span> <span data-ttu-id="3cb95-429">このメソッドには戻り値がないため、再検証が失敗したかどうかを示すことはできません。</span><span class="sxs-lookup"><span data-stu-id="3cb95-429">Because it does not have a return value, it cannot indicate whether revalidation has failed.</span></span> <span data-ttu-id="3cb95-430">再検証は失敗することがあります。たとえば、サーバーでユーザーの資格情報が変更された場合などです。</span><span class="sxs-lookup"><span data-stu-id="3cb95-430">Revalidation can fail, for example, if the user credentials have changed on the server.</span></span> <span data-ttu-id="3cb95-431">この場合、サービスの呼び出しが失敗した後に、明示的にユーザーを検証するコードを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-431">In this case, you might want to include code that explicitly validates users after a service call fails.</span></span> <span data-ttu-id="3cb95-432">詳細については、このチュートリアルの上述の「Web 設定にアクセスする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cb95-432">For more information, see the Accessing Web Settings section earlier in this walkthrough.</span></span>  
  
     <span data-ttu-id="3cb95-433">再検証後、前に追加した `SaveSettings` メソッドを呼び出すことで、このコードはローカルの Web 設定への変更をすべて保存します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-433">After revalidation, this code saves any changes to the local Web settings by calling the `SaveSettings` method that you added previously.</span></span> <span data-ttu-id="3cb95-434">続いて、プロジェクトの `Settings` クラスの <xref:System.Configuration.ApplicationSettingsBase.Reload%2A> メソッドを呼び出して、新しい値をすべて取得します (C# では `Properties.Settings.Default` として、Visual Basic では `My.Settings` としてアクセスします)。</span><span class="sxs-lookup"><span data-stu-id="3cb95-434">It then retrieves any new values on the server by calling the <xref:System.Configuration.ApplicationSettingsBase.Reload%2A> method of the project's `Settings` class (accessed as `Properties.Settings.Default` in C# and `My.Settings` in Visual Basic).</span></span>  
  
     [!code-csharp[ClientApplicationServices#080](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Form1.cs#080)]
     [!code-vb[ClientApplicationServices#080](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Form1.vb#080)]  
  
7.  <span data-ttu-id="3cb95-435">`Form1_Load` メソッドの末尾に次のコードを追加して、チェック ボックスが現在の接続状態を示すようにします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-435">Add the following code to the end of the `Form1_Load` method to make sure that the check box displays the current connection state.</span></span>  
  
     [!code-csharp[ClientApplicationServices#014](../../../samples/snippets/csharp/VS_Snippets_Winforms/ClientApplicationServices/CS/Form1.cs#014)]
     [!code-vb[ClientApplicationServices#014](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/ClientApplicationServices/VB/Form1.vb#014)]  
  
 <span data-ttu-id="3cb95-436">これで、サンプル アプリケーションが完成しました。</span><span class="sxs-lookup"><span data-stu-id="3cb95-436">This completes the example application.</span></span> <span data-ttu-id="3cb95-437">オフライン機能をテストするには、アプリケーションを実行し、従業員またはマネージャーとしてログインしてから、 **[Work offline]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-437">To test the offline capability, run the application, log in as either employee or manager, and then select **Work offline**.</span></span> <span data-ttu-id="3cb95-438">テキスト ボックスの値を変更してから、アプリケーションを終了します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-438">Modify the value in the text box, and then close the application.</span></span> <span data-ttu-id="3cb95-439">アプリケーションを再起動します</span><span class="sxs-lookup"><span data-stu-id="3cb95-439">Restart the application.</span></span> <span data-ttu-id="3cb95-440">ログインする前に、タスク バーの通知領域にある ASP.NET 開発サーバーのアイコンを右クリックしてから、 **[停止]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-440">Before you log in, right-click the ASP.NET Development Server icon in the notification area of the taskbar and then click **Stop**.</span></span> <span data-ttu-id="3cb95-441">次に、通常どおりにログインします。</span><span class="sxs-lookup"><span data-stu-id="3cb95-441">Then, log in like normal.</span></span> <span data-ttu-id="3cb95-442">サーバーが実行されていない場合でもログインできます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-442">Even when the server is not running, you can still log in.</span></span> <span data-ttu-id="3cb95-443">テキスト ボックスの値を変更してから、終了および再起動を行って、変更された値を確認します。</span><span class="sxs-lookup"><span data-stu-id="3cb95-443">Modify the text box value, exit, and restart to see the modified value.</span></span>  
  
## <a name="summary"></a><span data-ttu-id="3cb95-444">まとめ</span><span class="sxs-lookup"><span data-stu-id="3cb95-444">Summary</span></span>  
 <span data-ttu-id="3cb95-445">このチュートリアルでは、Windows フォーム アプリケーションでのクライアント アプリケーション サービスの有効化および使用方法について学習しました。</span><span class="sxs-lookup"><span data-stu-id="3cb95-445">In this walkthrough, you learned how to enable and use client application services in a Windows Forms application.</span></span> <span data-ttu-id="3cb95-446">テスト サーバーをセットアップした後、アプリケーションにコードを追加し、ユーザーを認証したり、サーバーからユーザーのロールとアプリケーションの設定を取得したりできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="3cb95-446">After setting up a test server, you added code to your application to authenticate users and retrieve user roles and application settings from the server.</span></span> <span data-ttu-id="3cb95-447">また、接続を使用できない場合に、アプリケーションがリモート サービスではなく、ローカル データ キャッシュを使用できるように、オフライン モードを有効にする方法についても学びました。</span><span class="sxs-lookup"><span data-stu-id="3cb95-447">You also learned how to enable offline mode so that your application uses a local data cache instead of the remote services when connectivity is not available.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="3cb95-448">次の手順</span><span class="sxs-lookup"><span data-stu-id="3cb95-448">Next Steps</span></span>  
 <span data-ttu-id="3cb95-449">実際のアプリケーションではリモート サーバーから多数のユーザーのデータを取得しますが、サーバーは常に使用可能であるとは限らず、予告なく停止する可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-449">In a real-world application, you will access data for many users from a remote server that may not always be available, or may go down without notice.</span></span> <span data-ttu-id="3cb95-450">アプリケーションを堅牢にするため、サービスが利用できない場合に状況に適切に対応する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cb95-450">To make your application robust, you must respond appropriately to situations where the service is not available.</span></span> <span data-ttu-id="3cb95-451">このチュートリアルには、サービスが利用できない場合に <xref:System.Net.WebException> をキャッチしてエラー メッセージを表示する try ブロックと catch ブロックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3cb95-451">This walkthrough includes try/catch blocks to catch a <xref:System.Net.WebException> and display an error message when the service is not available.</span></span> <span data-ttu-id="3cb95-452">実稼働コードでは、このケースに対処するため、オフライン モードに切り替えることや、アプリケーションを終了すること、特定の機能へのアクセスを拒否することができます。</span><span class="sxs-lookup"><span data-stu-id="3cb95-452">In production code, you might want to handle this case by switching to offline mode, exiting the application, or denying access to specific functionality.</span></span>  
  
 <span data-ttu-id="3cb95-453">アプリケーションのセキュリティを向上させるため、配置する前に必ずアプリケーションとサーバーを十分にテストしてください。</span><span class="sxs-lookup"><span data-stu-id="3cb95-453">To increase the security of your application, make sure to thoroughly test the application and server before deployment.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3cb95-454">参照</span><span class="sxs-lookup"><span data-stu-id="3cb95-454">See Also</span></span>  
 [<span data-ttu-id="3cb95-455">クライアント アプリケーション サービス</span><span class="sxs-lookup"><span data-stu-id="3cb95-455">Client Application Services</span></span>](../../../docs/framework/common-client-technologies/client-application-services.md)  
 [<span data-ttu-id="3cb95-456">クライアント アプリケーション サービスの概要</span><span class="sxs-lookup"><span data-stu-id="3cb95-456">Client Application Services Overview</span></span>](../../../docs/framework/common-client-technologies/client-application-services-overview.md)  
 [<span data-ttu-id="3cb95-457">方法 : クライアント アプリケーション サービスを構成する</span><span class="sxs-lookup"><span data-stu-id="3cb95-457">How to: Configure Client Application Services</span></span>](../../../docs/framework/common-client-technologies/how-to-configure-client-application-services.md)  
 [<span data-ttu-id="3cb95-458">ASP.NET Web サイト管理ツール</span><span class="sxs-lookup"><span data-stu-id="3cb95-458">ASP.NET Web Site Administration Tool</span></span>](https://msdn.microsoft.com/library/100ddd8b-7d11-4df9-91ef-0bbbe92e5aec)  
 [<span data-ttu-id="3cb95-459">SQL Server 向けアプリケーション サービス データベースの作成と構成</span><span class="sxs-lookup"><span data-stu-id="3cb95-459">Creating and Configuring the Application Services Database for SQL Server</span></span>](https://msdn.microsoft.com/library/ab894e83-7e2f-4af8-a116-b1bff8f815b2)  
 [<span data-ttu-id="3cb95-460">チュートリアル: ASP.NET アプリケーション サービスの使用</span><span class="sxs-lookup"><span data-stu-id="3cb95-460">Walkthrough: Using ASP.NET Application Services</span></span>](https://msdn.microsoft.com/library/f3f394f0-20d6-4361-aa8f-4b21bf4933eb)
