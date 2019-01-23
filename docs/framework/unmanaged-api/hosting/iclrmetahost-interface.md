---
title: ICLRMetaHost インターフェイス
ms.date: 03/30/2017
api_name:
- ICLRMetaHost
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost
helpviewer_keywords:
- ICLRMetaHost interface [.NET Framework hosting]
ms.assetid: c627fcdd-fc4f-4b1c-8e91-df8536f627d8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b52b12df9953dbafaeebfe223313288de0e559b4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54584049"
---
# <a name="iclrmetahost-interface"></a><span data-ttu-id="ee8c1-102">ICLRMetaHost インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ee8c1-102">ICLRMetaHost Interface</span></span>
<span data-ttu-id="ee8c1-103">そのバージョン番号に基づく共通言語ランタイム (CLR) の特定のバージョンを返す、インストールされている Clr のすべてを一覧表示、指定されたプロセスに読み込まれるすべてのランタイムの一覧で、アセンブリをコンパイル、プロセスを終了するために使用する CLR のバージョンを検出するメソッドを提供します。ランタイムがクリーン シャット ダウンとクエリのレガシ API バインドします。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-103">Provides methods that return a specific version of the common language runtime (CLR) based on its version number, list all installed CLRs, list all runtimes that are loaded in a specified process, discover the CLR version used to compile an assembly, exit a process with a clean runtime shutdown, and query legacy API binding.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ee8c1-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="ee8c1-104">Methods</span></span>  
  
|<span data-ttu-id="ee8c1-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="ee8c1-105">Method</span></span>|<span data-ttu-id="ee8c1-106">説明</span><span class="sxs-lookup"><span data-stu-id="ee8c1-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ee8c1-107">EnumerateInstalledRuntimes メソッド</span><span class="sxs-lookup"><span data-stu-id="ee8c1-107">EnumerateInstalledRuntimes Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-enumerateinstalledruntimes-method.md)|<span data-ttu-id="ee8c1-108">含む、有効な列挙体を返します[ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)コンピューターにインストールされている CLR のバージョンごとにインターフェイス ポインター。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-108">Returns an enumeration that contains a valid [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface pointer for each CLR version that is installed on a computer.</span></span>|  
|[<span data-ttu-id="ee8c1-109">EnumerateLoadedRuntimes メソッド</span><span class="sxs-lookup"><span data-stu-id="ee8c1-109">EnumerateLoadedRuntimes Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-enumerateloadedruntimes-method.md)|<span data-ttu-id="ee8c1-110">含む、有効な列挙体を返します[ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)特定のプロセスに読み込まれる各 CLR 用のインターフェイス ポインター。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-110">Returns an enumeration that contains a valid [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface pointer for each CLR that is loaded in a given process.</span></span> <span data-ttu-id="ee8c1-111">このメソッドは[GetVersionFromProcess](../../../../docs/framework/unmanaged-api/hosting/getversionfromprocess-function.md)します。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-111">This method supersedes [GetVersionFromProcess](../../../../docs/framework/unmanaged-api/hosting/getversionfromprocess-function.md).</span></span>|  
|[<span data-ttu-id="ee8c1-112">ExitProcess メソッド</span><span class="sxs-lookup"><span data-stu-id="ee8c1-112">ExitProcess Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-exitprocess-method.md)|<span data-ttu-id="ee8c1-113">すべての読み込まれたランタイムを適切にシャット ダウンしようとしてのプロセスを終了します。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-113">Attempts to shut down all loaded runtimes gracefully and then terminates the process.</span></span> <span data-ttu-id="ee8c1-114">も優先されます、 [CorExitProcess](../../../../docs/framework/unmanaged-api/hosting/corexitprocess-function.md)関数。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-114">Supersedes the [CorExitProcess](../../../../docs/framework/unmanaged-api/hosting/corexitprocess-function.md) function.</span></span>|  
|[<span data-ttu-id="ee8c1-115">GetRuntime メソッド</span><span class="sxs-lookup"><span data-stu-id="ee8c1-115">GetRuntime Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-getruntime-method.md)|<span data-ttu-id="ee8c1-116">取得、 [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)特定の CLR バージョンに対応するインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-116">Gets the [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface that corresponds to a particular CLR version.</span></span> <span data-ttu-id="ee8c1-117">このメソッドは、 [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)で使用される関数、 [STARTUP_LOADER_SAFEMODE](../../../../docs/framework/unmanaged-api/hosting/startup-flags-enumeration.md)フラグ。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-117">This method supersedes the [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) function used with the [STARTUP_LOADER_SAFEMODE](../../../../docs/framework/unmanaged-api/hosting/startup-flags-enumeration.md) flag.</span></span>|  
|[<span data-ttu-id="ee8c1-118">GetVersionFromFile メソッド</span><span class="sxs-lookup"><span data-stu-id="ee8c1-118">GetVersionFromFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-getversionfromfile-method.md)|<span data-ttu-id="ee8c1-119">指定されたファイル パスから、アセンブリの元の .NET Framework コンパイル バージョン (メタデータに格納されている) を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-119">Gets the assembly's original .NET Framework compilation version (stored in the metadata), given its file path.</span></span> <span data-ttu-id="ee8c1-120">このメソッドは[GetFileVersion](../../../../docs/framework/unmanaged-api/hosting/getfileversion-function.md)します。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-120">This method supersedes [GetFileVersion](../../../../docs/framework/unmanaged-api/hosting/getfileversion-function.md).</span></span>|  
|[<span data-ttu-id="ee8c1-121">QueryLegacyV2RuntimeBinding メソッド</span><span class="sxs-lookup"><span data-stu-id="ee8c1-121">QueryLegacyV2RuntimeBinding Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-querylegacyv2runtimebinding-method.md)|<span data-ttu-id="ee8c1-122">レガシ アクティブ化ポリシーが関連付けられて、例を使用してランタイムを表すインターフェイスを返します、`useLegacyV2RuntimeActivationPolicy`属性を[ \<startup > 要素](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)ダイレクトを使用して、構成ファイルのエントリレガシ アクティブ化 Api、または呼び出すことによって、 [iclrruntimeinfo::bindaslegacyv2runtime](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-bindaslegacyv2runtime-method.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-122">Returns an interface that represents a runtime to which legacy activation policy has been bound, for example by using the `useLegacyV2RuntimeActivationPolicy` attribute on the [\<startup> Element](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md) configuration file entry, by direct use of the legacy activation APIs, or by calling the [ICLRRuntimeInfo::BindAsLegacyV2Runtime](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-bindaslegacyv2runtime-method.md) method.</span></span>|  
|[<span data-ttu-id="ee8c1-123">RequestRuntimeLoadedNotification メソッド</span><span class="sxs-lookup"><span data-stu-id="ee8c1-123">RequestRuntimeLoadedNotification Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-requestruntimeloadednotification-method.md)|<span data-ttu-id="ee8c1-124">CLR バージョンは、最初に読み込まれたが、開始していない場合に、指定した関数ポインターへのコールバックを保証します。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-124">Guarantees a callback to the specified function pointer when a CLR version is first loaded, but not yet started.</span></span> <span data-ttu-id="ee8c1-125">このメソッドは[LockClrVersion](../../../../docs/framework/unmanaged-api/hosting/lockclrversion-function.md)</span><span class="sxs-lookup"><span data-stu-id="ee8c1-125">This method supersedes [LockClrVersion](../../../../docs/framework/unmanaged-api/hosting/lockclrversion-function.md)</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ee8c1-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="ee8c1-126">Remarks</span></span>  
 <span data-ttu-id="ee8c1-127">このインターフェイスのインスタンスを取得する唯一の方法は、呼び出すことによって、 [CLRCreateInstance](../../../../docs/framework/unmanaged-api/hosting/clrcreateinstance-function.md)関数の次のようにします。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-127">The only way to get an instance of this interface is by calling the [CLRCreateInstance](../../../../docs/framework/unmanaged-api/hosting/clrcreateinstance-function.md) function as follows:</span></span>  
  
```  
ICLRMetaHost *pMetaHost = NULL;  
HRESULT hr = CLRCreateInstance(CLSID_CLRMetaHost,  
                   IID_ICLRMetaHost, (LPVOID*)&pMetaHost);  
```  
  
## <a name="requirements"></a><span data-ttu-id="ee8c1-128">必要条件</span><span class="sxs-lookup"><span data-stu-id="ee8c1-128">Requirements</span></span>  
 <span data-ttu-id="ee8c1-129">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ee8c1-130">**ヘッダー:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="ee8c1-130">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="ee8c1-131">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="ee8c1-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ee8c1-132">**.NET Framework のバージョン:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ee8c1-132">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee8c1-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee8c1-133">See also</span></span>
- [<span data-ttu-id="ee8c1-134">ホスト インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ee8c1-134">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="ee8c1-135">ホスティング</span><span class="sxs-lookup"><span data-stu-id="ee8c1-135">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
