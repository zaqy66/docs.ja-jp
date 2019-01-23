---
title: CALL_ID 構造体
ms.date: 03/30/2017
api_name:
- CALL_ID
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- CALL_ID
helpviewer_keywords:
- CALL_ID structure [.NET Framework debugging]
ms.assetid: bfd46324-afec-4782-9c18-586d81fb4740
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 204c2dfbf28f95c1b8c2d2c1b757730e64a8e91d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54503704"
---
# <a name="callid-structure"></a><span data-ttu-id="cdf90-102">CALL_ID 構造体</span><span class="sxs-lookup"><span data-stu-id="cdf90-102">CALL_ID Structure</span></span>
<span data-ttu-id="cdf90-103">デバッガーが呼び出される関数に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="cdf90-103">Provides information to a debugger about a function that is being called.</span></span> <span data-ttu-id="cdf90-104">参照してください、 [INotifySink2](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)インターフェイスの詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="cdf90-104">See the [INotifySink2](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md) interface for more information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cdf90-105">構文</span><span class="sxs-lookup"><span data-stu-id="cdf90-105">Syntax</span></span>  
  
```  
typedef struct tagCALL_ID  
{  
    LPCOLESTR       szMachine;  
    DWORD           dwPid;  
    USER_THREAD     *pUserThread;  
    STACK_ADDRESS   addrStackPointer;  
    LPCOLESTR       szEntryPoint;  
    LPCOLESTR       szDestinationMachine;  
} CALL_ID;  
```  
  
## <a name="members"></a><span data-ttu-id="cdf90-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="cdf90-106">Members</span></span>  
  
|<span data-ttu-id="cdf90-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="cdf90-107">Member</span></span>|<span data-ttu-id="cdf90-108">説明</span><span class="sxs-lookup"><span data-stu-id="cdf90-108">Description</span></span>|  
|------------|-----------------|  
|`szMachine`|<span data-ttu-id="cdf90-109">呼び出しを行っているコンピューターを識別します。</span><span class="sxs-lookup"><span data-stu-id="cdf90-109">Identifies the machine that is making the call.</span></span>|  
|`dwPid`|<span data-ttu-id="cdf90-110">コンピューターのプロセッサを識別します。</span><span class="sxs-lookup"><span data-stu-id="cdf90-110">Identifies the machine processor.</span></span>|  
|`pUserThread`|<span data-ttu-id="cdf90-111">呼び出しを実行しているスレッドを識別します。</span><span class="sxs-lookup"><span data-stu-id="cdf90-111">Identifies the thread that is executing the call.</span></span>|  
|`addrStackPointer`|<span data-ttu-id="cdf90-112">呼び出し履歴のアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="cdf90-112">Specifies the address of the call stack.</span></span>|  
|`szEntryPoint`|<span data-ttu-id="cdf90-113">呼び出しのアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="cdf90-113">Specifies the address of the call.</span></span>|  
|`szDestinationMachine`|<span data-ttu-id="cdf90-114">呼び出しを実行するマシンを識別します。</span><span class="sxs-lookup"><span data-stu-id="cdf90-114">Identifies the machine that will execute the call.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="cdf90-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="cdf90-115">Requirements</span></span>  
 <span data-ttu-id="cdf90-116">**ヘッダー:** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="cdf90-116">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cdf90-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="cdf90-117">See also</span></span>
- [<span data-ttu-id="cdf90-118">INotifySink2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="cdf90-118">INotifySink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)
- [<span data-ttu-id="cdf90-119">シンボル ストア診断構造体</span><span class="sxs-lookup"><span data-stu-id="cdf90-119">Diagnostics Symbol Store Structures</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)
