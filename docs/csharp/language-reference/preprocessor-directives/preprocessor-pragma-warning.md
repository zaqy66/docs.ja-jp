---
title: '#pragma warning (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '#pragma warning'
helpviewer_keywords:
- '#pragma warning [C#]'
ms.assetid: 723493d5-9753-4cec-babb-54e2b8eb36b6
ms.openlocfilehash: 89ff8151d55ac58a1b114f7727297704ce26b9a7
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43481931"
---
# <a name="pragma-warning-c-reference"></a><span data-ttu-id="f699d-102">#pragma 警告 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="f699d-102">#pragma warning (C# Reference)</span></span>
<span data-ttu-id="f699d-103">`#pragma warning` を使用すると、特定の警告を有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f699d-103">`#pragma warning` can enable or disable certain warnings.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f699d-104">構文</span><span class="sxs-lookup"><span data-stu-id="f699d-104">Syntax</span></span>  
  
```csharp
#pragma warning disable warning-list  
#pragma warning restore warning-list  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f699d-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f699d-105">Parameters</span></span>  
 `warning-list`  
 <span data-ttu-id="f699d-106">警告番号のコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="f699d-106">A comma-separated list of warning numbers.</span></span> <span data-ttu-id="f699d-107">"CS" というプレフィックスは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="f699d-107">The "CS" prefix is optional.</span></span>  
  
 <span data-ttu-id="f699d-108">警告番号が指定されていないと、`disable` はすべての警告を無効にし、`restore` はすべての警告を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f699d-108">When no warning numbers are specified, `disable` disables all warnings and `restore` enables all warnings.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f699d-109">Visual Studio で警告番号を調べるには、プロジェクトをビルドし、**[出力]** ウィンドウで警告番号を探してください。</span><span class="sxs-lookup"><span data-stu-id="f699d-109">To find warning numbers in Visual Studio, build your project and then look for the warning numbers in the **Output** window.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f699d-110">例</span><span class="sxs-lookup"><span data-stu-id="f699d-110">Example</span></span>  
  
```csharp
// pragma_warning.cs  
using System;  
  
#pragma warning disable 414, CS3021  
[CLSCompliant(false)]  
public class C  
{  
    int i = 1;  
    static void Main()  
    {  
    }  
}  
#pragma warning restore CS3021  
[CLSCompliant(false)]  // CS3021  
public class D  
{  
    int i = 1;  
    public static void F()  
    {  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="f699d-111">参照</span><span class="sxs-lookup"><span data-stu-id="f699d-111">See Also</span></span>

- [<span data-ttu-id="f699d-112">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="f699d-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="f699d-113">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="f699d-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="f699d-114">C# プリプロセッサ ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="f699d-114">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)  
- [<span data-ttu-id="f699d-115">C# コンパイラ エラー</span><span class="sxs-lookup"><span data-stu-id="f699d-115">C# Compiler Errors</span></span>](../../../csharp/language-reference/compiler-messages/index.md)
