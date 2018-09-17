---
title: C# プリプロセッサ ディレクティブ
ms.date: 07/20/2015
f1_keywords:
- cs.preprocessor
helpviewer_keywords:
- preprocessor directives [C#]
- keywords [C#], preprocessor directives
ms.assetid: f2406090-b244-4f7e-ab72-3698fefed724
ms.openlocfilehash: 1c0a97cabce347be0bc9367f3d090a1fc699db19
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2018
ms.locfileid: "45694169"
---
# <a name="c-preprocessor-directives"></a><span data-ttu-id="c67c1-102">C# プリプロセッサ ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="c67c1-102">C# preprocessor directives</span></span>
<span data-ttu-id="c67c1-103">このセクションでは、次の C# プリプロセッサ ディレクティブについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c67c1-103">This section contains information about the following C# preprocessor directives:</span></span>

- [<span data-ttu-id="c67c1-104">#if</span><span class="sxs-lookup"><span data-stu-id="c67c1-104">#if</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md)
- [<span data-ttu-id="c67c1-105">#else</span><span class="sxs-lookup"><span data-stu-id="c67c1-105">#else</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-else.md)
- [<span data-ttu-id="c67c1-106">#elif</span><span class="sxs-lookup"><span data-stu-id="c67c1-106">#elif</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md)
- [<span data-ttu-id="c67c1-107">#endif</span><span class="sxs-lookup"><span data-stu-id="c67c1-107">#endif</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md)
- [<span data-ttu-id="c67c1-108">#define</span><span class="sxs-lookup"><span data-stu-id="c67c1-108">#define</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md)
- [<span data-ttu-id="c67c1-109">#undef</span><span class="sxs-lookup"><span data-stu-id="c67c1-109">#undef</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-undef.md)
- [<span data-ttu-id="c67c1-110">#warning</span><span class="sxs-lookup"><span data-stu-id="c67c1-110">#warning</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-warning.md)
- [<span data-ttu-id="c67c1-111">#error</span><span class="sxs-lookup"><span data-stu-id="c67c1-111">#error</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-error.md)
- [<span data-ttu-id="c67c1-112">#line</span><span class="sxs-lookup"><span data-stu-id="c67c1-112">#line</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-line.md)
- [<span data-ttu-id="c67c1-113">#region</span><span class="sxs-lookup"><span data-stu-id="c67c1-113">#region</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-region.md)
- [<span data-ttu-id="c67c1-114">#endregion</span><span class="sxs-lookup"><span data-stu-id="c67c1-114">#endregion</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-endregion.md)
- [<span data-ttu-id="c67c1-115">#pragma</span><span class="sxs-lookup"><span data-stu-id="c67c1-115">#pragma</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma.md)
- [<span data-ttu-id="c67c1-116">#pragma warning</span><span class="sxs-lookup"><span data-stu-id="c67c1-116">#pragma warning</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-warning.md)
- [<span data-ttu-id="c67c1-117">#pragma checksum</span><span class="sxs-lookup"><span data-stu-id="c67c1-117">#pragma checksum</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-checksum.md)

<span data-ttu-id="c67c1-118">詳細および例については、個々のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c67c1-118">See the individual topics for more information and examples.</span></span>

<span data-ttu-id="c67c1-119">コンパイラに個別のプリプロセッサはありませんが、このセクションに示すディレクティブは、ある場合と同じように処理されます。</span><span class="sxs-lookup"><span data-stu-id="c67c1-119">Although the compiler doesn't have a separate preprocessor, the directives described in this section are processed as if there were one.</span></span> <span data-ttu-id="c67c1-120">これらは条件付きコンパイルに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c67c1-120">They are used to help in conditional compilation.</span></span> <span data-ttu-id="c67c1-121">C や C++ のディレクティブとは異なり、マクロを作成するのにこれらのディレクティブを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="c67c1-121">Unlike C and C++ directives, you cannot use these directives to create macros.</span></span>

<span data-ttu-id="c67c1-122">プリプロセッサ ディレクティブは、行の唯一の命令である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c67c1-122">A preprocessor directive must be the only instruction on a line.</span></span>

## <a name="see-also"></a><span data-ttu-id="c67c1-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="c67c1-123">See also</span></span>

- [<span data-ttu-id="c67c1-124">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="c67c1-124">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="c67c1-125">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="c67c1-125">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
