---
title: LoadTypeLibWithResolver 関数
ms.date: 03/30/2017
api_name:
- LoadTypeLibWithResolver
api_location:
- TlbRef.dll
api_type:
- DLLExport
f1_keywords:
- LoadTypeLibWithResolver
helpviewer_keywords:
- LoadTypeLibWithResolver function [.NET Framework]
ms.assetid: 7123a89b-eb9b-463a-a552-a081e33b0a3a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b6a217e2212bb900d7ba83ccdd9cb00d30454baf
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44354140"
---
# <a name="loadtypelibwithresolver-function"></a><span data-ttu-id="afb44-102">LoadTypeLibWithResolver 関数</span><span class="sxs-lookup"><span data-stu-id="afb44-102">LoadTypeLibWithResolver Function</span></span>
<span data-ttu-id="afb44-103">タイプ ライブラリを読み込み、指定された使用[ITypeLibResolver インターフェイス](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md)任意の内部で参照されるタイプ ライブラリを解決します。</span><span class="sxs-lookup"><span data-stu-id="afb44-103">Loads a type library and uses the supplied [ITypeLibResolver interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md) to resolve any internally referenced type libraries.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="afb44-104">構文</span><span class="sxs-lookup"><span data-stu-id="afb44-104">Syntax</span></span>  
  
```  
HRESULT LoadTypeLibWithResolver(  
    [in]  LPCOLESTR           szFile,  
    [in]  REGKIND             regkind,  
    [in]  ITypeLibResolver   *pTlbResolver,  
    [out] ITypeLib          **pptlib);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="afb44-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="afb44-105">Parameters</span></span>  
 `szFile`  
 <span data-ttu-id="afb44-106">[in]タイプ ライブラリのファイル パス。</span><span class="sxs-lookup"><span data-stu-id="afb44-106">[in] The file path of the type library.</span></span>  
  
 `regkind`  
 <span data-ttu-id="afb44-107">[in]A [REGKIND 列挙](https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/ne-oleauto-tagregkind)タイプ ライブラリを登録する方法を制御するフラグ。</span><span class="sxs-lookup"><span data-stu-id="afb44-107">[in] A [REGKIND enumeration](https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/ne-oleauto-tagregkind) flag that controls how the type library is registered.</span></span> <span data-ttu-id="afb44-108">指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="afb44-108">Its possible values are:</span></span>  
  
-   <span data-ttu-id="afb44-109">`REGKIND_DEFAULT`: 既定の登録の動作を使用します。</span><span class="sxs-lookup"><span data-stu-id="afb44-109">`REGKIND_DEFAULT`: Use default registration behavior.</span></span>  
  
-   <span data-ttu-id="afb44-110">`REGKIND_REGISTER`: このタイプ ライブラリを登録します。</span><span class="sxs-lookup"><span data-stu-id="afb44-110">`REGKIND_REGISTER`: Register this type library.</span></span>  
  
-   <span data-ttu-id="afb44-111">`REGKIND_NONE`。 このタイプ ライブラリを登録できません操作を行います。</span><span class="sxs-lookup"><span data-stu-id="afb44-111">`REGKIND_NONE`: Do not register this type library.</span></span>  
  
 `pTlbResolver`  
 <span data-ttu-id="afb44-112">[in]実装へのポインター、 [ITypeLibResolver インターフェイス](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md)します。</span><span class="sxs-lookup"><span data-stu-id="afb44-112">[in] A pointer to the implementation of the [ITypeLibResolver interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md).</span></span>  
  
 `pptlib`  
 <span data-ttu-id="afb44-113">[out]読み込まれているタイプ ライブラリへの参照。</span><span class="sxs-lookup"><span data-stu-id="afb44-113">[out] A reference to the type library that is being loaded.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="afb44-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="afb44-114">Return Value</span></span>  
 <span data-ttu-id="afb44-115">次の表に記載した HRESULT 値の 1 つ。</span><span class="sxs-lookup"><span data-stu-id="afb44-115">One of the HRESULT values listed in the following table.</span></span>  
  
|<span data-ttu-id="afb44-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="afb44-116">Return value</span></span>|<span data-ttu-id="afb44-117">説明</span><span class="sxs-lookup"><span data-stu-id="afb44-117">Meaning</span></span>|  
|------------------|-------------|  
|`S_OK`|<span data-ttu-id="afb44-118">成功。</span><span class="sxs-lookup"><span data-stu-id="afb44-118">Success.</span></span>|  
|`E_OUTOFMEMORY`|<span data-ttu-id="afb44-119">メモリが不足しています。</span><span class="sxs-lookup"><span data-stu-id="afb44-119">Out of memory.</span></span>|  
|`E_POINTER`|<span data-ttu-id="afb44-120">1 つ以上のポインターが無効です。</span><span class="sxs-lookup"><span data-stu-id="afb44-120">One or more of the pointers are invalid.</span></span>|  
|`E_INVALIDARG`|<span data-ttu-id="afb44-121">1 つ以上の引数が無効です。</span><span class="sxs-lookup"><span data-stu-id="afb44-121">One or more of the arguments are invalid.</span></span>|  
|`TYPE_E_IOERROR`|<span data-ttu-id="afb44-122">関数は、ファイルに書き込めませんでした。</span><span class="sxs-lookup"><span data-stu-id="afb44-122">The function could not write to the file.</span></span>|  
|`TYPE_E_REGISTRYACCESS`|<span data-ttu-id="afb44-123">システムの登録情報データベースを開くことができませんでした。</span><span class="sxs-lookup"><span data-stu-id="afb44-123">The system registration database could not be opened.</span></span>|  
|`TYPE_E_INVALIDSTATE`|<span data-ttu-id="afb44-124">タイプ ライブラリを開くことができませんでした。</span><span class="sxs-lookup"><span data-stu-id="afb44-124">The type library could not be opened.</span></span>|  
|`TYPE_E_CANTLOADLIBRARY`|<span data-ttu-id="afb44-125">タイプ ライブラリまたは DLL を読み込むことができませんでした。</span><span class="sxs-lookup"><span data-stu-id="afb44-125">The type library or DLL could not be loaded.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="afb44-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="afb44-126">Remarks</span></span>  
 <span data-ttu-id="afb44-127">[Tlbexp.exe (タイプ ライブラリ エクスポーター)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md)呼び出し、`LoadTypeLibWithResolver`アセンブリをタイプ ライブラリへの変換処理中に機能します。</span><span class="sxs-lookup"><span data-stu-id="afb44-127">The [Tlbexp.exe (Type Library Exporter)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md) calls the `LoadTypeLibWithResolver` function during the assembly-to-type-library conversion process.</span></span>  
  
 <span data-ttu-id="afb44-128">この関数は、レジストリに最小限のアクセス権を持つ指定したタイプ ライブラリを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="afb44-128">This function loads the specified type library with minimal access to the registry.</span></span> <span data-ttu-id="afb44-129">関数は、内部で参照されるタイプ ライブラリ、それぞれが読み込まれ、親のタイプ ライブラリに追加する必要がありますのタイプ ライブラリを調べます。</span><span class="sxs-lookup"><span data-stu-id="afb44-129">The function then examines the type library for internally referenced type libraries, each of which must be loaded and added to the parent type library.</span></span>  
  
 <span data-ttu-id="afb44-130">参照されるタイプ ライブラリは、読み込まれる前に、ファイルの完全パスにファイルのパスを参照を解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="afb44-130">Before a referenced type library can be loaded, its reference file path must be resolved to a full file path.</span></span> <span data-ttu-id="afb44-131">これによって実現されます、 [ResolveTypeLib メソッド](../../../../docs/framework/unmanaged-api/tlbexp/resolvetypelib-method.md)によって提供される、 [ITypeLibResolver インターフェイス](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md)に渡される、`pTlbResolver`パラメーター。</span><span class="sxs-lookup"><span data-stu-id="afb44-131">This is accomplished through the [ResolveTypeLib method](../../../../docs/framework/unmanaged-api/tlbexp/resolvetypelib-method.md) that is provided by the [ITypeLibResolver interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md), which is passed in the `pTlbResolver` parameter.</span></span>  
  
 <span data-ttu-id="afb44-132">参照されるタイプ ライブラリの完全ファイル パスがわかっている場合、`LoadTypeLibWithResolver`関数が読み込みを結合されたマスターのタイプ ライブラリを作成する、親のタイプ ライブラリに参照されるタイプ ライブラリを追加します。</span><span class="sxs-lookup"><span data-stu-id="afb44-132">When the full file path of the referenced type library is known, the `LoadTypeLibWithResolver` function loads and adds the referenced type library to the parent type library, creating a combined master type library.</span></span>  
  
 <span data-ttu-id="afb44-133">関数は解決し、すべての内部で参照されるタイプ ライブラリを読み込み後で解決されたマスター タイプ ライブラリへの参照を返します、`pptlib`パラメーター。</span><span class="sxs-lookup"><span data-stu-id="afb44-133">After the function resolves and loads all internally referenced type libraries, it returns a reference to the master resolved type library in the `pptlib` parameter.</span></span>  
  
 <span data-ttu-id="afb44-134">`LoadTypeLibWithResolver`関数一般に、 [Tlbexp.exe (タイプ ライブラリ エクスポーター)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md)、独自の内部を供給する[ITypeLibResolver インターフェイス](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md)での実装、 `pTlbResolver`パラメーター。</span><span class="sxs-lookup"><span data-stu-id="afb44-134">The `LoadTypeLibWithResolver` function is generally called by the [Tlbexp.exe (Type Library Exporter)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md), which supplies its own internal [ITypeLibResolver interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md) implementation in the `pTlbResolver` parameter.</span></span>  
  
 <span data-ttu-id="afb44-135">呼び出す場合`LoadTypeLibWithResolver`を直接指定する必要あります独自[ITypeLibResolver インターフェイス](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md)実装します。</span><span class="sxs-lookup"><span data-stu-id="afb44-135">If you call `LoadTypeLibWithResolver` directly, you must supply your own [ITypeLibResolver interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md) implementation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="afb44-136">要件</span><span class="sxs-lookup"><span data-stu-id="afb44-136">Requirements</span></span>  
 <span data-ttu-id="afb44-137">**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="afb44-137">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="afb44-138">**ヘッダー:** TlbRef.h</span><span class="sxs-lookup"><span data-stu-id="afb44-138">**Header:** TlbRef.h</span></span>  
  
 <span data-ttu-id="afb44-139">**ライブラリ:** TlbRef.lib</span><span class="sxs-lookup"><span data-stu-id="afb44-139">**Library:** TlbRef.lib</span></span>  
  
 <span data-ttu-id="afb44-140">**.NET framework のバージョン:** 3.5、3.0、2.0</span><span class="sxs-lookup"><span data-stu-id="afb44-140">**.NET Framework Version:** 3.5, 3.0, 2.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="afb44-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="afb44-141">See Also</span></span>  
 [<span data-ttu-id="afb44-142">Tlbexp ヘルパー関数</span><span class="sxs-lookup"><span data-stu-id="afb44-142">Tlbexp Helper Functions</span></span>](../../../../docs/framework/unmanaged-api/tlbexp/index.md)  
 [<span data-ttu-id="afb44-143">LoadTypeLibEx 関数</span><span class="sxs-lookup"><span data-stu-id="afb44-143">LoadTypeLibEx Function</span></span>](https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-loadtypelibex)
