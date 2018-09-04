---
title: ICorDebug::CreateProcess メソッド
ms.date: 03/30/2017
api_name:
- ICorDebug.CreateProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::CreateProcess
helpviewer_keywords:
- ICorDebug::CreateProcess method [.NET Framework debugging]
- CreateProcess method, ICorDebugProcess interface [.NET Framework debugging]
ms.assetid: b6128694-11ed-46e7-bd4e-49ea1914c46a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dfda61706af3e1043d271c0aa74264bd99a4076c
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43508637"
---
# <a name="icordebugcreateprocess-method"></a><span data-ttu-id="cbf37-102">ICorDebug::CreateProcess メソッド</span><span class="sxs-lookup"><span data-stu-id="cbf37-102">ICorDebug::CreateProcess Method</span></span>
<span data-ttu-id="cbf37-103">プロセスと、デバッガーの制御下で、プライマリ スレッドを起動します。</span><span class="sxs-lookup"><span data-stu-id="cbf37-103">Launches a process and its primary thread under the control of the debugger.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cbf37-104">構文</span><span class="sxs-lookup"><span data-stu-id="cbf37-104">Syntax</span></span>  
  
```  
HRESULT CreateProcess (  
    [in]  LPCWSTR                     lpApplicationName,  
    [in]  LPWSTR                      lpCommandLine,  
    [in]  LPSECURITY_ATTRIBUTES       lpProcessAttributes,  
    [in]  LPSECURITY_ATTRIBUTES       lpThreadAttributes,  
    [in]  BOOL                        bInheritHandles,  
    [in]  DWORD                       dwCreationFlags,  
    [in]  PVOID                       lpEnvironment,  
    [in]  LPCWSTR                     lpCurrentDirectory,  
    [in]  LPSTARTUPINFOW              lpStartupInfo,  
    [in]  LPPROCESS_INFORMATION       lpProcessInformation,  
    [in]  CorDebugCreateProcessFlags  debuggingFlags,  
    [out] ICorDebugProcess            **ppProcess  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cbf37-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cbf37-105">Parameters</span></span>  
 `lpApplicationName`  
 <span data-ttu-id="cbf37-106">[in]実行中のプロセスによって実行されるモジュールを指定する null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cbf37-106">[in] Pointer to a null-terminated string that specifies the module to be executed by the launched process.</span></span> <span data-ttu-id="cbf37-107">モジュールは、呼び出し元のプロセスのセキュリティ コンテキストで実行されます。</span><span class="sxs-lookup"><span data-stu-id="cbf37-107">The module is executed in the security context of the calling process.</span></span>  
  
 `lpCommandLine`  
 <span data-ttu-id="cbf37-108">[in]実行中のプロセスによって実行されるコマンドラインを指定する null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cbf37-108">[in] Pointer to a null-terminated string that specifies the command line to be executed by the launched process.</span></span> <span data-ttu-id="cbf37-109">アプリケーション名 (たとえば、"SomeApp.exe") は、最初の引数である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cbf37-109">The application name (for example, "SomeApp.exe") must be the first argument.</span></span>  
  
 `lpProcessAttributes`  
 <span data-ttu-id="cbf37-110">[in]Win32 へのポインター`SECURITY_ATTRIBUTES`プロセスのセキュリティ記述子を指定する構造体。</span><span class="sxs-lookup"><span data-stu-id="cbf37-110">[in] Pointer to a Win32 `SECURITY_ATTRIBUTES` structure that specifies the security descriptor for the process.</span></span> <span data-ttu-id="cbf37-111">場合`lpProcessAttributes`が null の場合、既定のセキュリティ記述子は、プロセスに取得します。</span><span class="sxs-lookup"><span data-stu-id="cbf37-111">If `lpProcessAttributes` is null, the process gets a default security descriptor.</span></span>  
  
 `lpThreadAttributes`  
 <span data-ttu-id="cbf37-112">[in]Win32 へのポインター`SECURITY_ATTRIBUTES`プロセスのプライマリ スレッドのセキュリティ記述子を指定する構造体。</span><span class="sxs-lookup"><span data-stu-id="cbf37-112">[in] Pointer to a Win32 `SECURITY_ATTRIBUTES` structure that specifies the security descriptor for the primary thread of the process.</span></span> <span data-ttu-id="cbf37-113">場合`lpThreadAttributes`が null の場合、既定のセキュリティ記述子は、スレッドに取得します。</span><span class="sxs-lookup"><span data-stu-id="cbf37-113">If `lpThreadAttributes` is null, the thread gets a default security descriptor.</span></span>  
  
 `bInheritHandles`  
 <span data-ttu-id="cbf37-114">[in]設定`true`、実行中のプロセスによって呼び出し元のプロセスで継承可能な各ハンドルを継承することを示すまたは`false`ハンドルを継承しないことを示します。</span><span class="sxs-lookup"><span data-stu-id="cbf37-114">[in] Set to `true` to indicate that each inheritable handle in the calling process is inherited by the launched process, or `false` to indicate that the handles are not inherited.</span></span> <span data-ttu-id="cbf37-115">継承されたハンドルは、元のハンドルと同じ値とアクセス権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="cbf37-115">The inherited handles have the same value and access rights as the original handles.</span></span>  
  
 `dwCreationFlags`  
 <span data-ttu-id="cbf37-116">[in]ビットごとの組み合わせ、 [Win32 プロセス作成フラグ](https://go.microsoft.com/fwlink/?linkid=69981)優先度クラスと、実行中のプロセスの動作を制御します。</span><span class="sxs-lookup"><span data-stu-id="cbf37-116">[in] A bitwise combination of the [Win32 Process Creation Flags](https://go.microsoft.com/fwlink/?linkid=69981) that control the priority class and the behavior of the launched process.</span></span>  
  
 `lpEnvironment`  
 <span data-ttu-id="cbf37-117">[in]新しいプロセスの環境ブロックへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cbf37-117">[in] Pointer to an environment block for the new process.</span></span>  
  
 `lpCurrentDirectory`  
 <span data-ttu-id="cbf37-118">[in]プロセスの現在のディレクトリにフルパスを指定する null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cbf37-118">[in] Pointer to a null-terminated string that specifies the full path to the current directory for the process.</span></span> <span data-ttu-id="cbf37-119">このパラメーターが null の場合、新しいプロセスは、呼び出し元プロセスとして同じの現在のドライブとディレクトリがあります。</span><span class="sxs-lookup"><span data-stu-id="cbf37-119">If this parameter is null, the new process will have the same current drive and directory as the calling process.</span></span>  
  
 `lpStartupInfo`  
 <span data-ttu-id="cbf37-120">[in]Win32 へのポインター`STARTUPINFOW`ウィンドウ ステーション、デスクトップ、標準のハンドル、および実行中のプロセスのメイン ウィンドウの外観を指定する構造体。</span><span class="sxs-lookup"><span data-stu-id="cbf37-120">[in] Pointer to a Win32 `STARTUPINFOW` structure that specifies the window station, desktop, standard handles, and appearance of the main window for the launched process.</span></span>  
  
 `lpProcessInformation`  
 <span data-ttu-id="cbf37-121">[in]Win32 へのポインター`PROCESS_INFORMATION`を起動するプロセスに関する識別情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="cbf37-121">[in] Pointer to a Win32 `PROCESS_INFORMATION` structure that specifies the identification information about the process to be launched.</span></span>  
  
 `debuggingFlags`  
 <span data-ttu-id="cbf37-122">[in]デバッグ オプションを指定する CorDebugCreateProcessFlags 列挙型の値。</span><span class="sxs-lookup"><span data-stu-id="cbf37-122">[in] A value of the CorDebugCreateProcessFlags enumeration that specifies the debugging options.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="cbf37-123">[out]プロセスを表す ICorDebugProcess オブジェクトのアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cbf37-123">[out] A pointer to the address of a ICorDebugProcess object that represents the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cbf37-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="cbf37-124">Remarks</span></span>  
 <span data-ttu-id="cbf37-125">このメソッドのパラメーターは、Win32 のと同じ`CreateProcess`メソッド。</span><span class="sxs-lookup"><span data-stu-id="cbf37-125">The parameters of this method are the same as those of the Win32 `CreateProcess` method.</span></span>  
  
 <span data-ttu-id="cbf37-126">アンマネージの混在モードのデバッグを有効にするには設定`dwCreationFlags`DEBUG_PROCESS に&#124;DEBUG_ONLY_THIS_PROCESS します。</span><span class="sxs-lookup"><span data-stu-id="cbf37-126">To enable unmanaged mixed-mode debugging, set `dwCreationFlags` to DEBUG_PROCESS &#124; DEBUG_ONLY_THIS_PROCESS.</span></span> <span data-ttu-id="cbf37-127">マネージ デバッグのみを使用する場合は、これらのフラグを設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="cbf37-127">If you want to use only managed debugging, do not set these flags.</span></span>  
  
 <span data-ttu-id="cbf37-128">かどうか、デバッガーとプロセスをデバッグ (アタッチされたプロセス)、単一のコンソールを共有し、相互運用機能デバッグを使用する場合は、コンソールのロックを保持して、デバッグ イベントで停止にアタッチされたプロセスのことです。</span><span class="sxs-lookup"><span data-stu-id="cbf37-128">If the debugger and the process to be debugged (the attached process) share a single console, and if interop debugging is used, it is possible for the attached process to hold console locks and stop at a debug event.</span></span> <span data-ttu-id="cbf37-129">デバッガーにし、コンソールを使用しようがブロックされます。</span><span class="sxs-lookup"><span data-stu-id="cbf37-129">The debugger will then block any attempt to use the console.</span></span> <span data-ttu-id="cbf37-130">この問題を回避するで防ぐを設定、`dwCreationFlags`パラメーター。</span><span class="sxs-lookup"><span data-stu-id="cbf37-130">To avoid this problem, set the CREATE_NEW_CONSOLE flag in the `dwCreationFlags` parameter.</span></span>  
  
 <span data-ttu-id="cbf37-131">IA 64 ベースおよび AMD64 ベースのプラットフォームなどの Win9x と x86 以外のプラットフォームでは、相互運用機能デバッグはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="cbf37-131">Interop debugging is not supported on Win9x and non-x86 platforms such as IA-64-based and AMD64-based platforms.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cbf37-132">要件</span><span class="sxs-lookup"><span data-stu-id="cbf37-132">Requirements</span></span>  
 <span data-ttu-id="cbf37-133">**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cbf37-133">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cbf37-134">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cbf37-134">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cbf37-135">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cbf37-135">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cbf37-136">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cbf37-136">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cbf37-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="cbf37-137">See Also</span></span>  
 [<span data-ttu-id="cbf37-138">ICorDebug インターフェイス</span><span class="sxs-lookup"><span data-stu-id="cbf37-138">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
