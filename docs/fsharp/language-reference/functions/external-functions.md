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
# <a name="external-functions"></a>外部関数

このトピックでは、ネイティブ コードで関数を呼び出すための F# 言語サポートについて説明します。

## <a name="syntax"></a>構文

```fsharp
[<DllImport( arguments )>]
extern declaration
```

## <a name="remarks"></a>Remarks

前の構文で*引数*に渡される引数を表す、`System.Runtime.InteropServices.DllImportAttribute`属性。 最初の引数は、.dll 拡張子を除いた、この関数を含んでいる DLL の名前を表す文字列です。 パブリック プロパティのいずれかの追加の引数を指定することができます、`System.Runtime.InteropServices.DllImportAttribute`呼び出し規則などのクラス。

ネイティブ C++ DLL を次のエクスポート関数を含む必要があると仮定します。

```cpp
#include <stdio.h>
extern "C" void __declspec(dllexport) HelloWorld()
{
    printf("Hello world, invoked by F#!\n");
}
```

次のコードを使用して F# からこの関数を呼び出すことができます。

```fsharp
open System.Runtime.InteropServices

module InteropWithNative =
    [<DllImport(@"C:\bin\nativedll", CallingConvention = CallingConvention.Cdecl)>]
    extern void HelloWorld()

InteropWithNative.HelloWorld()
```

ネイティブ コードとの相互運用性と呼びます*プラットフォーム呼び出し*CLR の機能であるとします。 詳細については、「[アンマネージ コードとの相互運用](../../../../docs/framework/interop/index.md)」を参照してください。 そのセクションの情報は、F# に適用されます。

## <a name="see-also"></a>関連項目

- [関数](index.md)
