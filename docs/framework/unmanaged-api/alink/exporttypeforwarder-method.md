---
title: ExportTypeForwarder メソッド
ms.date: 03/30/2017
api_name:
- IALink.ExportTypeForwarder
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ExportTypeForwarder
helpviewer_keywords:
- ExportTypeForwarder method
ms.assetid: 55989fa9-ab43-4f08-8eb6-2eb56fa7ca76
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 03949fb52d23e3b0f107f9f1d5208208369c3960
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574614"
---
# <a name="exporttypeforwarder-method"></a><span data-ttu-id="69e9a-102">ExportTypeForwarder メソッド</span><span class="sxs-lookup"><span data-stu-id="69e9a-102">ExportTypeForwarder Method</span></span>
<span data-ttu-id="69e9a-103">指定したアセンブリの type テーブルへの型フォワーダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="69e9a-103">Adds a type forwarder to the type table of the given assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="69e9a-104">構文</span><span class="sxs-lookup"><span data-stu-id="69e9a-104">Syntax</span></span>  
  
```  
HRESULT ExportTypeForwarder(  
    mdAssemblyRef   tkAssemblyRef,  
    LPCWSTR         pszTypename,  
    DWORD           dwFlags,  
    mdExportedType* pType  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="69e9a-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="69e9a-105">Parameters</span></span>  
 `tkAssemblyRef`  
 <span data-ttu-id="69e9a-106">型フォワーダーが参照するアセンブリへの参照。</span><span class="sxs-lookup"><span data-stu-id="69e9a-106">Reference to the assembly to which the type forwarder refers.</span></span>  
  
 `pszTypename`  
 <span data-ttu-id="69e9a-107">エクスポートする完全修飾型名。</span><span class="sxs-lookup"><span data-stu-id="69e9a-107">Fully qualified type name to export.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="69e9a-108">`ComType` フラグなど`tdPublic`または`tdNested`します。</span><span class="sxs-lookup"><span data-stu-id="69e9a-108">`ComType` flags such as `tdPublic` or `tdNested`.</span></span> <span data-ttu-id="69e9a-109">この値に渡される[DefineExportedType メソッド](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md)します。</span><span class="sxs-lookup"><span data-stu-id="69e9a-109">This value may be passed to [DefineExportedType Method](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md).</span></span>  
  
 `pType`  
 <span data-ttu-id="69e9a-110">エクスポートされた型のトークンを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="69e9a-110">Receives the token of the exported type.</span></span> <span data-ttu-id="69e9a-111">これは、入れ子にされた型の生成にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="69e9a-111">This is necessary only for emitting nested types.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="69e9a-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="69e9a-112">Return Value</span></span>  
 <span data-ttu-id="69e9a-113">メソッドが成功した場合は、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="69e9a-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="69e9a-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="69e9a-114">Requirements</span></span>  
 <span data-ttu-id="69e9a-115">Alink.h が必要です。</span><span class="sxs-lookup"><span data-stu-id="69e9a-115">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="69e9a-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="69e9a-116">See also</span></span>
- [<span data-ttu-id="69e9a-117">IALink インターフェイス</span><span class="sxs-lookup"><span data-stu-id="69e9a-117">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="69e9a-118">IALink2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="69e9a-118">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="69e9a-119">ALink API</span><span class="sxs-lookup"><span data-stu-id="69e9a-119">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
