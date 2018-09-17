---
title: '#undef (C# リファレンス)'
ms.date: 06/30/2018
f1_keywords:
- '#undef'
helpviewer_keywords:
- '#undef directive [C#]'
ms.assetid: 686c92d2-7194-4be4-b2f4-80091712d513
ms.openlocfilehash: 3957d58f61e51fab01618f5e1146be9cd0da58fd
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2018
ms.locfileid: "45590755"
---
# <a name="undef-c-reference"></a><span data-ttu-id="b13a9-102">#undef (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="b13a9-102">#undef (C# Reference)</span></span>
<span data-ttu-id="b13a9-103">`#undef` を使用すると、シンボルを未定義にすることができます。未定義のシンボルを [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) ディレクティブで式として使用すると、その式は `false` と評価されます。</span><span class="sxs-lookup"><span data-stu-id="b13a9-103">`#undef` lets you undefine a symbol, such that, by using the symbol as the expression in a [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) directive, the expression will evaluate to `false`.</span></span>  
  
 <span data-ttu-id="b13a9-104">シンボルは、[#define](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md) ディレクティブまたは [-define](../../../csharp/language-reference/compiler-options/define-compiler-option.md) コンパイラ オプションのいずれかで定義できます。</span><span class="sxs-lookup"><span data-stu-id="b13a9-104">A symbol can be defined either with the [#define](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md) directive or the [-define](../../../csharp/language-reference/compiler-options/define-compiler-option.md) compiler option.</span></span> <span data-ttu-id="b13a9-105">`#undef` ディレクティブは、ファイル内で、ディレクティブではない他のステートメントよりも前に記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b13a9-105">The `#undef` directive must appear in the file before you use any statements that are not also directives.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b13a9-106">例</span><span class="sxs-lookup"><span data-stu-id="b13a9-106">Example</span></span>  

```csharp
// preprocessor_undef.cs  
// compile with: /d:DEBUG  
#undef DEBUG  
using System;  
class MyClass
{  
    static void Main()
    {  
#if DEBUG  
        Console.WriteLine("DEBUG is defined");  
#else  
        Console.WriteLine("DEBUG is not defined");  
#endif  
    }  
}  
```

<span data-ttu-id="b13a9-107">**DEBUG が定義されていません**</span><span class="sxs-lookup"><span data-stu-id="b13a9-107">**DEBUG is not defined**</span></span>

## <a name="see-also"></a><span data-ttu-id="b13a9-108">参照</span><span class="sxs-lookup"><span data-stu-id="b13a9-108">See Also</span></span>

- [<span data-ttu-id="b13a9-109">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="b13a9-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="b13a9-110">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="b13a9-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="b13a9-111">C# プリプロセッサ ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="b13a9-111">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
