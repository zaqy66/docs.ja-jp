---
title: '#else (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '#else'
helpviewer_keywords:
- '#else directive [C#]'
ms.assetid: 6a347322-cfa2-4a86-98f8-ddfa2cb7d4db
ms.openlocfilehash: 000cbaac4458a104214e3197442a21dcb4740a37
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43406155"
---
# <a name="else-c-reference"></a><span data-ttu-id="103e9-102">#else (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="103e9-102">#else (C# Reference)</span></span>
<span data-ttu-id="103e9-103">`#else` を使用すると、複合条件付きディレクティブを作成できるため、先行する [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) または (省略可能な) [#elif](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md) ディレクティブの式がいずれも `true` に評価されない場合は、コンパイラが `#else` と以降の `#endif` の間のすべてのコードを評価します。</span><span class="sxs-lookup"><span data-stu-id="103e9-103">`#else` lets you create a compound conditional directive, so that, if none of the expressions in the preceding [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) or (optional) [#elif](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md) directives evaluate to `true`, the compiler will evaluate all code between `#else` and the subsequent `#endif`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="103e9-104">コメント</span><span class="sxs-lookup"><span data-stu-id="103e9-104">Remarks</span></span>  
 <span data-ttu-id="103e9-105">[#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md) が、`#else` の後の次のプリプロセッサ ディレクティブになる必要があります。</span><span class="sxs-lookup"><span data-stu-id="103e9-105">[#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md) must be the next preprocessor directive after `#else`.</span></span> <span data-ttu-id="103e9-106">`#else` の使用例については、「[#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="103e9-106">See [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) for an example of how to use `#else`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="103e9-107">参照</span><span class="sxs-lookup"><span data-stu-id="103e9-107">See Also</span></span>

- [<span data-ttu-id="103e9-108">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="103e9-108">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="103e9-109">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="103e9-109">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="103e9-110">C# プリプロセッサ ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="103e9-110">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
