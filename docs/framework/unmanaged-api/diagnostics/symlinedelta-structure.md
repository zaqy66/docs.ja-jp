---
title: SYMLINEDELTA 構造体
ms.date: 03/30/2017
api_name:
- SYMLINEDELTA
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- SYMLINEDELTA
helpviewer_keywords:
- SYMLINEDELTA structure [.NET Framework debugging]
ms.assetid: 9634e995-d46d-4397-ab66-cc5781d11e4e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2d534ae381e0dc105731cf0a537f81afe80d87e0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732740"
---
# <a name="symlinedelta-structure"></a><span data-ttu-id="e1538-102">SYMLINEDELTA 構造体</span><span class="sxs-lookup"><span data-stu-id="e1538-102">SYMLINEDELTA Structure</span></span>
<span data-ttu-id="e1538-103">編集の結果として移動されたメソッドに関する情報をシンボル ハンドラーを提供します。</span><span class="sxs-lookup"><span data-stu-id="e1538-103">Provides information to the symbol handler about methods that were moved as a result of edits.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e1538-104">構文</span><span class="sxs-lookup"><span data-stu-id="e1538-104">Syntax</span></span>  
  
```  
typedef struct _SYMLINEDELTA  
    {  
        mdMethodDef  mdMethod;  
        INT32        delta;  
    } SYMLINEDELTA;  
```  
  
## <a name="members"></a><span data-ttu-id="e1538-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="e1538-105">Members</span></span>  
  
|<span data-ttu-id="e1538-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="e1538-106">Member</span></span>|<span data-ttu-id="e1538-107">説明</span><span class="sxs-lookup"><span data-stu-id="e1538-107">Description</span></span>|  
|------------|-----------------|  
|`mdMethod`|<span data-ttu-id="e1538-108">メソッドのメタデータ トークンです。</span><span class="sxs-lookup"><span data-stu-id="e1538-108">The method's metadata token.</span></span>|  
|`delta`|<span data-ttu-id="e1538-109">メソッドが移動された行の数。</span><span class="sxs-lookup"><span data-stu-id="e1538-109">The number of lines the method was moved.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e1538-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="e1538-110">Requirements</span></span>  
 <span data-ttu-id="e1538-111">**ヘッダー:** CorSym.idl</span><span class="sxs-lookup"><span data-stu-id="e1538-111">**Header:** CorSym.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1538-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1538-112">See also</span></span>
- [<span data-ttu-id="e1538-113">シンボル ストア診断構造体</span><span class="sxs-lookup"><span data-stu-id="e1538-113">Diagnostics Symbol Store Structures</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)
