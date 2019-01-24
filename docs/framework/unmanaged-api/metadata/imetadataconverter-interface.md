---
title: IMetaDataConverter インターフェイス
ms.date: 03/30/2017
api_name:
- IMetaDataConverter
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataConverter
helpviewer_keywords:
- IMetaDataConverter interface [.NET Framework metadata]
ms.assetid: 9caea662-0167-4267-b14a-2fa42c3be4ea
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fc1f813cac237642fdaab653cd47552ab7472ab0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732928"
---
# <a name="imetadataconverter-interface"></a><span data-ttu-id="fdb1a-102">IMetaDataConverter インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fdb1a-102">IMetaDataConverter Interface</span></span>
<span data-ttu-id="fdb1a-103">タイプ ライブラリをそれぞれのメタデータ署名にマップして、一方から他方に変換するメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="fdb1a-103">Provides methods to map type libraries to their metadata signatures, and to convert from one to the other.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fdb1a-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="fdb1a-104">Methods</span></span>  
  
|<span data-ttu-id="fdb1a-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="fdb1a-105">Method</span></span>|<span data-ttu-id="fdb1a-106">説明</span><span class="sxs-lookup"><span data-stu-id="fdb1a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fdb1a-107">GetMetaDataFromTypeInfo メソッド</span><span class="sxs-lookup"><span data-stu-id="fdb1a-107">GetMetaDataFromTypeInfo Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataconverter-getmetadatafromtypeinfo-method.md)|<span data-ttu-id="fdb1a-108">ポインターを取得、 [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) 、指定した参照されるタイプ ライブラリのメタデータ シグネチャを表すインスタンス`ITypeInfo`インスタンス。</span><span class="sxs-lookup"><span data-stu-id="fdb1a-108">Gets a pointer to an [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) instance that represents the metadata signature for the type library referenced by the specified `ITypeInfo` instance.</span></span>|  
|[<span data-ttu-id="fdb1a-109">GetMetaDataFromTypeLib メソッド</span><span class="sxs-lookup"><span data-stu-id="fdb1a-109">GetMetaDataFromTypeLib Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataconverter-getmetadatafromtypelib-method.md)|<span data-ttu-id="fdb1a-110">ポインターを取得、`IMetaDataImport`インスタンスを指定したによって表されるタイプ ライブラリのメタデータ シグネチャを表す`ITypeLib`インスタンス。</span><span class="sxs-lookup"><span data-stu-id="fdb1a-110">Gets a pointer to an `IMetaDataImport` instance that represents the metadata signature for the type library represented by the specified `ITypeLib` instance.</span></span>|  
|[<span data-ttu-id="fdb1a-111">GetTypeLibFromMetaData メソッド</span><span class="sxs-lookup"><span data-stu-id="fdb1a-111">GetTypeLibFromMetaData Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataconverter-gettypelibfrommetadata-method.md)|<span data-ttu-id="fdb1a-112">ポインターを取得、`ITypeLib`を指定したモジュールとライブラリの名前を持つタイプ ライブラリを表すインスタンス。</span><span class="sxs-lookup"><span data-stu-id="fdb1a-112">Gets a pointer to an `ITypeLib` instance that represents the type library that has the specified module and library names.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fdb1a-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="fdb1a-113">Requirements</span></span>  
 <span data-ttu-id="fdb1a-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fdb1a-114">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fdb1a-115">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="fdb1a-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="fdb1a-116">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="fdb1a-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="fdb1a-117">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fdb1a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fdb1a-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="fdb1a-118">See also</span></span>
- [<span data-ttu-id="fdb1a-119">メタデータ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fdb1a-119">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
- [<span data-ttu-id="fdb1a-120">IMetaDataImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fdb1a-120">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
