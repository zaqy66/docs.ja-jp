---
title: IAppDomainSetup インターフェイス
ms.date: 03/30/2017
api_name:
- IAppDomainSetup
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IAppDomainSetup
helpviewer_keywords:
- IAppDomainSetup interface [.NET Framework hosting]
ms.assetid: 1844da85-c031-40bf-bea4-1a3d12a36c8c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ef967039450c77b5927d501de63d53a245c90be0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54509832"
---
# <a name="iappdomainsetup-interface"></a><span data-ttu-id="a2f12-102">IAppDomainSetup インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2f12-102">IAppDomainSetup Interface</span></span>
<span data-ttu-id="a2f12-103">プロパティを構成するホストを提供します、<xref:System.AppDomain?displayProperty=nameWithType>型を呼び出す前に、 [icorruntimehost::createdomainex](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-createdomainex-method.md)メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2f12-103">Provides properties that allow the host to configure an <xref:System.AppDomain?displayProperty=nameWithType> type before calling the [ICorRuntimeHost::CreateDomainEx](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-createdomainex-method.md) method to create it.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="a2f12-104">プロパティ</span><span class="sxs-lookup"><span data-stu-id="a2f12-104">Properties</span></span>  
  
|<span data-ttu-id="a2f12-105">プロパティ</span><span class="sxs-lookup"><span data-stu-id="a2f12-105">Property</span></span>|<span data-ttu-id="a2f12-106">説明</span><span class="sxs-lookup"><span data-stu-id="a2f12-106">Description</span></span>|  
|--------------|-----------------|  
|<xref:System.AppDomainSetup.ApplicationBase%2A>|<span data-ttu-id="a2f12-107">取得またはアプリケーションを含むディレクトリの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="a2f12-107">Gets or sets the name of the directory that contains the application.</span></span>|  
|<xref:System.AppDomainSetup.ApplicationName%2A>|<span data-ttu-id="a2f12-108">アプリケーションの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a2f12-108">Gets or sets the name of the application.</span></span>|  
|<xref:System.AppDomainSetup.CachePath%2A>|<span data-ttu-id="a2f12-109">取得または設定領域の名前特定アプリケーションにファイルがシャドウ コピーされた場所。</span><span class="sxs-lookup"><span data-stu-id="a2f12-109">Gets or sets the name of an area specific to the application where files are shadow-copied.</span></span>|  
|<xref:System.AppDomainSetup.ConfigurationFile%2A>|<span data-ttu-id="a2f12-110">取得またはアプリケーションの構成ファイルの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="a2f12-110">Gets or sets the name of the configuration file for an application.</span></span>|  
|<xref:System.AppDomainSetup.DynamicBase%2A>|<span data-ttu-id="a2f12-111">取得または動的に生成されたファイルを格納し、アクセスする場所のディレクトリの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="a2f12-111">Gets or sets the name of the directory where dynamically generated files are stored and accessed.</span></span>|  
|<xref:System.AppDomainSetup.LicenseFile%2A>|<span data-ttu-id="a2f12-112">取得またはこのドメインに関連付けられているライセンス ファイルへのパスを設定します。</span><span class="sxs-lookup"><span data-stu-id="a2f12-112">Gets or sets the path to the license file that is associated with this domain.</span></span>|  
|<xref:System.AppDomainSetup.PrivateBinPath%2A>|<span data-ttu-id="a2f12-113">取得または設定組み合わせたディレクトリの一覧、<xref:System.AppDomainSetup.ApplicationBase%2A>プライベート アセンブリをプローブするディレクトリ。</span><span class="sxs-lookup"><span data-stu-id="a2f12-113">Gets or sets the list of directories combined with the <xref:System.AppDomainSetup.ApplicationBase%2A> directory to probe for private assemblies.</span></span>|  
|<xref:System.AppDomainSetup.PrivateBinPathProbe%2A>|<span data-ttu-id="a2f12-114">追加または除外する文字列値の設定を取得または<xref:System.AppDomainSetup.ApplicationBase%2A>アプリケーションの検索パスから。</span><span class="sxs-lookup"><span data-stu-id="a2f12-114">Gets or sets a string value that includes or excludes <xref:System.AppDomainSetup.ApplicationBase%2A> from the search path for the application.</span></span>|  
|<xref:System.AppDomainSetup.ShadowCopyDirectories%2A>|<span data-ttu-id="a2f12-115">取得またはアセンブリ シャドウ コピーにはが含まれているディレクトリの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="a2f12-115">Gets or sets the names of the directories that contain assemblies to be shadow-copied.</span></span>|  
|<xref:System.AppDomainSetup.ShadowCopyFiles%2A>|<span data-ttu-id="a2f12-116">取得または設定をオンまたはオフ シャドウ コピーになっているかどうかを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="a2f12-116">Gets or sets a string that indicates whether shadow-copying is turned on or off.</span></span> <span data-ttu-id="a2f12-117">有効な値は"true"または"false です"。</span><span class="sxs-lookup"><span data-stu-id="a2f12-117">Valid values are "true" or "false".</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a2f12-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="a2f12-118">Remarks</span></span>  
 <span data-ttu-id="a2f12-119">`IAppDomainSetup`インターフェイスに対応するマネージ<xref:System.IAppDomainSetup>が、インターフェイス、<xref:System.AppDomainSetup>実装を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2f12-119">The `IAppDomainSetup` interface corresponds to the managed <xref:System.IAppDomainSetup> interface, which the <xref:System.AppDomainSetup> type implements.</span></span> <span data-ttu-id="a2f12-120">参照してください<xref:System.IAppDomainSetup?displayProperty=nameWithType>そのプロパティの詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="a2f12-120">See <xref:System.IAppDomainSetup?displayProperty=nameWithType> for detailed descriptions of its properties.</span></span>  
  
 <span data-ttu-id="a2f12-121">`IAppDomainSetup` 追加できるアセンブリのバインド情報を表す、<xref:System.AppDomain>インスタンスを作成する前にします。</span><span class="sxs-lookup"><span data-stu-id="a2f12-121">`IAppDomainSetup` represents assembly binding information that can be added to an <xref:System.AppDomain> instance before its creation.</span></span> <span data-ttu-id="a2f12-122">たとえば、ホストを設定できます、<xref:System.AppDomainSetup.ApplicationBase%2A>マネージ アセンブリのプロパティを共通言語ランタイム (CLR) をプローブするルート ディレクトリを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2f12-122">For example, a host can set the <xref:System.AppDomainSetup.ApplicationBase%2A> property to establish a root directory, which the common language runtime (CLR) probes for managed assemblies.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a2f12-123">必要条件</span><span class="sxs-lookup"><span data-stu-id="a2f12-123">Requirements</span></span>  
 <span data-ttu-id="a2f12-124">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2f12-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a2f12-125">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a2f12-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a2f12-126">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="a2f12-126">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a2f12-127">**.NET Framework のバージョン:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a2f12-127">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2f12-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="a2f12-128">See also</span></span>
- <xref:System.AppDomain>
- <xref:System.AppDomainSetup>
- <xref:System.IAppDomainSetup>
- [<span data-ttu-id="a2f12-129">ホスト インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2f12-129">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
