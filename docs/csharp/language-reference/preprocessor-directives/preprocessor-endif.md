---
title: '#endif - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#endif'
helpviewer_keywords:
- '#endif directive [C#]'
ms.assetid: 6a5fca55-5aee-441f-86f6-1c99fbe9ec05
ms.openlocfilehash: 58e29363ca1298966ecf88e6b456f33f43a176b0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54573047"
---
# <a name="endif-c-reference"></a><span data-ttu-id="1bab1-102">#endif (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="1bab1-102">#endif (C# Reference)</span></span>
<span data-ttu-id="1bab1-103">`#endif` は [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md)ディレクティブで始まる、条件付きディレクティブの終了を指定します。</span><span class="sxs-lookup"><span data-stu-id="1bab1-103">`#endif` specifies the end of a conditional directive, which began with the [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) directive.</span></span> <span data-ttu-id="1bab1-104">たとえば、オブジェクトに適用された</span><span class="sxs-lookup"><span data-stu-id="1bab1-104">For example,</span></span>  
  
```csharp
#define DEBUG  
// ...  
#if DEBUG  
    Console.WriteLine("Debug version");  
#endif  
```  
  
## <a name="remarks"></a><span data-ttu-id="1bab1-105">コメント</span><span class="sxs-lookup"><span data-stu-id="1bab1-105">Remarks</span></span>  
 <span data-ttu-id="1bab1-106">`#if` ディレクティブで始まる条件付きディレクティブは、`#endif` ディレクティブで明示的に終了させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bab1-106">A conditional directive, beginning with a `#if` directive, must explicitly be terminated with a `#endif` directive.</span></span> <span data-ttu-id="1bab1-107">`#endif` の使用例については、「[#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1bab1-107">See [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) for an example of how to use `#endif`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1bab1-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="1bab1-108">See also</span></span>

- [<span data-ttu-id="1bab1-109">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="1bab1-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="1bab1-110">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="1bab1-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="1bab1-111">C# プリプロセッサ ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="1bab1-111">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
