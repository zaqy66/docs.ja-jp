---
title: 外部関数 (F#)
description: ネイティブ コードで関数を呼び出すための F# 言語サポートについて説明します。
ms.date: 05/16/2016
ms.openlocfilehash: db0d3362d867b07b333951f3380c6735ff471d5e
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "45973106"
---
# <a name="external-functions"></a><span data-ttu-id="3a662-103">外部関数</span><span class="sxs-lookup"><span data-stu-id="3a662-103">External Functions</span></span>

<span data-ttu-id="3a662-104">このトピックでは、ネイティブ コードで関数を呼び出すための F# 言語サポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3a662-104">This topic describes F# language support for calling functions in native code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a662-105">構文</span><span class="sxs-lookup"><span data-stu-id="3a662-105">Syntax</span></span>

```fsharp
[<DllImport( arguments )>]
extern declaration
```

## <a name="remarks"></a><span data-ttu-id="3a662-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="3a662-106">Remarks</span></span>

<span data-ttu-id="3a662-107">前の構文で*引数*に渡される引数を表す、`System.Runtime.InteropServices.DllImportAttribute`属性。</span><span class="sxs-lookup"><span data-stu-id="3a662-107">In the previous syntax, *arguments* represents arguments that are supplied to the `System.Runtime.InteropServices.DllImportAttribute` attribute.</span></span> <span data-ttu-id="3a662-108">最初の引数は、.dll 拡張子を除いた、この関数を含んでいる DLL の名前を表す文字列です。</span><span class="sxs-lookup"><span data-stu-id="3a662-108">The first argument is a string that represents the name of the DLL that contains this function, without the .dll extension.</span></span> <span data-ttu-id="3a662-109">パブリック プロパティのいずれかの追加の引数を指定することができます、`System.Runtime.InteropServices.DllImportAttribute`呼び出し規則などのクラス。</span><span class="sxs-lookup"><span data-stu-id="3a662-109">Additional arguments can be supplied for any of the public properties of the `System.Runtime.InteropServices.DllImportAttribute` class, such as the calling convention.</span></span>

<span data-ttu-id="3a662-110">ネイティブ C++ DLL を次のエクスポート関数を含む必要があると仮定します。</span><span class="sxs-lookup"><span data-stu-id="3a662-110">Assume you have a native C++ DLL that contains the following exported function.</span></span>

```cpp
#include <stdio.h>
extern "C" void __declspec(dllexport) HelloWorld()
{
    printf("Hello world, invoked by F#!\n");
}
```

<span data-ttu-id="3a662-111">次のコードを使用して F# からこの関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3a662-111">You can call this function from F# by using the following code.</span></span>

```fsharp
open System.Runtime.InteropServices

module InteropWithNative =
    [<DllImport(@"C:\bin\nativedll", CallingConvention = CallingConvention.Cdecl)>]
    extern void HelloWorld()

InteropWithNative.HelloWorld()
```

<span data-ttu-id="3a662-112">ネイティブ コードとの相互運用性と呼びます*プラットフォーム呼び出し*CLR の機能であるとします。</span><span class="sxs-lookup"><span data-stu-id="3a662-112">Interoperability with native code is referred to as *platform invoke* and is a feature of the CLR.</span></span> <span data-ttu-id="3a662-113">詳細については、「[アンマネージ コードとの相互運用](../../../../docs/framework/interop/index.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3a662-113">For more information, see [Interoperating with Unmanaged Code](../../../../docs/framework/interop/index.md).</span></span> <span data-ttu-id="3a662-114">そのセクションの情報は、F# に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3a662-114">The information in that section is applicable to F#.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a662-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="3a662-115">See also</span></span>

- [<span data-ttu-id="3a662-116">関数</span><span class="sxs-lookup"><span data-stu-id="3a662-116">Functions</span></span>](index.md)
