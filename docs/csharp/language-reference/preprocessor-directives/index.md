---
title: 'C# プリプロセッサ ディレクティブ'
ms.date: 07/20/2015
f1_keywords:
  - cs.preprocessor
helpviewer_keywords:
  - 'preprocessor directives [C#]'
  - 'keywords [C#], preprocessor directives'
ms.assetid: f2406090-b244-4f7e-ab72-3698fefed724
---
# <a name="c-preprocessor-directives"></a><span data-ttu-id="6c2c4-102">C# プリプロセッサ ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="6c2c4-102">C# preprocessor directives</span></span>
<span data-ttu-id="6c2c4-103">このセクションでは、次の C# プリプロセッサ ディレクティブについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6c2c4-103">This section contains information about the following C# preprocessor directives:</span></span>

- [<span data-ttu-id="6c2c4-104">#if</span><span class="sxs-lookup"><span data-stu-id="6c2c4-104">#if</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md)
- [<span data-ttu-id="6c2c4-105">#else</span><span class="sxs-lookup"><span data-stu-id="6c2c4-105">#else</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-else.md)
- [<span data-ttu-id="6c2c4-106">#elif</span><span class="sxs-lookup"><span data-stu-id="6c2c4-106">#elif</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md)
- [<span data-ttu-id="6c2c4-107">#endif</span><span class="sxs-lookup"><span data-stu-id="6c2c4-107">#endif</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md)
- [<span data-ttu-id="6c2c4-108">#define</span><span class="sxs-lookup"><span data-stu-id="6c2c4-108">#define</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md)
- [<span data-ttu-id="6c2c4-109">#undef</span><span class="sxs-lookup"><span data-stu-id="6c2c4-109">#undef</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-undef.md)
- [<span data-ttu-id="6c2c4-110">#warning</span><span class="sxs-lookup"><span data-stu-id="6c2c4-110">#warning</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-warning.md)
- [<span data-ttu-id="6c2c4-111">#error</span><span class="sxs-lookup"><span data-stu-id="6c2c4-111">#error</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-error.md)
- [<span data-ttu-id="6c2c4-112">#line</span><span class="sxs-lookup"><span data-stu-id="6c2c4-112">#line</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-line.md)
- [<span data-ttu-id="6c2c4-113">#region</span><span class="sxs-lookup"><span data-stu-id="6c2c4-113">#region</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-region.md)
- [<span data-ttu-id="6c2c4-114">#endregion</span><span class="sxs-lookup"><span data-stu-id="6c2c4-114">#endregion</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-endregion.md)
- [<span data-ttu-id="6c2c4-115">#pragma</span><span class="sxs-lookup"><span data-stu-id="6c2c4-115">#pragma</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma.md)
- [<span data-ttu-id="6c2c4-116">#pragma warning</span><span class="sxs-lookup"><span data-stu-id="6c2c4-116">#pragma warning</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-warning.md)
- [<span data-ttu-id="6c2c4-117">#pragma checksum</span><span class="sxs-lookup"><span data-stu-id="6c2c4-117">#pragma checksum</span></span>](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-checksum.md)

<span data-ttu-id="6c2c4-118">詳細および例については、個々のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c2c4-118">See the individual topics for more information and examples.</span></span>

<span data-ttu-id="6c2c4-119">コンパイラに個別のプリプロセッサはありませんが、このセクションに示すディレクティブは、ある場合と同じように処理されます。</span><span class="sxs-lookup"><span data-stu-id="6c2c4-119">Although the compiler doesn't have a separate preprocessor, the directives described in this section are processed as if there were one.</span></span> <span data-ttu-id="6c2c4-120">これらは条件付きコンパイルに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6c2c4-120">They are used to help in conditional compilation.</span></span> <span data-ttu-id="6c2c4-121">C や C++ のディレクティブとは異なり、マクロを作成するのにこれらのディレクティブを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="6c2c4-121">Unlike C and C++ directives, you cannot use these directives to create macros.</span></span>

<span data-ttu-id="6c2c4-122">プリプロセッサ ディレクティブは、行の唯一の命令である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c2c4-122">A preprocessor directive must be the only instruction on a line.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c2c4-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c2c4-123">See also</span></span>

- [<span data-ttu-id="6c2c4-124">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="6c2c4-124">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="6c2c4-125">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="6c2c4-125">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
